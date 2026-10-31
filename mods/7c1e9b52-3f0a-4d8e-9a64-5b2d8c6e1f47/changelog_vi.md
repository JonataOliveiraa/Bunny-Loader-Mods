# Nhật ký thay đổi

## 1.5.0
- Thêm tùy chọn **Tốc độ GIF** (0-60 fps, 0 = giữ tốc độ gốc) trong Cài đặt > Mod Configuration > Menu Media.

## 1.4.0
- Thêm tùy chọn trong game (Cài đặt > Mod Configuration > Menu Media): **Kích thước** (50-300%), **Vị trí X** và **Vị trí Y** (-1000 đến 1000 px), có nhãn tiếng Anh và tiếng Việt. Chúng thay cho `zoom`, `offsetX`, `offsetY` trong `config.json`.

## 1.3.2
- Sửa dải hở ở mép phải: vùng vẽ giờ là màn hình cộng thêm 12% bên phải (`padRight`), ảnh được fit và phóng to trong vùng đó. Thêm các tùy chọn `padLeft`, `padRight`, `padTop`, `padBottom` (tỉ lệ so với màn hình).

## 1.3.1
- Có một dòng trạng thái nhỏ ở góc trên bên trái menu khi GIF đang chuẩn bị/tải, hoặc khi bị lỗi (kèm lý do). Tắt bằng `"showStatus": false`.
- Thêm log (`Menu Media: selected theme ...`) để dễ tìm lỗi.

## 1.3.0
- Giảm lag mạnh với GIF: giới hạn tốc độ phát `maxFps` (mặc định 15, giữ nguyên thời lượng) và chia việc chuẩn bị thành các lát nhỏ rải qua nhiều khung hình (`budgetMs`).
- Ảnh được phóng to 1.15 lần mặc định, căn giữa (`zoom`, thêm `offsetX`/`offsetY` để nhích).
- Cache cũ sẽ được tạo lại một lần.

## 1.2.0
- Tiếng Anh là ngôn ngữ mặc định, thêm bản dịch tiếng Việt (mô tả, changelog, lệnh `/menumedia`).
- Thêm tùy chọn `language` trong `config.json` (`auto`, `en`, `vi`).

## 1.1.0
- Nền giờ nằm TRONG mod, ở `content/Assets/MenuThemes/`: mỗi GIF/ảnh (cùng file âm thanh trùng tên) là một theme menu. Thêm file, nén zip rồi import lại.
- Chọn theme ở Cài đặt > Theme menu; chỉ theme đang chọn mới được chuẩn bị.

## 1.0.0
- Phiên bản đầu (thư mục bên ngoài).
