---
published: true
layout: post
title: We Are API-First at Union Fashion
date: 2020-05-12T09:00:00.000Z
tags:
  - API-First
  - Philosophy
image: https://kinlane.github.io/vocabulary/images/api-first.png
author: Kin Lane
---
One phrase you hear thrown around a lot in the API sector is API-First. It is a catchy phrase, but what does it mean? Well, at Union Fashion we have worked to provide our team with a definition of what it means, something that is rooted in [our history as a company](https://github.com/union-fashion/home/blob/master/api-history/index.md), with [feedback provided by the core team](https://github.com/union-fashion/home/blob/master/api-first/index.md#team-feedback). To help teams adapt we have created an MVP version, helping them make the transition from API-last to API-first.

## TL;DR - The overview of our philosophy.
If you are just looking for a summary of what we mean by API-first, here is the breakdown. Providing you just a summary of each area, but something you will find linked to our official API-first strategy on GitHub if you want more detail.

- **[Applications](https://github.com/union-fashion/home/blob/master/api-first/index.md#applications)** - Prioritizing APIs over their applications.
- **[Teams](https://github.com/union-fashion/home/blob/master/api-first/index.md#teams)** - Ensuring everyone has a seat at the table.
- **[Workspaces](https://github.com/union-fashion/home/blob/master/api-first/index.md#workspaces)** - Providing a dedicate space to do work.
- **[Feedback](https://github.com/union-fashion/home/blob/master/api-first/index.md#feedback)** - Baking in a feedback loop by default.
- **[Specifications](https://github.com/union-fashion/home/blob/master/api-first/index.md#specification)** - Avoid reinventing the wheel with new APIs
- **[Definitions](https://github.com/union-fashion/home/blob/master/api-first/index.md#definitions)** - Anchoring all APIs in a machine & human readable contract.
- **[Collections](https://github.com/union-fashion/home/blob/master/api-first/index.md#collections)** - Driving API operations using API contract(s) collections.
- **[Examples](https://github.com/union-fashion/home/blob/master/api-first/index.md#examples)** - Providing examples of every operation in use.
- **[Environments](https://github.com/union-fashion/home/blob/master/api-first/index.md#environments)** - Abstracting away secrets and variables.
- **[Lifecycle](https://github.com/union-fashion/home/blob/master/api-first/index.md#lifecycle)** - Driving the API life cycle from an API contract(s).
- **[Mocking](https://github.com/union-fashion/home/blob/master/api-first/index.md#mocking)** - Providing a simulated representation of every API.
- **[Documentation](https://github.com/union-fashion/home/blob/master/api-first/index.md#documentation)** - Always be publish documentation for APIs.
- **[Testing](https://github.com/union-fashion/home/blob/master/api-first/index.md#mocking)** - There is always testing coverage in place for all APIs.
- **[Monitoring](https://github.com/union-fashion/home/blob/master/api-first/index.md#monitoring)** - All tests are run on schedule from regions using monitors.
- **[Collaboration](https://github.com/union-fashion/home/blob/master/api-first/index.md#collaboration)** - Stakeholders are always working together on APIs.
- **[Observability](https://github.com/union-fashion/home/blob/master/api-first/index.md#observability)** - The API life cycle is made more tangible using outputs.

API-first makes Union fashion a more agile and effective organization, and helps us deliver high quality, very precise services, while also making sure we always are considering the bigger picture when we deliver APIs across the organization.

## MVP - Where every team should begin.
We recognize that not everyone will be able to accomplish this the first time out and support a minimal viable edition of API-first, helping you begin your journey toward being API-first after years of doing things a little bit different.

- **[Applications](https://github.com/union-fashion/home/blob/master/api-first/index.md#applications)** - Prioritizing APIs over their applications.
- **[Teams](https://github.com/union-fashion/home/blob/master/api-first/index.md#teams)** - Ensuring everyone has a seat at the table.
- **[Workspaces](https://github.com/union-fashion/home/blob/master/api-first/index.md#workspaces)** - Providing a dedicate space to do work.
- **[Feedback](https://github.com/union-fashion/home/blob/master/api-first/index.md#feedback)** - Baking in a feedback loop by default.
- **[Specifications](https://github.com/union-fashion/home/blob/master/api-first/index.md#specification)** - Avoid reinventing the wheel with new APIs
- **[Definitions](https://github.com/union-fashion/home/blob/master/api-first/index.md#definitions)** - Anchoring all APIs in a machine & human readable contract.
- **[Collections](https://github.com/union-fashion/home/blob/master/api-first/index.md#collections)** - Driving API operations using API contract(s) collections.
- **[Documentation](https://github.com/union-fashion/home/blob/master/api-first/index.md#documentation)** - Always be publish documentation for APIs.
- **[Collaboration](https://github.com/union-fashion/home/blob/master/api-first/index.md#collaboration)** - Stakeholders are always working together on APIs.
- **[Observability](https://github.com/union-fashion/home/blob/master/api-first/index.md#observability)** - The API life cycle is made more tangible using outputs.

This provides a way to get started with the API-first approach with less overhead, focusing on the most important parts. We acknowledge that this shift will be difficult for many groups, and it is something that will take time. We also realize that we straight up have resistance in many corners, which we will be honest about throughout this process.

## Full Details
To help guide the sometimes heated discussions amongst teams we have worked to define every detail of what we mean by API-first here at Union Fashion. It is something we are versioning, and will keep evolving using GitHub. If you have questions, comments, and strong feelings about this, make sure you voice your opinions on GitHub to help us evolve.

### Applications
Before moving forward with any of these project you consider an API first.

- Building a new website.
- Developing web application.
- Developing a mobile application.
- Deploying a single page application.
- Publishing a badge, button, or widget.
- Integrating with any other systems.
- Purchasing a new SaaS software solution.
- Sharing a spreadsheet of data externally.

The API should become a first class aspect of each project moving forward.

### Teams
You have defined who your team of API stakeholders are, and their role.

- Defining who will be the core API development team.
- Established who the business stakeholders are.
- Identified web, mobile, and integration developers.
- Consider who will be involved to bring each API to market.

Every team should have an owner as well as list of all relevant stakeholders.

### Workspaces
You have established a dedicated space for executing the work for each API.

- You have defined the GitHub, GitLab, or Bitbucket repository space for each API.
- You have defined the Postman workspace for each API being developed.
- You have established the private, partner, and public nature of the workspace(s).

APIs spaces help us define the bounded context of our company moving forward.

### Feedback
You agree upon what the feedback loop will look like across teams members.

- Where will synchronous and asynchronous discussions between team members occur.
- Where will artifact comments and annotation occur and be made available for review.
- How will API consumers provide feedback on the overall design and delivery of APIs.

There should always be an owner for each API helping push the feedback loop forward.

### Specifications
You have researched and adopted existing specifications as part of your API design

- A variety of API specification formats are used as the base definition for all APIs.
- All objects, messages, requests, and responses are defined using schema specs.
- We are using Schema.org and other existing vocabulary behind our API designs.
- Authorization should always use and existing standard and never be re-invented.
- An exhaustive search for existing internal APIs should always be conducted.
- A robust search should always be conducted to see if an existing 3rd party API exists.

Every project should be aware of, build upon, and put existing work to use in APIs.

### Definitions
You are using a machine readable definitions the source of truth for API developed.

- OpenAPI 3.0 is the preferred format for all Union Fashion API contracts.
- Swagger 2.0 is regularly used for importing and integrating with 3rd party APIs.
- Support for RAML is available for customers who have adopted the format.
- Any GraphQL API should have a schema present for consumers to use.
- All schema objects are defined and published as JSON Schema files.

A single source of truth should exist for every API being developed and in operation.

### Collections
You are automating the generation of collections derived from the API source of truth.

- Generating the first instance of any collection used as part of the API life cycle.
- Maintaining an association between each collection in use for APIs being delivered.
- Validating each collection against its source of truth, maintaining alignment.
- A change log is present for each collection used as part of the operation of APIs.

While collections begin as generated, they are quickly curated and refined manually.

### Examples
Each API should possess robust and comprehensive examples for each operation.

- Every API request body should have an example representation present.
- Every API response body should have an example representation in collections.
- There should be examples for every media type used in an API design.

Examples are necessary for realizing the full potential of collections across the life cycle.

### Environments
Each API should have a clear set of variables defined for working with each API in a client.

- No secrets should exist in collection, relying on environments to apply.
- Common variables used across collections should be in environments.
- Environments should be centrally defined and shared across teams.
- Environments should help maintain operational state for each API.

Environments are used by developers in clients, and automated using runners and monitors.

### Lifecycle
You are maintaining high quality collections serving various life cycle and governance needs.

- Each API will possess a single collection dedicated to publishing documentation
- Each API will possess a single collection dedicated to publishing mock servers
- Each API will possess a single collection dedicated to contract testing.
- Each API will possess one or many collections dedicated to integration testing.
- Each API  will possess one or many collections dedicated to workflow testing.
- Each API definition is synced to GitHub for use throughout the API software lifecycle.

We are working to define and power each stop along the API life cycle with an active collection.

### Mocking
You are mocking your APIs to simulate behavior before setting up your back-end.

- Leveraging a dedicated RBAC control for delivering mock instances for each API.
- Ensuring that each collection behind mocks has robust and complete examples.
- Providing synthetic data for use in examples helping make mock servers useful.

Mocks are used to help speed up the iteration of API development and for driving API testing.

### Documentation
Every API should possess up to date and complete documentation for use by consumers.

- All documentation should be dynamically generated and published for consumers.
- All documentation should posses and a run in postman button for quick on-boarding.
- All documentation published should accompany an environment for keys and variables.

Documentation for all APIs will be auto discovered via the index for each API being developed.

### Testing
You have test coverage in place for all APIs throughout the life of each of the APIs.

- 100% of each API should be covered as part of API contract testing.
- 5% of each API should be covered as part of API performance testing.
- 100% of integrations with other APIs should have testing available for it.
- Common business workflows should be defined as collections and tested for.

Each API definition will be tested as contract, and validated it is meeting its SLA.

### Monitoring
All APIs should have monitors in place applying API tests on a regular schedule.

- Each API’s contract test should be monitored on a regular schedule.
- Each API’s performance test should be monitored on a regular schedule.
- Each API’s integration test(s) should be monitored on a regular schedule.
- Each API’s workflow test should be monitored on a regular schedule.

Monitors should be ran from multiple regions based upon consumer locations.

### Collaboration
Making all API elements discoverable, shareable, and supporting team collaboration.

- Make your API definition and collections are available via a shared team workspace.
- Make your API definitions, collections, and scripts are available via GitHub repository.
- Widen the network reach of your API making it known internally, privately, or publicly.
- Allow collaboration to be done asynchronously using history, activity, and logging.

APIs are never developed in isolation and always should be subjected to peer review.

### Observability
Operate your API in as observable manner as you possibly can highlighting the API first.

- Contact test results are published as a recurring artifact to each APIs space.
- Integration test results are published as a recurring artifact to each API space.
- Performance test results are published as a recurring artifact to each APIs space.
- Workflow test results are published as a recurring artifact to each API space.
- A road map is always published for each API being developed showing the future.
- A changed e log is always present for each API being developing show what has been done.

Every API should be made observability using the existing outputs of API infrastructure.

## Deployment
Our API-first philosophy tries to not be prescriptive for API deployment as long as it meets the SLA.

- Union fashion is platform, language, and framework agnostic when it comes to API deployments.
- Teams should always strive to turn their API deployment practice into a sharable blueprint.
- Code-first for APIs are an acceptable approach to doing API-first as long as it delivers end results.
- API-first is about establishing a consistent blueprint for how API resources are used by applications.

Deploy of an API may or may not be part of the API-first process, leaving it up to team to deliver each API.

### Deliverables
Each of these areas proposed should be delivering value to API operations in ways that benefits everyone.

- **Applications** - Applications are always have access to the latest data and content.
- **Teams** - You can always find the team behind an API and find targeted consumers.
- **Workspaces** - All of the artifacts and history for each API is available in known location.
- **Feedback** - The conversation around each API does not get lost in the greater noise.
- **Specifications** - Every API is build on the latest and most common set of specifications.
- **Definitions** - There is a human and machine readable contract behind each API delivered.
- **Collections** - API definitions can be leveraged to generate derivatives of each API definition.
- **Examples** - There is an example of every capability showing what is possible across the organization.
- **Environments** - Secrets and other common variables are abstracted, managed, and applied independent of collections.
- **Lifecycle** - Collections are used to consistently power and deliver by multiple stops along the API life cycle.
- **Mocking** - There is a safer representation of each API available for testing and on-boarding API consumers.
- **Documentation** - Up to date API documentation is always available for any being delivered across the organization.
- **Testing** - All APIs follow a testing-first approach to delivering the infrastructure behind all applications.
- **Monitoring** - Every API is monitored consistently allowing an SLA to be established for all API resources.
- **Collaboration** - All APIs are developed and delivered in a collaborate way amongst providers and consumers.
- **Observability** - All APIs are measured using the outputs that are available using existing infrastructure.

API-first is about investing in these 16 areas, building a more collaborative and reliable platform to do business.

### Business Outcomes
There are demonstrable business outcomes for adopting the Union Fashion API-first philosophy by...

- Helping reduce redundancy in the sources of data, content, and algorithms.
- Helping anchor the functionality behind each application in an API definition.
- Allowing machine readable definitions to be verified as compliant with SLA using tests.
- Ensuring all digital resources be more consistent across the entire organization.
- Increasing the speed at which we can deliver new applications and features across the organization.
- Pushing teams to work together, collaborate, and expand the circle behind each business capability.
- Leaving a breadcrumb that makes APIs more traceable, including the entire process behind their delivery.
- Delivering our digital capabilities as smaller more modular components that can be easily reused.
- Making sure all stakeholders are on the same page before too many resources and cycles are set in motion.
- Allowing the infrastructure behind all applications to be measured and validated as they evolve and change.
- Making integration much more of a priority with partners and service providers in use by the organization.
- Delivering more consistent, reliable, secure, and usable infrastructure that is in alignment our business.

Our API-first philosophy should support tangible, meaningful, and measurable business outcomes.

## Moving Towards API-First
As you can see, API-first does not always mean API-design first. It can, but it doesn't have to as long as you meet the other requirements of our organizational API governance. API-first is meant to help ensure we are all communicating, collaborating, and working as a team to deliver the infrastructure, applications, and integrations we need as an organization. It is not meant to get religious about how we deliver APIs. API-first is more about people, than it is about the technology, so let's not get too caught up on the technological, tooling, language, and platform dogma.

The Union Fashion API-First philosophy is meant to guide us as an organization. If there are parts that do not work you need to express your opinions via GitHub, and participate in the overall API operations and governance discussions. We are API-First at Union Fashion, but it is up to you to help define what exactly that means not just in word, but in practice on the ground across the organization. API-first means that APIs are a priority across all discussions at Union Fashion, not that the API is the first thing that gets built,
