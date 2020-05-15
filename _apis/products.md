---
name: Products
description: This is the API for the Union Fashion product catalog, providing read and write access to all of the products we are making available via our website, mobile, and partner applications. This page should give developers everything they need to get started using this API, while also look behind how this API is being developed.
image: http://union.fashion/images/api.png
tags:
- Commerce
- Products
- Catalog
created: '2020-05-13'
modified: '2019-05-14'
url: https://raw.githubusercontent.com/union-fashion/products/master/apis.json
specificationVersion: '0.14'
apis:
- name: Products
  description:
  image: http://union.fashion/images/products.png
  humanURL: http://developer.union.fashion/
  baseURL: http://api.union.fashion/
  x-mockUrl: https://f7785723-c31c-4944-baf1-08c58f186515.mock.pstmn.io
  tags:
  - Products
  - Commerce
  - Catalog
  properties:
  - type: x-postman-team
    x-name: Team
    url: https://union-fashion.postman.co/team
  - type: x-postman-workspace
    x-name: Workspace
    url: https://union-fashion.postman.co/workspaces/2990215b-b3e0-4431-b2ca-80cf01274a25/apis
  - type: x-github-organization
    x-name: Organization
    url: https://github.com/union-fashion  
  - type: x-github-repository
    x-name: Repository
    url: https://github.com/union-fashion/products    
  - type: x-postman-builder
    x-name: Builder
    url: https://union-fashion.postman.co/apis/b06cd7bd-51a8-40df-a036-d5cec42700c6?version=e9d51adf-9738-4e58-9c76-b0d11c196d1d          
  - type: x-openapi
    x-name: OpenAPI 3.0 Definition
    url: https://raw.githubusercontent.com/union-fashion/products/master/products-v1.json
  - type: x-postman-collection
    x-name: Collection
    url: https://www.getpostman.com/collections/48cbaf14a09dce8175bd       
  - type: x-postman-environment
    x-name: Environment
    url: https://raw.githubusercontent.com/union-fashion/products/master/products-environment-v1.json
  - type: x-documentation
    x-name: Documentation
    url: https://documenter.getpostman.com/view/10394726/SzS2xojt?version=latest           
  - type: x-contract-testing-monitor
    x-name: Contract Testing Monitor
    url: https://union-fashion.postman.co/monitors/1ea72f63-0700-4370-a289-9a749bc9dd81
  - type: x-performance-testing-monitor
    x-name: Performance Testing Monitor
    url: https://union-fashion.postman.co/monitors/1ea72f63-0700-4370-a289-9a749bc9dd81    
  - type: x-postman-history
    x-name: History
    url: https://union-fashion.postman.co/workspaces/2990215b-b3e0-4431-b2ca-80cf01274a25/history
  - type: x-postman-activity
    x-name: Activity
    url: https://union-fashion.postman.co/workspaces/2990215b-b3e0-4431-b2ca-80cf01274a25/activity
  - type: x-schema-org-object
    x-name: Schema.org Object
    url: https://schema.org/Product      
  - type: x-support
    x-name: Support
    url: https://github.com/union-fashion/products/issues    
  x-results:
    contract-testing:
      14/5/2020 @ 17:00:00:
        Add Product:
          Is 201 Status?: true
          Have body?: true
          Is valid JSON?: true
        Get Products:
          Is 200 Status?: true
          Have body?: true
          Is valid JSON?: true
          Is valid JSON Schema?: true
        Get Product:
          Is 200 Status?: true
          Have body?: true
          Is valid JSON?: false
          Is valid JSON Schema?: false
        Update Product:
          Is 204 Status?: false
          No Body?: true
        Delete Product:
          Is 204 Status?: false
          No Body?: true
    performance-testing:  
      14/5/2020 @ 18:00:00:
        response_time: 523
        meet_expectations: 0
    security-testing:
      14/5/2020 @ 18:00:00:
        Add Product (Security Injection):
          Is 201 Status?: true
          Have body?: true
          Is valid JSON?: true
        Get Products (Security Injection):
          Is 200 Status?: true
          Have body?: true
          Is valid JSON?: true
          Is valid JSON Schema?: true
        Get Product  (Security Injection):
          Is 200 Status?: false
          Have body?: true
          Is valid JSON?: true
          Is valid JSON Schema?: true
        Update Product (Security Injection):
          Is 204 Status?: false
          No Body?: true
        Delete Product (Security Injection):
          Is 204 Status?: false
          No Body?: true    
    governance-testing:
      14/5/2020 @ 19:00:00:
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
            Is there a life cycle collection?: true
            Is there a governance collection?: true
            Is there a documentation collection?: false
            Is there a contract collection?: true
            Is there a performance collection?: true
            Is there a security collection?: true
          Environment:
            Is there a development environment?: true
            Is there a mock development environment?: true
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
