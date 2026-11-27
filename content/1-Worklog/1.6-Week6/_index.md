---
title: "Week 6 Worklog"
date: 2026-09-14
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Release the first version v0.1.0 to production with the team.
* Review everything learned in weeks 1 to 5 and fill in the services shop-ai uses that I had not studied properly.
* Understand how API Gateway (HTTP API) authenticates with Cognito JWTs, how SNS and SQS work together, how to store secrets and run scheduled jobs.
* Understand protecting a static site on S3 with CloudFront, monitoring (X-Ray, Logs Insights, alarms) and CI/CD into AWS with OIDC.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                                                                                                                                                                                                                                                                                                                                        |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **The team releases the first version v0.1.0 to production** <br> - Learn Amazon Cognito User Pools: sign-up, sign-in, user groups, ID tokens and access tokens <br> - Learn Amazon API Gateway HTTP APIs and JWT authorizers: <br>&emsp; + Routes that need sign-in check the Cognito token, and a missing token returns 401 <br>&emsp; + Compare HTTP APIs with REST APIs (price, features) | 19/10/2026 | 19/10/2026      | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html> <br> <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-jwt-authorizer.html> <br> <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html>                                                                                                            |
| 3   | - Learn Amazon SNS and the SNS → SQS fan-out pattern: <br>&emsp; + One `order-confirmed` message reaches several queues (send email, record purchases for recommendations) <br> - Learn SQS: Standard and FIFO queues, visibility timeout, long polling                                                                                                                                         | 20/10/2026 | 20/10/2026      | <https://docs.aws.amazon.com/sns/latest/dg/sns-sqs-as-subscriber.html> <br> <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-visibility-timeout.html> <br> <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html>                                                                                    |
| 4   | - Learn AWS Systems Manager Parameter Store: SecureString parameters encrypted with KMS, read permissions by path <br> - Learn Amazon EventBridge Scheduler: invoke Lambda on a schedule (for example the 02:00 recommendation job) <br> - Learn DynamoDB Global Secondary Indexes (GSI) to query by a different key                                                                            | 21/10/2026 | 21/10/2026      | <https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html> <br> <https://docs.aws.amazon.com/systems-manager/latest/userguide/secure-string-parameter-kms-encryption.html> <br> <https://docs.aws.amazon.com/scheduler/latest/UserGuide/what-is-scheduler.html> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html> |
| 5   | - Learn serving a static site securely with S3 + CloudFront: <br>&emsp; + Origin Access Control (OAC): the bucket blocks public access and only CloudFront can read it <br>&emsp; + Response headers policies to add security headers <br>&emsp; + Cache behaviors: route `/api/*` to API Gateway                                                                                               | 22/10/2026 | 22/10/2026      | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/understanding-response-headers-policies.html> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html>                                  |
| 6   | - Learn monitoring serverless applications: <br>&emsp; + Powertools Logger and Tracer for Lambda (JSON logs with a correlation ID) <br>&emsp; + AWS X-Ray to follow one request across several Lambdas <br>&emsp; + CloudWatch Logs Insights to query logs <br>&emsp; + CloudWatch Alarms sending email through SNS                                                                             | 23/10/2026 | 23/10/2026      | <https://docs.aws.amazon.com/powertools/typescript/latest/features/logger/> <br> <https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html> <br> <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html> <br> <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html>                                                      |
| 7   | - Learn CI/CD into AWS with GitHub Actions and OIDC: <br>&emsp; + The job requests an OIDC token and assumes an IAM role, with no stored access keys <br>&emsp; + Trust policies restricted by repository, branch and environment <br> - Learn AWS CloudTrail: read `AssumeRoleWithWebIdentity` events to check who deployed                                                                    | 24/10/2026 | 24/10/2026      | <https://docs.github.com/en/actions/security-for-github-actions/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services> <br> <https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html> <br> <https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html>                                           |


### Week 6 Achievements:

* Released v0.1.0, the first version of shop-ai, to production with the team on 19/10.

* Reviewed the first 5 weeks and filled the gaps compared with shop-ai's real architecture.

* Authentication and APIs:
  * Understood how Cognito User Pools issue ID tokens, access tokens and user groups
  * HTTP APIs use a JWT authorizer to check the token before calling Lambda
  * Know why the project chose HTTP API over REST API: cheaper, with a built-in JWT authorizer

* Asynchronous messaging:
  * The SNS → multiple SQS fan-out pattern
  * Visibility timeout, long polling, Standard versus FIFO

* Secrets, schedules and data:
  * Store secret keys in Parameter Store as SecureString
  * Run scheduled jobs with EventBridge Scheduler
  * Use a GSI to query DynamoDB by a different key

* Understood how S3 + CloudFront + OAC keeps the bucket private while the site stays fast, with security headers and `/api/*` routing.

* Monitoring and deployment:
  * Read JSON logs, X-Ray traces and Logs Insights queries to track down errors
  * CloudWatch Alarms emailing through SNS
  * GitHub Actions deploying with OIDC and no access keys; verified with CloudTrail
