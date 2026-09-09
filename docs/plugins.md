# Plugin

Plugin chạy tự động khi có sự kiện tải — gửi thông báo, tải file lên nơi khác, xử lý
file sau khi tải xong.

## Cài plugin

**Cài đặt → Plugin → Nhập plugin**. Chọn file `.ywp`, xem thông tin, xác nhận.

Vidora kiểm tra chữ ký và checksum của gói trước khi cài. Gói không khớp bị từ chối.

## Plugin chạy lúc nào

| Sự kiện | Xảy ra khi |
| --- | --- |
| `download.queued` | Một mục vừa được thêm vào hàng đợi |
| `download.beforeStart` | Ngay trước khi bắt đầu tải |
| `download.completed` | Tải xong |
| `download.failed` | Tải lỗi |

Mỗi sự kiện có một thẻ riêng trong phần cài đặt, nơi bạn xếp thứ tự các plugin sẽ
chạy.

## Quyền

Mỗi plugin khai báo trước nó cần quyền gì. Bạn thấy danh sách đó lúc cài, trước khi
xác nhận. Không đồng ý thì đừng cài.

## Xem plugin đang làm gì

**Cài đặt → Plugin** hiện trạng thái từng plugin và log của lần chạy gần nhất.

## Gỡ

Bấm gỡ trong danh sách plugin. Plugin bị xoá khỏi mọi luồng sự kiện.

## Chỉ cài plugin bạn tin

Plugin chạy được với quyền nó xin. Chỉ cài từ nguồn bạn biết rõ.
