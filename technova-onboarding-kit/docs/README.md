# TechNova Onboarding Kit (`[Lop_MonHoc]_MiniProject_TechNova`)

Chào mừng bạn đến với **TechNova**! Đây là Bộ hồ sơ Onboarding Số dành cho nhân viên mới, giúp tổ chức không gian làm việc khoa học, bảo mật và làm chủ kỹ năng tự gỡ lỗi trong môi trường Startup công nghệ.

---

## 📌 1. Cấu trúc Cây Thư mục Dự án

```text
technova-onboarding-kit/
├── docs/
│   ├── README.md                   # Tài liệu hướng dẫn chính (Render Markdown chuẩn)
│   └── srs-onboarding-kit.docx     # Tài liệu SRS chuẩn Styles & Auto TOC
├── cloud-workspace/
│   └── phan-quyen-chia-se.md       # Cấu trúc 5 trụ cột & Bảng phân quyền chi tiết
├── browser-setup/
│   └── ho-so-trinh-duyet.md        # Cấu hình đa Profile, Bookmark & Extension
├── security/
│   ├── checklist-bao-mat.md        # Quy tắc bảo mật 5 KHÔNG, Bitwarden & 2FA
│   ├── .env.example                # Tệp mẫu cấu hình biến môi trường
│   └── .gitignore                  # Khai báo chặn tệp nhạy cảm commit
├── troubleshooting/
│   └── mau-bao-cao-loi.md          # Bug Reporting Framework & Toán tử Google
└── .env                            # Tệp chứa Secrets thực tế (Đã bị ẩn bởi .gitignore)
```

---

## 🛠️ 2. Hướng dẫn Sử dụng & Thiết lập Nhanh

Run command bên dưới để khởi tạo môi trường làm việc số và kiểm tra git status:

```bash
# 1. Clone dự án về máy local
git clone https://github.com/technova-org/technova-onboarding-kit.git
cd technova-onboarding-kit

# 2. Tạo tệp .env từ tệp mẫu .env.example
cp security/.env.example .env

# 3. Kiểm tra .gitignore đảm bảo tệp .env không bị theo dõi bởi Git
git status
```

---

## 📋 3. Checklist Onboarding (Lộ trình 7 Ngày đầu)

- [x] **Ngày 1:** Đăng ký tài khoản Bitwarden, bật 2FA cho Email công ty và GitHub.
- [x] **Ngày 2:** Tạo 2 Profile Trình duyệt (`Personal` & `TechNova_Work`), import bộ Bookmark chuẩn.
- [x] **Ngày 3:** Cài đặt Google Drive for Desktop, tạo cây thư mục 5 trụ cột theo `kebab-case`.
- [x] **Ngày 4:** Cấu hình Extension bảo mật, giới hạn Site Access về chế độ *On Click*.
- [x] **Ngày 5:** Thấu hiểu văn hóa giao tiếp: Reply in Thread, tag tên đúng người, không *No-Hello*.
- [x] **Ngày 6:** Thực hành tra cứu lỗi với toán tử Google (`site:`, `" "`, `-`) và soạn Prompt AI 3 thành phần.
- [x] **Ngày 7:** Hoàn thành kiểm tra thử nghiệm Bug Reporting Framework với phòng IT.

---

## 💻 4. Bảng Trang bị Thiết bị & Tài khoản Cấp phát

| Hạng mục | Thông tin Cấp phát / Quy chuẩn | Trạng thái | Ghi chú Bảo mật |
| :--- | :--- | :---: | :--- |
| **Thiết bị Workstation** | Dell Latitude / MacBook Pro M-Series | ✅ Đã bàn giao | Mã hóa ổ cứng BitLocker/FileVault |
| **Email Doanh nghiệp** | `username@technova.io` | ✅ Đã kích hoạt | Bắt buộc 2FA/TOTP qua App |
| **Google Workspace** | Quyền Editor/Viewer theo phòng ban | ✅ Đã phân quyền | Tuyệt đối KHÔNG share "Anyone with link" quyền Edit |
| **Kênh Lark/Slack** | Workspace TechNova Official | ✅ Đã join | Tắt thông báo ngoài giờ làm việc |
| **GitHub Enterprise** | SSO qua Email Công ty | ✅ Đã phân quyền | Bắt buộc lưu Backup Codes vào Bitwarden |

