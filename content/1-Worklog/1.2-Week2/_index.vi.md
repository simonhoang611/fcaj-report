---
title: "Worklog Tuần 2"
date: 2026-09-14
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tìm hiểu kết nối hybrid giữa on-premise và AWS: Hybrid DNS, Route 53 Resolver, VM Import/Export.
* Tự động hoá vận hành với Lambda và AWS Systems Manager; dựng hạ tầng bằng code với CloudFormation và CDK.
* Quản lý chi phí và bảo mật mạng: giới hạn tài nguyên bằng IAM, Data Lifecycle Manager, VPC Endpoint, AWS WAF.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                           | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                      |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------- |
| 2   | - Tìm hiểu Hybrid DNS, Route 53 Resolver, VM Import/Export <br> - **Thực hành:** <br>&emsp; + Kết nối Remote Desktop Gateway (RDGW) bằng giao thức RDP <br>&emsp; + Giả lập DNS on-premise với AWS Directory Service; thiết lập DNS <br>&emsp; + Import máy ảo vào AWS; export máy ảo từ on-premise và từ EC2 instance                                                              | 21/09/2026   | 21/09/2026      | <https://000010.awsfcaj.com/> <br> <https://000014.awsfcaj.com/>    |
| 3   | - Tìm hiểu AWS Lambda, AWS Systems Manager <br> - **Thực hành:** <br>&emsp; + Viết code và cấu hình Lambda để tự động hoá tác vụ <br>&emsp; + Dùng Systems Manager để quản lý Windows instance                                                                                                                                                                                      | 22/09/2026   | 22/09/2026      | <https://000022.awsfcaj.com/> <br> <https://000031.awsfcaj.com/>    |
| 4   | - Tìm hiểu CloudFormation và CDK nâng cao <br> - **Thực hành:** <br>&emsp; + Dùng CloudFormation cơ bản và nâng cao để tham chiếu tài nguyên giữa các stack <br>&emsp; + Dùng CDK dựng kiến trúc gồm API Gateway, Elastic Load Balancer, ECS và Lambda; dùng nested stack                                                                                                           | 23/09/2026   | 23/09/2026      | <https://000037.awsfcaj.com/> <br> <https://000076.awsfcaj.com/>    |
| 5   | - Tìm hiểu Infrastructure as Code và tối ưu tài nguyên EC2 <br> - **Thực hành:** tạo Lambda function và triển khai kiến trúc ba tầng (Three-Tier Architecture)                                                                                                                                                                                                                      | 24/09/2026   | 24/09/2026      | <https://000102.awsfcaj.com/> <br> <https://000032.awsfcaj.com/>    |
| 6   | - Tìm hiểu quản lý chi phí, sử dụng tài nguyên với IAM và Amazon Data Lifecycle Manager <br> - **Thực hành:** <br>&emsp; + Tạo policy giới hạn sử dụng dịch vụ theo Region, EC2 family, instance size và EBS volume <br>&emsp; + Xem snapshot do Data Lifecycle Manager quản lý trên EC2 console <br>&emsp; + Tạo policy tự động tạo và lưu snapshot theo nhiều lịch                | 25/09/2026   | 25/09/2026      | <https://000064.awsfcaj.com/> <br> <https://000088.awsfcaj.com/vi/> |
| 7   | - Tìm hiểu VPC Endpoint và AWS Web Application Firewall (WAF) <br> - **Thực hành:** <br>&emsp; + Dùng VPC Endpoint để workload truy cập dịch vụ AWS mà không đi qua Internet công cộng <br>&emsp; + Tạo luật WAF tuỳ chỉnh để chặn hoặc cho phép request HTTP từ bên ngoài <br> - Tham gia sự kiện Buildrathon Kickoff: Code the Future with CMC Global | 26/09/2026   | 26/09/2026      | <https://000111.awsfcaj.com/> <br> <https://000026.awsfcaj.com/>    |


### Kết quả đạt được tuần 2:

* Hiểu cách kết nối on-premise với AWS:
  * Hybrid DNS với Route 53 Resolver
  * Truy cập máy chủ qua Remote Desktop Gateway (RDP)
  * Chuyển máy ảo bằng VM Import/Export

* Tự động hoá vận hành:
  * Viết Lambda để tự động hoá tác vụ
  * Quản lý Windows instance bằng Systems Manager

* Dựng hạ tầng bằng code:
  * Tham chiếu tài nguyên giữa các stack CloudFormation
  * CDK với nested stack cho API Gateway, ELB, ECS, Lambda
  * Triển khai kiến trúc ba tầng

* Kiểm soát chi phí:
  * IAM policy giới hạn Region, EC2 family, instance size, EBS volume
  * Data Lifecycle Manager tự tạo và lưu snapshot theo lịch

* Bảo mật mạng:
  * VPC Endpoint để truy cập dịch vụ AWS không qua Internet
  * Luật WAF tuỳ chỉnh để chặn hoặc cho phép request HTTP

* Tham gia sự kiện Buildrathon Kickoff: Code the Future with CMC Global ngày 26/09, mở đầu cuộc thi Buildrathon của FCAJ.
