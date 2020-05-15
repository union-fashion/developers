---
published: true
layout: post
title: A Well Defined API Lifecycle
date: 2020-05-11T09:00:00.000Z
tags:
  - Lifecycle
  - Collections
image: /images/blog/copper-shipping-containers.jpg
author: Kin Lane
---
We wanted to invest in API governance at Union Fashion, but as soon as we began defining what we were going to measure we realized that we couldn't measure we wasn't defined. To help us be able to measure, track, discuss, and improve on how we deliver APIs at Union Fashion we need to map out how we were going to be delivering APIs from start to finish.

<ul>
<li><strong>Define</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#3c968356-0064-43ce-a16e-56c8ab6d5916">Docs</a>) - Providing guidelines for how APIs should be defined.</li>
<li><strong>Design</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#a8242433-c788-4c22-a432-035f2c7ce952">Docs</a>) - Training and guidance about how to design APIs.</li>
<li><strong>Mocking</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#5fe06cfd-8462-4089-ab79-65fabebd5f16">Docs</a>) - The ability to mock an API to assist in it's delivery.</li>
<li><strong>Documentation</strong>&nbsp;(<a href="https://github.com/union-fashion/home/blob/master">Docs</a>) - Always having consistent up to date documentation.</li>
<li><strong>Database (NoSQL)</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#111634f5-cdf5-455a-8205-80fbd8597b89">Docs</a>) - Ensuring there is always persistent data storage.</li>
<li><strong>Database (SQL)</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#05420759-44d9-46e3-9c22-a9f09a73338a">Docs</a>) - Ensuring there is always persistent data storage.</li>
<li><strong>Storage</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#d329e0d2-0176-4c8a-a73e-d9906d71267f">Docs</a>) - Providing a place to put objects as part of API operations.</li>
<li><strong>Compute</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#7d081afe-1b11-444d-b43a-d497b1eb24db">Docs</a>) - Having the appropriate amount of compute behind each API.</li>
<li><strong>Pipeline</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#7ba011e4-a9a7-4b25-910c-1f102430bb49">Docs</a>) - Making the delivery of code behind each API repeatable.</li>
<li><strong>Deployment</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#fd958817-4c85-447a-856b-8d5745ba484c">Docs</a>) - Making sure that APIs are deployed in repeatable ways.</li>
<li><strong>Management</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#1394eea4-59a1-4c76-bb82-01fa99e8a663">Docs</a>) - Ensuring that every API is being managed consistently.</li>
<li><strong>Logging</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#ea51db44-c8ab-402c-9234-824d128f6424">Docs</a>) - Establishing a centralized logging strategy across APIs.</li>
<li><strong>Encryption</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#24cd0f73-c2de-4e0e-884a-7f77d8c49fbe">Docs</a>) - Always making encryption the default response across APIs.</li>
<li><strong>DNS</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#b3b87c21-1814-4bcb-83f3-73d6afae8669">Docs</a>) - Having a strategy for how DNS is handled across groups and APIs.</li>
<li><strong>Portal</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#c3c525bc-f028-43cf-835d-a922e33a7bd9">Docs</a>) - Ensuring there is always a doorway to get at all APIs.</li>
<li><strong>Testing</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#a12b8298-b530-4792-a9df-1095bee2806c">Docs</a>) - Providing a consistent approach to testing all APIs.</li>
<li><strong>Security</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#8091e28b-210e-4d4c-8295-2a60631ca01d">Docs</a>) - Scanning and auditing the security landscape for each API.</li>
<li><strong>Monitoring</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#f5afa22d-84c1-4c0f-9350-06fe98b10154">Docs</a>) - Having monitors on a schedule ensuring the quality of APIs.</li>
<li><strong>Support</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#4057e585-c8b0-4eaa-8246-844789bb1370">Docs</a>) - Requiring there be support for every API being operated.</li>
<li><strong>Communications</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#96a779e8-49f8-49f9-bf0b-b71dbcced85b">Docs</a>) - Having consistent communication in place for APIs.</li>
<li><strong>Analytics</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#a08dc26e-3c28-496a-b2bc-45f3b5ff2a23">Docs</a>) - Establishing a layer for understanding what is happening.</li>
<li><strong>Deprecation</strong>&nbsp;(<a href="https://documenter.getpostman.com/view/10394726/SzYbxGrc?version=latest#50938295-1a99-4e88-a147-f0bfd52a09fc">Docs</a>) - Making sure there is a plan for how all APIs will be sunset.</li>
</ul>

This API lifecycle will continue to change and evolve over time. I twill probably posses a couple of forks in the road, but each of these areas have been define as a problem area for the company, and something we wanted to improve upon. You can follow each of the links above to the documentation for the API lifecycle collection showing one possible way APIs will be delivered from end to end here at Union Fashion.
