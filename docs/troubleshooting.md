# Xử lý sự cố

## Cài đặt

### Windows chặn file cài

Màn hình xanh *"Windows protected your PC"* hiện với mọi file cài chưa mua chứng chỉ
ký số của Microsoft. Bấm **More info** rồi **Run anyway**.

Muốn chắc chắn file nguyên vẹn thì đối chiếu SHA-256 với `SHA256SUMS.txt` —
xem [Cài đặt](installation.md#kiểm-tra-file-trước-khi-cài).

### AppImage không chạy

Chưa cấp quyền chạy:

```bash
chmod +x Vidora-Linux.AppImage
```

### Không đủ dung lượng

Cần khoảng 6 GB trống sau khi cài. File cài 1,5 GB còn cần thêm chỗ để giải nén trong
lúc cài.

## Đăng nhập và bản quyền

### Không kết nối được máy chủ

Kiểm tra mạng trước. Nếu mạng bình thường mà vẫn không vào được, có thể máy chủ đang
bảo trì — thử lại sau ít phút.

### Báo đã liên kết với thiết bị khác

Mã bản quyền đang gắn ở máy khác. Huỷ kích hoạt ở máy đó trước, xem
[Tài khoản và bản quyền](license.md#chuyển-sang-máy-mới).

### Ứng dụng khoá giữa chừng

Xem bảng thông báo trong [Tài khoản và bản quyền](license.md#khi-ứng-dụng-khoá-giữa-chừng).

## Phụ đề

### OCR chạy xong nhưng không ra dòng nào

Nguyên nhân hay gặp nhất là **chọn sai ngôn ngữ**. Chọn nhầm hệ chữ thì kết quả là
rỗng chứ không phải chữ sai. Kiểm tra lại ngôn ngữ rồi chạy lại.

Nếu ngôn ngữ đã đúng:

- Đổi sang chế độ **Chính xác** — nó có thêm bước khôi phục dòng
- Kiểm tra phụ đề có thật sự nằm trong hình không, hay là phụ đề mềm bật tắt được
- Chữ quá nhỏ hoặc quá mờ thì thử video bản chất lượng cao hơn

### OCR chạy rất chậm

Không có GPU thì chạy bằng CPU, chậm hơn nhiều lần. Kiểm tra trong
**Cài đặt → AI → Chẩn đoán** xem CUDA có được nhận không.

Chế độ **Nhanh** đổi độ chính xác lấy tốc độ.

### Nhận dạng giọng nói không chạy

Chưa cài model. Vào **Cài đặt → Thành phần**, cài một model Whisper —
xem [Tạo phụ đề từ giọng nói](speech-subtitles.md#trước-tiên-tải-model).

### Kết quả nhận dạng sai nhiều

Dùng model lớn hơn. Small là mặc định; Large v3 Turbo chính xác hơn nhiều mà không
chậm bằng Large v3.

## Tải video

### Một trang không tải được

Trang đó có thể vừa đổi cách hoạt động. Thử lại sau; công cụ tải bên dưới được cập
nhật thường xuyên theo bản mới của Vidora.

### Tải rất chậm

Cài `aria2c` rồi bật trong **Cài đặt → Phụ thuộc**.

### Trang Gallery không hoạt động

Cần `gallery-dl`, không nằm trong bộ cài. Xem **Cài đặt → Phụ thuộc**.

## Cập nhật

### Cập nhật xong app không mở

Cài đè bằng file `.msi` mới nhất từ [trang Releases](https://github.com/vidora-app/Vidora/releases/latest).
Thư viện và lịch sử không bị mất.

### Không thấy bản cập nhật

Vidora kiểm tra lúc khởi động. Nếu chưa tới lượt máy bạn trong đợt phát hành thì sẽ
chưa được mời cập nhật — đợi thêm, hoặc tải bản mới nhất về cài đè.

## Ngôn ngữ hiển thị

App hiện tiếng Anh vì hệ điều hành đang dùng tiếng Anh. Đổi trong
**Cài đặt → Chung → Ngôn ngữ**.

## Gửi log cho hỗ trợ

1. Mở trang **Nhật ký** trong ứng dụng.
2. Xuất file log.
3. Gửi kèm **phiên bản Vidora** và **thời điểm xảy ra lỗi**.

Trước khi chia sẻ công khai, xoá cookie, token và API key trong log.

Liên hệ qua kênh hỗ trợ đã được cấp cho bạn, hoặc mở
[issue trên GitHub](https://github.com/vidora-app/Vidora/issues).
