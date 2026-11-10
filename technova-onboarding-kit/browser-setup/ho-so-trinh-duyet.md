# Module 2: Thiết lập Trình duyệt Chuyên nghiệp Đa Profile (`browser-setup/`)

## 1. Nguyên lý Data Isolation & Tách biệt 2 Browser Profile
Tạo 2 Profile độc lập trên trình duyệt Google Chrome hoặc Microsoft Edge:
1. **Profile `Personal`:** Phục vụ giải trí, tài khoản cá nhân, mạng xã hội.
2. **Profile `TechNova_Work`:** Phục vụ công việc, chỉ đăng nhập Email công ty (`@technova.io`), GitHub Enterprise, Jira, Notion.

> **Lợi ích:** Tách biệt hoàn toàn Cookies, Sessions, History và Extension, tránh rủi ro lộ dữ liệu cá nhân hoặc nhầm lẫn tài khoản khi thao tác.

---

## 2. Quản lý Bookmark Manager theo 3 Thư mục Chuẩn
Cấu trúc thanh Dấu trang (Bookmark Bar) trên Profile `TechNova_Work`:

- 📁 **`01_Work_Dev`**: Contains GitHub TechNova Org, Jira Board, Figma Design, CI/CD Pipeline Dashboard.
- 📁 **`02_Onboarding_Docs`**: Contains SRS Document, Quy định Công ty, Google Drive Workspace, Sơ đồ Tổ chức.
- 📁 **`03_Tools`**: Contains Bitwarden Vault, StackOverflow, ChatGPT/Gemini, ColorPicker, JSON Viewer.

---

## 3. Bộ Extension & Phân quyền Quyền Truy cập (Site Access)

| Nhóm Extension | Tên Extension | Công dụng | Phân quyền Site Access |
| :--- | :--- | :--- | :--- |
| **Dev Suite** | JSON Viewer, Wappalyzer | Kiểm tra API response, phân tích công nghệ website | **On Click** (Chỉ chạy khi nhấp vào) |
| **Productivity Suite** | Google Docs Offline, Grammarly | Hỗ trợ soạn thảo, kiểm tra chính tả | On Specific Sites |
| **Security Suite** | Bitwarden, uBlock Origin | Quản lý mật khẩu, chặn quảng cáo độc hại | On All Sites |

> 🔒 **Quy định Security:** Đặt Site Access của các Extension không bắt buộc ở chế độ *"On Click"* để ngăn ngừa extension bị hacked thu thập dữ liệu nhạy cảm.

---

## 4. Thực hành DevTools (F12) Cơ bản cho Nhân viên Mới
- **Inspect Element (Ctrl+Shift+C):** Kiểm tra cấu trúc HTML/CSS của giao diện người dùng.
- **Phân biệt Cache vs Cookies:**
  - *Cookies:* Lưu phiên đăng nhập và định danh người dùng.
  - *Cache:* Lưu các tệp tĩnh (hình ảnh, CSS, JS) để tăng tốc độ tải trang.
- **Hard Reload & Empty Cache (Ctrl+F5 hoặc Shift+F5):** Thao tác bắt buộc trước khi kết luận giao diện bị lỗi để xóa sạch cache cũ và tải về bản mã nguồn mới nhất từ Server.
