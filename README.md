# UFO Anime – Hai Bạn May Mắn 🛸

Ứng dụng web chơi game UFO anime, chọn ngẫu nhiên **2 nhân vật khác nhau** từ danh sách tối đa **70 người**. Khi UFO hút hai nhân vật lên trời, màn hình hiện lời chúc mừng và hiệu ứng âm thanh.

## Chức năng

- Nhập tên nhanh: mỗi dấu cách hoặc xuống dòng là một nhân vật.
- Tạo danh sách mới hoặc thêm vào danh sách hiện tại.
- Hoạt cảnh UFO, nhân vật anime, hiệu ứng hút lên trời.
- Âm thanh, lời chúc mừng, chế độ toàn màn hình.
- Lưu tên bằng `localStorage` trên thiết bị.
- PWA hỗ trợ cài đặt và chơi offline sau lần truy cập đầu tiên.

## Chạy trên máy tính

Có thể mở `index.html` trực tiếp trong trình duyệt để chơi. Để thử **cài đặt PWA** và service worker, cần chạy qua localhost:

```bash
python -m http.server 8080
```

Sau đó mở `http://localhost:8080`.

## Đưa lên GitHub Pages

1. Tạo repository mới trên GitHub, ví dụ `ufo-anime-game`.
2. Giải nén dự án này và tải **toàn bộ nội dung** lên thư mục gốc repository, bao gồm `.github/workflows/deploy.yml`.
3. Trong **Settings → Pages → Build and deployment**, chọn **Source: GitHub Actions**.
4. Đẩy thay đổi lên nhánh `main` (hoặc bấm **Actions → Deploy GitHub Pages → Run workflow**).
5. Khi workflow thành công, mở `https://TEN-TAI-KHOAN.github.io/ufo-anime-game/` (thay tên tài khoản và repository thực tế).

> Nếu repository dùng nhánh khác `main`, đổi tên nhánh trong `.github/workflows/deploy.yml`.

## Ghi chú kỹ thuật

Ứng dụng dùng HTML, CSS và JavaScript thuần; không cần npm, backend hoặc API. Phối cảnh game là **đồ họa 3D mô phỏng bằng Canvas**, không phải mô hình 3D thực. Âm thanh trên trình duyệt có thể cần thao tác người dùng trước khi phát. Chế độ offline trên GitHub Pages chỉ sẵn sàng sau khi trang đã được mở thành công và lưu vào bộ nhớ đệm.
