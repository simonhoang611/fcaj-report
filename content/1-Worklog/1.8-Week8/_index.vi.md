---
title: "Worklog Tuần 8"
date: 2026-09-14
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Rà soát bảo mật luồng đặt hàng: chống lạm dụng, kiểm IDOR, quét ZAP baseline, phân quyền IAM theo tag giữa các môi trường.
* Làm lại trang chi tiết sản phẩm và tăng tốc độ tải trang; cùng nhóm phát hành v0.2.0; đăng bài blog 1 (05/11).
* Bắt đầu và hoàn thành trang quản trị đơn hàng; viết hướng dẫn xử lý khi DynamoDB bị quá tải.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                 |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Rà lại báo cáo bảo mật của nhóm, xác nhận các biện pháp chống lạm dụng đặt hàng đã có trong code: <br>&emsp; + Giới hạn 3 đơn chưa giao <br>&emsp; + Chặn xem đơn của người khác                                                                                                                                                                                                                                                                         | 02/11/2026   | 02/11/2026      | <https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html>                                                                                                  |
| 3   | - Tìm hiểu kiểm tra IDOR và quét ZAP baseline, áp dụng vào dự án: <br>&emsp; + Khách không xem hay huỷ được đơn của người khác bằng cách đổi mã đơn trên URL <br>&emsp; + Có bằng chứng quét bảo mật cho báo cáo <br> - Bắt đầu làm lại trang chi tiết sản phẩm: chia thành 7 phần nhỏ, xong phần header tự thu gọn khi cuộn trang                                                                                                                         | 03/11/2026   | 03/11/2026      | <https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html> <br> <https://www.zaproxy.org/docs/docker/baseline-scan/>                                        |
| 4   | - Tìm hiểu IAM theo tag (aws:ResourceTag) để Lambda của dev không đọc được người dùng của prod, vì dev, staging, prod dùng chung một tài khoản AWS <br> - Hoàn thành trang chi tiết sản phẩm mới: bảng thông số dạng ô, panel thông số có mục lục, hộp mua hàng <br> - Web bắt đầu ghi lại sản phẩm khách xem và thêm vào giỏ để hệ thống gợi ý học theo                                                                                                   | 04/11/2026   | 04/11/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_tags.html> <br> <https://react.dev/reference/react/useLayoutEffect>                                                                                   |
| 5   | - Áp dụng useInfiniteQuery cho danh sách "Xem thêm đơn": khách có nhiều đơn vẫn xem lịch sử nhanh thay vì tải hết một lần <br> - **Nhóm phát hành v0.2.0 lên production** <br> - Tăng tốc mở trang trên điện thoại: đưa font chữ vào chính web, tải dữ liệu sản phẩm sớm hơn <br> - Thêm số lượng trên biểu tượng giỏ kèm hiệu ứng sản phẩm bay vào giỏ <br> - **Đăng bài blog 1** về DynamoDB transactions: giữ tồn kho đúng khi nhiều người cùng bấm mua | 05/11/2026   | 05/11/2026      | <https://tanstack.com/query/latest/docs/framework/react/guides/infinite-queries> <br> <https://web.dev/articles/optimize-lcp> <br> <https://tanstack.com/query/latest/docs/framework/react/guides/prefetching> |
| 6   | - Đo lại tốc độ trang bằng Lighthouse: điện thoại tăng từ khoảng 82 lên 97–98 điểm, máy tính đạt 100 <br> - Bắt đầu trang quản trị đơn hàng: viết hợp đồng API và backend cho admin xem, chuyển trạng thái đơn                                                                                                                                                                                                                                             | 06/11/2026   | 06/11/2026      | <https://developer.chrome.com/docs/lighthouse/overview?hl=vi>                                                                                                                                                  |
| 7   | - Hoàn thành trang quản trị đơn hàng: hạ tầng AWS, kiểm thử tự động, màn hình <br> - Viết hướng dẫn xử lý sự cố khi DynamoDB bị quá tải (throttling), kèm biểu đồ theo dõi                                                                                                                                                                                                                                                                                 | 07/11/2026   | 07/11/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/throttling-diagnosing-workflow.html>                                                                                                         |


### Kết quả đạt được tuần 8:

* Rà soát bảo mật luồng đặt hàng:
  * Xác nhận giới hạn 3 đơn chưa giao và chặn xem đơn người khác đã có trong code
  * Kiểm IDOR: đổi mã đơn trên URL không xem hay huỷ được đơn người khác
  * Có kết quả quét ZAP baseline làm bằng chứng

* Hiểu cách dùng IAM theo tag (aws:ResourceTag) để tách quyền giữa dev, staging, prod dùng chung một tài khoản AWS.

* Trang chi tiết sản phẩm mới hoàn thành trong 2 ngày:
  * Header tự thu gọn khi cuộn
  * Bảng thông số dạng ô, panel thông số có mục lục, hộp mua hàng
  * Ghi lại sản phẩm khách xem và thêm vào giỏ cho hệ thống gợi ý

* Cùng nhóm phát hành v0.2.0 và tăng tốc trang:
  * Lighthouse điện thoại từ khoảng 82 lên 97–98, máy tính 100
  * Lịch sử đơn tải theo trang với useInfiniteQuery
  * Số lượng trên biểu tượng giỏ và hiệu ứng bay vào giỏ

* Hoàn thành trang quản trị đơn hàng (API, backend, hạ tầng, kiểm thử, màn hình) và runbook xử lý DynamoDB quá tải.

* Đăng bài blog 1 về DynamoDB transactions ngày 05/11.
