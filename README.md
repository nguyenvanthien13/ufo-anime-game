# UFO Anime V3 – Hai Bạn May Mắn 🛸

Ứng dụng web tĩnh (PWA), không cần Node.js hoặc npm.

## Chức năng

- Tối đa 70 nhân vật; nhập nhanh bằng dấu cách hoặc xuống dòng.
- Nhân vật anime cùng kích thước, chạy hỗn loạn; UFO hút hai người ngẫu nhiên ở cuối.
- Nhạc khi bắt đầu, âm thanh chúc mừng, bật/tắt tiếng.
- Phóng to toàn màn hình; bấm vào vùng game để bắt đầu hoặc chơi lại.
- Lưu tên trong localStorage; hỗ trợ offline sau khi tải lần đầu qua HTTPS/localhost.

## Chạy thử

Mở `index.html` bằng Chrome/Edge. Để thử PWA trên localhost:

```bash
python -m http.server 8080
```

Mở `http://localhost:8080`.

## Đăng GitHub Pages

1. Tạo repository **Public** trên GitHub, ví dụ `ufo-anime-game`.
2. Tải **nội dung bên trong** thư mục này lên **gốc** repository, giữ cả `.github/workflows/deploy.yml` và `.nojekyll`.
3. Vào **Settings → Pages → Build and deployment → Source → GitHub Actions**. Cần bật Pages trước khi workflow chạy, nếu không bước `configure-pages` có thể báo `Get Pages site failed: Not Found`.
4. Vào **Actions** chạy lại workflow `Deploy GitHub Pages`, hoặc commit lên `main`.
5. Sau khi deploy thành công, mở `https://USERNAME.github.io/ufo-anime-game/`.

> Nếu workflow báo lỗi quyền truy cập, kiểm tra **Settings → Actions → General → Workflow permissions** và chính sách GitHub Pages của tài khoản/tổ chức.

## Cấu trúc

- `index.html`: mã nguồn trò chơi.
- `manifest.webmanifest`: metadata cài PWA.
- `sw.js`: lưu cache để chơi offline.
- `assets/icon.svg`: biểu tượng.
- `.github/workflows/deploy.yml`: triển khai GitHub Pages.
- `.nojekyll`: tắt xử lý Jekyll.
