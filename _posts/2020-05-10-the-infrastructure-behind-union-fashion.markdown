---
published: true
layout: post
title: The Infrastructure Behind Union Fashion
date: 2020-05-10T09:00:00.000Z
tags:
  - API-First
  - Collections
  - AWS
  - Twitter
  - Postman
image: /images/blog/server-racks-words.jpg
author: Kin Lane
---
Providing APIs at Union Fashion always begins with the consumption of 3rd party APIs. We realize that APIs aren't just for delivering web and mobile applications but are also for delivering APIs. To help developers be more efficient in the delivery of reliable APIs we provide a number of infrastructre collections they can use to build API deployment, management, orchestration, and other operational level collections.

<ul>
<li><strong>Postman</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/631643/JsLs/?version=latest">API</a>) (<a href="https://documenter.getpostman.com/view/631643/JsLs/?version=latest">Docs</a>) - We use Postman as our API life cycle manager, helping deliver on a variety of stops along the life cycle for each API, and orchestrate how everything works using APIs.</li>
<li><strong>GitHub</strong>&nbsp;(<a href="https://developer.github.com/v3/">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEo?version=latest">Docs</a>) - We use GitHub as the underlying workspace for each API, working in sync with Postman workspaces to make the core definition of each API available across the entire life cycle.</li>
<li><strong>AWS API Gateway</strong>&nbsp;(<a href="https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/api-reference.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHAM?version=latest">Docs</a>) - All internal, partner, and public APIs are published using the AWS API Gateway, providing a content management layer across all APIs being delivered.</li>
<li><strong>AWS DynamoDB</strong>&nbsp;(<a href="https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/Welcome.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHAK?version=latest">Docs</a>) - For simpler data APIs we are using AWS DynamoDB for the persistent data storage behind APIs, allowing for simple NoSQL data storage for each individual APIs.</li>
<li><strong>AWS RDS Aurora</strong>&nbsp;(<a href="https://docs.aws.amazon.com/AmazonRDS/latest/APIReference/Welcome.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHAP?version=latest">Docs</a>) - For more complex data APIs we are using AWS RDS Aurora for persistent storage behind APIs, allowing for more complex relational data storage for each API.</li>
<li><strong>AWS Lambda</strong>&nbsp;(<a href="https://docs.aws.amazon.com/lambda/latest/dg/API_Reference.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHAQ?version=latest">Docs</a>) - For the serverless compute layer for many APIs we are using Lambda as the scalable power behind each API, allowing us to scale APIs at the most atopic level.</li>
<li><strong>AWS S3</strong>&nbsp;(<a href="https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEf?version=latest">Docs</a>) - Using AWS S3 for the storage of all images, videos, documents, and other heavy objects that are made available via Union Fashion APIs, giving each API it's own object store.</li>
<li><strong>AWS Cloudtrail</strong>&nbsp;(<a href="https://docs.aws.amazon.com/awscloudtrail/latest/APIReference/Welcome.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEg?version=latest">Docs</a>) - We are using AWS CloudTrail for the logging layer behind each API, gathering the exhaust of the database, storage, compute, and gateway layers of the APIs.</li>
<li><strong>AWS Identity &amp; Access Management (IAM)</strong>&nbsp;(<a href="https://docs.aws.amazon.com/IAM/latest/APIReference/Welcome.html">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEh?version=latest">Docs</a>) - AWS IAM is used to provide access to APIs for all the underlying services they are using across the AWS platform.</li>
<li><strong>CloudFlare</strong>&nbsp;(<a href="https://api.cloudflare.com/">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEm?version=latest">Docs</a>) - We are using CloudFlare as the DNS and certificate provider behind Union Fashion, providing addressing and encryption for all of the APIs being delivered.</li>
<li><strong>Twitter</strong>&nbsp;(<a href="https://developer.twitter.com/en">API</a>) (<a href="https://documenter.getpostman.com/view/10394726/SzYbxHEn?version=latest">Docs</a>) - We are using the Twitter API for updates, support, and other communication with the Union Square community.</li>
</ul>

At Union Fashion we are API-first in both providing APIs and consuming APIs. All of the services we purchase have APIs, allowing us to seamlessly integrate what they offer directly into our platform. Using APIs to deliver APIs, being API-first in everything we do, and opening up the possibilities for what is possible with the API resources we are buiilding.
