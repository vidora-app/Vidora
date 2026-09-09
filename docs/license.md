# Tài khoản và bản quyền

## Đăng nhập

Mở Vidora, nhập email và mật khẩu của tài khoản đã được cấp, bấm **Đăng nhập**.

Tích **Ghi nhớ đăng nhập** để lần sau không phải nhập lại. Thông tin đăng nhập được
lưu trong kho bảo mật của hệ điều hành, không nằm trong file thường.

## Kích hoạt máy

Một mã bản quyền gắn với một máy. Lần đầu chạy trên máy mới, nhập mã ở bước
**Bản quyền** rồi bấm kích hoạt.

Nếu mã đang gắn ở máy khác, kích hoạt sẽ báo:

> Tài khoản hoặc khóa này đã được liên kết với một thiết bị khác.

Xem phần [Chuyển sang máy mới](#chuyển-sang-máy-mới) bên dưới.

## Xem trạng thái

Hai nơi hiển thị cùng một thông tin:

- **Màn hình khởi động**, trước khi vào ứng dụng: trạng thái bản quyền, gói, chủ sở
  hữu, ngày hết hạn.
- **Cài đặt → Tài khoản & Bản quyền**, bên trong ứng dụng: thêm mốc *Lease hợp lệ đến*.

## Lease là gì

Máy của bạn giữ một giấy phép tạm thời có chữ ký, gọi là **lease**. Ứng dụng tự làm
mới nó trong lúc chạy, bạn không phải làm gì.

Muốn ép làm mới ngay — chẳng hạn sau khi được nâng gói — vào
**Cài đặt → Tài khoản & Bản quyền** rồi bấm **Làm mới lease**.

Lưu ý: chỉ có lease thì chưa đủ. Vidora vẫn cần kết nối máy chủ lúc khởi động và
kiểm tra lại định kỳ trong lúc chạy. Lease còn hạn nhưng mất mạng kéo dài thì ứng
dụng vẫn khoá lại.

## Chuyển sang máy mới

Trên máy cũ:

1. **Cài đặt → Tài khoản & Bản quyền**
2. Bấm **Huỷ kích hoạt thiết bị**

Trên máy mới: cài Vidora, đăng nhập cùng tài khoản, nhập lại mã bản quyền.

Máy cũ đã hỏng, không huỷ kích hoạt được thì liên hệ nơi bán để được gỡ ràng buộc
từ phía máy chủ.

## Đăng xuất

Bấm đăng xuất ở màn hình khởi động, hoặc trong **Cài đặt → Tài khoản & Bản quyền**.

Đăng xuất sẽ thu hồi phiên trên máy chủ và xoá thông tin đăng nhập khỏi kho bảo mật
của hệ điều hành. Ứng dụng quay về màn hình đăng nhập.

## Khi ứng dụng khoá giữa chừng

| Thông báo | Nguyên nhân | Cần làm |
| --- | --- | --- |
| Phiên của bạn đã hết hạn. Vui lòng đăng nhập lại. | Phiên kết thúc | Đăng nhập lại |
| Bản quyền này không còn hiệu lực. | Mã bị thu hồi hoặc tạm ngưng | Liên hệ nơi bán |
| Bản quyền này đã hết hạn. | Hết thời hạn sử dụng | Gia hạn hoặc mua mã mới |
| Thiết bị này đã bị thu hồi. Hãy đăng nhập và kích hoạt lại. | Ràng buộc thiết bị bị xoá từ máy chủ | Đăng nhập rồi kích hoạt lại |
| Không kết nối được máy chủ. | Mạng hoặc máy chủ | Kiểm tra mạng rồi thử lại |

## Bảo mật

Không chia sẻ mã bản quyền. Mã gắn với tài khoản và máy của bạn; người khác dùng sẽ
làm hỏng kích hoạt của chính bạn.

Khi gửi log để nhờ hỗ trợ, xoá cookie, token và API key trước — xem
[Xử lý sự cố](troubleshooting.md#gửi-log-cho-hỗ-trợ).
