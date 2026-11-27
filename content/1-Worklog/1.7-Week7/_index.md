---
title: "Week 7 Worklog"
date: 2026-09-14
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Finish AWS Cloud Practitioner Essentials with Module 13 (Well-Architected).
* Make shop-ai's ordering flow resilient: prevent duplicate orders (idempotency), handle SQS queue failures, send email through Amazon SES.
* Manage the project infrastructure with CDK v2 and cdk-nag security checks.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                       | Start Date | Completion Date | Reference Material                                                                                                                                                                                                                                       |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Learn developer services: AWS CodeBuild, CodePipeline, X-Ray, AppSync, Amplify <br> - Learn business application services: Amazon Connect, Amazon SES <br> - Learn end-user computing services: AppStream 2.0, WorkSpaces, WorkSpaces Secure Browser <br> - Learn AWS IoT Core           | 26/10/2026 | 26/10/2026      | AWS Cloud Practitioner Essentials, Module 13 - Well-Architected Solutions <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                                                  |
| 3   | - Learn the AWS Well-Architected Tool and how to optimise a cloud architecture                                                                                                                                                                                                             | 27/10/2026 | 27/10/2026      | AWS Cloud Practitioner Essentials, Module 13 - Well-Architected Solutions <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                                                  |
| 4   | - Learn Idempotency-Key, Powertools Idempotency and DynamoDB TTL, and apply them to the project: <br>&emsp; + If a customer clicks "Place order" twice or the network resends the request, only one order is created <br>&emsp; + The key table cleans itself up with TTL at no extra cost | 28/10/2026 | 28/10/2026      | <https://docs.aws.amazon.com/powertools/typescript/latest/features/idempotency/> <br> <https://datatracker.ietf.org/doc/html/draft-ietf-httpapi-idempotency-key-header> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/TTL.html> |
| 5   | - Learn and apply for the SQS-consuming Lambda: partial batch failure, DLQ, handling duplicate messages: <br>&emsp; + Orders are not lost when email or downstream systems fail or are overloaded <br>&emsp; + A duplicate message does not send two emails                                | 29/10/2026 | 29/10/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/services-sqs-errorhandling.html> <br> <https://docs.aws.amazon.com/powertools/typescript/latest/features/batch/>                                                                                           |
| 6   | - Learn infrastructure with CDK v2 and cdk-nag: <br>&emsp; + Every infrastructure change goes through code and a PR <br>&emsp; + dev, staging and prod can be recreated identically <br>&emsp; + Security misconfigurations are caught before deploying                                    | 30/10/2026 | 30/10/2026      | <https://github.com/cdklabs/cdk-nag> <br> <https://docs.aws.amazon.com/cdk/api/v2/docs/aws-cdk-lib.aws_apigatewayv2_authorizers-readme.html>                                                                                                             |
| 7   | - Apply Amazon SES (sandbox) to the project to send order confirmation and cancellation emails <br> - Understand why on the dev environment only verified email addresses receive mail                                                                                                     | 31/10/2026 | 31/10/2026      | <https://docs.aws.amazon.com/ses/latest/dg/request-production-access.html> <br> <https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html>                                                                                                     |


### Week 7 Achievements:

* Finished AWS Cloud Practitioner Essentials; understood the 6 Well-Architected pillars and used the Well-Architected Tool.

* Duplicate-safe ordering:
  * The API accepts an Idempotency-Key header
  * Powertools Idempotency stores the first result, so a double click still creates one order
  * Old keys are removed by DynamoDB TTL

* Resilient order queue:
  * The SQS-consuming Lambda reports failures per message (partial batch failure)
  * Messages that keep failing go to a DLQ instead of being lost
  * Duplicate messages do not send two emails

* Infrastructure with CDK v2 and cdk-nag:
  * Every change goes through code and a PR
  * dev, staging and prod are built the same way
  * Insecure configuration is blocked before deploying

* Order confirmation and cancellation emails go through Amazon SES; understood the sandbox limit and how to request production access.
