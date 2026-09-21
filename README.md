<p align="center">
  <img src="https://img.shields.io/badge/phi%C3%AAn%20b%E1%BA%A3n-v0.20.8%20(Ch%C3%ADnh%20th%E1%BB%A9c)-6957ff?style=for-the-badge" alt="Phiên bản chính thức 0.20.8">
  <img src="https://img.shields.io/badge/tr%E1%BA%A1ng%20th%C3%A1i-Ho%E1%BA%A1t%20%C4%91%E1%BB%99ng%20%E1%BB%95n%20%C4%91%E1%BB%8Bnh-success?style=for-the-badge" alt="Trạng thái">
  <img src="https://img.shields.io/badge/Windows%2010%2F11-x64-0078d4?style=for-the-badge" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Linux-x64-333?style=for-the-badge" alt="Linux x64">
  <img src="https://img.shields.io/badge/Gi%E1%BA%A5y%20ph%C3%A9p-MIT-orange?style=for-the-badge" alt="Giấy phép MIT">
</p>

<h1 align="center">Vidora v0.20.8</h1>

<p align="center">
  <strong>Giải pháp Desktop toàn diện cho Xử lý Phụ đề, Lồng tiếng AI, Trích xuất Hardsub & Tải Video Đa Nền Tảng</strong>
</p>

<p align="center">
  <em>Hoạt động Cục bộ (Local-First) &bull; Bảo mật Tuyệt đối &bull; Không Gửi Dữ liệu Ra Ngoài &bull; Sẵn sàng Offline</em>
</p>

---

## 🌟 Giới thiệu

**Vidora** là phần mềm desktop mạnh mẽ giúp người sáng tạo nội dung, biên dịch viên và người dùng cá nhân chuyển ngữ, làm phụ đề, lồng tiếng và xử lý video trọn gói ngay trên máy tính của mình mà không phải chuyển qua lại giữa nhiều công cụ phức tạp.

Từ phiên bản **v0.20.8**, Vidora chính thức tích hợp sẵn toàn bộ môi trường xử lý cục bộ: **PaddleOCR** nhận diện 9 ngôn ngữ, **Faster-Whisper** nhận dạng giọng nói chuẩn từng từ, **Smart Fit Voice Dubbing** tự khớp trường độ thoại, công cụ biên tập **Subtitle Workshop** với biểu đồ sóng âm (waveform), cùng runtime **Deno** độc lập tối ưu hóa cho công cụ trích xuất video yt-dlp hiện đại nhất.

---

## 📥 Tải về Phiên bản Chính thức (v0.20.8)

Mọi tệp cài đặt chính thức đều được ký số bảo mật và phát hành trực tiếp tại [GitHub Releases v0.20.8](https://github.com/vidora-app/Vidora/releases/tag/v0.20.8).

| Hệ điều hành | Tập tin cài đặt | Dung lượng | Hướng dẫn cài đặt nhanh |
| :--- | :--- | :---: | :--- |
| **Windows 10 / 11 (64-bit)** | [**Vidora-Windows-Setup.exe**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Windows-Setup.exe) | ~1.70 GB | Mở file, nhấn **Install**. Cài đặt riêng cho tài khoản người dùng (`%LOCALAPPDATA%`), **không cần quyền Admin / UAC**. |
| **Windows (Bản cập nhật)** | [**Vidora-Windows-Update.exe**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Windows-Update.exe) | ~33 MB | Gói cập nhật siêu nhẹ tự động khi máy đã cài sẵn bản Vidora trước đó. |
| **Linux (AppImage)** | [**Vidora-Linux.AppImage**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Linux.AppImage) | ~1.47 GB | Chạy ngay không cần cài đặt:<br>`chmod +x Vidora-Linux.AppImage && ./Vidora-Linux.AppImage` |
| **Linux (Debian / Ubuntu)** | [**Vidora-Linux.deb**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Linux.deb) | ~1.34 GB | Cài đặt bằng lệnh:<br>`sudo apt install ./Vidora-Linux.deb` |
| **Cẩm nang Hướng dẫn** | [**Huong_Dan_Su_Dung_Vidora_v0.20.8.docx**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Huong_Dan_Su_Dung_Vidora_v0.20.8.docx) | ~22 KB | File Word (.docx) cẩm nang hướng dẫn sử dụng chi tiết A-Z, phím tắt & khắc phục sự cố. |

> 💡 **Lưu ý về dung lượng**: Bộ cài đặt chứa trọn vẹn toàn bộ runtime xử lý ngoại tuyến (Python runtime, PaddleOCR, Faster-Whisper, FFmpeg, Deno, yt-dlp). Tải một lần, sử dụng vĩnh viễn không lo thiếu thư viện hay phải cài đặt thủ công bên ngoài.

---

## 🧩 Tiện ích Trình duyệt (Browser Extensions)

Gửi trực tiếp liên kết video, danh sách phát hoặc bài viết từ trình duyệt vào hàng đợi tải của Vidora chỉ với 1 cú click:

- 🌐 **Chrome / Edge / Cốc Cốc / Brave / Chromium**: [Tải tiện ích Chromium (Vidora-Extension-Chromium.zip)](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Extension-Chromium.zip)
  *(Vào `chrome://extensions`, bật Developer mode, giải nén và chọn Load unpacked)*.
- 🦊 **Mozilla Firefox**: [Cài tiện ích Firefox đã ký số AMO (Vidora-Extension-Firefox-signed.xpi)](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Extension-Firefox-signed.xpi)
  *(Kéo thả trực tiếp vào trình duyệt Firefox để kích hoạt ngay)*.

---

## 🚀 Khởi đầu Nhanh trong 3 Bước

1. **Cài đặt & Khởi động**: Tải file cài đặt phù hợp ở bảng trên, hoàn tất cài đặt và mở ứng dụng Vidora.
2. **Đăng nhập & Tài khoản**: Mở **Cài đặt** (biểu tượng bánh răng) &rarr; **Tài khoản** để tạo tài khoản hoặc đăng nhập tài khoản Vidora của bạn.
3. **Kích hoạt Bản quyền**: Dán mã bản quyền (License Key) và nhấn **Kích hoạt**. Hệ thống hỗ trợ làm việc ngoại tuyến (Offline Leases) liên tục ngay cả khi ngắt mạng.
   *(Chi tiết tại [Tài liệu Quản lý Bản quyền](docs/license.md))*.

---

## 🎯 Các Trụ cột Tính năng Nổi bật

### 1. Trích xuất Phụ đề Tự động (Offline Subtitle Extraction)
- **Trích xuất Hardsub OCR**: Đọc thẳng phụ đề đã bị nung cứng vào khung hình video thành file phụ đề có thể chỉnh sửa. Hỗ trợ 9 hệ ngôn ngữ chính (Tiếng Việt, Tiếng Anh, Trung Giản/Phồn thể, Nhật, Hàn, Nga, Ả Rập, Thái, Hindi...). Tự động theo vết phụ đề chuyển động, lọc hình mờ/logo góc video. Tận dụng tối đa sức mạnh GPU NVIDIA qua CUDA hoặc tự chuyển mượt mà sang CPU.
- **Tạo phụ đề từ giọng nói (Speech-to-Text)**: Nhận dạng lời thoại ngoại tuyến bằng Faster-Whisper, tạo mốc thời gian (timestamps) chính xác từng từ, tự động nhận diện ngôn ngữ nguồn và hỗ trợ khôi phục tiến trình khi bị gián đoạn.
- **Quy trình Kết hợp (Hybrid)**: Phân tích đồng thời cả dải hình ảnh và âm thanh để đạt độ chính xác phụ đề cao nhất.

### 2. Dịch thuật Đa ngôn ngữ & Lồng tiếng AI Thông minh
- **Dịch phụ đề linh hoạt**:
  - *Dịch Offline*: Sử dụng mô hình Argos tích hợp sẵn, dịch hoàn toàn trên máy tính cá nhân, bảo mật dữ liệu tuyệt đối 100%.
  - *Dịch AI Cloud*: Tích hợp linh hoạt các nhà cung cấp OpenAI, Claude, DeepSeek hoặc Vidora Cloud để xử lý câu văn mượt mà, tự nhiên theo ngữ cảnh.
- **Lồng tiếng AI & Smart Fit**: Tự động chuyển phụ đề đã dịch thành giọng đọc truyền cảm tự nhiên (kho hàng trăm giọng đọc Việt, Anh, v.v.). Tính năng **Smart Fit** độc quyền tự động tính toán và điều chỉnh nhịp đọc khớp hoàn hảo với trường độ lời thoại video gốc.
- **Xóa phụ đề gốc (Delogo/Inpainting)**: Xóa sạch dải phụ đề cứng cũ trên video và tái tạo lại khung hình trước khi gắn phụ đề mới.

### 3. Xưởng Biên tập Phụ đề Chuyên nghiệp (Subtitle Workshop)
- Trực quan hóa tiến trình bằng biểu đồ sóng âm (Audio Waveform) và thanh thời gian đa lớp.
- Đồng bộ mốc thời gian thời gian thực, tự động gộp/tách câu thông minh theo nhịp ngắt nghỉ.
- Bộ kiểm tra chất lượng (QC) tự động cảnh báo chồng lấn thời gian (overlap), tốc độ đọc quá nhanh (CPS/CPL).
- Hỗ trợ đầy đủ các định dạng: **SRT**, **VTT**, **ASS** (cho phép tạo kiểu font chữ, màu sắc, vị trí hiển thị bắt mắt).

### 4. Tải Video Tốc độ cao Đa Nền tảng
- Tải video, âm thanh từ hơn **1.800 trang web**: YouTube, TikTok, Facebook, Instagram, Bilibili, Douyin, X (Twitter), Youku...
- Hỗ trợ độ phân giải tối đa lên tới **8K**, 60 FPS, chuẩn màu HDR, bộ codec AV1, VP9, H.264, H.265.
- Tải trọn bộ danh sách phát (Playlist), toàn bộ kênh hoặc tải trước đoạn thời gian mong muốn.
- Tự động lọc quảng cáo với SponsorBlock, lưu kèm ảnh bìa (thumbnail) chất lượng cao và siêu dữ liệu (metadata).
- **Theo dõi Kênh Tự động**: Lên lịch tự động kiểm tra kênh yêu thích và tự tải nội dung mới về máy.

### 5. Xử lý Video bằng Lệnh Tự nhiên & Quản lý Thư viện
- Cắt, nén dung lượng, đổi kích thước, tách âm thanh, tạo ảnh GIF, chèn watermark bằng câu lệnh mô tả thông thường.
- Thư viện quản lý tập trung dựa trên SQLite bền bỉ: gắn tag, gom bộ sưu tập, tìm kiếm nhanh và tự phát hiện video trùng lặp.
- Xuất dữ liệu đa định dạng: Excel, CSV, Word, JSON, Markdown, SQLite.

---

## 💻 Yêu cầu Cấu hình Hệ thống

| Tiêu chí | Cấu hình Tối thiểu | Cấu hình Khuyến nghị |
| :--- | :--- | :--- |
| **Hệ điều hành** | Windows 10/11 (64-bit) / Linux 64-bit | Windows 11 (64-bit) / Ubuntu 22.04 LTS trở lên |
| **Bộ vi xử lý (CPU)** | Intel Core i3 / AMD Ryzen 3 trở lên | Intel Core i5/i7/i9 / AMD Ryzen 5/7/9 (6 nhân trở lên) |
| **Bộ nhớ RAM** | 8 GB RAM | 16 GB RAM hoặc cao hơn |
| **Dung lượng ổ cứng** | 10 GB trống (SSD) | 25 GB trống (NVMe SSD để xử lý video nhanh nhất) |
| **Card đồ họa (GPU)** | Card tích hợp (chạy CPU mode) | Card đồ họa rời **NVIDIA GTX 1060 / RTX Series** (có hỗ trợ CUDA để tăng tốc OCR và Whisper lên gấp 5–10 lần) |
| **Mạng Internet** | Cần kết nối khi kích hoạt và tải video | Băng thông ổn định |

---

## 🛡️ Xác minh Tính toàn vẹn Tập tin (SHA-256 Checksums)

Đối chiếu mã băm sau khi tải về để đảm bảo tập tin của bạn nguyên vẹn và không bị can thiệp:

```text
Vidora-Windows-Setup.exe:
1d8fa457cfd52b289984de166ff47910e7d1569c4b45646b7f18f19bb229d297

Vidora-Windows-Update.exe:
872c13f40e010d7c52a01cbc2e9d9edc14f4494f57b76b2a0a49eb220da19faa

Vidora-Linux.AppImage:
065f8c9c19046e9b644fe8b7819cb9cdc4d48c14f66bf52f61e5be9249c4dc87

Vidora-Linux.deb:
98201a13256215f21de5a635b3c595f52c3217eb26b0bf92ec0e1f46a7944634

Vidora-Extension-Chromium.zip:
2165fa61b39f650fe6c759c166505147f2bfd1c8461d52e064b3ee26a02d19b9

Vidora-Extension-Firefox-signed.xpi:
799ec5cbb5e27275ce0eefeebe232af6c866bb73c7c8777378d2ba8e1559fdfd
```

**Cách kiểm tra trên PowerShell (Windows):**
```powershell
(Get-FileHash .\Vidora-Windows-Setup.exe -Algorithm SHA256).Hash.ToLower()
```

**Cách kiểm tra trên Terminal (Linux):**
```bash
sha256sum Vidora-Linux.AppImage
```

---

## ❓ Xử lý Cảnh báo Windows Defender SmartScreen

Khi khởi chạy bộ cài mới trên Windows 10/11, màn hình xanh có thể xuất hiện với nội dung:
> *"Windows protected your PC - Microsoft Defender SmartScreen prevented an unrecognized app from starting."*

👉 **Cách mở bình thường:**
1. Nhấn vào dòng chữ **"More info"** (Thông tin khác).
2. Nhấn nút **"Run anyway"** (Vẫn chạy).
*(Cảnh báo xuất hiện do bộ cài phần mềm mới xuất xưởng chưa tích lũy chứng chỉ danh tiếng từ máy chủ Microsoft; tập tin hoàn toàn sạch và an toàn)*.

---

## 📚 Tài liệu Hướng dẫn Chuyên sâu

- 📘 **[Tải File Word (.docx) Cẩm nang Hướng dẫn Chi tiết Toàn diện](docs/Huong_Dan_Su_Dung_Vidora_v0.20.8.docx)**: Toàn bộ cẩm nang hướng dẫn đầy đủ từ A-Z được biên soạn sẵn định dạng Word chuẩn, tiện tra cứu ngoại tuyến và in ấn.
- [Mục lục Tài liệu Trực tuyến](docs/README.md)
- [Hướng dẫn Cài đặt & Khởi chạy Lần đầu](docs/installation.md)
- [Quản lý Bản quyền, Tài khoản & Thiết bị](docs/license.md)
- [Trích xuất Phụ đề Cháy (Hardsub OCR)](docs/hardsub-ocr.md)
- [Tạo Phụ đề từ Giọng nói (Speech-to-Text)](docs/speech-subtitles.md)
- [Dịch thuật Phụ đề & Lồng tiếng AI](docs/translate-dub.md)
- [Tải Video Nâng cao](docs/downloading.md)
- [Tiện ích Trình duyệt Vidora Extension](docs/browser-extension.md)
- [Xử lý Sự cố Thường gặp (Troubleshooting)](docs/troubleshooting.md)

---

## 🤝 Hỗ trợ & Liên hệ

- **Báo cáo lỗi & Đóng góp ý kiến**: Mở thảo luận hoặc gửi phản ánh tại [GitHub Issues](https://github.com/vidora-app/Vidora/issues).
- **Cộng đồng thảo luận**: [GitHub Discussions](https://github.com/vidora-app/Vidora/discussions).
- **Trang chủ Dịch vụ**: [https://vdora.site](https://vdora.site)

---

## 📜 Giấy phép (License)

Vidora được phát hành theo giấy phép nguồn mở [MIT License](LICENSE). Vui lòng tuân thủ bản quyền nội dung đa phương tiện theo quy định pháp luật sở tại khi sử dụng tính năng tải video.
