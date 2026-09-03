# Vidora

Ứng dụng desktop để tải, xử lý, dịch và biên tập video, âm thanh và phụ đề. Chạy
cục bộ trên máy bạn: yt-dlp, FFmpeg, OCR, nhận dạng giọng nói, dịch và giọng đọc
đều nằm trong bộ cài, không cần dịch vụ ngoài cho các tác vụ chính.

Đây là nơi phát hành bản cài chính thức. Mã nguồn nằm ở kho riêng.

## Tải về

| Nền tảng | File | Ghi chú |
| --- | --- | --- |
| Windows 10/11 x64 | [Vidora-Windows.msi](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Windows.msi) | Bản cài chính. Cũng là bản tự cập nhật dùng. |
| Linux x64 | [Vidora-Linux.AppImage](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.AppImage) | Chạy trực tiếp, không cần cài. `chmod +x` trước khi mở. |
| Linux x64 (Debian/Ubuntu) | [Vidora-Linux.deb](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.deb) | `sudo apt install ./Vidora-Linux.deb` |

macOS chưa có trong bản phát hành hiện tại.

Tất cả file phát hành nằm ở [trang Releases](https://github.com/vidora-app/Vidora/releases/latest).

### Vì sao file lớn

Mỗi bản cài từ 1,2 đến 1,7 GB. Bên trong là toàn bộ runtime xử lý: CPython kèm
PyTorch, PaddleOCR, faster-whisper, FFmpeg, Piper và các model giọng đọc. Bạn tải
một lần rồi dùng offline, thay vì để ứng dụng tự tải rời rạc về sau.

## Kiểm tra file trước khi cài

Mỗi bản phát hành kèm `SHA256SUMS.txt` phủ mọi file.

```bash
# Linux / macOS
sha256sum -c SHA256SUMS.txt --ignore-missing
```

```powershell
# Windows
(Get-FileHash Vidora-Windows.msi -Algorithm SHA256).Hash.ToLower()
# so sánh với dòng tương ứng trong SHA256SUMS.txt
```

Các file `.sig` đi kèm là chữ ký Minisign của bản cài. Ứng dụng tự kiểm tra chữ
ký này mỗi lần cập nhật; bạn không cần làm gì thủ công, nhưng nếu muốn tự xác
minh thì khoá công khai được ghim trong ứng dụng và công bố cùng bản phát hành.

## Cài đặt

**Windows** — mở `.msi` và làm theo trình cài đặt.

**Linux, AppImage** — không cần cài:

```bash
chmod +x Vidora-Linux.AppImage
./Vidora-Linux.AppImage
```

**Linux, .deb** — trên Debian, Ubuntu và các bản dẫn xuất:

```bash
sudo apt install ./Vidora-Linux.deb
```

## Yêu cầu

- Windows 10 trở lên (x64), hoặc Linux x64 hiện đại.
- Khoảng 6 GB trống sau khi cài.
- Kết nối Internet, tài khoản Vidora và mã bản quyền hợp lệ. Ứng dụng chính chỉ
  mở sau khi máy chủ xác minh tài khoản, thiết bị và bản quyền.
- Cửa sổ tối thiểu 1100 × 620.

Một số tính năng cần công cụ tự cài thêm: `gallery-dl` cho trang Gallery,
`aria2c` nếu muốn tăng tốc tải. Những thứ còn lại đã có sẵn trong bộ cài.

## Cập nhật

Vidora tự kiểm tra bản mới khi khởi động và cập nhật tại chỗ. Bạn không cần tải
lại bản cài cho mỗi phiên bản. Bản cập nhật được kiểm tra chữ ký trước khi áp
dụng; một file không khớp chữ ký sẽ bị từ chối.

## Tiện ích trình duyệt

Gửi liên kết từ trình duyệt thẳng vào hàng đợi tải:

- [Chromium / Chrome / Edge](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Chromium.zip)
- [Firefox](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Firefox-signed.xpi)

## Hỗ trợ

Gặp lỗi thì mở **Nhật ký** trong ứng dụng, xuất file và gửi kèm phiên bản Vidora
cùng thời điểm xảy ra lỗi. Xoá cookie, token và API key trước khi chia sẻ công
khai.

Liên hệ qua kênh hỗ trợ nhà cung cấp đã cấp cho bạn.

## Giấy phép

Vidora là bản fork rebrand của Youwee, giữ nguyên giấy phép MIT. Chi tiết giấy
phép của các thành phần bên thứ ba nằm trong `THIRD_PARTY_NOTICES.md` đi kèm mỗi
bản phát hành và trong thư mục cài đặt.

Chỉ tải nội dung bạn sở hữu, được cấp quyền, hoặc pháp luật cho phép.
