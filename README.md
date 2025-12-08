<p align="center">
  <h1 align="center">🚀 GDrive Turbo Copy</h1>
  <p align="center">
    <b>⚡ Copy folder Google Drive → Google Drive</b><br>
    <i>Nhanh • Ổn định • Hỗ trợ 2000GB+</i>
  </p>
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/kazeidk/GDrive_Turbo_Copy/blob/main/GDrive_Turbo_Copy.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
  </a>
</p>

---

## ✨ Tính năng

| | Tính năng | Mô tả |
|:---:|---|---|
| ⚡ | **Turbo Copy** | Copy trực tiếp, không scan trước |
| 📊 | **Real-time Stats** | Hiển thị file, dung lượng, tốc độ |
| 🎯 | **Exact Match** | Kiểm tra file chính xác 100% |
| 🔄 | **Auto Resume** | Tự tiếp tục khi timeout |
| 🔁 | **Smart Retry** | Retry 5 lần với exponential backoff |
| 💾 | **Checkpoint** | Lưu tiến độ + backup tự động |
| 📝 | **Full Log** | Ghi log chi tiết |
| 🔍 | **Smart Filter** | Lọc theo đuôi file |
| 📄 | **Export Docs** | Xuất Google Docs → PDF |
| 🔗 | **Shortcut Detection** | Phát hiện shortcuts |
| 🔔 | **Sound Alert** | Âm thanh khi hoàn tất |
| 🧹 | **Auto GC** | Tự dọn RAM |
| ♾️ | **Unlimited** | Không giới hạn dung lượng |

---

## ⚠️ Lưu ý

| Loại | Xử lý |
|---|---|
| 📄 **Google Docs/Sheets/Slides** | Mặc định bỏ qua. Bật "Export → PDF" nếu cần |
| 🔗 **Shortcuts** | Bỏ qua, liệt kê trong Cell 4 |

---

## 📖 Hướng dẫn

### 🚀 Quick Start
```
1️⃣ Click "Open in Colab" ở trên
2️⃣ Chạy Cell 1 → Nhập link
3️⃣ Chạy Cell 2 → Copy
4️⃣ Timeout? → Chạy lại Cell 2
```

### 📋 Các Cell

| Cell | Chức năng |
|:---:|---|
| 1️⃣ | 📝 Nhập thông tin |
| 2️⃣ | 🚀 Chạy copy |
| 3️⃣ | 🗑️ Xóa checkpoint |
| 4️⃣ | 📋 Xem log & lỗi |

---


## ⚙️ Tùy chọn

| Tùy chọn | Mô tả | Mặc định |
|---|---|:---:|
| 📁 **Folder đích** | Link folder của bạn | - |
| 📂 **Folder nguồn** | Link folder cần copy | - |
| 🚫 **Bỏ qua chứa** | Skip file có tên chứa text | - |
| ✅ **Chỉ lấy đuôi** | Chỉ copy file có đuôi này | - |
| ❌ **Bỏ qua đuôi** | Skip file có đuôi này | - |
| ⏭️ **Skip file đã có** | Bỏ qua file trùng tên | ✅ |
| 📄 **Export Docs** | Xuất Google Docs → PDF | ❌ |
| 👁️ **Dry-run** | Chỉ xem, không copy | ❌ |

---

## 💡 Pro Tips

| Tip | Mô tả |
|:---:|---|
| 🌙 | Chạy **ban đêm** = ít rate limit |
| 💪 | Dùng **Colab Pro** + **High RAM** |
| 🔄 | **Timeout?** Chạy lại Cell 2 |
| 📋 | Log tại `/content/gdrive_copy.log` |

---

## ❓ FAQ

<details>
<summary><b>🤔 Copy được Shared Drive không?</b></summary>
Có, chỉ cần có quyền view.
</details>

<details>
<summary><b>🤔 Colab Free dùng được không?</b></summary>
Có, nhưng hay timeout (~90 phút). Chạy lại sẽ tự resume.
</details>

<details>
<summary><b>🤔 Có mất dữ liệu không?</b></summary>
Không, tool chỉ copy. File gốc nguyên vẹn.
</details>

<details>
<summary><b>🤔 Tốc độ bao nhiêu?</b></summary>
Tùy Google API, trung bình 20-100 MB/s.
</details>

<details>
<summary><b>🤔 Sao không copy Google Docs?</b></summary>
Mặc định bỏ qua. Bật "Export → PDF" nếu cần.
</details>

---

## 📝 Changelog

### v1.0 🎉
- ⚡ Copy trực tiếp không scan
- 📊 Real-time stats
- 📄 Export Google Docs → PDF
- 🔗 Shortcut detection
- 💾 Checkpoint + backup
- 🔁 Auto-retry 5 lần
- 🎯 Exact match
- 🧹 Auto GC
- 🔔 Sound alert

---

## 👨‍💻 Tác giả

<table>
  <tr>
    <td align="center">
      <b>Nguyễn Ngọc Anh Tú</b><br><br>
      <a href="https://www.messenger.com/channel/NguyenNgocAnhTu.VN">📢 Kênh thông báo</a><br>
      <a href="https://www.facebook.com/NguyenNgocAnhTu.VN">📘 Facebook</a> •
      <a href="https://t.me/NguyenNgocAnhTu">✈️ Telegram</a> •
      <a href="https://github.com/kazeidk">🐙 GitHub</a>
    </td>
  </tr>
</table>

> 📢 **Theo dõi [Kênh thông báo](https://www.messenger.com/channel/NguyenNgocAnhTu.VN)** để nhận cập nhật mới nhất!

---

<p align="center">
  <b>📄 MIT License</b> - Tự do sử dụng và chỉnh sửa
</p>
