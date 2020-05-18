---
published: true
layout: post
title: Pushing Forward Our AWS API Deployment
date: 2020-05-13T09:00:00.000Z
tags:
  - API Deployment
  - AWS
  - Lambda
  - RDS
image: https://kinlane.github.io/vocabulary/images/api.png
author: Kin Lane
---
In an effort to better map out API deployment practices at Union Fashion we wanted to write up and share the current outline for our leading AWS deployment collection, and work to explain it in plain terms so that it is accessible to more of our business stakeholders. While doing this we are also working to further flesh out and expand upon our current definition to make it more usable, and covering more of our needs. Right now we can deploy [a simple NoSQL API for use in defining very basic APIs](https://github.com/union-fashion/operations#deployment), as well as [a slightly more advanced CRUD version that uses AWS RDS, and backed by individual Lambdas](https://github.com/union-fashion/operations#deployment). This post represents our current work on defining how we deploy APIs at Union Fashion, which is something we'd love to get your feedback on.

## Pull OpenAPI
The API deployment process begins with pulling a valid, complete OpenAPI definition from the Postman API builder, providing the entire definition for the API we are deploying. The OpenAPI should contain every details that will be needed across this entire process, providing a single artifact for what ends up being delivered.

- **Pull API** - This process begins with a call to the Postman API API, pulling the API we are currently working with.
- **Pull Version** - Then we pull the version of the API that we are wanting to eventually deploy to the gateway.
- **Pull OpenAPI** - Now we can pull the actual OpenAPI definition for the API we are targeting for deployment.
- **Store in Environment** -  The OpenAPI is stored in the API deployment environment for each API being deployed.

The OpenAPI is the central definition for each API. This work is designed to flesh out everything we need across the deployment process, and make sure it is reflected in the OpenAPI, stored in the API deployment environment, and made available across this entire API deployment process. Here are a few areas that are still needing attention when it comes to pulling the OpenAPI.

- **Governance**** ([Issue](https://github.com/union-fashion/operations/issues/6)) - Right now we make a lot of assumptions that things are present in the OpenAPI, and governance is how we will actually make sure this is true.
- **JSON Schema** ([Issue](https://github.com/union-fashion/operations/issues/7)) - Should we pull out each individual object and store as separate key / value in the API deployment environment.
- **Vendor Extensions** ([Issue](https://github.com/union-fashion/operations/issues/8)) - Are we going to be investing in vendor extensions being stored in the master, or should they always exist in a derivative that is part of each operational collection?

Governance is the big challenge here. It has to be run before this collection and both the deployment collection and governance collection need to be in alignment about what is being asked. This is the biggest challenge, but also the biggest opportunity when it comes to governing not just the design of each API, but also the deployment of APIs.

## Create Table
We will need a SQL table behind the API we are deploying and since we have the schema for our API as part of the so OpenAPI contract we can take that schema and turn it into the SQL schema we need to create our backend database.

- **Pull OpenAPI from Environment** - We can use the OpenAPI we have stored in our environment to create table.
- **Pull JSON Schema** - Grab the JSON Schema from the bottom of the OpenAPI for generating our MySQL script.
- **Generate MySQL Script** - Produce a MySQL script for the creation of our AWS RDS Aurora table we need.
- **Generate Lambda** - Since we can only create RDS tables using SQL, we need a temporary Lambda to execute.
- **Execute Lambda** - Now we need to actually run the Lambda we created, executing our MySQL create script.
- **Cleanup Lambda** - We do not need our Lambda anymore so we can clean up after ourselves and remove it.

This is where we will add any future enhancements and configuration to our database backend for any API we are deploying using this pattern. Hover we still have a lot of work to be done here to help make this robust and address all of the functionality we need—here are a few of those ongoing needs:

- **Multiple Schema** ([Issue](https://github.com/union-fashion/operations/issues/9)) - Right now it will only handle a single schema per API, and it needs to handle multiple schema per API.
- **Sub-Resources** ([Issue](https://github.com/union-fashion/operations/issues/10)) - Right now this only creates one table for a single primary resource, and we need sub-resources relationships.
- **Indexing** ([Issue](https://github.com/union-fashion/operations/issues/11)) - What indexes can be created and optimized when it comes to the performance of the database behind the API.
- **Redundancy** ([Issue](https://github.com/union-fashion/operations/issues/12)) - What can we do to improve the redundancy of the database, clustering, and scaling across regions.

You can find all of these questions as GitHub issues when it comes to tracking the API deployment conversation across Union Fashion. This work will be dedicated to AWS using RDS, but will also be something we try to replicate and make work across Azure and Google.

## Create Lambda Layer
To run Node.js Lambdas on AWS we need to include all of the dependencies needed to operate the scripts we apply behind each individual API method. AWS Lambda gives you the ability to manage dependencies and apply them in a bulk way across the scripts you are deploying using Lambda layers. Here are the steps we are taking to prepare for behind the API being deployed.

- **Pull Layer Package** - We already have a layer package with all of our Node.js dependencies deployed to AWS S3.
- **Publish Layer** - We need to publish this layer to AWS Lambda so that it can be referenced with each script we are deploying.

This provides us a great way to manage all the dependencies behind the scripts we are using to power our APIs, giving us a clear snapshot of what is behind each API. It does open us up for more work and management of dependencies properly across all of our APIs, and here are a few of them:

- **Management** ([Issue](https://github.com/union-fashion/operations/issues/13)) - How are these packages managed as part of the overall API life cycle and governance practices.
- **Versioned** ([Issue](https://github.com/union-fashion/operations/issues/14)) - Are we managing versions of layers alongside the version of each API being developed and deployed.
- **Artifact** ([Issue](https://github.com/union-fashion/operations/issues/15)) - Are layers documented and identified as part of the OpenAPI artifact rather than just being assumed?
- **Cross API** ([Issue](https://github.com/union-fashion/operations/issues/16)) - What efforts will go into helping developers reuse and work together on defining layers across many APIs.

AWS Lambda layers provides a pretty unique opportunity for us to get a handle on the Node.js dependency sprawl that exists across Union Fashion. The Node.js programming language is easy to use across Postman and AWS, but it tends to create kind of a mess when it comes to how it is managed, making it a pretty ideal place to revisit and better understand how we can improve things.

## Lambda Packager
We need to dynamically build individual Lambda Node.js scripts behind each of the individual API methods in our APIs. Ironically we are using a Lambda to package up our Lambdas. Overall the process for setting up Lambdas is pretty cumbersome, but once setup it provides a pretty powerful way to deliver the compute between APIs being published via the AWS API Gateway. Here are the individual elements of the Lambda packager being used for deployment currently.

- **Generate index.js** - We need to create the primary script for each individual method, using patterns for each HTTP method type.
- **Generate package.json** - We also ned to create a package.json for each individual script, providing a manifest of what is happening.
- **Create Lambda Packager** - We create a Lambda function which we will be using to package up each individual method Lambda.
- **Run Lambda Packager** - We need to run the lambda packager, packaging up our scripts for deployment behind the API.
- **Deploy Packages** - Now we need to actually deploy the Lambda for each individual HTTP method we are deploying.
- **Remove Packager Function** - With all the packages built we no longer need our Lambda packager so we can just clean up after ourselves.

This gives gives us individual Lambda functions for each of the HTTP methods defined in our OpenAPI definition. The scaffolding is there, but there are plenty of things missing from this to make the APIs actually work for most of Union Fashion needs. Here are the areas we are working to improve upon this process and help it scale for what we need.

- **Sub-Resources** ([Issue](https://github.com/union-fashion/operations/issues/17)) - This only works for on-dimension of CRUD, so it will not handle any properties being of object or array.
- **Initial Logic** ([Issue](https://github.com/union-fashion/operations/issues/18)) - We have no way of injecting business logic at beginning of each individual Lambda behind each HTTP method.
- **Closing Logic** ([Issue](https://github.com/union-fashion/operations/issues/19)) - We have no way of injecting business logic at end of each individual Lambda behind each HTTP method.
- **Environment Variables** ([Issue](https://github.com/union-fashion/operations/issues/20)) - What is the strategy for allowing environment variables to passed into each of the functions? (Both Postman & Lambda)
- **Artifact** ([Issue](https://github.com/union-fashion/operations/issues/21)) - Right now bindings are defined using OpenAPI extensions, how will logic, variables and other things be handled?
- **CI/CD** ([Issue](https://github.com/union-fashion/operations/issues/22)) - What does the CI/CD process look like for custom code, or even generated code, ensuring everything is repeatable.
- **Storage** ([Issue](https://github.com/union-fashion/operations/issues/23)) - What does each API use as its storage? Ensuring each API has a bucket to put objects into within each function.

There will be additional needs that emerge as we continue building out our API deployment strategy, but addresses sub-resources, and business logic are the two top priorities when it comes to automating the deployment of APIs using Postman. Our goal is to make things as repeatable and API driven as possible, sticking with our core philosophy of API-First.

## Gateway Deployment
Now we should have all the moving parts we need behind our API. Allowing us to actually deploy our API to the AWS API Gateway, wiring up all of the connections behind it to Lambda and RDS, giving us a usable API from our OpenAPI definition defined using the Postman API builder. Here are the steps we take to actually deploy each API to the gateway.

- **Pull OpenAPI** - We pull the current OpenAPI definition from the environment and prepare it for publishing.
- **OpenAPI Extensions** - Next we craft extensions for each individual HTTP method and publish to the OpenAPI mapping to each Lambda function.
- **Publish OpenAPI** - Now we take our OpenAPI with extensions and publish to AWS API Gateway, making it available as an API.
- **Deploy to Stage** - Now we can deploy our API to either development or production stage, making it available via URL.
- **Map to Subdomain** - Lastly, we need to map our deployed API to a specific custom subdomain that has been established for use.

We now have an API. There is one more step in this process, but as it stands we have deployed an API. Going from OpenAPI in the Postman API builder to functional API on AWS using the API Gateway. There is still more work to be done here, to help make sure we are deploying our APIs as consistently as possible.

- **Domain Management** ([Issue](https://github.com/union-fashion/operations/issues/24)) - Right now domain and sub-domain management Is manual, and we need a collection for this area of operations.
- **Certificates** ([Issue](https://github.com/union-fashion/operations/issues/25)) - Right now certificate management is manual, but we will need a collection to help manage this part of operations.
- **Stages** ([Issue](https://github.com/union-fashion/operations/issues/26)) - Currently there are only development and production stages, are there additional stages that will be need, and how do we track?
- **Status Codes** ([Issue](https://github.com/union-fashion/operations/issues/31)) - There is no coherent strategy between the status codes in OpenAPI and the available gateway responses in AWS API Gateway.

These are areas of API deployment that normally get done once, or happen behind the scenes. Losing the details in the cracks, and leaving lots of shadows when it comes to how APIs are actually deployed. Beyond deployment, there are other overlapping considerations with other stops along the API life cycle that we need to address--most importantly, API management.

## Management
The last step in this process is to ensure that all APIs are consistently managed, making sure there is no open APIs that go out the door, requiring that all API consumers obtain a valid API key before they can use each API, no matter whether they are internal or external to the organization. Here are the final API management steps that are taken as part of this API deployment process.

- **Usage Plan** - First we’ll need an API specific usage plan registered with the gateway apply rate limits to each API deployed.
- **API Key** - Now we need to create a default API key for the system to use when interacting with our API as part of operations.
- **Associate Key with Plan** - Now we need to associate our API key with our API plan, allowing it to access the API we deployed.

Now we have a management layer in place for our API, as well as a key so that we can begin making calls to the API we have deployed. The usage plan, key, and other elements of the API management strategy should fit in with the wider Union Fashion API management strategy, ensuring that all APIs have a management layer, and we are logging, reporting, and rate limiting across operations in a consistent way. Here are a few of the remaining areas of work:

- **Usage Plans** ([Issue](https://github.com/union-fashion/operations/issues/27)) - Right now we are just doing product specific usage plans. What other usage plans will be needed across applications?
- **Policies**  ([Issue](https://github.com/union-fashion/operations/issues/28))- There are no granular policies in place for APIs. Can we being to get more granular for how APIs are actually accessed.
- **Usage Reporting** ([Issue](https://github.com/union-fashion/operations/issues/29)) - There is no plan in place for how API usage is reported and published as part of the wider API portal strategy.
- **Auditing** ([Issue](https://github.com/union-fashion/operations/issues/30)) - We have no practice for auditing plans, keys, and other players of the API management across all APIs—we need something.

We will be breaking out management into its own set of collections to help focus on it as a separate stop along the API life cycle, but for right now it will remain as a management addendum to this AWS API deployment collection. We are still figuring out the best way to define operational collections, allowing for the most granular, but also guided approaches to realizing each individual stop along the API life cycle.

## Quantified API Deployment
One of the most pressing legacy illnesses of API operations at Union Fashion is that we do not have a well defined, documented, and repeatable way of deploying APIs across teams. Resulting in a wide mix of APIs in operation, and competing skills needed to manage and evolve these APIs. Even with the introduction of a CI/CD process the entire end to end API deployment process has not been repeatable. This is an attempt to continue to define, evolve, and apply a consistent approach to deploying APIs. It has become clear the we can train new developers, measure the productivity of existing developers, or collectively discuss something that wasn’t quantified, so this work is meant to help move things forward.

To help address concerns amongst existing teams, this work does not dictate a single approach to deploying APIs at Union Fashion. It is merely an attempt to define one of the most common approaches we’ve seen already in use with one of the most prominent platforms—-AWS. Moving forward teams will need to accomplish two specific things to satisfy governance practices when it comes to API deployment:

1. **Existing Patterns** - Adopt an existing API deployment pattern in use and push forward that definition to make it work for all of your needs.
2. **Document Pattern** - Produce an end to end Postman collection for your API deployment pattern exhaustively defining each individual step.

If you choose to adopt an existing pattern, much of the work will already be done for you. If you are determined that your API deployment pattern is the right choice, then all you need to do is document it, and make it something that other teams can also implement. Allowing API deployment at Union Fashion to remain agnostic about platforms, tooling, and programming languages, while ensuring that we can consistently deliver high quality APIs that continue to meet business objectives at scale. Making sure we are all on the same page when it comes to API deployment, moving us out of the dark ages we’ve existed in for about 20 years when it comes to how APIs are actually deployed into production.

Here are the links to the documentation for each of the current AWS API deployment patterns, with the second one being the most advanced, and providing the foundation for this work.

- [AWS API Gateway + DynamoDB](https://github.com/union-fashion/operations#deployment)
- [AWS API Gateway + Lambda + RDS](https://github.com/union-fashion/operations#deployment).

You can access all of this information under [the operations GitHub repository](https://github.com/union-fashion/operations), and the [issues for API deployment work under this repository](https://github.com/union-fashion/operations/issues?q=is%3Aissue+is%3Aopen+label%3Adeployment), labeled as deployment.
