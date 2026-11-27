---
title: "Worklog Tuần 6"
date: 2026-09-14
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Cùng nhóm phát hành bản đầu tiên v0.1.0 lên production.
* Rà lại toàn bộ kiến thức đã học từ tuần 1 đến tuần 5, bổ sung các dịch vụ mà dự án shop-ai dùng nhưng chưa học bài bản.
* Nắm cách API Gateway (HTTP API) xác thực bằng JWT của Cognito, cách SNS và SQS phối hợp, cách lưu bí mật và chạy job theo lịch.
* Nắm cách bảo vệ web tĩnh trên S3 bằng CloudFront, cách giám sát (X-Ray, Logs Insights, alarm) và cách CI/CD vào AWS bằng OIDC.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                                                                                                                                                                                            |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Nhóm phát hành bản đầu tiên v0.1.0 lên production** <br> - Tìm hiểu Amazon Cognito User Pool: đăng ký, đăng nhập, nhóm người dùng, ID token và access token <br> - Tìm hiểu Amazon API Gateway HTTP API và JWT authorizer: <br>&emsp; + Route cần đăng nhập thì kiểm token Cognito, thiếu token trả 401 <br>&emsp; + So sánh HTTP API với REST API (giá, tính năng) | 19/10/2026   | 19/10/2026      | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html> <br> <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-jwt-authorizer.html> <br> <https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-vs-rest.html>                                                                                                            |
| 3   | - Tìm hiểu Amazon SNS và mô hình fan-out SNS → SQS: <br>&emsp; + Một tin `order-confirmed` gửi tới nhiều hàng đợi (gửi email, ghi lượt mua cho gợi ý) <br> - Tìm hiểu SQS: hàng đợi Standard và FIFO, visibility timeout, long polling                                                                                                                                  | 20/10/2026   | 20/10/2026      | <https://docs.aws.amazon.com/sns/latest/dg/sns-sqs-as-subscriber.html> <br> <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-visibility-timeout.html> <br> <https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html>                                                                                    |
| 4   | - Tìm hiểu AWS Systems Manager Parameter Store: tham số SecureString mã hoá bằng KMS, phân quyền đọc theo đường dẫn <br> - Tìm hiểu Amazon EventBridge Scheduler: gọi Lambda theo lịch (ví dụ job tính gợi ý lúc 02:00) <br> - Tìm hiểu DynamoDB Global Secondary Index (GSI) để truy vấn theo khoá khác                                                                | 21/10/2026   | 21/10/2026      | <https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html> <br> <https://docs.aws.amazon.com/systems-manager/latest/userguide/secure-string-parameter-kms-encryption.html> <br> <https://docs.aws.amazon.com/scheduler/latest/UserGuide/what-is-scheduler.html> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html> |
| 5   | - Tìm hiểu cách phục vụ web tĩnh an toàn bằng S3 + CloudFront: <br>&emsp; + Origin Access Control (OAC): bucket chặn truy cập công khai, chỉ CloudFront đọc được <br>&emsp; + Response headers policy để thêm header bảo mật <br>&emsp; + Cache behavior: tách đường dẫn `/api/*` sang API Gateway                                                                      | 22/10/2026   | 22/10/2026      | <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/understanding-response-headers-policies.html> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html>                                  |
| 6   | - Tìm hiểu giám sát ứng dụng serverless: <br>&emsp; + Powertools Logger và Tracer cho Lambda (log JSON có mã tương quan) <br>&emsp; + AWS X-Ray xem đường đi của một request qua nhiều Lambda <br>&emsp; + CloudWatch Logs Insights để truy vấn log <br>&emsp; + CloudWatch Alarm gửi email qua SNS                                                                     | 23/10/2026   | 23/10/2026      | <https://docs.aws.amazon.com/powertools/typescript/latest/features/logger/> <br> <https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html> <br> <https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html> <br> <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html>                                                      |
| 7   | - Tìm hiểu CI/CD vào AWS bằng GitHub Actions và OIDC: <br>&emsp; + Job xin token OIDC rồi assume IAM role, không lưu access key <br>&emsp; + Trust policy giới hạn theo repo, nhánh, environment <br> - Tìm hiểu AWS CloudTrail: đọc sự kiện `AssumeRoleWithWebIdentity` để kiểm tra ai đã deploy                                                                       | 24/10/2026   | 24/10/2026      | <https://docs.github.com/en/actions/security-for-github-actions/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services> <br> <https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html> <br> <https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html>                                           |


### Kết quả đạt được tuần 6:

* Cùng nhóm phát hành v0.1.0, bản đầu tiên của shop-ai, lên production ngày 19/10.

* Rà lại kiến thức 5 tuần đầu và lấp được các chỗ còn thiếu so với kiến trúc thật của shop-ai.

* Xác thực và API:
  * Hiểu Cognito User Pool cấp ID token, access token và nhóm người dùng
  * HTTP API dùng JWT authorizer kiểm token trước khi gọi Lambda
  * Biết vì sao dự án chọn HTTP API thay vì REST API: rẻ hơn, có sẵn JWT authorizer

* Nhắn tin bất đồng bộ:
  * Mô hình fan-out SNS → nhiều SQS
  * Visibility timeout, long polling, khác biệt Standard và FIFO

* Bí mật, lịch chạy và dữ liệu:
  * Lưu khoá bí mật trong Parameter Store dạng SecureString
  * Chạy job theo lịch bằng EventBridge Scheduler
  * Dùng GSI để truy vấn DynamoDB theo khoá khác

* Hiểu cách S3 + CloudFront + OAC giữ bucket riêng tư mà web vẫn tải nhanh, kèm header bảo mật và tách đường dẫn `/api/*`.

* Giám sát và triển khai:
  * Đọc log JSON, trace X-Ray và truy vấn Logs Insights để lần ra lỗi
  * Alarm CloudWatch báo email qua SNS
  * GitHub Actions deploy bằng OIDC, không cần access key; kiểm lại bằng CloudTrail
