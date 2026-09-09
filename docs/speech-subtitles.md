# Tạo phụ đề từ giọng nói

Nghe lời thoại trong video rồi viết ra phụ đề có mốc thời gian. Chạy ngay trên máy,
không gửi file đi đâu.

## Trước tiên: tải model

Đây là thứ **duy nhất** Vidora còn phải tải thêm. Mọi model OCR đều nằm sẵn trong bộ
cài, riêng model nhận dạng giọng nói thì không, vì kích cỡ nào hợp là tuỳ máy bạn.

Vào **Cài đặt → Thành phần**, chọn một model rồi bấm **Cài trong app**.

| Model | Dung lượng tải | Dùng khi |
| --- | --- | --- |
| Tiny | 78 MB | Máy yếu, chỉ cần bản nháp |
| Base | 148 MB | Máy yếu, khá hơn Tiny |
| **Small** | **486 MB** | **Khuyến nghị.** Cân bằng tốt nhất |
| Medium | 1,5 GB | Máy khá, cần chính xác hơn |
| Large v3 | 3,0 GB | Máy mạnh, chính xác cao nhất |
| Large v3 Turbo | 1,6 GB | Gần bằng Large v3 nhưng nhanh hơn |

Chưa chọn gì thì Vidora dùng **Small**.

Bảng xếp theo chất lượng chứ không theo dung lượng: Large v3 Turbo là bản rút gọn
của Large v3 nên đứng sau, dù nhẹ hơn.

Nếu mạng qua app chậm, mỗi dòng đều có nút **Link trực tiếp** để tải bằng trình tải
của bạn.

## Tạo phụ đề

1. Mở trang **Video → Phụ đề**.
2. Chọn video hoặc file âm thanh.
3. Chọn nguồn là **giọng nói**.
4. Chọn ngôn ngữ, hoặc để **tự dò**.
5. Bấm chạy.

Kết quả có mốc thời gian tới từng từ, nên chỉnh trong Subtitle Workshop rất sát.

## Video dài

Chạy được video nhiều giờ. Nếu bị gián đoạn giữa chừng, chạy lại sẽ tiếp tục từ chỗ
dở chứ không làm lại từ đầu.

## GPU

Có GPU NVIDIA thì nhanh hơn nhiều lần. Không có thì chạy CPU, vẫn ra kết quả nhưng
lâu hơn — model càng lớn càng chênh.

## Chọn model nào

Bắt đầu bằng **Small**. Nếu thấy sai nhiều ở từ chuyên ngành hoặc giọng vùng miền,
lên **Large v3 Turbo**. Chỉ dùng **Large v3** khi máy đủ mạnh và cần chính xác tối đa.

Máy cũ, RAM ít thì **Base** hoặc **Tiny** để lấy bản nháp rồi sửa tay.

## Sau khi tạo xong

- Sửa trong **Subtitle Workshop**: nội dung, thời gian, tách gộp câu, kiểm tra tốc độ đọc
- [Dịch và lồng tiếng](translate-dub.md)
- Xuất SRT, VTT, ASS
