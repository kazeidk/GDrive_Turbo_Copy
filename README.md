<h1 align="center">🚀 GDrive Turbo Copy v1.0</h1>

<p align="center">
  <strong>Công cụ sao chép Google Drive mạnh mẽ và không giới hạn</strong>
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
    <img src="https://img.shields.io/badge/Open%20In-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Open In Colab"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0-blue?style=flat-square" alt="Version"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Python-3.x-yellow?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-orange?style=flat-square" alt="Platform"/>
</p>

---

## 🎯 Giới thiệu

**GDrive Turbo Copy** là công cụ copy folder Google Drive sang Google Drive với tốc độ cao, sử dụng Google Drive API để copy trực tiếp trên server (không download/upload qua máy bạn).

### ✨ Điểm nổi bật

| Tính năng | Mô tả |
|:---|:---|
| ♾️ **Không giới hạn** | Copy 100GB, 1TB, 10TB+ - không giới hạn dung lượng |
| 🚀 **TURBO MODE** | Cache thông minh, giảm 50% API calls, tốc độ 50-150 MB/s |
| ⚡ **Server-side** | Copy trực tiếp trên server Google, không qua máy bạn |
| 🔄 **Auto resume** | Timeout? Chạy lại là tự tiếp tục, không mất tiến độ |
| 💾 **Smart checkpoint** | Lưu tiến độ tự động + backup |
| 🛡️ **An toàn** | Chỉ copy, không xóa - file gốc luôn nguyên vẹn |

---

## 📋 Tính năng đầy đủ

| Icon | Tính năng | Chi tiết |
|:---:|:---|:---|
| ♾️ | Unlimited Copy | Không giới hạn dung lượng - copy bao nhiêu cũng được |
| ⚡ | Server-side Copy | Copy trực tiếp trên server, không qua máy bạn |
| 🚀 | TURBO MODE | Cache thông minh, giảm 50% API calls |
| 🔄 | Auto Resume | Tự động tiếp tục khi timeout hoặc lỗi |
| 💾 | Smart Checkpoint | Lưu tiến độ tự động + backup |
| 🔁 | Auto Retry | Tự động retry với exponential backoff |
| 📊 | Real-time Stats | Hiển thị số file, dung lượng, tốc độ, thời gian |
| 🎯 | Exact Match | Kiểm tra file trùng chính xác 100% |
| 🔍 | Smart Filter | Lọc theo tên file, đuôi file linh hoạt |
| 📄 | Export Docs | Xuất Google Docs/Sheets/Slides sang PDF |
| 🔗 | Shortcut Detection | Phát hiện và báo cáo shortcuts |
| 🔔 | Sound Alert | Âm thanh thông báo khi hoàn tất |
| 🧹 | Auto GC | Tự động dọn RAM, chạy ổn định |
| 📝 | Full Logging | Ghi log chi tiết mọi hoạt động |
| 🎨 | Auto Collapse | Code tự động thu gọn, giao diện gọn gàng |

---

## 🚀 Hướng dẫn sử dụng

### Bước 1: Mở Colab

Click nút bên dưới để mở notebook:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb)

### Bước 2: Nhập thông tin

Chạy **Cell 1** và nhập:
- 📁 **Folder đích**: Link folder Google Drive của bạn (nơi lưu file copy)
- 📂 **Folder nguồn**: Link folder cần copy (có thể là Shared Drive)

### Bước 3: Bắt đầu copy

Chạy **Cell 2** và đợi hoàn tất.

> 💡 **Timeout?** Đừng lo - chỉ cần chạy lại Cell 2, tool sẽ tự động tiếp tục từ chỗ dừng!

---

## 🎮 Các Cell trong Notebook

| Cell | Tên | Chức năng |
|:---:|:---|:---|
| 1️⃣ | Nhập thông tin | Nhập link folder và cài đặt bộ lọc |
| 2️⃣ | Run Copy | Thực hiện copy |
| 3️⃣ | Xóa checkpoint | Reset để copy lại từ đầu |
| 4️⃣ | Xem Log | Xem thống kê, file lỗi, shortcuts |

---

## ⚙️ Các tùy chọn

| Tùy chọn | Mô tả | Mặc định |
|:---|:---|:---:|
| 📁 Folder đích | Link folder của bạn | Bắt buộc |
| 📂 Folder nguồn | Link folder cần copy | Bắt buộc |
| 🚫 Bỏ qua chứa | Skip file có tên chứa text này | Trống |
| ✅ Chỉ lấy đuôi | Chỉ copy file có đuôi này | Trống |
| ❌ Bỏ qua đuôi | Skip file có đuôi này | Trống |
| ⏭️ Skip file đã có | Bỏ qua file trùng tên | Bật |
| 📄 Export Docs | Xuất Google Docs sang PDF | Tắt |
| 👁️ Dry-run | Chỉ xem preview, không copy | Tắt |

---

## 💡 Mẹo sử dụng

### Để copy nhanh nhất:
- 🌙 Chạy **ban đêm** - ít rate limit hơn
- 💪 Dùng **Colab Pro** + **High RAM** runtime
- 📶 Đảm bảo mạng ổn định
- 🔄 Timeout? Chạy lại Cell 2 ngay

### Theo dõi tiến độ:
- 📊 Xem real-time stats trên màn hình
- 📝 Log chi tiết tại `/content/gdrive_copy.log`
- 📋 Chạy **Cell 4** để xem thống kê đầy đủ

---

## ❓ Câu hỏi thường gặp

<details>
<summary><strong>Copy được bao nhiêu dung lượng?</strong></summary>

**Không giới hạn!** Tool sử dụng Google Drive API `files().copy()` - copy trực tiếp trên server Google. Bạn có thể copy 100GB, 1TB, thậm chí 10TB+ mà không gặp vấn đề.
</details>

<details>
<summary><strong>Copy được Shared Drive không?</strong></summary>

**Có!** Tool hỗ trợ đầy đủ Shared Drive. Chỉ cần bạn có quyền view folder nguồn là copy được.
</details>

<details>
<summary><strong>Colab Free dùng được không?</strong></summary>

**Có!** Colab Free hoạt động tốt, chỉ hay bị timeout (~90 phút). Chạy lại Cell 2 là tự động resume.
</details>

<details>
<summary><strong>Có mất dữ liệu gốc không?</strong></summary>

**Không!** Tool chỉ copy, không xóa hay sửa file gốc. Dữ liệu nguồn luôn an toàn 100%.
</details>

<details>
<summary><strong>Tốc độ copy bao nhiêu?</strong></summary>

Với TURBO MODE, tốc độ trung bình **50-150 MB/s** (tùy Google API). Ban đêm thường nhanh hơn.
</details>

<details>
<summary><strong>Sao không copy được Google Docs?</strong></summary>

Google Docs/Sheets/Slides là file đặc biệt, không có dung lượng thực. Mặc định tool bỏ qua. Bật **"Export Docs"** nếu cần xuất ra PDF.
</details>

<details>
<summary><strong>Bị rate limit thì sao?</strong></summary>

Tool tự động retry 5 lần với exponential backoff. Nếu vẫn lỗi, đợi vài phút rồi chạy lại Cell 2.
</details>

---

## ⚠️ Lưu ý quan trọng

| Loại file | Xử lý |
|:---|:---|
| 📄 Google Docs/Sheets/Slides | Mặc định bỏ qua. Bật "Export Docs" để xuất PDF |
| 🔗 Shortcuts | Bỏ qua, liệt kê trong Cell 4 |
| 📁 Folder trống | Vẫn tạo folder, không báo lỗi |

---

## 📝 Changelog

### v1.0
- ♾️ Copy không giới hạn dung lượng
- ⚡ Server-side copy siêu nhanh
- 🚀 **TURBO MODE** - Cache thông minh, giảm 50% API calls
- 🔄 Auto resume khi timeout
- 💾 Checkpoint + backup thông minh
- 🔁 Auto retry với exponential backoff
- 📊 Real-time stats
- 📄 Export Google Docs sang PDF
- 🔗 Shortcut detection
- 🔍 Smart filter
- 🔔 Sound alert
- 🧹 Auto GC
- 🎨 **Auto Collapse** - Code cells tự động thu gọn khi mở notebook

---

## 👨‍💻 Tác giả

**Nguyễn Ngọc Anh Tú**

| Liên kết | |
|:---|:---|
| 📢 Kênh thông báo | [Messenger Channel](https://www.messenger.com/channel/NguyenNgocAnhTu.VN) |
| 📘 Facebook | [NguyenNgocAnhTu.VN](https://www.facebook.com/NguyenNgocAnhTu.VN) |
| ✈️ Telegram | [NguyenNgocAnhTu](https://t.me/NguyenNgocAnhTu) |
| 🐙 GitHub | [kazeidk](https://github.com/kazeidk) |

---

## ⭐ Ủng hộ dự án

Nếu tool hữu ích với bạn:
- ⭐ **Star** repo này trên GitHub
- 🔄 **Share** cho bạn bè cần dùng
- 📢 **Follow** [kênh thông báo](https://www.messenger.com/channel/NguyenNgocAnhTu.VN) để nhận update mới

---

<p align="center">
  <strong>📄 MIT License</strong> - Tự do sử dụng và chỉnh sửa
</p>

<p align="center">
  Made with ❤️ by Nguyễn Ngọc Anh Tú
</p>
