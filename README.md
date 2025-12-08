# ⚡ GDrive Turbo Copy

> **Google Drive folder copy tool - runs on Google Colab**

<a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## 🤔 Tool này để làm gì?

**GDrive Turbo Copy** giúp bạn **copy toàn bộ folder từ Google Drive này sang Google Drive khác** một cách nhanh chóng.

### Ví dụ sử dụng:

| Tình huống | Giải pháp |
|------------|-----------|
| 🎬 Bạn bè share folder phim 500GB, muốn copy về Drive của mình | ✅ Dùng tool này |
| 📚 Có folder tài liệu trên Shared Drive công ty, muốn backup | ✅ Dùng tool này |
| 💾 Muốn copy folder từ Drive cũ sang Drive mới | ✅ Dùng tool này |
| 🎮 Ai đó share folder game/software, muốn lưu lại | ✅ Dùng tool này |

### Tại sao không copy thủ công?

| Cách | Vấn đề |
|------|--------|
| **Tải về máy rồi upload lại** | Chậm, tốn băng thông, hay lỗi |
| **Dùng "Add shortcut"** | Không phải copy thật, xóa gốc là mất |
| **Dùng "Make a copy"** | Chỉ copy được 1 file, không copy folder |

### Tool này giải quyết như thế nào?

- ✅ Copy **trực tiếp trên server Google** (không qua máy bạn)
- ✅ Copy **cả folder** với toàn bộ file bên trong
- ✅ **Nhanh hơn** so với tải về rồi upload
- ✅ **Tự động tiếp tục** nếu bị ngắt giữa chừng
- ✅ **Miễn phí** - chạy trên Google Colab

---

## ✨ Tính năng

| Tính năng | Mô tả |
|-----------|-------|
| 🎯 **Exact match** | Kiểm tra file chính xác (không trùng lặp) |
| 🔄 **Auto-resume** | Lưu checkpoint, tự tiếp tục khi timeout |
| 🔁 **Auto-retry** | Tự động retry khi rate limit |
| 📊 **Progress bar** | Hiển thị tiến độ copy |
| 🔍 **Dry-run** | Xem trước không copy thật |
| 🎛️ **Filter** | Lọc theo đuôi file hoặc tên |
| 💾 **Checkpoint** | Lưu tiến độ mỗi 10 files |
| 📝 **Log chi tiết** | Ghi log để debug |

---

## 📦 Yêu cầu

- Tài khoản Google
- Quyền truy cập folder nguồn (view hoặc edit)
- Quyền truy cập folder đích (edit)

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Mở notebook trên Colab

Click badge **"Open in Colab"** ở trên hoặc link:
https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb

### Bước 2: Cấu hình Colab (tùy chọn)

Vào **Runtime** → **Change runtime type**:

#### Cho Colab Pro+ (khuyến nghị):
| Setting | Chọn |
|---------|------|
| Kiểu thời gian chạy | **Python 3** |
| Bộ tăng tốc phần cứng | **GPU A100** |
| RAM cao | **BẬT** ✅ |

#### Cho Colab Free:
| Setting | Chọn |
|---------|------|
| Kiểu thời gian chạy | **Python 3** |
| Bộ tăng tốc phần cứng | **Bộ xử lý (CPU)** |

---

### Bước 3: Chạy cell "Cài đặt thư viện"

1. Click vào cell `1️⃣ Cài đặt thư viện`
2. Nhấn **Shift + Enter**
3. Đợi đến khi hiện `✅ Đã cài đặt xong!`

---

### Bước 4: Chạy cell "Nhập thông tin"

1. Click vào cell `2️⃣ Nhập thông tin`
2. Nhấn **Shift + Enter**
3. Điền thông tin:

| Field | Mô tả | Ví dụ |
|-------|-------|-------|
| **📁 Folder đích** | Link folder Google Drive của bạn | `https://drive.google.com/drive/folders/abc123...` |
| **📂 Folder nguồn** | Link folder cần copy | `https://drive.google.com/drive/folders/xyz789...` |
| **💾 Giới hạn (GB)** | 0 = không giới hạn | `0` |

---

### Bước 5: Chạy cell "Run"

1. Click vào cell `3️⃣ Run - GDrive Turbo Copy`
2. Nhấn **Shift + Enter**
3. **Lần đầu**: Click "Allow" để cấp quyền truy cập Google Drive
4. Đợi tool chạy

Khi hoàn tất:
```
==================================================
📊 KẾT QUẢ
✅ Copied: 1234 | ⏭️ Skipped: 56 | ❌ Errors: 0
💾 45.67GB | ⏱️ 930s | 🚀 52.3MB/s
==================================================
🎉 HOÀN TẤT!
```

---

## 📖 Giải thích các tùy chọn

| Tùy chọn | Mô tả | Ví dụ |
|----------|-------|-------|
| **Folder đích** | Link folder nơi bạn muốn copy đến | |
| **Folder nguồn** | Link folder cần copy | |
| **Giới hạn (GB)** | Dừng khi đạt dung lượng này. 0 = không giới hạn | `100` |
| **Bỏ qua chứa** | Bỏ qua file có tên chứa chuỗi này | `.tmp, backup` |
| **Chỉ copy đuôi** | Chỉ copy file có đuôi này | `.pdf, .mp4` |
| **Bỏ qua đuôi** | Bỏ qua file có đuôi này | `.tmp, .log` |
| **Dry-run** | Chỉ xem sẽ copy gì, không copy thật | |
| **Ghi đè nếu size khác** | Ghi đè file nếu size khác | |

---

## 🔧 Xử lý sự cố

### Bị timeout / disconnect

**Giải pháp**: Chạy lại cell "Run" - tool sẽ tự động resume từ checkpoint

### Rate limit (lỗi 403/429)

**Giải pháp**: Tool tự động retry với exponential backoff

### Không truy cập được folder

**Giải pháp**:
1. Kiểm tra link folder đúng chưa
2. Đảm bảo có quyền view folder nguồn
3. Đảm bảo có quyền edit folder đích

### Muốn copy lại từ đầu

**Giải pháp**: Chạy cell `4️⃣ Tiện ích - Xóa checkpoint`

---

## ❓ FAQ

### Q: Copy được Shared Drive không?
**A**: Có, chỉ cần bạn có quyền view folder đó.

### Q: Copy được Google Docs/Sheets/Slides không?
**A**: Không, tool chỉ copy file thường (PDF, video, zip...).

### Q: Colab Free có dùng được không?
**A**: Có, nhưng hay timeout (~90 phút). Chạy lại sẽ tự resume.

### Q: Có mất dữ liệu không?
**A**: Không, tool chỉ copy (không xóa/move). File gốc vẫn nguyên.

---

## 📝 License

MIT License

---

Made with ❤️ by kazeidk
