# Tiện ích trình duyệt

Gửi link từ trang đang xem thẳng vào hàng đợi tải của Vidora.

## Tải về

| Trình duyệt | File |
| --- | --- |
| Chrome, Edge, Brave, Opera, Vivaldi, Cốc Cốc | [Vidora-Extension-Chromium.zip](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Chromium.zip) |
| Firefox | [Vidora-Extension-Firefox-signed.xpi](https://github.com/vidora-app/Vidora/releases/latest/download/Vidora-Extension-Firefox-signed.xpi) |

## Cài trên Chrome, Edge và các trình duyệt Chromium

1. Giải nén `Vidora-Extension-Chromium.zip`.
2. Mở `chrome://extensions` (Edge dùng `edge://extensions`).
3. Bật **Developer mode**.
4. Bấm **Load unpacked**.
5. Chọn thư mục vừa giải nén.

Đừng xoá thư mục đó — trình duyệt đọc trực tiếp từ đấy.

## Cài trên Firefox

1. Tải file `.xpi`.
2. Kéo thả vào cửa sổ Firefox.
3. Xác nhận cài đặt.

## Điều kiện

- Đã cài ứng dụng Vidora
- Đã mở Vidora **ít nhất một lần**, để hệ điều hành đăng ký giao thức `vidora://`

## Dùng thế nào

**Nút nổi** hiện trên các trang được hỗ trợ: YouTube, TikTok, Instagram, Facebook,
X/Twitter, Vimeo, Twitch, Bilibili, Dailymotion, SoundCloud.

**Popup của tiện ích** dùng được trên mọi trang http/https, kể cả trang không có nút
nổi.

Ở cả hai chỗ đều chọn được:

- **Loại**: Video hoặc Audio
- **Chất lượng**: Best, 8K, 4K, 2K, 1080p, 720p, 480p, 360p — audio thì Auto hoặc 128 kbps
- **Hành động**: *Tải ngay* hoặc *Thêm vào hàng đợi*

Link YouTube được chuẩn hoá tự động: nếu URL có cả video lẫn playlist, Vidora chỉ lấy
video, không kéo cả playlist ngoài ý muốn.

Link đã có trong hàng đợi thì Vidora nhảy tới mục cũ thay vì tạo mục trùng.

## Ẩn nút nổi

Thu gọn nút thành tab nhỏ, hoặc tắt hẳn. Bật lại trong popup của tiện ích.

## Khi không gửi được

| Hiện tượng | Cách xử lý |
| --- | --- |
| Báo *scheme does not have a registered handler* | Mở Vidora một lần rồi thử lại |
| Hộp thoại mở app hiện ra rồi tắt ngay | Kiểm tra Vidora đã cài đúng chỗ; thử gửi lại bằng popup |
| Không thấy nút nổi | Trang không nằm trong danh sách hỗ trợ; dùng popup. Hoặc bật lại nút nổi trong popup |
| Vẫn không được | Dùng nút copy URL trong popup rồi dán tay vào Vidora, để biết lỗi nằm ở tiện ích hay ở app |
