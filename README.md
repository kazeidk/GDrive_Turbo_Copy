# ⚡ GDrive Turbo Copy

Blazing fast Google Drive folder copy - parallel processing, auto-resume, runs on Colab

<a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## ✨ Tính năng

| Tính năng | Mô tả |
|-----------|-------|
| ⚡ Copy song song | Tăng tốc 2-5x với multi-threading |
| 🔄 Auto-resume | Tự động tiếp tục khi Colab timeout |
| 🎯 Exact match | Kiểm tra file tồn tại chính xác |
| 🔁 Auto-retry | Tự động retry khi rate limit |
| 📊 Progress bar | Hiển thị tiến độ realtime |
| 🔍 Dry-run | Xem trước không copy thật |
| 🎛️ Filter | Lọc theo đuôi file hoặc tên |
| 📝 Log chi tiết | Ghi log để debug |

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Mở notebook
Click **"Open in Colab"** ở trên

### Bước 2: Chạy cell "Cài đặt"
Chạy 1 lần để cài thư viện

### Bước 3: Nhập thông tin
- **Folder đích**: Link folder Google Drive của bạn
- **Folder nguồn**: Link folder cần copy (có thể là Shared Drive)
- **Số luồng**: 5-8 cho Colab Pro+

### Bước 4: Chạy
Chạy cell "Run" và đợi hoàn tất

---

## 💡 Tips

- **Colab Pro+**: Tăng số luồng lên 5-8
- **Timeout?** Chạy lại - checkpoint tự resume
- **Dry-run**: Bật để xem trước trước khi copy thật
- **Log**: Xem tại `/content/copy_log.txt`

---

## �  Files sau khi chạy

| File | Mô tả |
|------|-------|
| `/content/copy_checkpoint.json` | Lưu tiến độ để resume |
| `/content/copy_log.txt` | Log chi tiết |

---

## ⚠️ Lưu ý

- Copy trực tiếp server-to-server (không qua máy bạn)
- Không copy được Google Docs/Sheets/Slides native
- Cần quyền truy cập folder nguồn và đích

---

## � Li cense

MIT License
