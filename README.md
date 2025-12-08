# ⚡ GDrive Turbo Copy

> **Blazing fast Google Drive folder copy tool - runs on Google Colab**

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
- ✅ **Nhanh gấp 10-50 lần** so với tải về rồi upload
- ✅ **Tự động tiếp tục** nếu bị ngắt giữa chừng
- ✅ **Miễn phí** - chạy trên Google Colab

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Yêu cầu](#-yêu-cầu)
- [Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng)
- [Cấu hình tối ưu](#-cấu-hình-tối-ưu)
- [Giải thích các tùy chọn](#-giải-thích-các-tùy-chọn)
- [Xử lý sự cố](#-xử-lý-sự-cố)
- [FAQ](#-faq)

---

## 🎯 Giới thiệu

**GDrive Turbo Copy** là công cụ copy folder Google Drive siêu nhanh, chạy trên Google Colab. Tool copy trực tiếp server-to-server (không tải về máy bạn), hỗ trợ Shared Drive, tự động resume khi timeout.

### Tại sao dùng tool này?

| So sánh | Copy thủ công | GDrive Turbo Copy |
|---------|---------------|-------------------|
| Tốc độ | Chậm (qua máy bạn) | **Nhanh 10-50x** (server-to-server) |
| Folder lớn | Hay lỗi | **Tự động resume** |
| Shared Drive | Khó copy | **Hỗ trợ đầy đủ** |
| Rate limit | Bị chặn | **Tự động retry** |

---

## ✨ Tính năng

| Tính năng | Mô tả |
|-----------|-------|
| ⚡ **Copy song song** | Lên đến 15 luồng, tăng tốc 5-10x |
| 🎯 **Auto-detect** | Tự nhận diện Colab tier & set luồng tối ưu |
| 🔄 **Auto-resume** | Lưu checkpoint, tự tiếp tục khi timeout |
| 🔁 **Auto-retry** | Tự động retry 5 lần khi rate limit |
| 📊 **Progress + ETA** | Hiển thị tiến độ và thời gian còn lại |
| 📈 **Scan trước** | Đếm tổng số file trước khi copy |
| 🔍 **Dry-run** | Xem trước không copy thật |
| 🎛️ **Filter** | Lọc theo đuôi file hoặc tên |
| 📝 **Log chi tiết** | Ghi log để debug |
| � **oThông báo** | Âm thanh khi hoàn tất |

---

## 📦 Yêu cầu

- Tài khoản Google
- Quyền truy cập folder nguồn (view hoặc edit)
- Quyền truy cập folder đích (edit)

### Khuyến nghị

- **Colab Pro+** với **GPU A100** + **RAM cao** để đạt tốc độ tối đa
- Colab Free vẫn chạy được nhưng chậm hơn và hay timeout

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Cấu hình Colab (quan trọng!)

1. Mở notebook trên Colab (click badge "Open in Colab" ở trên)

2. Vào **Runtime** → **Change runtime type**

3. Cấu hình như sau:


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

4. Nhấn **Lưu/Save**

---

### Bước 2: Chạy cell "Cài đặt thư viện"

1. Click vào cell đầu tiên `1️⃣ Cài đặt thư viện`
2. Nhấn **Shift + Enter** hoặc click nút ▶️ Play
3. Đợi vài giây cho đến khi hiện `✅ Đã cài đặt xong!`

---

### Bước 3: Chạy cell "Nhập thông tin"

1. Click vào cell `2️⃣ Nhập thông tin`
2. Nhấn **Shift + Enter**
3. Tool sẽ tự động detect cấu hình máy:

```
🔥================================================🔥
🚀 DETECTED: A100 TURBO
💾 System RAM: 167.1 GB
🎮 GPU: NVIDIA A100-SXM4-40GB
⚡ Auto-set: 15 workers (MAX POWER!)
🔥================================================🔥
```

4. Điền thông tin vào form:

| Field | Mô tả | Ví dụ |
|-------|-------|-------|
| **📁 Folder đích** | Link folder Google Drive của bạn | `https://drive.google.com/drive/folders/abc123...` |
| **📂 Folder nguồn** | Link folder cần copy | `https://drive.google.com/drive/folders/xyz789...` |
| **⚡ Số luồng** | Đã tự động set, có thể chỉnh | `15` |
| **💾 Giới hạn (GB)** | 0 = không giới hạn | `0` |

---

### Bước 4: Chạy cell "Run"

1. Click vào cell `3️⃣ Run - GDrive Turbo Copy`
2. Nhấn **Shift + Enter**
3. **Lần đầu**: Google sẽ yêu cầu đăng nhập
   - Click "Allow" để cấp quyền truy cập Google Drive
4. Đợi tool chạy:

```
🔐 Đang xác thực...
✅ Xác thực thành công
📂 Nguồn: My Folder
📂 Đích: My Drive
📊 Đang scan tổng số file...
📊 Tổng: 1234 files
--------------------------------------------------
📊 150 files, 10 folders
Copying: 100%|██████████| 150/150 [02:30<00:00]
✅ file1.mp4 (500.0MB, 85.2MB/s) ETA:5m30s
...
```

5. Khi hoàn tất sẽ có âm thanh thông báo và hiện:

```
==================================================
📊 KẾT QUẢ
✅ Copied: 1234 | ⏭️ Skipped: 56 | ❌ Errors: 0
💾 45.67GB | ⏱️ 15m30s | 🚀 52.3MB/s
📄 Log: /content/copy_log.txt
==================================================
🎉 HOÀN TẤT!
```

---

## ⚙️ Cấu hình tối ưu

### Auto-detect theo cấu hình máy:

| Cấu hình | RAM | Số luồng auto |
|----------|-----|---------------|
| 🔥 **A100 TURBO** | > 100GB | **15** |
| 🚀 A100 | > 50GB | 12 |
| ⚡ Pro+ High-RAM | > 20GB | 10 |
| 💪 Pro | > 12GB | 6 |
| 🆓 Free | ≤ 12GB | 3 |

### Setting tối đa cho Pro+:

| Setting | Giá trị |
|---------|---------|
| GPU | A100 |
| RAM cao | BẬT |
| Số luồng | 15 (auto) |
| Giới hạn GB | 0 |

---

## 📖 Giải thích các tùy chọn

### Thông tin chính

| Tùy chọn | Mô tả |
|----------|-------|
| **Folder đích** | Link folder Google Drive nơi bạn muốn copy đến |
| **Folder nguồn** | Link folder Google Drive cần copy (có thể là Shared Drive) |

### Phân trang

| Tùy chọn | Mô tả |
|----------|-------|
| **Từ trang** | Bắt đầu từ trang nào (0 = từ đầu) |
| **Đến trang** | Kết thúc ở trang nào (0 = đến cuối) |

*Mỗi trang = 1000 files. Dùng khi folder quá lớn muốn chia nhỏ.*

### Cấu hình

| Tùy chọn | Mô tả |
|----------|-------|
| **Giới hạn (GB)** | Dừng khi đạt dung lượng này. 0 = không giới hạn |
| **Số luồng** | Số file copy song song. Auto-detect theo RAM |

### Bộ lọc

| Tùy chọn | Mô tả | Ví dụ |
|----------|-------|-------|
| **Bỏ qua chứa** | Bỏ qua file/folder có tên chứa chuỗi này | `.tmp, backup, test` |
| **Chỉ copy đuôi** | Chỉ copy file có đuôi này | `.pdf, .mp4, .zip` |
| **Bỏ qua đuôi** | Bỏ qua file có đuôi này | `.tmp, .log, .bak` |

### Tùy chọn

| Tùy chọn | Mô tả |
|----------|-------|
| **Dry-run** | Chỉ xem sẽ copy gì, không copy thật |
| **Ghi đè nếu size khác** | Nếu file đã tồn tại nhưng size khác thì ghi đè |

---

## 🔧 Xử lý sự cố

### Bị timeout / disconnect

**Nguyên nhân**: Colab tự ngắt sau một thời gian

**Giải pháp**:
1. Chạy lại cell "Run"
2. Tool sẽ tự động resume từ checkpoint
3. Các file đã copy sẽ được skip

### Rate limit (lỗi 403/429)

**Nguyên nhân**: Google Drive API giới hạn số request

**Giải pháp**: Tool tự động retry với exponential backoff (đợi 2s, 4s, 8s, 16s, 32s)

### Không truy cập được folder

**Nguyên nhân**: Không có quyền

**Giải pháp**:
1. Kiểm tra link folder đúng chưa
2. Đảm bảo bạn có quyền view folder nguồn
3. Đảm bảo bạn có quyền edit folder đích

### Muốn copy lại từ đầu

**Giải pháp**: Chạy cell `4️⃣ Tiện ích - Xóa checkpoint`

---

## 📁 Files sau khi chạy

| File | Mô tả |
|------|-------|
| `/content/copy_checkpoint.json` | Lưu tiến độ để resume |
| `/content/copy_log.txt` | Log chi tiết quá trình copy |

---

## ❓ FAQ

### Q: Copy được Shared Drive không?
**A**: Có, chỉ cần bạn có quyền view folder đó.

### Q: Copy được Google Docs/Sheets/Slides không?
**A**: Không, tool chỉ copy file thường (PDF, video, zip...). Google Docs native không có size nên không copy được.

### Q: Tốc độ copy bao nhiêu?
**A**: Tùy thuộc vào:
- Cấu hình Colab (A100 nhanh nhất)
- Kích thước file (file lớn nhanh hơn)
- Thời điểm (đêm khuya nhanh hơn)

Trung bình: **30-100 MB/s** với A100

### Q: Colab Free có dùng được không?
**A**: Có, nhưng:
- Chậm hơn (3 luồng)
- Hay timeout (~90 phút)
- Chạy lại sẽ tự resume

### Q: Có mất dữ liệu không?
**A**: Không, tool chỉ copy (không xóa/move). File gốc vẫn nguyên.

---

## 📝 License

MIT License - Tự do sử dụng và chỉnh sửa

---

## 🙏 Credits

Made with ❤️ by kazeidk
