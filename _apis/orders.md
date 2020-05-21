---
name: Orders
description: This is the API for the Union Fashion order system. Developing our own API for creating, accessing, and fulfilling orders that are placed with our customers. Providing us with the ability to order via our website and mobile applications, but also something we open up to our trusted partners.
image: http://union.fashion/images/api.png
tags:
- Orders
created: '2020-05-13'
modified: '2019-05-13'
url: https://raw.githubusercontent.com/union-fashion/orders/master/apis.json
specificationVersion: '0.14'
apis:
- name: Orders
  description:
  image: http://union.fashion/images/orders.png
  humanURL: http://developer.union.fashion/
  baseURL: http://api.union.fashion/
  x-mockUrl:
  tags:
  - Orders
  - Commerce
  - Catalog
  properties:
    - type: x-postman-team
      x-name: Team
      url: https://union-fashion.postman.co/team
    - type: x-postman-workspace
      x-name: Workspace
      url: https://union-fashion.postman.co/workspaces/67f9508f-a375-4a65-8450-b7f0aabc4cc4/apis
    - type: x-github-organization
      x-name: Organization
      url: https://github.com/union-fashion  
    - type: x-github-repository
      x-name: Repository
      url: https://github.com/union-fashion/orders
    - type: x-postman-builder
      x-name: Builder
      url: https://union-fashion.postman.co/apis/b06cd7bd-51a8-40df-a036-d5cec42700c6?version=e9d51adf-9738-4e58-9c76-b0d11c196d1d         
    - type: x-openapi
      x-name: OpenAPI 3.0 Definition
      url: https://raw.githubusercontent.com/union-fashion/orders/master/orders-v1.json
    - type: x-postman-collection
      x-name: Collection
      url: https://www.getpostman.com/collections/0495a2c4e6d64179ddcd
    - type: x-postman-environment
      x-name: Environment
      url: https://raw.githubusercontent.com/union-fashion/orders/master/orders-environment-v1.json       
    - type: x-documentation
      x-name: Documentation
      url: https://documenter.getpostman.com/view/10394726/SzYXXzLu?version=latest
    - type: x-contract-testing-monitor
      x-name: Contract Testing Monitor
      url: https://union-fashion.postman.co/monitors/1ea73007-dcc3-42b0-8b82-5a8c983bf84c
    - type: x-performance-testing-monitor
      x-name: Performance Testing Monitor
      url: https://union-fashion.postman.co/monitors/1ea96132-d58f-40d0-a018-71484ff4b7ff
    - type: x-postman-history
      x-name: History
      url: https://union-fashion.postman.co/workspaces/67f9508f-a375-4a65-8450-b7f0aabc4cc4/history
    - type: x-postman-activity
      x-name: Activity
      url: https://union-fashion.postman.co/workspaces/67f9508f-a375-4a65-8450-b7f0aabc4cc4/activity
    - type: x-schema-org-object
      x-name: Schema.org Object
      url: https://schema.org/      
    - type: x-support
      x-name: Support
      url: https://github.com/union-fashion/orders/issues
  x-results:
    contract-testing:   
      20/5/2020 @ 20:00:00:
        All:
          Is 200 Status?: true
          Have body?: true
          Is valid JSON?: true
          Is valid JSON Schema?: true     
    performance-testing:  
      20/5/2020 @ 20:00:00:
        response_time: 523
        meet_expectations: 0     
    security-testing:   
      20/5/2020 @ 20:00:00:
      All:
        Is 200 Status?: true
        Have body?: true
        Is valid JSON?: true
        Is valid JSON Schema?: true  
    governance-testing:  
      20/5/2020 @ 20:00:00:
        Definition:
          Workspace:
            Is there a Postman workspace?: true
            Is workspace named properly?: true
          Organization:
            Is there a GitHub organization?: true
          Repository:
            Is there a GitHub repository?: true
          APIs:
            Is there a Postman API?: true
            Is there an OpenAPI?: true
            Is there a valid OpenAPI?: false
          Collections:
            Is there a life cycle collection?: false
            Is there a governance collection?: false
            Is there a documentation collection?: true
            Is there a contract collection?: false
            Is there a performance collection?: true
            Is there a security collection?: false
          Environment:
            Is there a development environment?: false
            Is there a mock development environment?: false
            Is there a production environment?: true
            Is there a mock production environment?: true
          Owner:
            Is there a contact for the API?: false
            Is there a contact name for this API?: false
            Is there a contact email for the API?: false
        Design:
          Info:
            Does the name of the API meet requirements?: true
            Does the description of the API meet requirements?: true
          Paths:
            Are paths using words?: true
          Methods:
            Parameters:
              Are all parameters using camelCase?: true
              Do all parameters have descriptions?: true
            Request Bodies:
              Do only POST, PUT, and PATCH have bodies?: false
              Do request bodies have a description?: false
              Do request bodies have a JSON media type?: false
              Do request boeis have schema?: false
              Do request bodies have examples?: false
            Responses:
              Do all methods have an HTTP Status Success (2xx)?: true
              Do all methods have an HTTP Status Failure (5xx)?: false
            Does GET, POST, PUT, and DELEETE exist for all resources?: true
            Do all methods have summaries?: true
            Do all methods have descriptions?: false
            Do all methods have operation ids?: true
            Do all methods have tags?: false
          Schema:
            Do all schema have properties?: true
            Do all schema properties have descriptions?: false
        Mocks:
          Is there a mock development server?: true
          Is there a mock production server?: true
        Development:
          Is there a development server?: true
          Is there a development stage defined with the API gateway? (COMING SOON): false
        Production:
          Is there a production server?: true
          Is there a production stage defined with the API gateway? (COMING SOON) Copy: false
        Management:
          Is there an API plan?: false
          Is there an API key?: false
        Testing:
          Contract Testing:
            Is there output from contract tests?: true
            Did the API pass the contract tests?: false
          Security Testing:
            Is there output from security tests?: true
            Did the API pass the security tests?: false
          Performance Testing:
            Is there output from performance tests?: true
            Did the API pass the performance tests?: false
        Monitoring:
          Is there a contract testing collection monitor?: false
          Is there a performance testing collection monitor?: false
          Is there a security testing collection monitor?: false
        Support:
          Road Map:
            Is GitHub issues setup for tracking roadmap?: false
            How many road map entries are there?: false
          Issues:
            Is GitHub issues setup for tracking issues?: false
            How many open issue entries are there? (COMING SOON): false
            How many close issue entries are there? (COMING SOON): false
          Change Log:
            How many change log entries are there? (COMING SOON): false
            Is GitHub issues setup for tracking change log?: false
        LIcense:
          Is there a license for the API??: false
          How many road map entries are there? (COMING SOON): false     
include: []
x-common:
- type: website
  name: Website
  url: http://union.fashion
- type: twitter
  name: Twitter
  url: https://twitter.com/unionfashionapi
- type: github-organization
  name: GitHub Organization
  url: http://union.fashion      
maintainers:
- FN: Kin
  x-twitter: kinlane
  x-github: kinlane
  email: mail@union.fashion
---
