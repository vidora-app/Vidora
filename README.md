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

### Trích phụ đề cháy trong hình

Phụ đề đã nung vào khung hình thì không có file nào để lấy ra. Vidora đọc thẳng
từ hình ảnh và dựng lại thành phụ đề có thể sửa được.

**Nhận diện không phụ thuộc chữ viết.** Bộ dò làm việc bằng tương phản nét, cạnh
và thành phần liên thông — không phải bằng hình dạng ký tự. Nó tìm ra dòng phụ
đề bất kể đó là chữ Hán, kana, Hangul, Kirin, Ả Rập, Devanagari hay Latin.

**70 mã ngôn ngữ, 8 đầu nhận dạng riêng.** Mỗi hệ chữ đi vào đúng model của nó:
Trung giản thể và phồn thể, Nhật, Hàn, Latin (41 ngôn ngữ, có tiếng Việt), Kirin
(10), Ả Rập (6), Devanagari (7), Hy Lạp, Thái. Định tuyến sai một hệ chữ không
cho ra chữ xấu — nó cho ra chuỗi rỗng — nên bảng định tuyến được kiểm tra chặt.

**Bám theo phụ đề di chuyển.** Một khung cố định không đủ: chỗ phụ đề trượt đi
thì lọt ra ngoài, chỗ khung quét qua thì che nhầm nền trống. Vidora theo dõi
từng dòng phụ đề từ lúc hiện tới lúc tắt, ghép vết bằng IoU, tâm, chiều cao,
chiều rộng và nội dung, tối đa 12 vùng trên một video.

**Phân biệt phụ đề với watermark bằng hành vi, không bằng độ tin cậy.** OCR đọc
watermark rõ y như đọc lời thoại, nên điểm tin cậy không giúp gì. Vidora chấm
theo cách chữ *cư xử theo thời gian*: một dòng thoại chia màn hình với gần như
không gì khác, còn watermark sống lâu hơn hàng chục dòng không liên quan và quay
lại sau những khoảng trống. Bằng chứng yếu thì giữ nguyên dòng — mất một câu
thoại thật tệ hơn nhiều so với sót một dòng thừa.

**Ba chế độ.** Nhanh dùng cặp model gọn để đổi độ chính xác lấy tốc độ. Tự động
và Chính xác dùng model nặng hơn, và Chính xác còn chạy thêm bước khôi phục dòng
để một dòng OCR hợp lệ không bị mất chỉ vì bộ dò hình ảnh không dựng được ứng
viên.

**Chạy được video dài.** Bộ theo dõi chỉ giữ ảnh đại diện đang hoạt động cùng
vài khung chờ, nên bộ nhớ không phình theo độ dài video. Kết quả OCR được lưu
đệm bền theo danh tính suy luận và bằng chứng ảnh, nên chạy lại không làm lại
việc cũ. Có GPU thì dùng CUDA, không có thì tự lùi về CPU.

Sau khi trích xong, mở thẳng trong Subtitle Workshop để sửa, hoặc đưa qua dịch
và lồng tiếng.

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
