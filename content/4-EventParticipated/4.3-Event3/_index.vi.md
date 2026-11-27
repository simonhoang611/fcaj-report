---
title: "Event 3"
date: 2026-09-14
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch "Fireside Chat with Dr. Werner"

### Thông tin sự kiện

- **Thời gian:** 09:00 (UTC+7) ngày 02/10/2026
- **Địa điểm:** Tầng 26, tòa nhà Bitexco Financial Tower, số 2 đường Hải Triều, phường Sài Gòn, TP. Hồ Chí Minh
- **Vai trò:** Người tham dự

### Mục đích của sự kiện

- Kết nối cộng đồng sinh viên, lập trình viên, kiến trúc sư giải pháp và kỹ sư với CTO của Amazon.
- Chia sẻ góc nhìn về tương lai của Cloud, AI và chuyển đổi số.
- Truyền cảm hứng về đổi mới và cách xây dựng hệ thống ở quy mô toàn cầu.

### Diễn giả

- **Dr. Werner Vogels** - Chief Technology Officer, Amazon

### Nội dung và hoạt động chính

Buổi giao lưu cộng đồng với Dr. Werner Vogels, Giám đốc Công nghệ (CTO) của Amazon và là một trong những người tiên phong của điện toán đám mây. Nội dung xoay quanh tương lai của Cloud và AI, bài học từ việc xây dựng và vận hành hệ thống ở quy mô toàn cầu, đổi mới và xu hướng công nghệ, kèm phần hỏi đáp và giao lưu với cộng đồng.

#### Tương lai của Cloud và AI

- Góc nhìn của Dr. Vogels về cách Cloud và AI đang định hình thế hệ chuyển đổi số tiếp theo.

#### Bài học từ hệ thống quy mô toàn cầu

- Kinh nghiệm xây dựng và vận hành hệ thống của Amazon ở quy mô toàn cầu.
- Đổi mới, vai trò dẫn dắt và các xu hướng công nghệ đáng chú ý.

#### Hỏi đáp và giao lưu

- Phần hỏi đáp trực tiếp với Dr. Vogels và giao lưu với các builder, sinh viên và người làm nghề trong cộng đồng.

### Những gì học được

- Ở quy mô lớn, lỗi là chuyện chắc chắn xảy ra; hệ thống tốt là hệ thống được thiết kế để chịu lỗi và tự phục hồi.
- Công nghệ cần phục vụ bài toán thật của người dùng, không phải chạy theo xu hướng.
- Người xây dựng hệ thống cũng nên là người vận hành và chịu trách nhiệm về nó.

### Ứng dụng vào công việc

- Trong dự án, nhóm thiết kế cho trường hợp lỗi: hàng đợi SQS có DLQ, xử lý partial batch failure, Idempotency-Key để tránh tạo đơn trùng, và bật PITR cho các bảng quan trọng trên prod.
- Theo dõi hệ thống bằng log, metric và correlationId (Powertools) để phát hiện và xử lý sự cố nhanh, kèm runbook khi DynamoDB bị throttle.

### Bài học rút ra

- Được nghe trực tiếp từ người tiên phong giúp tôi hiểu các nguyên tắc thiết kế không chỉ là lý thuyết mà đến từ kinh nghiệm vận hành thật.
- Luôn giữ tinh thần học hỏi và tò mò với công nghệ mới.

### Một số hình ảnh khi tham gia sự kiện

<img src="/fcaj-report/images/Fireside%20Chat%20with%20Dr.%20Werner%281%29.jpg" alt="Fireside Chat with Dr. Werner (1)" width="700">

<img src="/fcaj-report/images/Fireside%20Chat%20with%20Dr.%20Werner%282%29.jpg" alt="Fireside Chat with Dr. Werner (2)" width="700">

> Đây là cơ hội hiếm có để nghe trực tiếp từ một trong những người đặt nền móng cho điện toán đám mây hiện đại, và là nguồn cảm hứng lớn cho tôi trong kỳ thực tập.
