# Portfolio CV - Nguyễn Tấn Dũng

## 1. Tên dự án

**Portfolio CV cá nhân - Nguyễn Tấn Dũng** là website giới thiệu cá nhân và các dự án tiêu biểu dành cho vị trí Frontend Developer.

## 2. Mô tả

Đây là website portfolio tĩnh, trình bày thông tin giới thiệu, kỹ năng, dự án và cách liên hệ. Giao diện được xây dựng theo hướng mobile-first, có thể xem trên máy tính, máy tính bảng và điện thoại.

Dự án chỉ gồm HTML và CSS, không có backend, cơ sở dữ liệu, bước biên dịch hay thư viện runtime cần cài đặt. Có thể mở trực tiếp bằng trình duyệt, chạy qua máy chủ HTTP cục bộ hoặc dùng Docker với Nginx.

## 3. Chức năng

- Giới thiệu tác giả và vai trò Frontend Developer.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày danh sách kỹ năng và các dự án bằng bố cục co giãn theo kích thước màn hình.
- Hiển thị ảnh đại diện và ảnh minh họa trong thư mục `assets/img/`.
- Cung cấp liên kết email và các mục liên hệ mạng nghề nghiệp.
- Có liên kết quay về đầu trang.
- Hỗ trợ bố cục responsive, điều hướng bằng bàn phím và tùy chọn giảm chuyển động của hệ điều hành.

> Các dự án và một số liên kết mạng xã hội trên trang hiện mang tính giới thiệu/mẫu; xem mục [Cấu hình](#7-cấu-hình) trước khi công khai website.

## 4. Công nghệ

- **HTML5:** cấu trúc và nội dung trang.
- **CSS3:** giao diện, biến CSS, Flexbox, CSS Grid, responsive và hỗ trợ `prefers-reduced-motion`.
- **Trình duyệt web hiện đại:** hiển thị website.
- **Docker và Nginx (tùy chọn):** chạy website tĩnh trong container; không yêu cầu Dockerfile.

## 5. Yêu cầu môi trường

### Chạy trực tiếp hoặc bằng máy chủ cục bộ

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không cần cài Node.js, npm hay thư viện bên thứ ba.
- Python 3 chỉ cần thiết nếu muốn chạy máy chủ HTTP theo hướng dẫn bên dưới.

### Chạy bằng Docker

- Docker Engine trên Linux hoặc Docker Desktop trên Windows/macOS.
- Docker đang chạy và có kết nối Internet lần đầu để tải image `nginx:alpine`.

## 6. Cài đặt

Tải hoặc giải nén mã nguồn vào một thư mục trên máy. Nếu sử dụng Git, thay `<URL-repository>` bằng địa chỉ repository thực tế:

```bash
git clone <URL-repository>
cd <ten-thu-muc-du-an>
```

Sau khi cài đặt, chuyển terminal đến thư mục gốc dự án — thư mục chứa `index.html` và `assets/` — trước khi chạy các lệnh hướng dẫn.

## 7. Cấu hình

Dự án không cần file cấu hình môi trường, khóa API, cơ sở dữ liệu hoặc bước build. Có thể tùy chỉnh như sau:

- Sửa tiêu đề, nội dung, email và liên kết trong `index.html`.
- Thay ảnh trong `assets/img/`; giữ nguyên tên tệp đang được tham chiếu trong HTML hoặc cập nhật đường dẫn tương ứng.
- Điều chỉnh màu sắc, phông chữ, kích thước và bố cục trong `assets/css/styles.css`. Các biến CSS chính nằm trong khối `:root` ở đầu tệp.
- Trước khi phát hành, kiểm tra tên tác giả, nội dung bản quyền, văn bản thay thế của ảnh và đường dẫn ảnh.

Email hiện hiển thị là `dung.fvn2k7@gmail.com`. Liên kết GitHub, LinkedIn và các liên kết xem chi tiết dự án hiện chưa có đích đến thực tế; hãy cập nhật URL phù hợp hoặc bỏ các liên kết mẫu trước khi công khai.

## 8. Chạy thử

### Mở trực tiếp

Trên Windows, macOS hoặc Linux, mở `index.html` bằng trình duyệt. Cách này phù hợp để xem nhanh giao diện. Để kiểm tra qua HTTP hoặc Docker, hãy dùng một trong các cách sau.

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục gốc dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu không có lệnh `py` nhưng đã cài Python, dùng:

```powershell
python -m http.server 8000
```

Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` trong terminal để dừng máy chủ.

### macOS

Mở Terminal, chuyển đến thư mục gốc dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

### Linux

Mở Terminal tại thư mục gốc dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác, chẳng hạn `8080`, rồi truy cập đúng cổng đó.

### Docker với Nginx

Đảm bảo Docker đang chạy và terminal đang ở thư mục gốc dự án. Các lệnh dưới đây dùng image `nginx:alpine`, gắn thư mục dự án ở chế độ chỉ đọc và ánh xạ cổng `8080` trên máy đến cổng `80` trong container. Lần chạy đầu tiên Docker cần tải image từ Internet.

**Windows PowerShell:**

```powershell
docker run --rm --name portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**Windows Command Prompt:**

```cmd
docker run --rm --name portfolio -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux:**

```bash
docker run --rm --name portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Sau khi container khởi động, mở `http://localhost:8080`. Nhấn `Ctrl+C` để dừng và xóa container. Nếu cổng `8080` đã được sử dụng, đổi cổng phía máy trong `-p 8080:80`, ví dụ `-p 8081:80`, rồi mở `http://localhost:8081`.

## 9. Thông tin liên hệ

- **Tác giả:** Nguyễn Tấn Dũng
- **Email:** [dung.fvn2k7@gmail.com](mailto:dung.fvn2k7@gmail.com)
- **GitHub:** cập nhật URL tài khoản thực tế trong `index.html`.
- **LinkedIn:** cập nhật URL hồ sơ thực tế trong `index.html`.
