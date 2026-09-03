# Vidora

Ứng dụng desktop tải, xử lý, dịch và biên tập video, âm thanh, hình ảnh và phụ
đề. Mọi tác vụ nặng chạy ngay trên máy bạn — nhận dạng giọng nói, OCR phụ đề
cháy, dịch và lồng tiếng đều không cần gửi file đi đâu.

## Tải về

| Nền tảng | File | Ghi chú |
| --- | --- | --- |
| Windows 10/11 x64 | [Vidora-Windows.msi](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Windows.msi) | Bản cài chính |
| Linux x64 | [Vidora-Linux.AppImage](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.AppImage) | Chạy trực tiếp, `chmod +x` trước khi mở |
| Linux x64 (Debian/Ubuntu) | [Vidora-Linux.deb](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Linux.deb) | `sudo apt install ./Vidora-Linux.deb` |

macOS chưa có trong bản phát hành hiện tại.

Toàn bộ file nằm ở [trang Releases](https://github.com/vidora-app/Vidora/releases/latest).

## Tính năng

### Tải video

**YouTube** — dán một URL, nhiều URL, hoặc tìm bằng từ khoá. Chọn video hay chỉ
âm thanh, chất lượng tới 8K, định dạng và codec, FPS. Tải cả playlist hoặc chọn
phạm vi mục. Tải livestream từ đầu. Cắt sẵn một khoảng thời gian thay vì tải cả
video. Hẹn giờ tải. Kèm phụ đề, thumbnail, SponsorBlock. Tự thử lại khi lỗi.

**Đa nền tảng** — TikTok, Instagram, Facebook, X/Twitter, Bilibili, Youku,
Douyin và hơn 1.800 website khác.

**Gallery** — bộ sưu tập ảnh, feed creator, chương truyện tranh.

**Kênh** — theo dõi kênh trên YouTube, Bilibili, Youku, TikTok, Vimeo,
Dailymotion, Twitch, SoundCloud, Niconico. Bật tự động tải, đặt chu kỳ kiểm tra,
chất lượng và bộ lọc từ khoá; nội dung mới về hàng đợi mà không cần bạn mở app.

### Phụ đề và dịch video

**Tạo phụ đề từ giọng nói** — nhận dạng chạy cục bộ, có mốc thời gian từng từ,
tự dò ngôn ngữ, xử lý được video dài nhiều giờ và tiếp tục được nếu gián đoạn.

**Trích phụ đề cháy trong hình** — khoanh vùng chứa phụ đề, chọn ngôn ngữ nguồn
và chế độ Nhanh / Tự động / Chính xác. OCR đọc chữ ngay trong khung hình rồi
dựng lại thành file phụ đề.

**Subtitle Workshop** — sửa nội dung và thời gian từng câu, tìm và thay thế,
tách hoặc gộp câu, kiểm tra tốc độ đọc và lỗi chồng thời gian, đồng bộ theo
waveform và cảnh cắt. Xuất SRT, VTT, ASS. Chuyển đổi hàng loạt.

**Dịch** — dịch offline không cần mạng, hoặc dùng AI bạn tự cấu hình. Kết quả
hiện dần theo từng đoạn thay vì đợi cả file dịch xong.

**Lồng tiếng** — đọc phụ đề đã dịch thành giọng nói và ghép lại vào video.

### Xử lý và tổ chức

**Xử lý video** — mô tả việc cần làm bằng lời: cắt đoạn, nén, đổi kích thước,
tách âm thanh, tạo GIF, chèn watermark, ghép file. Vidora dựng lệnh, cho bạn xem
trước rồi mới chạy.

**Tóm tắt AI** — tóm tắt video theo kiểu và ngôn ngữ bạn chọn, lưu thẳng vào
thư viện.

**Xuất dữ liệu** — lấy metadata từ playlist, kênh, từ khoá hoặc danh sách URL
rồi xuất CSV, Excel, JSON, Markdown, XML, YAML, SQLite, Word. Tải kèm thumbnail,
phụ đề, bình luận khi nguồn có.

**Thư viện** — lịch sử lâu dài của mọi thứ đã tải. Tìm kiếm, gắn tag, tạo bộ
sưu tập, phát trực tiếp, đổi tên, tải lại, cắt file. Tự phát hiện video đã tải
trùng.

**Mở rộng** — plugin, tải từ xa, và tiện ích trình duyệt gửi link thẳng vào
hàng đợi.

## Cài đặt

**Windows** — mở `.msi` và làm theo trình cài đặt.

**Linux, AppImage**

```bash
chmod +x Vidora-Linux.AppImage
./Vidora-Linux.AppImage
```

**Linux, .deb**

```bash
sudo apt install ./Vidora-Linux.deb
```

### Vì sao file lớn

Bản cài từ 1,2 đến 1,7 GB vì mang sẵn toàn bộ runtime xử lý cục bộ. Bạn tải một
lần rồi dùng được offline, thay vì để ứng dụng tải rời rạc về sau giữa lúc đang
làm việc.

## Kiểm tra file trước khi cài

Mỗi bản phát hành kèm `SHA256SUMS.txt` phủ mọi file.

```bash
# Linux
sha256sum -c SHA256SUMS.txt --ignore-missing
```

```powershell
# Windows
(Get-FileHash Vidora-Windows.msi -Algorithm SHA256).Hash.ToLower()
# so sánh với dòng tương ứng trong SHA256SUMS.txt
```

File `.sig` đi kèm là chữ ký của bản cài. Ứng dụng tự kiểm tra chữ ký này mỗi
lần cập nhật, nên bạn không cần làm gì thủ công.

## Yêu cầu

- Windows 10 trở lên (x64), hoặc Linux x64 hiện đại.
- Khoảng 6 GB trống sau khi cài.
- Kết nối Internet, tài khoản và mã bản quyền hợp lệ.
- Cửa sổ tối thiểu 1100 × 620.

Hai công cụ tuỳ chọn cần tự cài nếu dùng tới: `gallery-dl` cho trang Gallery,
`aria2c` nếu muốn tăng tốc tải. Phần còn lại đã có sẵn trong bộ cài.

## Cập nhật

Vidora tự kiểm tra bản mới khi khởi động và cập nhật tại chỗ, không cần tải lại
bản cài cho mỗi phiên bản. Bản cập nhật được kiểm tra chữ ký trước khi áp dụng;
file không khớp chữ ký sẽ bị từ chối.

## Tiện ích trình duyệt

Gửi liên kết từ trình duyệt thẳng vào hàng đợi tải:

- [Chromium / Chrome / Edge](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Chromium.zip)
- [Firefox](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Firefox-signed.xpi)

## Hỗ trợ

Gặp lỗi thì mở **Nhật ký** trong ứng dụng, xuất file và gửi kèm phiên bản Vidora
cùng thời điểm xảy ra lỗi. Xoá cookie, token và API key trước khi chia sẻ công
khai.

Liên hệ qua kênh hỗ trợ đã được cấp cho bạn.

## Giấy phép

Vidora phát hành theo giấy phép MIT. Giấy phép đầy đủ và thông tin giấy phép của
các thành phần bên thứ ba nằm trong `THIRD_PARTY_NOTICES.md` đi kèm mỗi bản phát
hành và trong thư mục cài đặt.

Chỉ tải nội dung bạn sở hữu, được cấp quyền, hoặc pháp luật cho phép.
