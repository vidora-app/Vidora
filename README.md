<p align="center">
  <img src="https://img.shields.io/github/v/release/vidora-app/Vidora?label=phi%C3%AAn%20b%E1%BA%A3n&color=6957ff" alt="Phiên bản mới nhất">
  <img src="https://img.shields.io/github/downloads/vidora-app/Vidora/total?label=l%C6%B0%E1%BB%A3t%20t%E1%BA%A3i&color=6957ff" alt="Lượt tải">
  <img src="https://img.shields.io/badge/Windows%2010%2F11-x64-0078d4" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Linux-x64-333" alt="Linux x64">
</p>

# Vidora

**Dịch video, tạo phụ đề, lồng tiếng và tải video — trong một ứng dụng desktop.**

Vidora biến video nước ngoài thành nội dung tiếng Việt (hoặc ngược lại) mà không
cần chuyển qua lại giữa năm công cụ: trích phụ đề cháy trong hình, nhận dạng
giọng nói, dịch, đọc lồng tiếng, xoá phụ đề cũ và xuất video hoàn chỉnh. Mọi
tác vụ nặng chạy ngay trên máy bạn — file của bạn không phải gửi đi đâu.

---

## Tải về

| Nền tảng | Tải | Cài đặt |
| --- | --- | --- |
| **Windows 10 / 11 (64-bit)** | [Vidora-Windows-Setup.exe](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Windows-Setup.exe) | Chạy file, bấm *Install*. Cài cho tài khoản Windows hiện tại, **không cần quyền quản trị**. |
| **Linux (64-bit) — AppImage** | [Vidora-Linux.AppImage](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.AppImage) | `chmod +x Vidora-Linux.AppImage && ./Vidora-Linux.AppImage` |
| **Linux — Debian / Ubuntu** | [Vidora-Linux.deb](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.deb) | `sudo apt install ./Vidora-Linux.deb` |

macOS chưa có trong bản phát hành hiện tại.

Bộ cài nặng khoảng **1,7–2 GB** vì mang sẵn toàn bộ runtime xử lý cục bộ (OCR,
nhận dạng giọng nói, FFmpeg, yt-dlp). Tải một lần, dùng offline; ứng dụng không
tải rời rạc thêm gì giữa lúc bạn đang làm việc (trừ model Whisper khi bạn bật
tính năng tạo phụ đề từ giọng nói).

Tất cả file của mọi phiên bản: [trang Releases](https://github.com/vidora-app/Vidora/releases).

## Bắt đầu trong 3 bước

1. **Cài** Vidora bằng file ở bảng trên và mở ứng dụng.
2. **Đăng nhập** hoặc tạo tài khoản ngay trong app (*Cài đặt → Tài khoản*).
3. **Dán mã bản quyền** và bấm *Kích hoạt*. Xong — chi tiết về tài khoản, đổi máy
   và gia hạn ở [Tài khoản và bản quyền](docs/license.md).

## Vidora làm được gì

### Phụ đề

- **Trích phụ đề cháy trong hình (OCR)** — đọc thẳng phụ đề đã nung vào khung
  hình thành file phụ đề sửa được. Nhận diện 9 hệ chữ (Việt, Anh, Trung giản/
  phồn thể, Nhật, Hàn, Nga, Ả Rập, Thái, Hindi…), bám theo phụ đề di chuyển,
  tự phân biệt phụ đề với watermark, chạy được video nhiều giờ. Có GPU thì dùng
  CUDA, không có thì tự chuyển sang CPU. → [Hướng dẫn](docs/hardsub-ocr.md)
- **Tạo phụ đề từ giọng nói** — nhận dạng cục bộ, mốc thời gian từng từ, tự dò
  ngôn ngữ, tiếp tục được nếu gián đoạn. → [Hướng dẫn](docs/speech-subtitles.md)
- **Subtitle Workshop** — sửa nội dung và thời gian từng câu, tìm/thay thế,
  tách/gộp câu, kiểm tra tốc độ đọc và chồng thời gian, đồng bộ theo waveform.
  Xuất SRT, VTT, ASS; chuyển đổi hàng loạt.

### Dịch và lồng tiếng

- **Dịch phụ đề** — dịch offline không cần mạng, hoặc dùng AI bạn tự cấu hình.
  Kết quả hiện dần theo từng đoạn.
- **Lồng tiếng AI** — đọc phụ đề đã dịch thành giọng nói tự nhiên, *Smart Fit*
  tự căn thời lượng cho khớp với lời gốc thay vì bạn phải kéo từng câu.
- **Xoá phụ đề cũ, giữ nguyên khung hình** — xoá phụ đề nung trong video và
  dựng lại vùng bị che trước khi ghép phụ đề mới. → [Dịch và lồng tiếng](docs/translate-dub.md)

### Tải video

- **YouTube** — một hoặc nhiều URL, tìm theo từ khoá, playlist, chọn chất lượng
  tới 8K / codec / FPS, chỉ lấy âm thanh, cắt sẵn một khoảng thời gian, tải
  livestream từ đầu, hẹn giờ, kèm phụ đề / thumbnail / SponsorBlock.
- **TikTok, Douyin, Bilibili, Instagram, Facebook, X, Youku** và hơn 1.800
  trang khác. Gallery ảnh, feed creator, chương truyện tranh.
- **Theo dõi kênh** — bật tự động tải, đặt chu kỳ kiểm tra và bộ lọc; nội dung
  mới tự về hàng đợi. → [Hướng dẫn](docs/downloading.md)

### Xử lý và tổ chức

- **Xử lý video bằng lời** — mô tả việc cần làm (cắt, nén, đổi kích thước, tách
  âm thanh, tạo GIF, chèn watermark, ghép file); Vidora dựng lệnh, cho xem trước
  rồi mới chạy.
- **Tóm tắt AI**, **xuất metadata** (CSV, Excel, JSON, Markdown, SQLite, Word…),
  **thư viện** có tìm kiếm, tag, bộ sưu tập, phát hiện trùng.
- **Mở rộng** — [plugin](docs/plugins.md), [tải từ xa](docs/remote-download.md),
  [dòng lệnh](docs/cli.md) và [tiện ích trình duyệt](docs/browser-extension.md).

## Hướng dẫn sử dụng

[Mục lục đầy đủ](docs/README.md) — mỗi trang trả lời một việc cụ thể:

| Bắt đầu | Phụ đề | Tải video | Khi trục trặc |
| --- | --- | --- | --- |
| [Cài đặt và chạy lần đầu](docs/installation.md) | [Trích phụ đề cháy](docs/hardsub-ocr.md) | [Tải video và âm thanh](docs/downloading.md) | [Xử lý sự cố](docs/troubleshooting.md) |
| [Tài khoản và bản quyền](docs/license.md) | [Phụ đề từ giọng nói](docs/speech-subtitles.md) | [Tiện ích trình duyệt](docs/browser-extension.md) | |
| | [Dịch và lồng tiếng](docs/translate-dub.md) | [Tải từ xa](docs/remote-download.md) | |

## Tiện ích trình duyệt

Gửi liên kết từ trình duyệt thẳng vào hàng đợi tải của Vidora:

- [Chrome / Edge / Chromium](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Chromium.zip)
- [Firefox](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Firefox-signed.xpi)

Cách cài: [Tiện ích trình duyệt](docs/browser-extension.md).

## Yêu cầu máy

| | Tối thiểu |
| --- | --- |
| Hệ điều hành | Windows 10 trở lên (64-bit) hoặc Linux 64-bit hiện đại |
| Dung lượng trống | Khoảng 6 GB sau khi cài |
| Màn hình | Cửa sổ tối thiểu 1100 × 620 |
| Mạng | Cần Internet để đăng nhập, kích hoạt và tải video; xử lý phụ đề/dịch offline chạy không cần mạng |
| GPU | Không bắt buộc. Card NVIDIA có CUDA giúp OCR và nhận dạng giọng nói nhanh hơn nhiều |

Hai công cụ tuỳ chọn cần tự cài nếu dùng tới: `gallery-dl` cho trang Gallery,
`aria2c` để tăng tốc tải. Mọi thứ khác đã có sẵn trong bộ cài.

## Cập nhật

Vidora tự kiểm tra bản mới khi khởi động và **cập nhật tại chỗ** — không cần
tải lại bộ cài, không hiện hộp thoại quyền quản trị. Mỗi bản cập nhật được kiểm
tra chữ ký số trước khi áp dụng; file không khớp chữ ký sẽ bị từ chối.

## Kiểm tra file trước khi cài

Trên [trang Releases](https://github.com/vidora-app/Vidora/releases/latest),
mỗi file đều hiện mã **SHA-256** ngay bên cạnh tên. So sánh với mã bạn tính trên
máy:

```powershell
# Windows (PowerShell)
(Get-FileHash .\Vidora-Windows-Setup.exe -Algorithm SHA256).Hash.ToLower()
```

```bash
# Linux
sha256sum Vidora-Linux.AppImage
```

Nếu Windows SmartScreen hiện cảnh báo với bộ cài mới tải, xem cách xử lý ở
[Cài đặt và chạy lần đầu](docs/installation.md).

## Hỗ trợ

- **Báo lỗi**: mở một [Issue](https://github.com/vidora-app/Vidora/issues) kèm
  phiên bản Vidora, hệ điều hành, thời điểm xảy ra lỗi và file nhật ký (mở
  trang **Nhật ký** trong app → *Xuất*). Xoá cookie, token và API key khỏi file
  trước khi đính kèm.
- **Hỏi đáp và góp ý**: [Discussions](https://github.com/vidora-app/Vidora/discussions).
- **Lịch sử thay đổi**: ghi chú của từng phiên bản nằm ngay trên
  [trang Releases](https://github.com/vidora-app/Vidora/releases).

## Giấy phép

Vidora phát hành theo giấy phép [MIT](LICENSE). Chỉ tải và xử lý nội dung bạn
sở hữu, được cấp quyền, hoặc pháp luật cho phép.
