# Module 3: Củng cố An toàn Thông tin Cá nhân (`security/`)

## 1. Digital Vault trung tâm: Bitwarden Password Manager
- **Nguyên tắc vàng:** *1 Tài khoản – 1 Mật khẩu ngẫu nhiên độc nhất.*
- **Cấu hình Generator:** Độ dài từ 16–32 ký tự, bao gồm chữ hoa, chữ thường, chữ số và ký tự đặc biệt (`!@#$%^&*`).
- Không lưu mật khẩu trên ghi chú máy tính, file Excel hoặc tính năng ghi nhớ mặc định của Trình duyệt.

---

## 2. Kích hoạt Xác thực 2 Yếu tố (2FA / TOTP)
- **Phương thức ưu tiên:** Authenticator App (Bitwarden Authenticator, Google Authenticator) tạo mã TOTP 6 chữ số thay đổi mỗi 30 giây.
- **Cấm chọn SMS OTP:** Tránh nguy cơ bị SIM Swapping hoặc chặn bắt tin nhắn SMS.
- **Lưu trữ Backup Codes:** Ngay khi bật 2FA trên GitHub / Google Email, lưu danh sách mã dự phòng (Backup Codes) trực tiếp vào mục Secure Notes trong Bitwarden.

---

## 3. Quy tắc 5 KHÔNG trong Phụ trách An toàn Thông tin

1. **KHÔNG** click vào liên kết lạ, email nghi vấn Phishing hoặc Typosquatting (ví dụ: `g00gle.com`, `techn0va.io`).
2. **KHÔNG** tải và cài đặt phần mềm Crack, Keygen, Torrent trên máy tính làm việc.
3. **KHÔNG** cắm USB/Thẻ nhớ lạ vào thiết bị công ty mà chưa qua quét mã độc.
4. **KHÔNG** chia sẻ mật khẩu hay OTP cho bất kỳ ai (kể cả người tự xưng là IT Support).
5. **KHÔNG** làm việc trên mạng Wi-Fi công cộng mở (Coffee shop, Sân bay) mà không bật VPN Công ty.

---

## 4. Quản lý Secrets trong Phát triển Phần mềm
- **Tệp `.env`:** Chứa thông tin đăng nhập cơ sở dữ liệu, API Keys, JWT Tokens ở môi trường local.
- **Tệp `.gitignore`:** Phải chứa khai báo `.env` ngay từ commit đầu tiên để ngăn ngừa việc đẩy vô tình mật khẩu lên GitHub Repository.
- **Tệp `.env.example`:** Tệp mẫu chứa tên các biến môi trường với giá trị dummy (giá trị giả định) để chia sẻ cho đồng đội.
