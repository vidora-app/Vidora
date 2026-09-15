# Cài đặt và chạy lần đầu

## Tải về

| Nền tảng | File |
| --- | --- |
| Windows 10/11 x64 | [Vidora-Windows-Setup.exe](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Windows-Setup.exe) |
| Linux x64 | [Vidora-Linux.AppImage](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.AppImage) |
| Linux x64 (Debian/Ubuntu) | [Vidora-Linux.deb](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.deb) |

macOS chưa có trong bản phát hành hiện tại.

## Windows

Mở `Vidora-Windows-Setup.exe` và bấm **Install**. Bộ cài đặt vào tài khoản Windows
đang dùng (`%LOCALAPPDATA%\Programs\Vidora`), không hỏi quyền quản trị và không
hiện hộp thoại UAC — cả khi cài lần đầu lẫn khi tự cập nhật sau này.

### Windows sẽ hiện cảnh báo

Lần đầu mở file cài, Windows hiện màn hình xanh:

> **Windows protected your PC**
> Microsoft Defender SmartScreen prevented an unrecognised app from starting.

Bấm **More info**, rồi bấm **Run anyway**.

Đây không phải dấu hiệu file có vấn đề. Windows hiện cảnh báo này cho mọi file cài
chưa mua chứng chỉ ký số của Microsoft. Nếu muốn tự kiểm tra trước, xem phần
[Kiểm tra file trước khi cài](#kiểm-tra-file-trước-khi-cài) bên dưới.

## Linux — AppImage

```bash
chmod +x Vidora-Linux.AppImage
./Vidora-Linux.AppImage
```

Không cần cài. File chạy trực tiếp.

## Linux — .deb

```bash
sudo apt install ./Vidora-Linux.deb
```

Sau đó mở Vidora từ menu ứng dụng.

## Kiểm tra file trước khi cài

Trên [trang Releases](https://github.com/vidora-app/Vidora/releases/latest), GitHub
hiện mã **SHA-256** ngay cạnh tên từng file. Tính mã của file đã tải rồi so sánh:

Windows PowerShell:

```powershell
(Get-FileHash .\Vidora-Windows-Setup.exe -Algorithm SHA256).Hash.ToLower()
```

Linux:

```bash
sha256sum Vidora-Linux.AppImage
```

Khớp là file nguyên vẹn. Bản cập nhật tự động còn được kiểm tra chữ ký số trước khi
áp dụng, nên bạn không phải làm gì thủ công cho các lần cập nhật sau.

## Vì sao file cài lớn

File cài khoảng 1,7–2 GB vì mang sẵn toàn bộ thứ cần để xử lý ngay trên máy: bộ nhận
dạng chữ, FFmpeg, Python runtime, giọng đọc tiếng Việt và bộ dịch offline.

Đổi lại, cài xong là dùng được ngay, kể cả khi mất mạng. Không có chuyện đang làm
giữa chừng thì app dừng lại để tải thêm thứ gì.

Ngoại lệ duy nhất là model nhận dạng giọng nói — xem
[Tạo phụ đề từ giọng nói](speech-subtitles.md).

## Yêu cầu máy

- Windows 10 trở lên (x64), hoặc Linux x64 hiện đại
- Khoảng 6 GB trống sau khi cài
- Cửa sổ tối thiểu 1100 × 620
- Kết nối Internet, tài khoản và mã bản quyền hợp lệ

Có GPU NVIDIA thì OCR và nhận dạng giọng nói chạy nhanh hơn nhiều. Không có thì vẫn
chạy được bằng CPU, chỉ lâu hơn.

Hai công cụ tuỳ chọn, chỉ cần khi dùng tới:

- `gallery-dl` — cho trang Gallery
- `aria2c` — tăng tốc tải

Phần còn lại đã có sẵn trong bộ cài.

## Chạy lần đầu

1. Mở Vidora. Cửa sổ đăng nhập hiện ra.
2. Đăng nhập bằng tài khoản đã được cấp.
3. Nhập mã bản quyền nếu máy này chưa kích hoạt — xem [Tài khoản và bản quyền](license.md).
4. Bấm **Khởi động** để vào ứng dụng.

## Ngôn ngữ hiển thị

Lần đầu chạy, Vidora dùng ngôn ngữ của hệ điều hành. Máy cài Windows tiếng Anh thì
app hiện tiếng Anh.

Đổi trong **Cài đặt → Chung → Ngôn ngữ**. Lựa chọn được ghi nhớ cho những lần sau.

## Cập nhật

Vidora tự kiểm tra bản mới khi khởi động và cập nhật tại chỗ. Bạn không phải tải lại
file cài cho mỗi phiên bản.

Bản cập nhật được kiểm tra chữ ký trước khi áp dụng; file không khớp chữ ký bị từ
chối, không cài.

## Gỡ cài đặt

Windows: **Settings → Apps → Vidora → Uninstall**.

Linux `.deb`:

```bash
sudo apt remove vidora
```

Linux AppImage: xoá file là xong.

Thư viện và lịch sử tải nằm riêng trong thư mục dữ liệu người dùng, gỡ app không xoá
chúng.
