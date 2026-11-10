# Module 1: Tổ chức Không gian Cộng tác Đám mây (`cloud-workspace/`)

## 1. Mô hình Hybrid Workflow (Local vs Cloud)
- **Local Workspace:** Làm việc trực tiếp trên ổ cứng cá nhân (`C:\TechNova\` hoặc `~/TechNova/`) để đảm bảo tốc độ phản hồi nhanh, không lag khi mở các file lớn hay compile code.
- **Cloud Synchronization:** Cài đặt **Google Drive for Desktop**, thiết lập chế độ **Stream files** hoặc **Mirror files** tự động sao lưu toàn bộ thư mục công việc lên Google Cloud thời gian thực.

---

## 2. Cấu trúc Cây Thư mục Dự án 5 Trụ cột (`kebab-case`)
Toàn bộ tên thư mục và tập tin phải viết hoa chữ cái đầu hoặc dùng `kebab-case`, không dấu, không khoảng trắng:

```text
technova-workspace/
├── 01-project-docs/          # Tài liệu thiết kế, SRS, Roadmap, Biên bản họp
├── 02-source-code/           # Mã nguồn dự án, tệp cấu hình local
├── 03-design-assets/         # Hình ảnh, UI/UX Mockups, Logo, Design Systems
├── 04-reports-analytics/     # Báo cáo tuần/tháng, chỉ số KPIs, dữ liệu phân tích
└── 05-personal-archive/      # Ghi chú cá nhân, nháp công việc, chứng chỉ học tập
```

---

## 3. Bảng Ma trận Phân quyền Chia sẻ Dữ liệu

| Vai trò Người dùng | Mức quyền Google Drive | Phạm vi Truy cập | Kênh Giao tiếp (Lark/Slack) | Quy tắc Ứng xử |
| :--- | :--- | :--- | :--- | :--- |
| **Nhân viên mới (Owner tài liệu cá nhân)** | **Editor** | Thư mục cá nhân (`05-personal-archive`) | `#onboarding` | Hỏi đáp 1-1 riêng với Mentor trực tiếp |
| **Đồng đội cùng dự án** | **Editor** | Thư mục dự án chung (`01-project-docs`, `02-source-code`) | `#dev-<ten-du-an>` | Thảo luận kỹ thuật, code review |
| **Thực tập sinh phòng ban khác** | **Commenter** | Thư mục báo cáo & thiết kế chung | `#thong-bao` | Chỉ xem và để lại phản hồi/góp ý |
| **Đối tác / Khách mời ngoài** | **Viewer (Restricted)** | Chỉ định đích danh Email khách | *Không cấp quyền* | Tuyệt đối không cho phép truy cập Workspace nội bộ |

> ⚠️ **BẪY PHÂN QUYỀN (CRITICAL):** Tuyệt đối không bao giờ bật tính năng **"Anyone with the link"** đi kèm với quyền **Editor**. Hành vi này mở cửa cho bất kỳ ai có liên kết đều có thể sửa/xóa dữ liệu công ty.

---

## 4. Văn hóa Giao tiếp Nhóm theo Channel - Thread chuẩn Doanh nghiệp
1. **Reply in Thread:** Luôn trả lời trực tiếp vào Thread của tin nhắn gốc. Không nhắn đè vào kênh chính gây trôi tin nhắn.
2. **Nguyên tắc "No-Hello":** Không nhắn tin đơn độc "Alo anh ơi", "Hi bạn". Hãy gõ đầy đủ: **[Chào hỏi] + [Nội dung cần hỗ trợ] + [Context/Hình ảnh]** trong cùng một tin nhắn.
3. **Tagging Đúng người:** Chỉ `@here` hoặc `@channel` trong trường hợp sự cố khẩn cấp (P0/P1). Sử dụng `@username` cho người trực tiếp giải quyết.
4. **Tắt Thông báo Ngoài giờ:** Tôn trọng thời gian nghỉ ngơi của đồng đội, cài đặt chế độ Do Not Disturb (DND) từ 19:00 đến 08:00 sáng hôm sau.
