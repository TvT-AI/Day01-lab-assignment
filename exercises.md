# Ngày 1 — Bài Tập & Phản Ánh

## Nền Tảng LLM API | Phiếu Thực Hành

---

## Phần 2 — Bài Tập Mở Rộng (1:00–1:30)

### Bài tập 2.1 — Độ Nhạy Của Temperature

**Bạn nhận thấy quy luật gì qua bốn phản hồi?**
Khi temperature thấp ví dụ như 0 thì spam câu hỏi qua nhiều lần câu trả lời k khác nhau là mấy. Khi temperature tăng lên câu trả lời trở nên đa dạng, sáng tạo hơn nhưng cũng dễ ảo tưởng. Temperature càng cao thì mức độ ngẫu nhiên trong quá trình sinh text càng lớn.

**Bạn sẽ đặt temperature bao nhiêu cho chatbot hỗ trợ khách hàng, và tại sao?**
chọn thấp 0-0.2 để rag bớt bịa chuyện, ưu tiên trả lời chính xác.

---

### Bài tập 2.2 — Đánh Đổi Chi Phí

**Ước tính xem GPT-4o đắt hơn GPT-4o-mini bao nhiêu lần cho workload này:**
nếu mà mỗi ngày có:

* 10.000 ng dùng
* 3 req/ng
* 350 token/req

Tổng ngày:

10.000 × 3 × 350 = 10.500.000 tokens

Theo giá:

* GPT-4o: $0.010 / 1K output tokens
* GPT-4o-mini: $0.0006 / 1K output tokens

Chi phí:

0.010 / 0.0006 ≈ 16.7 lần

GPT-4o đắt hơn khoảng 16–17 lần so với GPT-4o-mini cho cùng workload.

**Mô tả một trường hợp mà chi phí cao hơn của GPT-4o là xứng đáng, và một trường hợp GPT-4o-mini là lựa chọn tốt hơn:**
GPT-4o phù hợp cho các tác vụ yêu cầu suy luận mạnh và độ chính xác cao như trợ lý lập trình, phân tích tài liệu hoặc hỗ trợ chuyên môn. GPT-4o-mini phù hợp cho chatbot FAQ, ứng dụng phản hồi nhanh hoặc hệ thống có lượng request lớn cần tối ưu chi phí.

---

### Bài tập 2.3 — Trải Nghiệm Người Dùng với Streaming

Streaming đặc biệt quan trọng trong các ứng dụng chatbot hoặc trợ lý AI thời gian thực vì người dùng có thể thấy phản hồi xuất hiện ngay lập tức thay vì phải chờ toàn bộ câu trả lời hoàn thành, làm trải nghiệm tự nhiên với giảm delay. Ngược lại, non-streaming khi cần xử lý ngắn gọn, trả về kết quả hoàn chỉnh một lần hoặc khi hệ thống cần hậu xử lý toàn bộ output trước khi hiển thị cho người dùng.

---

## Danh Sách Kiểm Tra Nộp Bài

* [V] Tất cả tests pass: `pytest tests/ -v`
* [V] `call_openai` đã triển khai và kiểm thử
* [V] `call_openai_mini` đã triển khai và kiểm thử
* [V] `compare_models` đã triển khai và kiểm thử
* [V] `streaming_chatbot` đã triển khai và kiểm thử
* [V] `retry_with_backoff` đã triển khai và kiểm thử
* [V] `batch_compare` đã triển khai và kiểm thử
* [V] `format_comparison_table` đã triển khai và kiểm thử
* [V] `exercises.md` đã điền đầy đủ
* [V] Sao chép bài làm vào folder `solution` và đặt tên theo quy định
