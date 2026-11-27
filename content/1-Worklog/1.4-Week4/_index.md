---
title: "Week 4 Worklog"
date: 2026-09-14
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Start my part of the shop-ai project: sign-up (Cognito PreSignUp), safe ordering with DynamoDB, and the web interface.
* Finish the cart module: guest cart, cart merge and the server-side cart API.
* Study AI/ML and data analytics services (Module 8 of AWS Cloud Practitioner Essentials).

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                                                                                                                                                                             |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 2   | - Learn the PreSignUp Lambda trigger, cold starts, memory and timeouts <br> - **Project:** when a customer signs up, detect a duplicate username and show the right message, instead of a generic error caused by Lambda running over 3 seconds                                                                 | 05/10/2026 | 05/10/2026      | <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-lambda-pre-sign-up.html> <br> <https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html>                                              |
| 3   | - Apply DynamoDB transactions and condition expressions (stock decrement, open-order counter) to the project: <br>&emsp; + An order can never sell more than the stock <br>&emsp; + Stock is never decremented without removing the item from the cart <br>&emsp; + A strict limit of 3 open orders per account | 06/10/2026 | 06/10/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_TransactWriteItems.html> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/BestPractices_PessimisticLocking.html>                     |
| 4   | - Build the cart module (one week ahead of plan): <br>&emsp; + Guest cart and merging the cart on sign-in (#56, #58) <br>&emsp; + Server-side cart API (#94): the cart Lambda only reads the products table with BatchGetItem <br>&emsp; + Cart merge API `POST /cart/merge` (#97)                              | 07/10/2026 | 07/10/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_BatchGetItem.html>                                                                                                                                         |
| 5   | - Learn pre-built AI services: Amazon Comprehend, Polly, Transcribe, Translate, Kendra, Rekognition, Lex, Personalize <br> - Learn Amazon SageMaker AI, and ML infrastructure and frameworks on AWS                                                                                                             | 08/10/2026 | 08/10/2026      | AWS Cloud Practitioner Essentials, Module 8 - AI/ML and Data Analytics <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                           |
| 6   | - Learn data ingestion services: Amazon Kinesis Data Streams, Data Firehose, S3, Redshift <br> - Learn data processing services: AWS Glue, Amazon EMR <br> - Learn data analysis and visualisation services: Amazon Athena, Redshift, QuickSight, OpenSearch Service                                            | 09/10/2026 | 09/10/2026      | AWS Cloud Practitioner Essentials, Module 8 - AI/ML and Data Analytics <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                           |
| 7   | - Learn and apply React Router, TanStack Query, CSS Modules and design tokens to the project: <br>&emsp; + The web app caches data and makes no unnecessary API calls <br>&emsp; + A consistent interface following the design system without a UI library                                                      | 10/10/2026 | 10/10/2026      | <https://tanstack.com/query/latest/docs/framework/react/overview> <br> <https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties> <br> <https://github.com/css-modules/css-modules> |


### Week 4 Achievements:

* Fixed the sign-up error with the PreSignUp Lambda:
  * Detect duplicate usernames and show the right message
  * Understood how cold starts, memory and timeouts affect Lambda run time

* Ordering uses conditional DynamoDB transactions:
  * Stock decrement, cart removal and order counter succeed or fail together
  * Stock is never oversold
  * The 3-open-order limit per account always holds

* Finished the cart module:
  * Guest cart and cart merge on sign-in
  * Server-side cart API, with the cart Lambda limited to BatchGetItem on the products table
  * Finished one week ahead of plan

* Got the overall picture of AI/ML and data on AWS:
  * Pre-built AI services and Amazon SageMaker AI
  * Ingestion: Kinesis, Data Firehose
  * Processing: Glue, EMR
  * Analysis: Athena, Redshift, QuickSight, OpenSearch

* Project web interface:
  * TanStack Query caches data and avoids unnecessary API calls
  * React Router for navigation
  * CSS Modules and design tokens, no UI library needed
