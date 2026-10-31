# Menu Media

Mỗi **GIF** (hoặc ảnh) trong thư mục `content/Assets/MenuThemes/` của mod trở thành một **theme menu chính**. Nếu có file âm thanh **cùng tên** đặt cạnh, file đó là nhạc của theme; không có thì phát nhạc menu mặc định của game.

## Thêm theme

1. Giải nén mod và bỏ file vào `content/Assets/MenuThemes/`:
   - `beach.gif` + `beach.mp3` → theme **beach**, có nhạc riêng;
   - `night.png` → theme **night**, dùng nhạc mặc định của game.
2. Nén lại thành ZIP (`manifest.json` phải nằm ở gốc ZIP) rồi import vào Bunny Loader.
3. Trong game: Cài đặt > **Theme menu** để chuyển giữa các theme.

Nền: `.gif`, `.png`, `.jpg`. Âm thanh: `.mp3`, `.ogg`, `.wav`, `.m4a`, `.aac`, `.flac`.

## Kích thước, vị trí và tốc độ GIF

Trong game: **Cài đặt > Mod Configuration > Menu Media** (cũng có trong menu tạm dừng khi đang ở trong thế giới). Có bốn thanh trượt:

| Tùy chọn | Mặc định | Phạm vi |
|---|---|---|
| Kích thước | `115%` | 50% đến 300% |
| Vị trí X | `0 px` | -1000 đến 1000 (âm = sang trái) |
| Vị trí Y | `0 px` | -1000 đến 1000 (âm = lên trên) |
| Tốc độ GIF | `0` | 0 đến 60 fps. `0` = giữ tốc độ gốc của GIF; giá trị khác thì mỗi khung được hiện `1000 / fps` ms. |

Bấm **Apply** là nền menu đổi ngay. **Default** đặt lại về mặc định. Ảnh được phóng to quanh tâm màn hình rồi mới dịch theo X/Y.

Thanh tốc độ chỉ đổi tốc độ phát các khung đã giữ lại. Số khung được giữ quyết định lúc chuẩn bị GIF (`maxFps`, mặc định 15): muốn mượt hơn trên 15 fps, tăng `maxFps` trong `config.json` (tốn bộ nhớ hơn).

## Video

Game không có trình phát video nào để mod dùng, nên mod **không mở trực tiếp MP4/MKV**. Hãy đổi trên máy tính bằng `convert-video.sh` (Linux/macOS) hoặc `convert-video.bat` (Windows), có kèm theo mod (cần ffmpeg):

```
./convert-video.sh my-video.mp4 10 12 480
```

Script tạo `my-video.gif` và, **nếu video có tiếng**, `my-video.mp3`. Bỏ cả hai vào thư mục theme. Video không tiếng chỉ thành GIF và nhạc vẫn là nhạc mặc định của game.

## Lần đầu dùng một GIF

GIF được giải mã ngay trong game, chia thành nhiều lát nhỏ rải qua nhiều khung hình (để menu vẫn mượt), rồi lưu thành PNG trong `cache/` (thư mục dữ liệu của mod, nằm ngoài gói). Lần đầu, nền chỉ hiện khi chuẩn bị xong (game có thể hơi giật); những lần sau mở ngay. Lệnh `/menumedia` cho biết trạng thái từng theme.

## config.json (tùy chọn, đặt trong thư mục theme)

| Khóa | Mặc định | Tác dụng |
|---|---|---|
| `language` | `"auto"` | Ngôn ngữ của lệnh `/menumedia`: `auto`, `en` hoặc `vi`. |
| `fit` | `"cover"` | `cover` phủ kín màn hình và cắt phần thừa, `contain` hiện nguyên ảnh với viền đen, `stretch` kéo giãn. |
| `padLeft`, `padRight`, `padTop`, `padBottom` | `0`, `0.12`, `0`, `0` | Mở rộng vùng vẽ ra ngoài mép màn hình (tỉ lệ so với màn hình). Nếu vẫn còn dải nền gốc của game ở một phía, tăng phía đó (ví dụ `"padRight": 0.2`). |
| `areaScale` | `1` | Nâng cao: nhân kích thước màn hình dùng để vẽ. |
| `maxSide` | `480` | Cạnh dài nhất của một khung (px). |
| `maxFps` | `15` | Giới hạn fps khi phát. GIF nhanh hơn sẽ bị bỏ bớt khung (giữ nguyên thời lượng), nhẹ hơn nhiều. |
| `maxFrames` | `120` | Số khung tối đa mỗi theme; GIF dài hơn sẽ gộp khung nhưng giữ nguyên thời lượng. |
| `maxPixels` | `16000000` | Tổng số pixel các khung của một theme (bộ nhớ). |
| `preloadPerFrame` | `1` | Số khung đưa lên GPU mỗi lượt làm việc. |
| `showStatus` | `true` | Hiện dòng trạng thái ở góc trên bên trái menu khi GIF đang chuẩn bị, hoặc lý do nếu bị lỗi. |
| `budgetMs` | `8` | Số ms làm việc mục tiêu mỗi khung hình khi đang chuẩn bị GIF. Nhỏ hơn = mượt hơn nhưng chuẩn bị lâu hơn. |

## Giới hạn

- Các khung của theme đang dùng vẫn nằm trong bộ nhớ sau khi bạn vào thế giới.
- Nhạc của theme chỉ phát khi theme đó đang được chọn.
