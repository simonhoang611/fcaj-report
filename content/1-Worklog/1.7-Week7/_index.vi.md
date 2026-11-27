---
title: "Worklog Tuần 7"
date: 2026-09-14
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Hoàn thành khoá AWS Cloud Practitioner Essentials với Module 13 (Well-Architected).
* Làm cho luồng đặt hàng của shop-ai bền vững: chống tạo đơn trùng (idempotency), xử lý lỗi hàng đợi SQS, gửi email qua Amazon SES.
* Đưa hạ tầng dự án qua CDK v2 kèm kiểm tra bảo mật cdk-nag.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                                                           |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Tìm hiểu nhóm dịch vụ phát triển: AWS CodeBuild, CodePipeline, X-Ray, AppSync, Amplify <br> - Tìm hiểu nhóm ứng dụng doanh nghiệp: Amazon Connect, Amazon SES <br> - Tìm hiểu nhóm máy tính người dùng cuối: AppStream 2.0, WorkSpaces, WorkSpaces Secure Browser <br> - Tìm hiểu AWS IoT Core | 26/10/2026   | 26/10/2026      | AWS Cloud Practitioner Essentials, Module 13 - Well-Architected Solutions <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                                                  |
| 3   | - Tìm hiểu AWS Well-Architected Tool và cách tối ưu một kiến trúc đám mây                                                                                                                                                                                                                        | 27/10/2026   | 27/10/2026      | AWS Cloud Practitioner Essentials, Module 13 - Well-Architected Solutions <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                                                  |
| 4   | - Tìm hiểu Idempotency-Key, Powertools Idempotency, DynamoDB TTL và áp dụng vào dự án: <br>&emsp; + Khách bấm "Đặt hàng" hai lần hoặc mạng gửi lại request thì vẫn chỉ tạo một đơn <br>&emsp; + Bảng lưu khoá tự dọn bằng TTL, không tốn thêm chi phí                                            | 28/10/2026   | 28/10/2026      | <https://docs.aws.amazon.com/powertools/typescript/latest/features/idempotency/> <br> <https://datatracker.ietf.org/doc/html/draft-ietf-httpapi-idempotency-key-header> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/TTL.html> |
| 5   | - Tìm hiểu và áp dụng cho Lambda đọc SQS: partial batch failure, DLQ, xử lý message nhận trùng: <br>&emsp; + Đơn không bị mất khi email hay hệ thống phía sau lỗi hoặc quá tải <br>&emsp; + Message nhận trùng không gửi hai email                                                               | 29/10/2026   | 29/10/2026      | <https://docs.aws.amazon.com/lambda/latest/dg/services-sqs-errorhandling.html> <br> <https://docs.aws.amazon.com/powertools/typescript/latest/features/batch/>                                                                                           |
| 6   | - Tìm hiểu hạ tầng bằng CDK v2 và cdk-nag: <br>&emsp; + Mọi thay đổi hạ tầng đi qua code và PR <br>&emsp; + Tạo lại được dev, staging, prod giống nhau <br>&emsp; + Bắt lỗi cấu hình bảo mật trước khi deploy                                                                                    | 30/10/2026   | 30/10/2026      | <https://github.com/cdklabs/cdk-nag> <br> <https://docs.aws.amazon.com/cdk/api/v2/docs/aws-cdk-lib.aws_apigatewayv2_authorizers-readme.html>                                                                                                             |
| 7   | - Áp dụng Amazon SES (sandbox) cho dự án để gửi thư xác nhận và thư huỷ đơn cho khách <br> - Tìm hiểu vì sao trên môi trường dev chỉ email đã xác minh mới nhận được thư                                                                                                                         | 31/10/2026   | 31/10/2026      | <https://docs.aws.amazon.com/ses/latest/dg/request-production-access.html> <br> <https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html>                                                                                                     |


### Kết quả đạt được tuần 7:

* Hoàn thành khoá AWS Cloud Practitioner Essentials; nắm 6 trụ cột Well-Architected và dùng Well-Architected Tool.

* Đặt hàng chống trùng:
  * API nhận header Idempotency-Key
  * Powertools Idempotency lưu kết quả lần đầu, bấm hai lần vẫn chỉ ra một đơn
  * Khoá cũ tự xoá bằng DynamoDB TTL

* Hàng đợi đơn hàng bền vững:
  * Lambda đọc SQS báo lỗi theo từng message (partial batch failure)
  * Message lỗi nhiều lần vào DLQ thay vì mất
  * Message nhận trùng không gửi hai email

* Hạ tầng bằng CDK v2 và cdk-nag:
  * Mọi thay đổi đi qua code và PR
  * dev, staging, prod dựng giống nhau
  * Chặn cấu hình thiếu bảo mật trước khi deploy

* Email xác nhận và huỷ đơn chạy qua Amazon SES; hiểu giới hạn sandbox và thủ tục xin quyền production.
