<h1 align="center">
  <img src="https://em-content.zobj.net/source/apple/391/rocket_1f680.png" width="50" height="50" alt="🚀"/>
  <br/>
  GDrive Turbo Copy v1.0
</h1>

<p align="center">
  <b>⚡ Copy Google Drive → Google Drive | Siêu nhanh • Ổn định • ♾️ KHÔNG GIỚI HẠN</b>
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
    <img src="https://img.shields.io/badge/▶_OPEN_IN_COLAB-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Open In Colab"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-667eea?style=flat-square&labelColor=764ba2" alt="Version"/>
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

## ⚡ Tại sao chọn GDrive Turbo Copy?

| | Tính năng | Mô tả |
|:---:|:---|:---|
| ♾️ | **UNLIMITED** | Copy 100GB, 1TB, 10TB+ - không giới hạn |
| ⚡ | **SERVER-SIDE** | Copy trực tiếp trên server Google |
| 🚀 | **TURBO MODE** | Cache thông minh, tốc độ 50-150 MB/s |
| 🔄 | **AUTO RESUME** | Timeout? Chạy lại là tự tiếp tục |
| 💾 | **CHECKPOINT** | Lưu tiến độ tự động + backup |
| 🛡️ | **SAFE** | Chỉ copy, không xóa - file gốc nguyên vẹn |

---

## 🎯 Tính năng đầy đủ

| Icon | Tính năng | Mô tả |
|:---:|:---|:---|
| ♾️ | **Unlimited Copy** | Copy không giới hạn dung lượng |
| ⚡ | **Server-side Copy** | Copy trực tiếp trên server Google |
| 🚀 | **Turbo Mode** | Cache thông minh, giảm 50% API calls |
| 🔄 | **Auto Resume** | Tự động tiếp tục khi timeout |
| 💾 | **Smart Checkpoint** | Lưu tiến độ tự động mỗi 30s |
| 🔁 | **Auto Retry** | Retry với exponential backoff |
| 📊 | **Progress Bar** | Thanh tiến trình đẹp với hiệu ứng shine animation |
| 🎯 | **Exact Match** | Kiểm tra file trùng chính xác |
| 🔍 | **Smart Filter** | Lọc theo tên, đuôi file |
| 📄 | **Export Docs** | Xuất Google Docs sang PDF |
| 🔗 | **Shortcut Detection** | Phát hiện và báo cáo shortcuts |
| 🔔 | **Sound Alert** | Âm thanh thông báo hoàn tất |
| 🧹 | **Auto GC** | Tự động dọn RAM |
| 📝 | **Full Logging** | Ghi log chi tiết |

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Mở Colab
<a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### Bước 2: Nhập thông tin (Cell 1)
- 📁 **Folder đích:** Link folder Google Drive của bạn
- 📂 **Folder nguồn:** Link folder cần copy

### Bước 3: Chạy copy (Cell 2)
```
[22:10:05] 🔐 Đang xác thực...
[22:10:08] ✅ Xác thực OK!
[22:10:08] 📂 Nguồn: MyFolder
[22:10:08] 📁 Đích: Backup
[22:10:08] ⚡ TURBO MODE: Cache + Optimized
[22:10:08] ♾️ Mode: KHÔNG GIỚI HẠN dung lượng
────────────────────────────────────────

📁 MyFolder: 20 files, 3 folders
┌──────────────────────────────────────────────────┐
│██████████████████████████████████████████  100%  │  ← Thanh xanh với hiệu ứng shine
└──────────────────────────────────────────────────┘
🚀 20/20 files | 💾 1.5GB | ⚡ 45.2MB/s | ⏱️ 33s | ETA: 0s

✅ HOÀN TẤT!
📁 Copied: 139 files | ⏭️ Skipped: 0 | ❌ Errors: 0
💾 3.81GB | ⏱️ 2m53s | 🚀 22.5 MB/s
```

> 💡 **Timeout?** Chạy lại Cell 2 - tự động resume từ chỗ dừng!

---

## 🎮 Các Cell

| Cell | Chức năng |
|:---:|:---|
| 1️⃣ | **Nhập thông tin** - Link folder, cài đặt bộ lọc |
| 2️⃣ | **Run Copy** - Thực hiện copy |
| 3️⃣ | **Xóa checkpoint** - Reset để copy lại từ đầu |
| 4️⃣ | **Xem Log** - Thống kê, file lỗi, shortcuts |

---

## ⚙️ Tùy chọn

| Tùy chọn | Mô tả | Mặc định |
|:---|:---|:---:|
| 🚫 **Bỏ qua chứa** | Skip file có tên chứa text (VD: `.tmp, backup`) | - |
| ✅ **Chỉ lấy đuôi** | Chỉ copy file có đuôi này (VD: `.mp4, .pdf`) | - |
| ❌ **Bỏ qua đuôi** | Skip file có đuôi này (VD: `.log, .bak`) | - |
| ⏭️ **Skip file đã có** | Bỏ qua file trùng tên | ✅ |
| 📄 **Export Docs** | Xuất Google Docs sang PDF | ❌ |
| 👁️ **Dry-run** | Chỉ xem preview, không copy | ❌ |

---

## 💡 Tips

- 🌙 Chạy **ban đêm** để ít rate limit hơn
- 💪 Dùng **Colab Pro + High RAM** để ổn định hơn
- 🔄 **Timeout?** Chạy lại Cell 2 ngay - tự động resume
- 📋 Xem log chi tiết tại `/content/gdrive_copy.log`
- 🎯 Dùng **bộ lọc** để copy chính xác file cần thiết

---

## ❓ FAQ

<details>
<summary><b>♾️ Copy được bao nhiêu dung lượng?</b></summary>

**Không giới hạn!** Copy 100GB, 1TB, 10TB+ đều OK.
</details>

<details>
<summary><b>🔗 Copy được Shared Drive không?</b></summary>

**Có!** Chỉ cần có quyền view folder nguồn.
</details>

<details>
<summary><b>💰 Colab Free dùng được không?</b></summary>

**Có!** Chỉ hay timeout (~90 phút). Chạy lại Cell 2 là tự resume.
</details>

<details>
<summary><b>🛡️ Có mất dữ liệu gốc không?</b></summary>

**Không!** Tool chỉ copy, không xóa hay sửa file gốc.
</details>

<details>
<summary><b>🚀 Tốc độ copy bao nhiêu?</b></summary>

Trung bình **50-150 MB/s** tùy Google API.
</details>

<details>
<summary><b>📄 Sao không copy được Google Docs?</b></summary>

Bật **"Export Docs"** để xuất ra PDF.
</details>

---

## 📋 Changelog

### v1.0
- ♾️ Copy không giới hạn dung lượng
- ⚡ Server-side copy siêu nhanh
- 🚀 Turbo Mode với cache thông minh
- 🔄 Auto resume khi timeout
- 💾 Checkpoint + backup
- 📊 Progress bar đẹp với hiệu ứng shine animation màu xanh lá
- 📄 Export Google Docs sang PDF
- 🔍 Smart filter
- 🔔 Sound alert

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

<p align="center">
  ⭐ <b>Star</b> repo nếu thấy hữu ích • 🔄 <b>Share</b> cho bạn bè
</p>

<p align="center">
  <img src="https://img.shields.io/badge/📄_MIT_License-28a745?style=flat-square" alt="License"/>
</p>

<p align="center">
  Made with ❤️ by <b>Nguyễn Ngọc Anh Tú</b>
</p>
