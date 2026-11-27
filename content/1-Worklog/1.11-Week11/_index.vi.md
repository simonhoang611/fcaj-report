---
title: "Worklog Tuần 11"
date: 2026-09-14
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Cùng nhóm phát hành bản chính thức v1.0.0; viết chương Workshop 5.4 (luồng bán hàng).
* Làm tính năng admin quản lý sản phẩm, gồm tải ảnh sản phẩm lên S3.
* Chuẩn bị bản sửa lỗi v1.0.1 và đưa site báo cáo thực tập FCAJ lên GitHub Pages.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                             |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Nhóm phát hành bản chính thức v1.0.0** <br> - Viết chương Workshop 5.4 (luồng bán hàng) và dựng một bản shop riêng trên AWS để chụp ảnh hướng dẫn từng bước                                                                           | 23/11/2026   | 23/11/2026      | <https://testing-library.com/docs/dom-testing-library/api-async/>                                                                                                          |
| 3   | - Hoàn thiện chương Workshop 5.4: 24 ảnh, sơ đồ luồng bán hàng và bảng chi phí                                                                                                                                                            | 24/11/2026   | 24/11/2026      |                                                                                                                                                                            |
| 4   | - Làm tính năng admin quản lý sản phẩm (thêm theo mẫu, sửa, ẩn, xoá có thể khôi phục): <br>&emsp; + Phân tích, thiết kế màn hình <br>&emsp; + API, trang danh sách, trang thêm/sửa <br> - Sửa thông số sai của 2 laptop trong dữ liệu mẫu | 25/11/2026   | 25/11/2026      |                                                                                                                                                                            |
| 5   | - Cho admin tải ảnh sản phẩm từ máy lên: <br>&emsp; + Trình duyệt gửi ảnh thẳng lên S3 bằng presigned URL có hạn 5 phút <br>&emsp; + Giới hạn loại file và tối đa 3 MB <br>&emsp; + Ảnh hiển thị qua CloudFront                           | 26/11/2026   | 26/11/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/API/> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html> |
| 6   | - Lập danh sách kiểm tra cho bản sửa lỗi v1.0.1 (nội dung sản phẩm mới, đặt hàng, huỷ đơn, quên mật khẩu) <br> - Đổi header, thêm trang "Hàng mới về" <br> - Đưa site báo cáo thực tập FCAJ lên GitHub Pages                              | 27/11/2026   | 27/11/2026      | <https://hcm-rules.awsfcaj.com/project#hinh-thuc>                                                                                                                          |


### Kết quả đạt được tuần 11:

* Cùng nhóm phát hành v1.0.0, bản chính thức của shop-ai.

* Hoàn thành chương Workshop 5.4 (luồng bán hàng):
  * 24 ảnh chụp từ một bản shop dựng riêng trên AWS
  * Sơ đồ luồng bán hàng
  * Bảng chi phí

* Admin quản lý sản phẩm:
  * Thêm theo mẫu, sửa, ẩn, xoá có thể khôi phục
  * Tải ảnh thẳng lên S3 bằng presigned URL hạn 5 phút, tối đa 3 MB
  * Ảnh hiển thị qua CloudFront

* Có danh sách kiểm tra cho v1.0.1; header mới và trang "Hàng mới về"; site báo cáo thực tập FCAJ chạy trên GitHub Pages.
