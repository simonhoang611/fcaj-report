---
title: "Worklog Tuần 10"
date: 2026-09-14
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Hoàn thành tính năng admin huỷ đơn và trang tài khoản (đổi mật khẩu, đổi username).
* Làm xác thực hai lớp bằng ứng dụng tạo mã và đồng bộ trạng thái đăng nhập giữa các tab; đăng bài blog 3 về Cognito (19/11).
* Nghiệm thu phần của mình cho v1.0.0; vẽ sơ đồ kiến trúc AWS của dự án.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                  |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Hoàn thành tính năng admin huỷ đơn (API, hạ tầng, màn hình): đơn huỷ thì hàng tự trả lại kho <br> - Sửa 2 lỗi giao diện nhỏ: nút đổi màu sai khi rê chuột, thiếu biểu tượng trang <br> - Chốt thiết kế trang tài khoản                                  | 16/11/2026   | 16/11/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_TransactWriteItems.html>                                                                                                                    |
| 3   | - Làm trang tài khoản: <br>&emsp; + Khách đổi được mật khẩu, đổi xong tự đăng xuất ở mọi thiết bị <br>&emsp; + Đổi username <br>&emsp; + Sửa lỗi tải lại trang bị đẩy về trang đăng nhập <br> - Tìm hiểu xác thực hai lớp bằng ứng dụng tạo mã và passkey | 17/11/2026   | 17/11/2026      | <https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_AdminUserGlobalSignOut.html> <br> <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-mfa-totp.html> |
| 4   | - Viết tài liệu cho tính năng bật/tắt xác thực hai lớp (quét mã QR bằng Google Authenticator) và mở PR nháp để nhóm góp ý                                                                                                                                 | 18/11/2026   | 18/11/2026      |                                                                                                                                                                                                                 |
| 5   | - Code xong xác thực hai lớp với công tắc Bật/Tắt <br> - Phân tích lỗi tab cũ vẫn hiện tài khoản cũ khi tab khác đổi người đăng nhập <br> - **Đăng bài blog 3** về Amazon Cognito                                                                         | 19/11/2026   | 19/11/2026      | <https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/status_role> <br> <https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel>                                          |
| 6   | - Hoàn thành chức năng các tab tự đồng bộ khi đổi người đăng nhập <br> - Nghiệm thu phần của mình cho bản v1.0.0 <br> - Tự vẽ sơ đồ kiến trúc AWS của dự án bằng draw.io                                                                                  | 20/11/2026   | 20/11/2026      | <https://developer.mozilla.org/en-US/docs/Web/API/Page_Visibility_API> <br> <https://www.youtube.com/watch?v=l8isyDe-GwY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=2>                                       |
| 7   | - Tham gia sự kiện AWS Student Community Day Vietnam 2026 tại văn phòng để giao lưu và lắng nghe chia sẻ kiến thức                                                                                                                                        | 21/11/2026   | 21/11/2026      | <https://www.facebook.com/groups/awsstudentbuildergroupvn/posts/4571875389749943>                                                                                                                               |


### Kết quả đạt được tuần 10:

* Admin huỷ được đơn; trạng thái đơn và tồn kho cập nhật trong cùng một DynamoDB transaction nên hàng luôn được trả lại kho.

* Trang tài khoản hoàn chỉnh:
  * Đổi mật khẩu, đổi xong đăng xuất mọi thiết bị
  * Đổi username
  * Hết lỗi tải lại trang bị đẩy về đăng nhập

* Xác thực hai lớp (TOTP):
  * Quét mã QR bằng Google Authenticator
  * Công tắc Bật/Tắt
  * Viết tài liệu và mở PR nháp để nhóm góp ý trước khi code

* Các tab tự đồng bộ khi đổi người đăng nhập nhờ BroadcastChannel và Page Visibility API.

* Nghiệm thu phần của mình cho v1.0.0; tự vẽ sơ đồ kiến trúc AWS của dự án bằng draw.io.

* Đăng bài blog 3 về Cognito ngày 19/11; tham gia AWS Student Community Day Vietnam 2026.
