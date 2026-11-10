# Module 4: Bộ kỹ năng Tự Tra cứu & Gỡ lỗi (`troubleshooting/`)

## 1. Cheat-Sheet Toán tử Tìm kiếm Google Nâng cao

| Toán tử | Ý nghĩa & Cú pháp mẫu | Mục đích sử dụng |
| :--- | :--- | :--- |
| **`site:`** | `site:stackoverflow.com "fatal error: Unexpected token"` | Chỉ tìm kiếm trong đúng website chỉ định |
| **`" "` (Ngoặc kép)** | `"CORS policy: No 'Access-Control-Allow-Origin'"` | Tìm kiếm chính xác từng cụm từ nguyên văn |
| **`-` (Dấu trừ)** | `git commit error -svn` | Loại bỏ các kết quả chứa từ khóa không liên quan |
| **Kết hợp** | `site:github.com/facebook/react "Warning: Each child in a list" -vue` | Tra cứu Issue React chính xác trên GitHub |

> ⚠️ **Bẫy Tìm kiếm:** Tránh gõ nguyên câu văn nói dài dòng. Cẩn trọng với bài viết StackOverflow đăng **quá 5 năm** vì cú pháp thư viện có thể đã thay đổi.

---

## 2. Phương pháp Soạn Prompt AI 3 Thành phần
Khi cần Trợ lý AI (Gemini, ChatGPT) hỗ trợ giải thích lỗi, hãy áp dụng công thức:

1. **Ngữ cảnh (Context):** Môi trường đang làm việc (HĐH, Ngôn ngữ, Framework, Version).
2. **Lỗi Nguyên văn (Raw Error):** Sao chép toàn bộ StackTrace/Log lỗi trong cặp dấu ` ``` `.
3. **Yêu cầu Cụ thể (Actionable Request):** Đề nghị giải thích nguyên nhân và đưa ra các bước sửa chữa.

**Mẫu Prompt Chuẩn:**
> *"Tôi đang phát triển ứng dụng Node.js v20 với Express trên Windows 11. Khi gọi API POST /api/v1/login thì nhận được log lỗi sau: `Error: ECONNREFUSED 127.0.0.1:5432`. Hãy giải thích nguyên nhân gây ra lỗi này và hướng dẫn tôi 3 bước kiểm tra sửa lỗi."*

---

## 3. Bug Reporting Framework 4 Bước cho Phòng IT Support
Khi không thể tự gỡ lỗi, hãy tạo Ticket hoặc gửi tin nhắn báo lỗi cho IT theo khung 4 bước:

```text
[MẪU BÁO CÁO LỖI CHUẨN - TECHNOVA BUG REPORT]

1. Ngữ cảnh (Context):
   - Người báo cáo: Nguyễn Văn A (Phòng Dev)
   - Thiết bị: MacBook Pro M2, macOS Sonoma
   - Môi trường/Phần mềm: Docker Desktop v4.28

2. Kết quả Mong đợi (Expected Result):
   - Chạy lệnh `docker-compose up` thành công và container PostgreSQL lắng nghe ở cổng 5432.

3. Kết quả Thực tế (Actual Result):
   - Container PostgreSQL bị ngắt kết nối liên tục, báo trạng thái `Exited (1)`.

4. Log lỗi & Hình ảnh (Log / Screenshot):
   - Log chi tiết: `panic: could not open file "global/pg_control": Permission denied`
   - [Đính kèm ảnh chụp màn hình F12/Terminal nguyên văn lỗi]
```
