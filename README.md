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

**Vidora** là phần mềm desktop giúp bạn chuyển ngữ video nước ngoài, làm phụ đề, đọc lồng tiếng và tải video trọn gói ngay trên máy tính của mình. Mọi tác vụ xử lý nặng đều chạy trực tiếp trên phần cứng máy bạn, bảo mật dữ liệu tuyệt đối và không phải gửi video hay thông tin ra bất kỳ máy chủ bên ngoài nào.

Từ phiên bản **v0.20.8**, Vidora chính thức tích hợp sẵn toàn bộ môi trường xử lý:
- **PaddleOCR**: Trích xuất phụ đề nung cứng (Hardsub) hỗ trợ 9 hệ ngôn ngữ.
- **Faster-Whisper**: Tự động nhận dạng giọng nói thành văn bản chuẩn xác từng từ.
- **Smart Fit Voice Dubbing**: Tự động điều chỉnh nhịp đọc của giọng AI khớp khít với thời lượng lời thoại gốc.
- **Subtitle Workshop**: Xưởng biên tập phụ đề chuyên nghiệp với biểu đồ sóng âm (Waveform).
- **Tải Video Tốc độ cao**: Hỗ trợ hơn 1.800 trang web video phổ biến nhất hiện nay.

---

## 📥 Tải về Cài đặt (v0.20.8)

| Nền tảng | Tập tin tải về | Dung lượng | Hướng dẫn nhanh |
| :--- | :--- | :---: | :--- |
| **Windows 10 / 11 (64-bit)** | [**Vidora-Windows-Setup.exe**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Windows-Setup.exe) | ~1.70 GB | Tải về mở file và bấm **Install**. Cài đặt riêng cho tài khoản người dùng, **không cần quyền Admin / UAC**. |
| **Linux (AppImage)** | [**Vidora-Linux.AppImage**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Linux.AppImage) | ~1.47 GB | Chạy trực tiếp không cần cài đặt:<br>`chmod +x Vidora-Linux.AppImage && ./Vidora-Linux.AppImage` |
| **Linux (Debian / Ubuntu)** | [**Vidora-Linux.deb**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Linux.deb) | ~1.34 GB | Cài đặt bằng lệnh:<br>`sudo apt install ./Vidora-Linux.deb` |
| **Cẩm nang Hướng dẫn** | [**Huong_Dan_Su_Dung_Vidora_v0.20.8.docx**](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Huong_Dan_Su_Dung_Vidora_v0.20.8.docx) | ~22 KB | File Word (.docx) hướng dẫn chi tiết toàn bộ tính năng, phím tắt & cách sử dụng. |

> 💡 **Bộ cài đầy đủ (All-in-One)**: Ứng dụng tích hợp sẵn toàn bộ công cụ cần thiết (Python runtime, PaddleOCR, Whisper, FFmpeg, Deno, yt-dlp). Bạn chỉ cần tải một lần duy nhất là có thể dùng ngoại tuyến, không cần cài đặt thêm phần mềm phụ trợ.

---

## 🧩 Tiện ích Trình duyệt (Browser Extensions)

Gửi liên kết video trực tiếp từ trình duyệt vào hàng đợi tải của Vidora:

- 🌐 **Chrome / Edge / Cốc Cốc / Brave**: [Tải tiện ích Chromium (Vidora-Extension-Chromium.zip)](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Extension-Chromium.zip)
  *(Mở `chrome://extensions`, bật Developer mode, giải nén và chọn Load unpacked)*.
- 🦊 **Mozilla Firefox**: [Cài tiện ích Firefox (Vidora-Extension-Firefox-signed.xpi)](https://github.com/vidora-app/Vidora/releases/download/v0.20.8/Vidora-Extension-Firefox-signed.xpi)
  *(Đã được Mozilla AMO ký số chính thức, kéo thả vào Firefox để kích hoạt)*.

---

## 🚀 Bắt đầu Sử dụng trong 3 Bước

1. **Cài đặt & Khởi động**: Tải file cài đặt phù hợp ở bảng trên và mở ứng dụng Vidora.
2. **Đăng nhập Tài khoản**: Vào **Cài đặt** (biểu tượng bánh răng) &rarr; **Tài khoản** để đăng nhập hoặc tạo tài khoản mới.
3. **Kích hoạt Bản quyền**: Dán mã bản quyền (License Key) và nhấn **Kích hoạt**. Ứng dụng hỗ trợ làm việc ngoại tuyến liên tục ngay cả khi không có mạng.

---

## 🎯 Các Tính năng Nổi bật

### 1. Trích xuất Phụ đề Tự động
- **Trích xuất phụ đề cháy (Hardsub OCR)**: Đọc thẳng chữ phụ đề đã bị nung cứng vào khung hình video thành file phụ đề có thể chỉnh sửa. Hỗ trợ 9 hệ ngôn ngữ chính (Tiếng Việt, Tiếng Anh, Trung Giản/Phồn thể, Nhật, Hàn, Nga, Ả Rập, Thái, Hindi...). Tự động bám theo chữ chuyển động, lọc logo và hình mờ góc màn hình. Tận dụng card đồ họa rời NVIDIA (CUDA) hoặc tự động chạy trên CPU.
- **Tạo phụ đề từ giọng nói (Speech-to-Text)**: Nhận dạng lời thoại tự động bằng Faster-Whisper, tạo mốc thời gian (timestamps) chính xác từng từ, tự động nhận biết ngôn ngữ đối thoại.
- **Chế độ tự động / kết hợp (Hybrid)**: Quét dải hình ảnh và âm thanh để đạt độ chuẩn xác phụ đề tối đa.

### 2. Dịch thuật Đa ngôn ngữ & Lồng tiếng AI
- **Dịch phụ đề**: Hỗ trợ dịch offline ngoại tuyến không cần mạng bằng mô hình Argos, hoặc dịch thông qua các mô hình AI trực tuyến với văn phong mượt mà theo ngữ cảnh.
- **Lồng tiếng AI & Smart Fit**: Chuyển phụ đề đã dịch thành giọng đọc truyền cảm tự nhiên (kho hàng trăm giọng đọc Việt, Anh...). Tính năng độc quyền **Smart Fit** tự động tính toán và điều chỉnh nhịp đọc của giọng AI khớp khít với trường độ câu thoại của nhân vật trong video gốc.
- **Xóa phụ đề gốc (Inpainting)**: Xóa vệt phụ đề cứng cũ trên video và tái tạo lại phông nền trước khi gắn phụ đề mới.

### 3. Xưởng Biên tập Phụ đề Chuyên nghiệp (Subtitle Workshop)
- Trực quan hóa âm thanh với biểu đồ sóng âm (Waveform) và thanh thời gian đa tầng.
- Kéo thả mốc thời gian trực tiếp bằng chuột, đồng bộ thời gian thực với video.
- Tự động gộp / tách câu thông minh theo nhịp ngắt nghỉ tự nhiên.
- Bộ kiểm tra chất lượng (QC) tự động cảnh báo chồng lấn thời gian (overlap) hoặc tốc độ đọc quá nhanh.
- Xuất đầy đủ các định dạng: **SRT**, **VTT**, **ASS** (tùy biến kiểu chữ, màu sắc, viền và hiệu ứng hiển thị).

### 4. Tải Video Tốc độ cao Đa Nền tảng
- Tải video và âm thanh từ hơn **1.800 trang web**: YouTube, TikTok, Facebook, Instagram, Bilibili, Douyin, X (Twitter), Youku...
- Hỗ trợ chất lượng tối đa lên đến **8K**, 60 FPS, chuẩn màu HDR.
- Tải hàng loạt danh sách liên kết, tải trọn bộ danh sách phát (Playlist) hoặc toàn bộ kênh.
- Cắt sẵn khoảng thời gian cần lấy trước khi tải để tiết kiệm dung lượng và thời gian.
- Tự động bỏ qua phân đoạn quảng cáo tài trợ với SponsorBlock.
- **Theo dõi Kênh tự động**: Lên lịch kiểm tra kênh định kỳ và tự tải video mới về máy.

### 5. Xử lý Video bằng Lệnh Tự nhiên & Quản lý Thư viện
- Cắt, ghép, nén dung lượng, đổi kích thước, tách âm thanh MP3, tạo ảnh GIF bằng câu lệnh tiếng Việt thông thường.
- Thư viện quản lý cá nhân bền bỉ trên SQLite: Gắn tag, tạo bộ sưu tập, tìm kiếm nhanh và tự động phát hiện video trùng lặp.
- Xuất báo cáo và dữ liệu: Excel, CSV, Word, JSON, Markdown.

---

## 💻 Yêu cầu Cấu hình Hệ thống

| Tiêu chí | Cấu hình Tối thiểu | Cấu hình Khuyến nghị |
| :--- | :--- | :--- |
| **Hệ điều hành** | Windows 10/11 (64-bit) / Linux 64-bit | Windows 11 (64-bit) / Ubuntu 22.04 LTS trở lên |
| **Bộ vi xử lý (CPU)** | Intel Core i3 / AMD Ryzen 3 trở lên | Intel Core i5/i7/i9 hoặc AMD Ryzen 5/7 trở lên |
| **Bộ nhớ RAM** | 8 GB RAM | 16 GB RAM trở lên |
| **Ổ đĩa trống** | 10 GB trống (SSD) | 25 GB trống (Ổ cứng SSD NVMe) |
| **Card đồ họa (GPU)** | Card tích hợp (chạy CPU mode) | Card đồ họa rời **NVIDIA (hỗ trợ CUDA)** để tăng tốc OCR và Whisper nhanh hơn |

---

## ❓ Xử lý Cảnh báo Windows Defender SmartScreen

Khi mở file cài đặt lần đầu trên Windows, nếu xuất hiện màn hình xanh cảnh báo:
> *"Windows protected your PC - Microsoft Defender SmartScreen prevented an unrecognized app from starting."*

👉 **Cách mở ứng dụng:**
1. Nhấn vào dòng chữ **"More info"** (Thông tin khác).
2. Nhấn nút **"Run anyway"** (Vẫn chạy) để bắt đầu cài đặt bình thường.

---

## 📚 Tài liệu Hướng dẫn

- 📘 **[Tải File Word (.docx) Cẩm nang Hướng dẫn Chi tiết A-Z](docs/Huong_Dan_Su_Dung_Vidora_v0.20.8.docx)**: Tài liệu Word đầy đủ, tiện in ấn và tra cứu ngoại tuyến.
- [Mục lục Tài liệu Hướng dẫn](docs/README.md)
- [Cài đặt và Chạy lần đầu](docs/installation.md)
- [Quản lý Bản quyền & Thiết bị](docs/license.md)
- [Trích xuất Phụ đề Cháy (Hardsub OCR)](docs/hardsub-ocr.md)
- [Tạo Phụ đề từ Giọng nói (Speech-to-Text)](docs/speech-subtitles.md)
- [Dịch thuật & Lồng tiếng AI](docs/translate-dub.md)
- [Tải Video Nâng cao](docs/downloading.md)
- [Tiện ích Trình duyệt Vidora Extension](docs/browser-extension.md)
- [Xử lý Sự cố Thường gặp](docs/troubleshooting.md)

---

## 🤝 Hỗ trợ & Liên hệ

- **Báo cáo lỗi & Góp ý**: [GitHub Issues](https://github.com/vidora-app/Vidora/issues)
- **Cộng đồng thảo luận**: [GitHub Discussions](https://github.com/vidora-app/Vidora/discussions)

---

## 📜 Giấy phép (License)

Vidora được phát hành theo giấy phép nguồn mở [MIT License](LICENSE).
