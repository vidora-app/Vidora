# Dòng lệnh

Thêm link từ terminal bằng lệnh `vidora`. Việc tải chạy nền, không bắt cửa sổ chính
phải bật lên.

## Cài lệnh

**Cài đặt → Chung → Dòng lệnh (CLI)** → bấm **Cài lệnh CLI**.

Thẻ đó hiện trạng thái, đường dẫn đã cài, và nút cài lại.

| Nền tảng | Cài vào đâu |
| --- | --- |
| Windows | File `vidora.cmd` trong thư mục lệnh của người dùng. **Mở terminal mới** sau khi cài |
| Linux | Bản `.deb` đã có sẵn `/usr/bin/vidora`. Trường hợp khác thì tạo liên kết ở `~/.local/bin/vidora` |
| macOS | Liên kết ở `/usr/local/bin/vidora`, không ghi được thì lùi về `~/.local/bin/vidora` |

Nếu app báo *"đường dẫn tồn tại nhưng không nằm trong PATH"*, thêm thư mục đó vào
PATH rồi mở terminal mới.

## Dùng

```
vidora <url> [tuỳ chọn]
vidora --url <url> [tuỳ chọn]
vidora --help
vidora --version
```

Vidora đang chạy thì link được chuyển vào đó. Chưa chạy thì app tự khởi động, có thể
nằm ở khay hệ thống.

## Tuỳ chọn

| Cờ | Viết tắt | Ý nghĩa |
| --- | --- | --- |
| `<url>` | | Link cần tải, đặt ngay sau lệnh |
| `--url <url>` | `-u` | Cách khác để truyền link |
| `--quality <q>` | `-q` | Video: `best`, `8k`, `4k`, `2k`, `1080`, `720`, `480`, `360`. Audio: `128` hoặc `auto` |
| `--output <dir>` | `-o` | Thư mục lưu cho lần tải này, phải là đường dẫn tuyệt đối |
| `--audio` | `-a` | Chỉ lấy âm thanh |
| `--queue-only` | | Thêm vào hàng đợi, không tải ngay |
| `--target <t>` | `-t` | `auto` (mặc định), `youtube`, `universal` |

## Ví dụ

```bash
vidora "https://www.youtube.com/watch?v=..."
vidora "https://..." -q 1080
vidora "https://..." --audio -q 128
vidora "https://..." --queue-only
vidora "https://..." -o /home/ten/Videos
```
