# Tải từ xa qua Telegram

Gửi link cho Vidora khi bạn đang ở ngoài. Máy ở nhà nhận và tải.

Vidora phải đang chạy trên máy đó — tính năng này điều khiển app đang mở, không đánh
thức máy đã tắt.

## Thiết lập

**Cài đặt → Tải từ xa** có sẵn hướng dẫn 5 bước ngay trong app. Tóm tắt:

1. Nhắn với **@BotFather** trên Telegram, tạo bot mới.
2. Copy **bot token** BotFather đưa cho, dạng `123456789:AA...`.
3. Nhắn `/start` cho bot vừa tạo.
4. Lấy **chat ID** của bạn — app có nút hướng dẫn lấy qua `getUpdates`.
5. Dán token và chat ID vào Vidora, bật lên, nhắn `/help` cho bot để thử.

## Hai ô bắt buộc

**Bot Token** — của riêng bạn, giữ kín. Ai có token này điều khiển được bot.

**Chat ID được phép** — ít nhất một. Ngăn cách bằng dấu phẩy nếu nhiều
(`123456789, -1001234567890`). Chỉ những chat ID trong danh sách mới ra lệnh được.

## Lệnh

| Lệnh | Việc |
| --- | --- |
| `/start` | Bắt đầu |
| `/add <url>` | Thêm vào hàng đợi, chưa tải |
| `/download <url>` | Tải ngay |
| `/status` | Xem đang chạy gì |
| `/queue` | Xem hàng đợi |
| `/run` | Chạy hàng đợi |
| `/stop` | Dừng |
| `/help` | Danh sách lệnh |

Chất lượng nhận: `best, 8k, 4k, 2k, 1080, 720, 480, 360, audio, mp3`.

Nhắn mỗi link không kèm lệnh cũng được. Việc xảy ra tuỳ cài đặt: **Tải ngay** (mặc
định) hoặc **Thêm vào hàng đợi**.

## Trạng thái kết nối

Dòng **Trạng thái kết nối** trong phần cài đặt báo **Đang chạy**, **Lỗi** kèm nội
dung lỗi, hoặc **Đã tắt**.

## An toàn

Bot token nằm trong kho bảo mật của hệ điều hành, không nằm trong file thường.

Đừng đưa token cho ai. Lỡ lộ thì nhắn `/revoke` cho BotFather để huỷ token cũ rồi
lấy token mới.
