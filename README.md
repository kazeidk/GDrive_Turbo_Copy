# 🚀 Copy Folder Google Drive to Google Drive - 1TouchPro

Tool copy toàn bộ folder từ Google Drive (bao gồm Shared Drive) sang Google Drive của bạn, chạy trên Google Colab.

---

## 📦 V2 (Khuyên dùng)

<a href="https://colab.research.google.com/github/nqthaivl/Copy-Folder-Google-Drive-to-Google-Drive/blob/main/GDrive_Turbo_Copy.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open GDrive Turbo Copy"/></a>

### ✨ Tính năng V2:
| Tính năng | Mô tả |
|-----------|-------|
| ✅ Exact match | Kiểm tra file tồn tại chính xác (fix bug V1) |
| ✅ Retry mechanism | Tự động retry khi rate limit, network error |
| ✅ Copy song song | Tăng tốc 2-5x với multi-threading |
| ✅ Checkpoint/Resume | Lưu tiến độ, chạy lại tiếp tục từ chỗ dừng |
| ✅ Log chi tiết | Ghi log vào `/content/copy_log.txt` |
| ✅ Filter extension | Chỉ copy hoặc bỏ qua theo đuôi file |
| ✅ Dry-run mode | Xem trước sẽ copy gì mà không copy thật |
| ✅ Progress bar | Hiển thị tiến độ realtime |
| ✅ So sánh size | Phát hiện file cần update |
| ✅ Xử lý tên đặc biệt | Emoji, unicode, ký tự đặc biệt |

---

## 📖 Hướng dẫn sử dụng V2

### Bước 1: Mở notebook trên Colab
Click vào badge "Open in Colab" ở trên

### Bước 2: Chạy cell "Cài đặt thư viện"
- Click vào cell đầu tiên
- Nhấn `Shift + Enter` hoặc click nút Play ▶️
- Chờ cài đặt xong (vài giây)

### Bước 3: Chạy cell "Nhập thông tin"
- Chạy cell thứ 2
- Điền thông tin vào form:
  - **Folder đích**: Link folder Google Drive của bạn (nơi muốn copy đến)
  - **Folder nguồn**: Link folder cần copy (có thể là Shared Drive)
  - **Số luồng**: 5 (recommend cho Colab Pro+, có thể tăng lên 8)
  - Các tùy chọn khác nếu cần

### Bước 4: Chạy cell "Run"
- Chạy cell thứ 3
- Đăng nhập Google khi được yêu cầu
- Chờ copy hoàn tất

### 💡 Tips cho Colab Pro+:
- **Số luồng**: Tăng lên 5-8 để copy nhanh hơn
- **Timeout**: Nếu bị timeout, chạy lại - checkpoint sẽ tự động resume
- **Dry-run**: Bật để xem trước trước khi copy thật
- **Runtime**: Chọn "High-RAM" trong Runtime settings để xử lý folder lớn

---

## 📁 Các file quan trọng (sau khi chạy)

| File | Mô tả |
|------|-------|
| `/content/copy_checkpoint.json` | Lưu tiến độ, dùng để resume |
| `/content/copy_log.txt` | Log chi tiết quá trình copy |
| `/content/copy_errors.txt` | Danh sách file bị lỗi |

---

## 🔧 Xử lý sự cố

### Bị timeout/disconnect
→ Chạy lại cell "Run", checkpoint sẽ tự động skip file đã copy

### Muốn copy lại từ đầu
→ Chạy cell "Tiện ích" để xóa checkpoint

### Rate limit (403/429)
→ Tool sẽ tự động retry với exponential backoff

### File bị lỗi
→ Xem `/content/copy_errors.txt` để biết chi tiết
→ Chạy lại để retry các file lỗi

---

## 📦 V1 (Phiên bản cũ)

<a href="https://colab.research.google.com/github/nqthaivl/Copy-Folder-Google-Drive-to-Google-Drive/blob/main/Copy_Folder_Google_Drive_to_Google_Drive.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open V1 In Colab"/></a>

---

## ⚠️ Lưu ý

- Tool copy trực tiếp server-to-server (không tải về máy)
- Không copy được Google Docs/Sheets/Slides native (chỉ copy file thường)
- Cần quyền truy cập vào cả folder nguồn và folder đích
- Tuân thủ quota Google Drive API

---

## 📝 License

MIT License - Tự do sử dụng và chỉnh sửa
