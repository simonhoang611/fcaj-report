---
title: "Worklog Tuần 9"
date: 2026-09-14
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Làm lại các trang đơn hàng của shop-ai theo kế hoạch 5 phần, bắt đầu từ các thành phần giao diện dùng chung.
* Cùng nhóm nghiệm thu và phát hành bản ứng viên v1.0.0-rc.1.
* Cải tiến đăng nhập và làm chức năng quên mật khẩu với Amazon Cognito; đăng bài blog 2 về SQS (11/11).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                                    | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                          |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Lên kế hoạch làm lại các trang đơn hàng thành 5 phần <br> - Làm trước các thành phần giao diện dùng chung: nút, nhãn trạng thái, khối trống, hộp xác nhận                                                                                                                  | 09/11/2026   | 09/11/2026      |                                                                                                                                                                                                         |
| 3   | - Nghiệm thu bản ứng viên phát hành rc.1 trên staging: các luồng chính và tốc độ trang đều đạt                                                                                                                                                                               | 10/11/2026   | 10/11/2026      |                                                                                                                                                                                                         |
| 4   | - Phân tích cải tiến trang đăng nhập (nút ẩn/hiện mật khẩu, ô nhập mã 6 số) và chức năng quên mật khẩu với Amazon Cognito <br> - **Đăng bài blog 2** về hàng đợi Amazon SQS                                                                                                  | 11/11/2026   | 11/11/2026      | <https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_ConfirmForgotPassword.html> <br> <https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/autocomplete> |
| 5   | - **Nhóm phát hành bản v1.0.0-rc.1** <br> - Hoàn thành trang quên mật khẩu <br> - Bắt đầu tính năng admin huỷ đơn                                                                                                                                                            | 12/11/2026   | 12/11/2026      | <https://docs.amplify.aws/react/build-a-backend/auth/manage-users/manage-passwords/>                                                                                                                    |
| 6   | - Tổng hợp 33 kiến thức mới đã áp dụng vào dự án từ đầu kỳ, mỗi mục ghi: <br>&emsp; + Là gì <br>&emsp; + Dùng để làm gì trong dự án <br>&emsp; + Đã dùng ở đâu (số issue, PR) <br>&emsp; + Nguồn tài liệu chính thức <br> - Kiểm lại các link nguồn, làm nền để viết worklog | 13/11/2026   | 13/11/2026      |                                                                                                                                                                                                         |
| 7   | - Tham gia sự kiện Cloud Mastery tại văn phòng để giao lưu và lắng nghe chia sẻ kiến thức                                                                                                                                                                                    | 14/11/2026   | 14/11/2026      |                                                                                                                                                                                                         |


### Kết quả đạt được tuần 9:

* Có bộ thành phần giao diện dùng chung (nút, nhãn trạng thái, khối trống, hộp xác nhận) cho các trang đơn hàng.

* Nghiệm thu rc.1 trên staging đạt cả luồng chính lẫn tốc độ trang; cùng nhóm phát hành v1.0.0-rc.1.

* Cải tiến đăng nhập với Amazon Cognito:
  * Nút ẩn/hiện mật khẩu, ô nhập mã 6 số
  * Trang quên mật khẩu: nhận mã qua email và đặt mật khẩu mới

* Đăng bài blog 2 về Amazon SQS ngày 11/11.

* Có bản tổng hợp 33 kiến thức đã áp dụng vào dự án, kèm nơi dùng và nguồn chính thức, làm nền cho worklog.

* Tham gia sự kiện Cloud Mastery, giao lưu và học thêm từ chia sẻ của các diễn giả.
