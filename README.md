<h1 align="center">
  <img src="https://em-content.zobj.net/source/apple/391/rocket_1f680.png" width="50" height="50" alt="🚀"/>
  <br/>
  GDrive Turbo Copy v2.0
</h1>

<p align="center">
  <b>⚡ Copy Google Drive → Google Drive | Parallel Copy • MD5 Verify • ♾️ KHÔNG GIỚI HẠN</b>
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
    <img src="https://img.shields.io/badge/▶_OPEN_IN_COLAB-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Open In Colab"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.0-667eea?style=flat-square&labelColor=764ba2" alt="Version"/>
  <img src="https://img.shields.io/badge/License-MIT-28a745?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Platform-Google_Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white" alt="Platform"/>
  <img src="https://img.shields.io/badge/Status-Active-00d26a?style=flat-square" alt="Status"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/♾️_Unlimited-Copy_không_giới_hạn-667eea?style=flat-square" alt="Unlimited"/>
  <img src="https://img.shields.io/badge/🚀_Turbo-50~150_MB/s-00d26a?style=flat-square" alt="Speed"/>
  <img src="https://img.shields.io/badge/🔄_Auto_Resume-Checkpoint-17a2b8?style=flat-square" alt="Resume"/>
</p>

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Yêu cầu hệ thống](#-yêu-cầu-hệ-thống)
- [Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng)
- [Multi-Account Resume](#-multi-account-resume-mới)
- [Cấu trúc Notebook](#-cấu-trúc-notebook)
- [Tùy chọn nâng cao](#️-tùy-chọn-nâng-cao)
- [Cách hoạt động](#-cách-hoạt-động)
- [Xử lý sự cố](#-xử-lý-sự-cố)
- [FAQ](#-faq)
- [Changelog](#-changelog)
- [Tác giả](#-tác-giả)

---

## 📖 Giới thiệu

**GDrive Turbo Copy** là công cụ copy dữ liệu từ Google Drive sang Google Drive khác, chạy trên nền tảng Google Colab. Sử dụng phương thức **server-side copy** (copy trực tiếp trên server Google) nên:

- ✅ Không cần tải file về máy
- ✅ Không giới hạn dung lượng
- ✅ Tốc độ cao (50-150 MB/s)
- ✅ Hỗ trợ Shared Drive

### Tại sao chọn GDrive Turbo Copy?

| | Tính năng | Mô tả |
|:---:|:---|:---|
| ♾️ | **UNLIMITED** | Copy 100GB, 1TB, 10TB+ - không giới hạn |
| ⚡ | **SERVER-SIDE** | Copy trực tiếp trên server Google, không qua máy local |
| 🚀 | **TURBO MODE** | Cache thông minh, giảm 50% API calls |
| 🔄 | **AUTO RESUME** | Timeout? Chạy lại là tự tiếp tục từ chỗ dừng |
| 💾 | **CHECKPOINT** | Lưu tiến độ tự động mỗi 30s + backup |
| 🛡️ | **SAFE** | Chỉ copy, không xóa - file gốc nguyên vẹn |

---

## ✨ Tính năng

### Tính năng chính

| Icon | Tính năng | Mô tả |
|:---:|:---|:---|
| ♾️ | **Unlimited Copy** | Copy không giới hạn dung lượng |
| ⚡ | **Server-side Copy** | Copy trực tiếp trên server Google |
| 🚀 | **Turbo Mode** | Cache thông minh, tối ưu API calls |
| 🔄 | **Auto Resume** | Tự động tiếp tục khi timeout |
| 💾 | **Smart Checkpoint** | Lưu tiến độ tự động mỗi 30s |

### Tính năng bổ sung

| Icon | Tính năng | Mô tả |
|:---:|:---|:---|
| 🔁 | **Auto Retry** | Retry với exponential backoff khi gặp lỗi |
| 📊 | **Progress Bar** | Thanh tiến trình với hiệu ứng animation |
| 📈 | **Quota Estimate** | Ước tính % quota đã dùng (~750GB/ngày) |
| ⚠️ | **Quota Warning** | Cảnh báo khi gần hết quota (>90%) |
| 🎯 | **Exact Match** | Kiểm tra file trùng chính xác theo tên |
| 🔍 | **Smart Filter** | Lọc file theo tên hoặc đuôi file |
| 📄 | **Export Docs** | Xuất Google Docs/Sheets/Slides sang PDF |
| 🔗 | **Shortcut Detection** | Phát hiện và báo cáo shortcuts |
| 🔔 | **Sound Alert** | Âm thanh thông báo khi hoàn tất |
| 🧹 | **Auto GC** | Tự động dọn RAM định kỳ |
| 🗑️ | **Auto Cleanup** | Tự động xóa checkpoint khi copy xong |
| 📝 | **Full Logging** | Ghi log chi tiết mọi hoạt động |

---

## 💻 Yêu cầu hệ thống

### Bắt buộc
- Tài khoản Google
- Quyền **View** folder nguồn (folder cần copy)
- Quyền **Edit** folder đích (folder muốn copy vào)

### Khuyến nghị
- Google Colab Pro (ổn định hơn, ít timeout)
- High RAM runtime (cho folder lớn)

### Hỗ trợ
- ✅ My Drive → My Drive
- ✅ Shared Drive → My Drive
- ✅ My Drive → Shared Drive
- ✅ Shared Drive → Shared Drive

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Mở Notebook trên Colab

<a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Click vào badge trên hoặc truy cập trực tiếp link Colab.

### Bước 2: Chạy Cell 1 - Nhập thông tin

Chạy Cell 1 và điền thông tin:

| Trường | Mô tả | Ví dụ |
|:---|:---|:---|
| 📁 **Folder đích** | Link folder Google Drive của bạn | `https://drive.google.com/drive/folders/xxx` |
| 📂 **Folder nguồn** | Link folder cần copy | `https://drive.google.com/drive/folders/yyy` |

### Bước 3: Chạy Cell 2 - Bắt đầu copy

Chạy Cell 2, tool sẽ:
1. Yêu cầu xác thực tài khoản Google
2. Kiểm tra quyền truy cập
3. Bắt đầu copy

### Bước 4: Theo dõi tiến trình

```
[22:10:05] 🔐 Đang xác thực...
[22:10:08] ✅ Xác thực OK!
[22:10:08] 📂 Nguồn: MyFolder
[22:10:08] 📁 Đích: Backup
[22:10:08] ⚡ TURBO MODE: Cache + Optimized
[22:10:08] ♾️ Mode: KHÔNG GIỚI HẠN dung lượng
[22:10:08] ☁️ Multi-Account: Checkpoint lưu trên Drive
────────────────────────────────────────

📁 MyFolder: 20 files, 3 folders
[████████████████████████] 100%
⚡ 20/20 | 💾 500GB (67% quota) | 🚀 45.2MB/s | ⏱️ 33s

✅ HOÀN TẤT!
📁 Copied: 139 files | ⏭️ Skipped: 0 | ❌ Errors: 0
💾 700GB (~93% quota) | ⏱️ 2m53s | 🚀 22.5 MB/s
⚠️ Gần hết quota! Chuẩn bị account khác để tiếp tục.
```

### Bước 5: Xử lý timeout (nếu có)

> ⚠️ **Colab Free** thường timeout sau ~90 phút

**Giải pháp:** Chạy lại Cell 2 - tool sẽ tự động resume từ checkpoint.

---

## 🔄 Multi-Account Resume (MỚI)

Tính năng cho phép **nhiều tài khoản Google** tiếp tục copy khi một tài khoản bị giới hạn quota.

### Cách hoạt động

```
Account A: Copy 750GB → Bị limit
    ↓
Share folder đích cho Account B (Editor)
Share folder nguồn cho Account B (Viewer)
    ↓
Account B: Mở Colab → Nhập link → Chạy Cell 2
    ↓
Tool hiện: "☁️ Resume từ Drive: xxx files (750GB)"
    ↓
Copy tiếp phần còn lại
```

### Hướng dẫn chi tiết

1. **Khi Account A bị limit:**
   - Dừng lại, checkpoint đã được lưu tự động lên Google Drive

2. **Share folder cho Account B:**
   - Folder đích: Share với quyền **Editor**
   - Folder nguồn: Share với quyền **Viewer** (nếu chưa có)

3. **Account B tiếp tục:**
   - Mở Colab bằng Account B
   - Nhập cùng link nguồn/đích
   - Chạy Cell 2 → Tool tự động đọc checkpoint từ Drive

### Lưu ý

- Checkpoint được lưu tại folder đích với tên `.gdrive_turbo_checkpoint.json`
- Có thể dùng nhiều account (A → B → C → ...) để copy không giới hạn
- Mỗi account có quota riêng

### Quota Estimate

Tool hiển thị ước tính % quota đã dùng dựa trên giới hạn ~750GB/ngày:

```
⚡ 15/20 | 💾 500GB (67% quota) | 🚀 45.2MB/s | ⏱️ 2m30s
```

- **< 90%**: Tiếp tục copy bình thường
- **> 90%**: Hiện cảnh báo, chuẩn bị đổi account
- **Lưu ý**: Con số 750GB là ước tính, thực tế có thể khác tùy loại tài khoản

---

## 📑 Cấu trúc Notebook

| Cell | Tên | Chức năng |
|:---:|:---|:---|
| 1️⃣ | **Nhập thông tin** | Nhập link folder nguồn/đích, cài đặt bộ lọc |
| 2️⃣ | **Run Copy** | Thực hiện copy (chạy lại nếu timeout) |
| 3️⃣ | **Xóa checkpoint** | Reset để copy lại từ đầu |
| 4️⃣ | **Xem Log** | Xem thống kê, file lỗi, shortcuts |

---

## ⚙️ Tùy chọn nâng cao

### Bộ lọc file

| Tùy chọn | Mô tả | Ví dụ |
|:---|:---|:---|
| 🚫 **Bỏ qua chứa** | Skip file có tên chứa text này | `.tmp, backup, test` |
| ✅ **Chỉ lấy đuôi** | Chỉ copy file có đuôi này | `.mp4, .pdf, .zip` |
| ❌ **Bỏ qua đuôi** | Skip file có đuôi này | `.log, .bak, .tmp` |

### Cài đặt

| Tùy chọn | Mô tả | Mặc định |
|:---|:---|:---:|
| ⏭️ **Skip file đã có** | Bỏ qua file trùng tên ở đích | ✅ Bật |
| 📄 **Export Docs** | Xuất Google Docs/Sheets/Slides sang PDF | ❌ Tắt |
| 👁️ **Dry-run** | Chỉ xem preview, không copy thật | ❌ Tắt |

### Ví dụ sử dụng bộ lọc

**Chỉ copy video:**
```
✅ Chỉ lấy đuôi: .mp4, .mkv, .avi, .mov
```

**Bỏ qua file tạm:**
```
🚫 Bỏ qua chứa: temp, backup, old
❌ Bỏ qua đuôi: .tmp, .log, .bak
```

---

## 🔧 Cách hoạt động

### Quy trình copy

```
1. Xác thực Google Account
         ↓
2. Đọc danh sách file/folder từ nguồn
         ↓
3. Tạo folder tương ứng ở đích
         ↓
4. Gọi API files().copy() cho từng file
         ↓
5. Lưu checkpoint mỗi 30s
         ↓
6. Hoàn tất / Resume nếu timeout
```

### Cơ chế Checkpoint

- **Lưu tự động** mỗi 30 giây
- **Backup** file checkpoint cũ trước khi ghi mới
- **Resume** tự động khi chạy lại Cell 2
- **Vị trí:** `/content/checkpoint.json`

### Rate Limit Handling

- **Adaptive delay:** Tự động tăng delay khi gặp rate limit
- **Exponential backoff:** Retry với thời gian chờ tăng dần
- **Auto recovery:** Giảm delay khi API ổn định

---

## 🔧 Xử lý sự cố

### Lỗi thường gặp

| Lỗi | Nguyên nhân | Giải pháp |
|:---|:---|:---|
| `❌ URL không hợp lệ` | Link folder sai format | Kiểm tra lại link, đảm bảo là link folder |
| `❌ Không truy cập được` | Không có quyền | Kiểm tra quyền view/edit folder |
| `⚠️ Rate limit` | Quá nhiều request | Đợi tool tự retry, hoặc chạy lại sau |
| `Timeout` | Colab ngắt kết nối | Chạy lại Cell 2 để resume |

### Tips tối ưu

| Tip | Mô tả |
|:---|:---|
| 🌙 **Chạy ban đêm** | Ít rate limit hơn do ít người dùng |
| 💪 **Colab Pro** | Ổn định hơn, ít timeout |
| 🧠 **High RAM** | Chọn runtime High RAM cho folder lớn |
| 🔍 **Dùng bộ lọc** | Chỉ copy file cần thiết, nhanh hơn |

### Xem log chi tiết

- **Log file:** `/content/gdrive_copy.log`
- **Checkpoint:** `/content/checkpoint.json`
- **Xem trong Colab:** Chạy Cell 4

---

## ❓ FAQ

<details>
<summary><b>♾️ Copy được bao nhiêu dung lượng?</b></summary>

**Không giới hạn!** Tool sử dụng server-side copy nên có thể copy 100GB, 1TB, 10TB+ mà không gặp vấn đề về dung lượng.
</details>

<details>
<summary><b>🔗 Copy được Shared Drive không?</b></summary>

**Có!** Tool hỗ trợ đầy đủ:
- My Drive → My Drive
- Shared Drive → My Drive
- My Drive → Shared Drive
- Shared Drive → Shared Drive

Chỉ cần có quyền view folder nguồn và edit folder đích.
</details>

<details>
<summary><b>💰 Colab Free dùng được không?</b></summary>

**Có!** Colab Free hoạt động tốt, chỉ hay timeout sau ~90 phút. Khi timeout, chạy lại Cell 2 là tool tự động resume từ checkpoint.
</details>

<details>
<summary><b>🛡️ Có mất dữ liệu gốc không?</b></summary>

**Không!** Tool chỉ thực hiện thao tác copy, không xóa hay sửa đổi bất kỳ file nào ở folder nguồn.
</details>

<details>
<summary><b>🚀 Tốc độ copy bao nhiêu?</b></summary>

Trung bình **50-150 MB/s** tùy thuộc vào:
- Tình trạng API Google
- Kích thước file (file lớn nhanh hơn)
- Thời điểm trong ngày
</details>

<details>
<summary><b>📄 Sao không copy được Google Docs?</b></summary>

Google Docs/Sheets/Slides là file đặc biệt, không có dung lượng thực. Để copy:
1. Bật tùy chọn **"Export Docs"** ở Cell 1
2. Tool sẽ xuất ra file PDF
</details>

<details>
<summary><b>🔗 Shortcuts có được copy không?</b></summary>

**Không.** Shortcuts chỉ là liên kết, không phải file thực. Tool sẽ phát hiện và báo cáo danh sách shortcuts ở Cell 4.
</details>

<details>
<summary><b>🔄 Làm sao copy lại từ đầu?</b></summary>

Chạy **Cell 3** để xóa checkpoint, sau đó chạy lại Cell 2.
</details>

---

## 📋 Changelog

### v2.0 (Parallel & Smart Verify)
- 🧵 **Parallel Copy**: Copy song song với ThreadPoolExecutor (1-6 threads, mặc định 3)
- ✅ **MD5+Size Verify**: Skip file trùng dựa trên tên + size, verify bằng md5Checksum
- 📊 **Overall Progress**: Pre-scan tổng số files + hiển thị progress tổng thể với ETA
- 📄 **Multi-format Export**: Google Docs→DOCX, Sheets→XLSX, Slides→PPTX (hoặc PDF)
- 🔗 **Resolve Shortcuts**: Option copy file gốc mà shortcut trỏ tới
- 🛡️ **Smart Error Handling**: Phân loại lỗi (RATE_LIMIT/NOT_FOUND/PERMISSION_DENIED/SERVER_ERROR/TIMEOUT)
- 🔄 **Smart Retry**: Cell 5 tự động bỏ qua file NOT_FOUND/PERMISSION_DENIED, chỉ retry lỗi tạm thời
- 🔒 **Thread-safe**: Lock + Semaphore bảo vệ shared state khi copy song song
- 📊 **Checkpoint Schema v2**: Thêm schema versioning cho checkpoint
- 🎨 **HTML Summary**: Bảng summary cuối cùng với HTML table đẹp hơn
- 📉 **Optimized API**: Dùng `fields` param giảm data transfer trong mọi API call

### v1.2 (Stability & Performance)
- ⏱️ **API Timeout**: Thêm timeout 5 phút cho API calls, tránh treo vô hạn
- 🧹 **Memory Management**: Tự động clear cache khi vượt 10,000 entries
- 🔧 **Lambda Fix**: Sửa closure bug trong loop với lambda
- ✅ **Verify Consistency**: Verify giờ dùng cùng filter như copy (exclude_str, include_ext, exclude_ext)
- 🛡️ **Null Check**: Thêm kiểm tra null trước khi verify
- 🆔 **Session ID**: Thêm session tracking để debug
- 📝 Code cleanup và cải thiện error handling

### v1.1 (Multi-Account Support)
- 🔄 **Multi-Account Resume**: Checkpoint lưu lên Google Drive, cho phép nhiều account tiếp tục copy
- ☁️ Cloud checkpoint: Tự động sync checkpoint lên folder đích
- 📈 **Quota Estimate**: Hiển thị % quota đã dùng (~750GB/ngày)
- ⚠️ **Quota Warning**: Cảnh báo khi gần hết quota (>90%)
- 🧹 **Auto-cleanup**: Tự động xóa checkpoint khi copy hoàn tất không lỗi
- 🔧 Cải thiện Cell 3: Xóa checkpoint cả local và trên Drive
- 📝 Cập nhật hướng dẫn

### v1.0 (Initial Release)
- ♾️ Copy không giới hạn dung lượng
- ⚡ Server-side copy siêu nhanh
- 🚀 Turbo Mode với cache thông minh
- 🔄 Auto resume khi timeout
- 💾 Checkpoint + backup tự động
- 📊 Progress bar với animation
- 📄 Export Google Docs sang PDF
- 🔍 Smart filter theo tên/đuôi file
- 🔔 Sound alert khi hoàn tất
- 📝 Full logging

---

## 👨‍💻 Tác giả

<p align="center">
  <b>Nguyễn Ngọc Anh Tú</b>
</p>

<p align="center">
  <a href="https://www.messenger.com/channel/NguyenNgocAnhTu.VN">
    <img src="https://img.shields.io/badge/📢_Kênh_TB-Messenger-0084FF?style=for-the-badge" alt="Messenger"/>
  </a>
  <a href="https://www.facebook.com/NguyenNgocAnhTu.VN">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook"/>
  </a>
  <a href="https://t.me/NguyenNgocAnhTu">
    <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"/>
  </a>
  <a href="https://github.com/kazeidk">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

---

## 📄 License

MIT License - Xem file [LICENSE](LICENSE) để biết thêm chi tiết.

---

<p align="center">
  ⭐ <b>Star</b> repo nếu thấy hữu ích • 🔄 <b>Share</b> cho bạn bè
</p>

<p align="center">
  Made with ❤️ by <b>Nguyễn Ngọc Anh Tú</b>
</p>
