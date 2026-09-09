# Trích phụ đề cháy trong hình

Phụ đề đã nung vào khung hình thì không có file nào để lấy ra. Vidora đọc thẳng từ
hình ảnh và dựng lại thành phụ đề sửa được.

## Làm nhanh

1. Mở trang **Video → Phụ đề**.
2. Chọn video.
3. Chọn chế độ chất lượng: **Nhanh**, **Tự động** hoặc **Chính xác**.
4. Bấm chạy.
5. Xong thì mở kết quả trong Subtitle Workshop để sửa, hoặc đưa thẳng sang dịch.

Không phải tải model gì cả. Toàn bộ bộ nhận dạng chữ đã nằm sẵn trong bộ cài.

## Chọn chế độ nào

| Chế độ | Dùng khi |
| --- | --- |
| **Nhanh** | Chữ to, nền sạch, cần kết quả gấp |
| **Tự động** | Mặc định. Cân bằng giữa tốc độ và độ chính xác |
| **Chính xác** | Chữ nhỏ, nền nhiễu, phụ đề mờ. Chậm hơn nhưng bắt được dòng mà chế độ khác bỏ sót |

Chế độ **Chính xác** chạy thêm một bước khôi phục dòng: khi bộ dò hình ảnh không
dựng được vùng chữ nhưng OCR vẫn đọc ra chữ hợp lệ, dòng đó vẫn được giữ.

## Ngôn ngữ

Chọn ngôn ngữ của phụ đề trong video. Vidora dùng nó để chọn bộ nhận dạng phù hợp.

Điều quyết định không phải ngôn ngữ mà là **hệ chữ**. Tiếng Việt, Anh, Pháp, Đức,
Tây Ban Nha đều dùng chung một bộ nhận dạng chữ Latin. Tiếng Hàn có bộ riêng, tiếng
Nga và các thứ tiếng Kirin dùng bộ khác, tiếng Ả Rập, Thái, Hy Lạp, Devanagari mỗi
nhóm một bộ.

Chọn sai nhóm chữ thì kết quả không phải chữ xấu mà là **rỗng**. Nếu chạy xong không
ra dòng nào, kiểm tra lại ngôn ngữ trước tiên.

## Chất lượng thực tế

Khác nhau theo hệ chữ. Các đường được kiểm nhiều nhất là tiếng Việt, Anh, Trung,
Nhật, Hàn. Những hệ chữ còn lại đọc được nhưng chưa có số đo riêng.

Với video khó, chạy thử một đoạn ngắn trước khi xử lý cả file.

## Phụ đề di chuyển

Vidora không dùng một khung cố định. Nó theo dõi từng dòng phụ đề từ lúc hiện đến
lúc tắt, nên phụ đề trượt vị trí giữa video vẫn được bắt.

Tối đa 12 vùng phụ đề trên một video.

## Watermark

OCR đọc watermark rõ y như đọc lời thoại, nên không thể phân biệt bằng độ tin cậy.

Vidora phân biệt bằng **hành vi theo thời gian**: một dòng thoại chiếm màn hình vài
giây rồi biến mất, còn watermark sống dai qua hàng chục dòng khác và quay lại sau
những khoảng trống.

Khi bằng chứng chưa đủ rõ, Vidora **giữ lại dòng**. Sót một dòng thừa dễ xoá hơn
nhiều so với mất một câu thoại thật.

## Video dài

Chạy được. Bộ nhớ không phình theo độ dài video vì Vidora chỉ giữ các vùng đang hoạt
động.

Kết quả OCR được lưu đệm, nên chạy lại cùng video không làm lại từ đầu.

## GPU

Có GPU NVIDIA thì Vidora dùng CUDA, nhanh hơn nhiều lần. Không có thì tự lùi về CPU,
vẫn chạy nhưng lâu hơn.

Xem trạng thái trong **Cài đặt → AI → Chẩn đoán**.

## Sau khi trích xong

- Mở trong **Subtitle Workshop** để sửa nội dung và thời gian
- Đưa sang [dịch và lồng tiếng](translate-dub.md)
- Xuất ra SRT, VTT hoặc ASS

## Không ra kết quả

Xem [Xử lý sự cố → OCR ra chuỗi rỗng](troubleshooting.md#ocr-chạy-xong-nhưng-không-ra-dòng-nào).
