---
title: "Worklog Tuần 4"
date: 2026-09-14
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Bắt đầu làm phần việc của mình trong dự án shop-ai: đăng ký tài khoản (Cognito PreSignUp), đặt hàng an toàn với DynamoDB, giao diện web.
* Làm xong module giỏ hàng: giỏ khách vãng lai, gộp giỏ và API giỏ phía server.
* Học nhóm dịch vụ AI/ML và phân tích dữ liệu (Module 8 khoá AWS Cloud Practitioner Essentials).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                                 |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 2   | - Tìm hiểu Lambda trigger PreSignUp, cold start, bộ nhớ và timeout <br> - **Dự án:** khi khách đăng ký, kiểm được username trùng và báo đúng câu cho khách, thay vì lỗi chung do Lambda chạy quá 3 giây                                                                                   | 05/10/2026   | 05/10/2026      | <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-lambda-pre-sign-up.html> <br> <https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html>                                              |
| 3   | - Áp dụng DynamoDB transaction và condition expression (trừ kho, bộ đếm đơn đang mở) vào dự án: <br>&emsp; + Đặt đơn không bao giờ bán quá tồn kho <br>&emsp; + Không có chuyện trừ kho mà quên bỏ món khỏi giỏ <br>&emsp; + Giới hạn đúng tuyệt đối 3 đơn đang mở cho mỗi tài khoản      | 06/10/2026   | 06/10/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_TransactWriteItems.html> <br> <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/BestPractices_PessimisticLocking.html>                     |
| 4   | - Làm module giỏ hàng (xong sớm 1 tuần so với kế hoạch): <br>&emsp; + Giỏ cho khách chưa đăng nhập và gộp giỏ khi đăng nhập (#56, #58) <br>&emsp; + API giỏ hàng phía server (#94): Lambda cart chỉ đọc bảng sản phẩm bằng BatchGetItem <br>&emsp; + API gộp giỏ `POST /cart/merge` (#97) | 07/10/2026   | 07/10/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_BatchGetItem.html>                                                                                                                                         |
| 5   | - Tìm hiểu nhóm dịch vụ AI dựng sẵn: Amazon Comprehend, Polly, Transcribe, Translate, Kendra, Rekognition, Lex, Personalize <br> - Tìm hiểu Amazon SageMaker AI, hạ tầng và framework ML trên AWS                                                                                         | 08/10/2026   | 08/10/2026      | AWS Cloud Practitioner Essentials, Module 8 - AI/ML and Data Analytics <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                           |
| 6   | - Tìm hiểu dịch vụ thu nhận dữ liệu: Amazon Kinesis Data Streams, Data Firehose, S3, Redshift <br> - Tìm hiểu dịch vụ xử lý dữ liệu: AWS Glue, Amazon EMR <br> - Tìm hiểu dịch vụ phân tích và trực quan hoá: Amazon Athena, Redshift, QuickSight, OpenSearch Service                     | 09/10/2026   | 09/10/2026      | AWS Cloud Practitioner Essentials, Module 8 - AI/ML and Data Analytics <br> <https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7>                                                           |
| 7   | - Tìm hiểu và áp dụng React Router, TanStack Query, CSS Modules và design token vào dự án: <br>&emsp; + Web có cache dữ liệu, không gọi API thừa <br>&emsp; + Giao diện thống nhất theo design system mà không cần thư viện UI                                                            | 10/10/2026   | 10/10/2026      | <https://tanstack.com/query/latest/docs/framework/react/overview> <br> <https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties> <br> <https://github.com/css-modules/css-modules> |


### Kết quả đạt được tuần 4:

* Sửa được lỗi đăng ký tài khoản bằng Lambda PreSignUp:
  * Kiểm username trùng và báo đúng câu cho khách
  * Hiểu cold start, bộ nhớ, timeout ảnh hưởng tới thời gian chạy Lambda

* Luồng đặt hàng dùng DynamoDB transaction có điều kiện:
  * Trừ kho, bỏ món khỏi giỏ, tăng bộ đếm đơn cùng thành công hoặc cùng thất bại
  * Không bán quá tồn kho
  * Giới hạn 3 đơn đang mở mỗi tài khoản luôn đúng

* Hoàn thành module giỏ hàng:
  * Giỏ cho khách chưa đăng nhập và gộp giỏ khi đăng nhập
  * API giỏ phía server, Lambda cart chỉ có quyền BatchGetItem trên bảng sản phẩm
  * Xong sớm 1 tuần so với kế hoạch

* Nắm bức tranh AI/ML và dữ liệu trên AWS:
  * Dịch vụ AI dựng sẵn và Amazon SageMaker AI
  * Thu nhận dữ liệu: Kinesis, Data Firehose
  * Xử lý: Glue, EMR
  * Phân tích: Athena, Redshift, QuickSight, OpenSearch

* Giao diện web của dự án:
  * TanStack Query cache dữ liệu, không gọi API thừa
  * React Router để điều hướng
  * CSS Modules và design token, không cần thư viện UI
