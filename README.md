<div align="center">

<a href="https://zagham-portfolio.vercel.app">
  <img src="./assets/header.svg" alt="Zagham Arif, Senior Full-Stack Software Engineer. Node.js, TypeScript, React, Next.js, AWS. 5+ years in production, 12 projects shipped, 7 teams worked with." width="100%"/>
</a>

<h3>I build backends that hold up under real traffic and real money,<br/>and I ship them faster with AI in the loop.</h3>

<p><b>Remote · Pakistan (UTC+5)</b> · Open to contract and full-time work · Overlaps with US and EU hours</p>

[![Portfolio](https://img.shields.io/badge/Portfolio-Live%20site-3B5BFD?style=for-the-badge&logo=vercel&logoColor=white)](https://zagham-portfolio.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge)](https://www.linkedin.com/in/zagham-arif)
[![Upwork](https://img.shields.io/badge/Upwork-Hire%20me-6FDA44?style=for-the-badge&logo=upwork&logoColor=white)](https://www.upwork.com/freelancers/~01b58b210c60ff7195)
[![Topmate](https://img.shields.io/badge/Topmate-Book%20a%20call-E44332?style=for-the-badge)](https://topmate.io/zagham_arif)

[![Email](https://img.shields.io/badge/Email-zaghamarif@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zaghamarif@gmail.com)
[![Fiverr](https://img.shields.io/badge/Fiverr-Services-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white)](https://www.fiverr.com/zagham123)
<img src="https://img.shields.io/badge/Discord-zagham__arif-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord: zagham_arif"/>

</div>

## About

I build the backend systems that keep products fast, reliable and correct with their data: APIs, queues, caches, data pipelines and the AWS infrastructure underneath. I work across the stack, so I also ship the React and Next.js front ends that sit on top of those services.

Five years in, I have worked with seven teams across product companies and agencies, delivered for clients in the US, Germany and Turkey, and led a team of four engineers on a real-time stats platform. Most of my recent work is data-heavy and payments-heavy, where correctness matters more than speed of delivery.

Right now I am freelancing full time, building a recurring donations and payments platform for a direct client.

**On confidentiality:** most of my client work lives in private repositories under NDA, and I keep those agreements after a project ships, after a contract closes, and after the work ends on my side. That is why some projects below are described without the client or product name, and why most of my GitHub activity is private.

## What I do

<table>
<tr>
<td width="50%" valign="top">
<h4>Backend and APIs</h4>
Fast, typed APIs your apps and partners can rely on. REST and GraphQL in Node.js and TypeScript, validated with Zod, documented with Swagger.
</td>
<td width="50%" valign="top">
<h4>Cloud and serverless</h4>
Infrastructure that scales up for busy days and costs less on quiet ones. AWS Lambda, ECS Fargate, SQS and S3, monoliths moved to microservices, Terraform for everything.
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h4>Data, queues and caching</h4>
Millions of records moved, and pages that stay instant. Redis queues and caches, Kinesis streams, worker pools with backpressure.
</td>
<td width="50%" valign="top">
<h4>Full-stack and team lead</h4>
From the first client call to a shipped product. Next.js front ends, estimates, sprint planning, code review and leading delivery teams.
</td>
</tr>
</table>

## Featured work

<table>
<tr>
<th width="22%" align="left">Project</th>
<th width="26%" align="left">The problem</th>
<th width="30%" align="left">What I did</th>
<th width="22%" align="left">What changed</th>
</tr>
<tr>
<td valign="top"><b>Safety Compliance Platform</b><br/><sub>Enterprise · AWS serverless<br/>Client and product name withheld</sub></td>
<td valign="top">Company hierarchies 20 to 30 levels deep took 3 to 4 minutes to assemble in Lambda and often timed out. The database could not be changed.</td>
<td valign="top">Precomputed the hierarchy as JSON in S3, rebuilt by a sync Lambda on every change through SQS. Moved monolithic APIs to serverless microservices with Terraform.</td>
<td valign="top">No recursion on the read path and the timeouts are gone. Infrastructure cost down by around <b>30%</b>.</td>
</tr>
<tr>
<td valign="top"><b>Recurring Donations Platform</b><br/><sub>Payments · live migration<br/>Client and product name withheld</sub></td>
<td valign="top">A live recurring-payments platform had to move to a new Postgres backend and auth provider, with a daily charge run that could never be missed.</td>
<td valign="top">Wrote and rehearsed the migration on staging first. Built scheduled recurring transactions with retry, idempotency and reconciliation on Supabase, Deno edge functions and Next.js.</td>
<td valign="top"><b>0</b> downtime, <b>0</b> records lost, <b>0</b> missed charge runs.</td>
</tr>
<tr>
<td valign="top"><b>PlayerTotals</b><br/><sub>Sports data · public product<br/>Team of 4</sub></td>
<td valign="top">Near-real-time NBA, NFL and MLB stats on top of external APIs with hard rate limits.</td>
<td valign="top">Cron ingestion every 5 minutes into versioned MongoDB history, with a bounded Redis hot window in front. Led the team of four engineers.</td>
<td valign="top">Stats refresh <b>every 5 minutes</b> within the provider's rate limits, and history survives even if the provider drops it.</td>
</tr>
</table>

### All projects

| Project | What it is | Built with |
| --- | --- | --- |
| **Retail Price-Auditing Backend** <br/><sub>Data pipeline · Retail</sub> | Backend for a mobile-first price auditing product used by a US retailer, designed from scratch. Over 2 million records per run pulled from an external feed, queued through Redis and written in parallel by Node.js worker threads, then served back paginated and queryable. | Node.js, Express, TypeScript, TypeORM, Redis, AWS ECS Fargate, Terraform, Datadog, Okta |
| **Recurring Donations Platform** <br/><sub>Payments · Non-profit</sub> | Recurring donations and payments platform for a direct client, with scheduled recurring transactions, authentication, storage and edge functions. Client and product name withheld. | Next.js, TypeScript, Supabase, Deno, PostgreSQL |
| **PlayerTotals** <br/><sub>Real-time · Sports</sub> | Live sports statistics platform covering NBA, NFL and MLB, fetched on a 5-minute cycle with Redis queues and MongoDB for high-throughput processing. | Node.js, TypeScript, React, MongoDB, Redis |
| **Memberstore** <br/><sub>Commerce · Payments</sub> | One storefront serving multiple independent merchants, each selling under their own brand. Stripe handles payments, merchant onboarding and webhook reconciliation. | KeystoneJS, GraphQL, MongoDB, Next.js, TypeScript, Stripe |
| **CivaSource** <br/><sub>AI matching · Marketplace</sub> | AI-assisted product matching for a supply marketplace. Extracts up to 1,000 products per minute using asyncio with Redis caching, behind a FastAPI service with authentication. | Python, FastAPI, Redis, PostgreSQL |
| **Safety Compliance Platform** <br/><sub>Compliance · Enterprise</sub> | Safety checklists and compliance workflows across multiple industrial sites, with a multi-site audit trail. Client and product name withheld. | Node.js, TypeScript, AWS Lambda, SQS, Kinesis, S3, PostgreSQL, Terraform |
| **Real Time Gaming Platform** <br/><sub>Real-time · Gaming</sub> | JavaScript bot libraries and WebSocket connections for in-game bot behavior, plus the UI and command libraries used to control them. Client and product name withheld. | JavaScript, Node.js, WebSocket |
| **[TradeFundrr](https://tradefundrr.com)** <br/><sub>EdTech · CRM</sub> | Trading education platform with an integrated CRM used by its own sales team. | Python, Flask, Django, React, PostgreSQL |
| **Al Khair Traders POS** <br/><sub>Business app · Wholesale</sub> | Replaced a paper process for a wholesale trader: products, suppliers, purchases, sales, returns and quotations in one system, with role-based permissions down to the module level. | Node.js, Express, React, TypeScript, TypeORM, TanStack Query, MySQL, JWT |
| **[AutoTempest](https://www.autotempest.com)** <br/><sub>Search · Automotive</sub> | Car search across many listing sites at once, filtered in a single form. Built the responsive React front end and the REST API over scraped listings. | React, Node.js, MySQL, REST APIs, Web Scraping |
| **Points App** <br/><sub>Loyalty · Payments</sub> | Customer loyalty scheme where points convert into mobile top-up codes, including the redemption flow and payment processing. | Node.js, React, MySQL |
| **N1QL-to-Firebase Automation Tool** <br/><sub>Developer tool · Final year project</sub> | Converts Couchbase N1QL queries into Firebase Cloud Functions and deploys them, removing the hand translation step. | Node.js, Firebase, Couchbase, N1QL, JavaScript |

## Tech stack

<table>
<tr>
<td valign="top" width="170"><b>Languages</b></td>
<td>
<img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&amp;logo=javascript&amp;logoColor=black" alt="JavaScript" height="22"/>
<img src="https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&amp;logo=typescript&amp;logoColor=white" alt="TypeScript" height="22"/>
<img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&amp;logo=python&amp;logoColor=white" alt="Python" height="22"/>
<img src="https://img.shields.io/badge/-SQL-4479A1?style=flat-square" alt="SQL" height="22"/>
<img src="https://img.shields.io/badge/-PHP-777BB4?style=flat-square&amp;logo=php&amp;logoColor=white" alt="PHP" height="22"/>
<img src="https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&amp;logo=html5&amp;logoColor=white" alt="HTML5" height="22"/>
<img src="https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&amp;logo=css&amp;logoColor=white" alt="CSS3" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>Backend and APIs</b></td>
<td>
<img src="https://img.shields.io/badge/-Node.js-339933?style=flat-square&amp;logo=nodedotjs&amp;logoColor=white" alt="Node.js" height="22"/>
<img src="https://img.shields.io/badge/-Express-000000?style=flat-square&amp;logo=express&amp;logoColor=white" alt="Express" height="22"/>
<img src="https://img.shields.io/badge/-NestJS-E0234E?style=flat-square&amp;logo=nestjs&amp;logoColor=white" alt="NestJS" height="22"/>
<img src="https://img.shields.io/badge/-Deno-000000?style=flat-square&amp;logo=deno&amp;logoColor=white" alt="Deno" height="22"/>
<img src="https://img.shields.io/badge/-FastAPI-009688?style=flat-square&amp;logo=fastapi&amp;logoColor=white" alt="FastAPI" height="22"/>
<img src="https://img.shields.io/badge/-Django-092E20?style=flat-square&amp;logo=django&amp;logoColor=white" alt="Django" height="22"/>
<img src="https://img.shields.io/badge/-Flask-000000?style=flat-square&amp;logo=flask&amp;logoColor=white" alt="Flask" height="22"/>
<img src="https://img.shields.io/badge/-REST%20APIs-0B7285?style=flat-square" alt="REST APIs" height="22"/>
<img src="https://img.shields.io/badge/-GraphQL-E10098?style=flat-square&amp;logo=graphql&amp;logoColor=white" alt="GraphQL" height="22"/>
<img src="https://img.shields.io/badge/-WebSocket-334155?style=flat-square" alt="WebSocket" height="22"/>
<img src="https://img.shields.io/badge/-Socket.IO-010101?style=flat-square&amp;logo=socketdotio&amp;logoColor=white" alt="Socket.IO" height="22"/>
<img src="https://img.shields.io/badge/-TypeORM-FE0803?style=flat-square&amp;logo=typeorm&amp;logoColor=white" alt="TypeORM" height="22"/>
<img src="https://img.shields.io/badge/-Zod-3E67B1?style=flat-square&amp;logo=zod&amp;logoColor=white" alt="Zod" height="22"/>
<img src="https://img.shields.io/badge/-Swagger-85EA2D?style=flat-square&amp;logo=swagger&amp;logoColor=black" alt="Swagger" height="22"/>
<img src="https://img.shields.io/badge/-Worker%20Threads-339933?style=flat-square&amp;logo=nodedotjs&amp;logoColor=white" alt="Worker Threads" height="22"/>
<img src="https://img.shields.io/badge/-asyncio-3776AB?style=flat-square&amp;logo=python&amp;logoColor=white" alt="asyncio" height="22"/>
<img src="https://img.shields.io/badge/-Microservices-334155?style=flat-square" alt="Microservices" height="22"/>
<img src="https://img.shields.io/badge/-Web%20Scraping-334155?style=flat-square" alt="Web Scraping" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>Frontend</b></td>
<td>
<img src="https://img.shields.io/badge/-React-61DAFB?style=flat-square&amp;logo=react&amp;logoColor=black" alt="React" height="22"/>
<img src="https://img.shields.io/badge/-Next.js-000000?style=flat-square&amp;logo=nextdotjs&amp;logoColor=white" alt="Next.js" height="22"/>
<img src="https://img.shields.io/badge/-Redux-764ABC?style=flat-square&amp;logo=redux&amp;logoColor=white" alt="Redux" height="22"/>
<img src="https://img.shields.io/badge/-TanStack%20Query-FF4154?style=flat-square&amp;logo=reactquery&amp;logoColor=white" alt="TanStack Query" height="22"/>
<img src="https://img.shields.io/badge/-Tailwind%20CSS-06B6D4?style=flat-square&amp;logo=tailwindcss&amp;logoColor=white" alt="Tailwind CSS" height="22"/>
<img src="https://img.shields.io/badge/-shadcn%2Fui-000000?style=flat-square&amp;logo=shadcnui&amp;logoColor=white" alt="shadcn/ui" height="22"/>
<img src="https://img.shields.io/badge/-Bootstrap-7952B3?style=flat-square&amp;logo=bootstrap&amp;logoColor=white" alt="Bootstrap" height="22"/>
<img src="https://img.shields.io/badge/-Electron-47848F?style=flat-square&amp;logo=electron&amp;logoColor=white" alt="Electron" height="22"/>
<img src="https://img.shields.io/badge/-Micro--frontends-334155?style=flat-square" alt="Micro-frontends" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>Databases and caching</b></td>
<td>
<img src="https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&amp;logo=postgresql&amp;logoColor=white" alt="PostgreSQL" height="22"/>
<img src="https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&amp;logo=mongodb&amp;logoColor=white" alt="MongoDB" height="22"/>
<img src="https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&amp;logo=mysql&amp;logoColor=white" alt="MySQL" height="22"/>
<img src="https://img.shields.io/badge/-Redis-DC382D?style=flat-square&amp;logo=redis&amp;logoColor=white" alt="Redis" height="22"/>
<img src="https://img.shields.io/badge/-Firebase-FFCA28?style=flat-square&amp;logo=firebase&amp;logoColor=black" alt="Firebase" height="22"/>
<img src="https://img.shields.io/badge/-Firestore-FFCA28?style=flat-square&amp;logo=firebase&amp;logoColor=black" alt="Firestore" height="22"/>
<img src="https://img.shields.io/badge/-Couchbase-EA2328?style=flat-square&amp;logo=couchbase&amp;logoColor=white" alt="Couchbase" height="22"/>
<img src="https://img.shields.io/badge/-N1QL-EA2328?style=flat-square&amp;logo=couchbase&amp;logoColor=white" alt="N1QL" height="22"/>
<img src="https://img.shields.io/badge/-AWS%20RDS-527FFF?style=flat-square" alt="AWS RDS" height="22"/>
<img src="https://img.shields.io/badge/-AWS%20DynamoDB-4053D6?style=flat-square" alt="AWS DynamoDB" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>AWS</b></td>
<td>
<img src="https://img.shields.io/badge/-Lambda-FF9900?style=flat-square" alt="Lambda" height="22"/>
<img src="https://img.shields.io/badge/-ECS%20Fargate-FF9900?style=flat-square" alt="ECS Fargate" height="22"/>
<img src="https://img.shields.io/badge/-EC2-FF9900?style=flat-square" alt="EC2" height="22"/>
<img src="https://img.shields.io/badge/-SQS-FF4F8B?style=flat-square" alt="SQS" height="22"/>
<img src="https://img.shields.io/badge/-Kinesis-8C4FFF?style=flat-square" alt="Kinesis" height="22"/>
<img src="https://img.shields.io/badge/-S3-569A31?style=flat-square" alt="S3" height="22"/>
<img src="https://img.shields.io/badge/-CloudFront-8C4FFF?style=flat-square" alt="CloudFront" height="22"/>
<img src="https://img.shields.io/badge/-Lightsail-FF9900?style=flat-square" alt="Lightsail" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>DevOps and observability</b></td>
<td>
<img src="https://img.shields.io/badge/-Terraform-7B42BC?style=flat-square&amp;logo=terraform&amp;logoColor=white" alt="Terraform" height="22"/>
<img src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&amp;logo=docker&amp;logoColor=white" alt="Docker" height="22"/>
<img src="https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat-square&amp;logo=githubactions&amp;logoColor=white" alt="GitHub Actions" height="22"/>
<img src="https://img.shields.io/badge/-GitLab%20CI%2FCD-FC6D26?style=flat-square&amp;logo=gitlab&amp;logoColor=white" alt="GitLab CI/CD" height="22"/>
<img src="https://img.shields.io/badge/-Datadog-632CA6?style=flat-square&amp;logo=datadog&amp;logoColor=white" alt="Datadog" height="22"/>
<img src="https://img.shields.io/badge/-Vercel-000000?style=flat-square&amp;logo=vercel&amp;logoColor=white" alt="Vercel" height="22"/>
<img src="https://img.shields.io/badge/-Netlify-00C7B7?style=flat-square&amp;logo=netlify&amp;logoColor=white" alt="Netlify" height="22"/>
<img src="https://img.shields.io/badge/-DigitalOcean-0080FF?style=flat-square&amp;logo=digitalocean&amp;logoColor=white" alt="DigitalOcean" height="22"/>
<img src="https://img.shields.io/badge/-Heroku-430098?style=flat-square" alt="Heroku" height="22"/>
<img src="https://img.shields.io/badge/-Cloudinary-3448C5?style=flat-square&amp;logo=cloudinary&amp;logoColor=white" alt="Cloudinary" height="22"/>
<img src="https://img.shields.io/badge/-Linux-FCC624?style=flat-square&amp;logo=linux&amp;logoColor=black" alt="Linux" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>Platforms, payments and auth</b></td>
<td>
<img src="https://img.shields.io/badge/-Supabase-3ECF8E?style=flat-square&amp;logo=supabase&amp;logoColor=white" alt="Supabase" height="22"/>
<img src="https://img.shields.io/badge/-KeystoneJS-166BFF?style=flat-square&amp;logo=keystone&amp;logoColor=white" alt="KeystoneJS" height="22"/>
<img src="https://img.shields.io/badge/-Strapi-4945FF?style=flat-square&amp;logo=strapi&amp;logoColor=white" alt="Strapi" height="22"/>
<img src="https://img.shields.io/badge/-Stripe-635BFF?style=flat-square&amp;logo=stripe&amp;logoColor=white" alt="Stripe" height="22"/>
<img src="https://img.shields.io/badge/-Okta-007DC1?style=flat-square&amp;logo=okta&amp;logoColor=white" alt="Okta" height="22"/>
<img src="https://img.shields.io/badge/-JWT-000000?style=flat-square&amp;logo=jsonwebtokens&amp;logoColor=white" alt="JWT" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>AI tools I use daily</b></td>
<td>
<img src="https://img.shields.io/badge/-Claude-D97757?style=flat-square&amp;logo=claude&amp;logoColor=white" alt="Claude" height="22"/>
<img src="https://img.shields.io/badge/-Claude%20Code-D97757?style=flat-square&amp;logo=claude&amp;logoColor=white" alt="Claude Code" height="22"/>
<img src="https://img.shields.io/badge/-ChatGPT-10A37F?style=flat-square" alt="ChatGPT" height="22"/>
<img src="https://img.shields.io/badge/-Gemini-1A73E8?style=flat-square&amp;logo=googlegemini&amp;logoColor=white" alt="Gemini" height="22"/>
<img src="https://img.shields.io/badge/-Google%20Stitch-4285F4?style=flat-square&amp;logo=google&amp;logoColor=white" alt="Google Stitch" height="22"/>
</td>
</tr>
<tr>
<td valign="top" width="170"><b>Tools and collaboration</b></td>
<td>
<img src="https://img.shields.io/badge/-Git-F05032?style=flat-square&amp;logo=git&amp;logoColor=white" alt="Git" height="22"/>
<img src="https://img.shields.io/badge/-GitHub-181717?style=flat-square&amp;logo=github&amp;logoColor=white" alt="GitHub" height="22"/>
<img src="https://img.shields.io/badge/-GitLab-FC6D26?style=flat-square&amp;logo=gitlab&amp;logoColor=white" alt="GitLab" height="22"/>
<img src="https://img.shields.io/badge/-Bitbucket-0052CC?style=flat-square&amp;logo=bitbucket&amp;logoColor=white" alt="Bitbucket" height="22"/>
<img src="https://img.shields.io/badge/-Jira-0052CC?style=flat-square&amp;logo=jira&amp;logoColor=white" alt="Jira" height="22"/>
<img src="https://img.shields.io/badge/-Confluence-172B4D?style=flat-square&amp;logo=confluence&amp;logoColor=white" alt="Confluence" height="22"/>
<img src="https://img.shields.io/badge/-ClickUp-7B68EE?style=flat-square&amp;logo=clickup&amp;logoColor=white" alt="ClickUp" height="22"/>
<img src="https://img.shields.io/badge/-Trello-0052CC?style=flat-square&amp;logo=trello&amp;logoColor=white" alt="Trello" height="22"/>
<img src="https://img.shields.io/badge/-Notion-000000?style=flat-square&amp;logo=notion&amp;logoColor=white" alt="Notion" height="22"/>
<img src="https://img.shields.io/badge/-Slack-4A154B?style=flat-square" alt="Slack" height="22"/>
<img src="https://img.shields.io/badge/-Discord-5865F2?style=flat-square&amp;logo=discord&amp;logoColor=white" alt="Discord" height="22"/>
<img src="https://img.shields.io/badge/-Zoom-0B5CFF?style=flat-square&amp;logo=zoom&amp;logoColor=white" alt="Zoom" height="22"/>
<img src="https://img.shields.io/badge/-Microsoft%20Teams-6264A7?style=flat-square" alt="Microsoft Teams" height="22"/>
<img src="https://img.shields.io/badge/-Postman-FF6C37?style=flat-square&amp;logo=postman&amp;logoColor=white" alt="Postman" height="22"/>
<img src="https://img.shields.io/badge/-Figma-F24E1E?style=flat-square&amp;logo=figma&amp;logoColor=white" alt="Figma" height="22"/>
<img src="https://img.shields.io/badge/-VS%20Code-007ACC?style=flat-square" alt="VS Code" height="22"/>
<img src="https://img.shields.io/badge/-PyCharm-000000?style=flat-square&amp;logo=pycharm&amp;logoColor=white" alt="PyCharm" height="22"/>
<img src="https://img.shields.io/badge/-Windows-0078D6?style=flat-square" alt="Windows" height="22"/>
<img src="https://img.shields.io/badge/-macOS-000000?style=flat-square&amp;logo=apple&amp;logoColor=white" alt="macOS" height="22"/>
<img src="https://img.shields.io/badge/-Agile%20and%20Scrum-334155?style=flat-square" alt="Agile and Scrum" height="22"/>
</td>
</tr>
</table>

**Strongest in:** Node.js, TypeScript, Express, PostgreSQL, MongoDB, Redis, Next.js and React, which I have built with every day since 2021.

## Experience

| Role | Company | Period | Focus |
| --- | --- | --- | --- |
| **Freelance Full-Stack Developer** | Self-employed, Remote | Aug 2025 to present | Building a recurring donations and payments platform for a direct client, end to end. |
| **Senior Software Engineer** | Xavor Corporation, Lahore | May 2025 to Jul 2025 | Designed the backend of a retail price auditing product from scratch, for a US retailer, on AWS. |
| **Senior Software Engineer** | Hashlogics, Lahore | Aug 2022 to Feb 2025 | Led delivery teams across four products, from AI product matching to serverless compliance platforms. Employee of the Month. |
| **Software Engineer** | Memberhood Inc., Germany (Remote) | Mar 2022 to Mar 2023 | Backend and storefront of a multi-merchant membership commerce platform with Stripe. |
| **Software Engineer** | SKUPREME, USA (Remote) | Jun 2022 to Aug 2022 | Front-end work on the web dashboard of a supply chain and inventory product. |
| **Software Engineer** | Homeats, Turkey (Remote) | Mar 2022 to Jun 2022 | Full-stack work on the dashboard and APIs of an online healthy food marketplace. |
| **Associate Software Engineer** | GulzarSoft Software House, Gujrat | Feb 2021 to Feb 2022 | Full-stack JavaScript across several client web applications. |

**Education:** Bachelor of Software Engineering, University of Gujrat, Hafiz Hayat Campus (2016 to 2020)

## How I work

| 1. I find out what you really need | 2. I design within your limits | 3. I deliver on time, honestly |
| --- | --- | --- |
| Even when the full picture is not clear yet. I ask until it is, and explain the options in plain words. | The database you cannot change, the access you cannot give, the budget you have. I solve it inside those. | You hear about risks early, and you get what we agreed, when we agreed it. |

## AI in my work

**How I use it today.** AI is part of my daily engineering workflow. I use Claude and Claude Code, ChatGPT and Gemini for planning, coding, debugging and documentation, and Google Stitch for first-draft UI. It makes me faster, and I still review, test and own everything that ships.

**Where I have worked near it.** At Hashlogics I worked on CivaSource, an AI-assisted product matching service for a supply marketplace, on the Python and FastAPI services and the Redis pipeline that feeds it up to 1,000 products a minute.

**What I am learning next.** LLM engineering: RAG pipelines, agent orchestration, MCP servers and evaluation harnesses, alongside the data stack (ETL pipelines, analytical SQL, dbt, Airflow). The direction is forward deployed engineering, where the job is owning an ambiguous customer problem end to end.

**Open to:** backend and full-stack contracts, platform and API architecture work, backend rescues, AI features in web products, and forward deployed or solutions engineering roles.

## GitHub activity

Every card here updates on its own. The contribution cards count private repositories as well as public ones; the language cards cover public repositories only.

<div align="center">

<img src="https://streak-stats.demolab.com?user=Zagham-Arif&mode=weekly&hide_border=true&card_width=830&background=0B1120&ring=6F8BFF&fire=84CC16&currStreakNum=EEF1F7&sideNums=EEF1F7&currStreakLabel=6F8BFF&sideLabels=A3ADC0&dates=7C869C&stroke=1C2436" alt="Zagham Arif's total GitHub contributions and weekly contribution streak" width="100%"/>

<img src="https://github-readme-activity-graph.ashutosh-dwivedi0710.workers.dev/graph?username=Zagham-Arif&bg_color=0b1120&color=a3adc0&line=6f8bff&point=eef1f7&area=true&area_color=6f8bff&hide_border=true&radius=12&custom_title=Contributions%20in%20the%20last%2031%20days" alt="Zagham Arif's GitHub contributions per day over the last 31 days" width="100%"/>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Zagham-Arif&theme=github_dark" alt="Zagham Arif's top languages by commit, public repositories" height="180"/>
<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Zagham-Arif&theme=github_dark" alt="Zagham Arif's repositories per language, public repositories" height="180"/>

[![Coding time on WakaTime](https://wakatime.com/badge/user/100a5bcb-5d54-4c30-8c40-91745016eff8.svg?style=for-the-badge)](https://wakatime.com/@100a5bcb-5d54-4c30-8c40-91745016eff8)

</div>

## Let's talk

Got a backend that needs to hold up? Freelance projects, backend rescues, or a senior remote role: tell me what you are building.

<div align="center">

[![Book a call](https://img.shields.io/badge/Book%20a%20call-Topmate-E44332?style=for-the-badge)](https://topmate.io/zagham_arif)
[![Hire me on Upwork](https://img.shields.io/badge/Hire%20me-Upwork-6FDA44?style=for-the-badge&logo=upwork&logoColor=white)](https://www.upwork.com/freelancers/~01b58b210c60ff7195)
[![Email](https://img.shields.io/badge/Email-zaghamarif@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zaghamarif@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-zagham--portfolio.vercel.app-3B5BFD?style=for-the-badge&logo=vercel&logoColor=white)](https://zagham-portfolio.vercel.app)

</div>
