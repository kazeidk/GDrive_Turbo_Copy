# 🚀 GDrive Turbo Copy

Tool copy folder Google Drive sang Google Drive nhanh chóng và ổn định, hỗ trợ folder lớn (2000GB+).

<a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## ✨ Tính năng

| Tính năng | Mô tả |
|-----------|-------|
| ⚡ **Copy ngay** | Không scan, copy trực tiếp luôn |
| 🔔 **Âm thanh** | Thông báo khi hoàn tất |
| 🎯 **Exact match** | Kiểm tra file chính xác (không bị trùng như tool cũ) |
| 🔄 **Auto-resume** | Tự tiếp tục khi timeout/disconnect |
| 🔁 **Auto-retry** | Tự retry 5 lần với exponential backoff khi rate limit |
| 💾 **Checkpoint** | Lưu tiến độ mỗi 20 files + backup file |
| 🔍 **Filter** | Lọc theo đuôi file (.mp4, .pdf...) |
| 🧹 **Auto GC** | Tự dọn RAM mỗi 60s, tránh crash |
| ♾️ **Không giới hạn** | Không giới hạn dung lượng copy |

---

## ⚠️ Lưu ý quan trọng

**Không hỗ trợ Google Docs/Sheets/Slides:**
- Tool chỉ copy các file thực (video, PDF, ZIP, hình ảnh...)
- Google Docs, Sheets, Slides, Forms... sẽ bị bỏ qua
- Lý do: Các file Google Workspace không có dung lượng thực và cần export sang định dạng khác

---

## 📖 Cách sử dụng

### Bước 1: Mở notebook trên Colab

Click nút **"Open in Colab"** ở trên

### Bước 2: Cấu hình Colab (khuyến nghị cho folder lớn)

1. Vào **Runtime** → **Change runtime type**
2. Chọn:
   - **GPU**: A100 (nếu có Pro+)
   - **High RAM**: BẬT (nếu có Pro+)
3. Nhấn **Save**

### Bước 3: Chạy từng cell theo thứ tự

| Cell | Mô tả |
|------|-------|
| **1️⃣ Cài đặt** | Cài thư viện cần thiết |
| **2️⃣ Nhập thông tin** | Nhập link folder nguồn và đích |
| **3️⃣ Run** | Bắt đầu copy |
| **4️⃣ Xóa checkpoint** | Chạy lại từ đầu (nếu cần) |

### Bước 4: Nếu bị timeout

Chạy lại **Cell 3** → Tool tự động resume từ chỗ dừng

---

## ⚙️ Giải thích các tùy chọn

| Tùy chọn | Mô tả | Ví dụ |
|----------|-------|-------|
| **Folder đích** | Link folder Google Drive của bạn | `https://drive.google.com/drive/folders/abc123` |
| **Folder nguồn** | Link folder cần copy (Shared Drive OK) | `https://drive.google.com/drive/folders/xyz789` |
| **Bỏ qua chứa** | Bỏ qua file/folder có tên chứa text này | `.tmp, backup, test` |
| **Chỉ đuôi** | Chỉ copy file có đuôi này | `.mp4, .pdf, .zip` |
| **Bỏ đuôi** | Bỏ qua file có đuôi này | `.tmp, .log, .bak` |
| **Bỏ qua file đã có** | Skip file đã tồn tại ở đích | ✅ (khuyến nghị) |
| **Dry-run** | Chỉ xem sẽ copy gì, không copy thật | ❌ |

---

## 🔥 Tips cho folder lớn (>500GB)

- Dùng **Colab Pro+** với **GPU A100** + **High RAM**
- Chạy **ban đêm** (ít rate limit hơn)
- Nếu **timeout** → chạy lại Cell 3, tool tự resume
- **Không cần** giữ tab mở, Colab chạy nền

---

## ❓ FAQ

### Q: Copy được Shared Drive không?
**A:** Có, chỉ cần bạn có quyền view folder đó.

### Q: Colab Free có dùng được không?
**A:** Có, nhưng hay timeout (~90 phút). Chạy lại sẽ tự resume.

### Q: Có mất dữ liệu không?
**A:** Không, tool chỉ copy (không xóa/move). File gốc vẫn nguyên.

### Q: Tốc độ copy bao nhiêu?
**A:** Tùy thuộc vào Google API, trung bình 20-100 MB/s.

### Q: Sao không copy được Google Docs?
**A:** Google Docs/Sheets/Slides không phải file thực, cần export. Tool này chỉ copy file có dung lượng thực.

---

## 📝 Changelog

### v1.0
- Copy tuần tự ổn định (không multi-thread để tránh crash)
- Checkpoint + backup file
- Auto-retry 5 lần với exponential backoff
- Exact match kiểm tra file (fix bug tool cũ dùng `contains`)
- Hỗ trợ folder 2000GB+
- Không giới hạn dung lượng
- Auto garbage collection

---

## 👤 Tác giả

**Nguyễn Ngọc Anh Tú**

- Facebook: [https://www.facebook.com/NguyenNgocAnhTu.VN](https://www.facebook.com/NguyenNgocAnhTu.VN)
- Telegram: [https://t.me/NguyenNgocAnhTu](https://t.me/NguyenNgocAnhTu)
- GitHub: [kazeidk](https://github.com/kazeidk)

---

## 📄 License

MIT License - Tự do sử dụng và chỉnh sửa
