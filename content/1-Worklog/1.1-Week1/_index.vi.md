---
title: "Worklog Tuần 1"
date: 2026-09-14
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Nắm nội quy, quy định của đơn vị thực tập; tạo tài khoản AWS Free Tier và nhận credit thực hành.
* Làm quen các dịch vụ nền tảng của AWS: IAM, VPC, EC2, Auto Scaling, CloudWatch.
* Thực hành nhóm dịch vụ lưu trữ và cơ sở dữ liệu: S3, CloudFront, RDS, DynamoDB, ElastiCache; thử AWS Managed Directory Service.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                         |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập <br> - Tạo tài khoản AWS Free Tier                                                                                                                                                                                                                                                                                                   | 14/09/2026   | 14/09/2026      | <https://hcm-rules.awsfcaj.com/1-regulations/> <br> <https://000001.awsfcaj.com/1-aws-free-tier-2025-revolution/>                      |
| 3   | - Hoàn thành 5 bài lab trên AWS Console để nhận $100 credit                                                                                                                                                                                                                                                                                                                                   | 15/09/2026   | 15/09/2026      | <https://000001.awsfcaj.com/3-chi%E1%BA%BFn-l%C6%B0%E1%BB%A3c-nh%E1%BA%ADn-%C4%91%E1%BB%A7-200-credit/>                                |
| 4   | - Tìm hiểu IAM Access Control và workshop Amazon VPC, AWS Site-to-Site VPN <br> - **Thực hành:** <br>&emsp; + Tạo IAM Group, Role, User; chuyển đổi giữa các role <br>&emsp; + Tạo VPC, Subnet, Internet Gateway, Route Table, Security Group <br>&emsp; + Bật VPC Flow Logs; triển khai EC2 instance trong VPC                                                                               | 16/09/2026   | 16/09/2026      | <https://000002.awsfcaj.com/> <br> <https://000003.awsfcaj.com/>                                                                       |
| 5   | - Tìm hiểu Amazon EC2, EC2 Auto Scaling, CloudWatch <br> - **Thực hành:** <br>&emsp; + Khởi tạo instance Windows, Linux; triển khai Node.js trên Amazon Linux và EC2 Windows <br>&emsp; + Tạo Launch Template, Auto Scaling Group; thiết lập Load Balancer <br>&emsp; + Triển khai CloudFormation stack; quan sát CloudWatch Metrics, Logs, Alarms, Dashboards                                | 17/09/2026   | 17/09/2026      | <https://000004.awsfcaj.com/> <br> <https://000006.awsfcaj.com/> <br> <https://000008.awsfcaj.com/>                                    |
| 6   | - Tìm hiểu AWS CloudShell, Amazon S3, Amazon RDS, DynamoDB <br> - **Thực hành:** <br>&emsp; + Tạo môi trường CloudShell và thao tác bằng AWS CLI <br>&emsp; + Thao tác với S3 bucket; dùng CloudFront để tăng tốc website tĩnh trên S3 <br>&emsp; + Khởi tạo RDS database instance và sử dụng database <br>&emsp; + Tạo bảng, ghi, đọc, truy vấn DynamoDB bằng Console, CloudShell và AWS SDK | 18/09/2026   | 18/09/2026      | <https://000049.awsfcaj.com/> <br> <https://000057.awsfcaj.com/> <br> <https://000005.awsfcaj.com/> <br> <https://000060.awsfcaj.com/> |
| 7   | - Tìm hiểu Amazon ElastiCache (Redis), CloudFront, AWS Managed Directory Service <br> - **Thực hành:** <br>&emsp; + Tạo ElastiCache cluster bằng Console và CLI; ghi, đọc dữ liệu bằng AWS SDK <br>&emsp; + Lưu trữ nội dung web tĩnh trong S3 bucket <br>&emsp; + Triển khai AWS Managed Directory Service; cấu hình EC2 kết nối với AD Manager                                              | 19/09/2026   | 19/09/2026      | <https://000061.awsfcaj.com/> <br> <https://000094.awsfcaj.com/> <br> <https://000095.awsfcaj.com/>                                    |


### Kết quả đạt được tuần 1:

* Nắm được nội quy, quy định và cách làm việc tại đơn vị thực tập.

* Tạo thành công tài khoản AWS Free Tier, hoàn thành 5 bài lab để nhận $100 credit.

* Thực hành được các dịch vụ nền tảng:
  * IAM: tạo Group, User, Role và chuyển đổi giữa các role
  * VPC: Subnet, Internet Gateway, Route Table, Security Group, VPC Flow Logs
  * EC2: instance Linux và Windows, triển khai Node.js
  * Launch Template, Auto Scaling Group và Load Balancer

* Làm quen giám sát và hạ tầng dạng code:
  * Triển khai stack CloudFormation
  * Đọc CloudWatch Metrics, Logs; tạo Alarm và Dashboard

* Thực hành nhóm lưu trữ và cơ sở dữ liệu:
  * CloudShell và AWS CLI
  * S3 website tĩnh phân phối qua CloudFront
  * RDS, DynamoDB (Console, CLI, SDK)
  * ElastiCache Redis qua AWS SDK

* Triển khai AWS Managed Directory Service và nối EC2 vào domain.
