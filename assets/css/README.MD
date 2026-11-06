# Portfolio CV - Nguyễn Tấn Dũng

## 1. Tên dự án

**Portfolio CV cá nhân - Nguyễn Tấn Dũng**, giao diện giới thiệu cá nhân dành cho vị trí Frontend Developer.

## 2. Mô tả

Đây là website portfolio tĩnh, trình bày thông tin giới thiệu, kỹ năng, các dự án tiêu biểu và cách liên hệ. Giao diện được xây dựng theo hướng mobile-first, có thể xem trên máy tính, máy tính bảng và điện thoại.

Website chỉ sử dụng HTML và CSS, không có backend, cơ sở dữ liệu hoặc bước biên dịch.

## 3. Chức năng

- Hiển thị phần giới thiệu và vai trò Frontend Developer.
- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày danh sách kỹ năng và các dự án bằng bố cục co giãn theo kích thước màn hình.
- Hiển thị ảnh đại diện và ảnh minh họa dự án trong thư mục `assets/img/`.
- Cung cấp liên kết email và các liên kết mạng nghề nghiệp.
- Hỗ trợ cuộn đến đầu trang từ chân trang.

## 4. Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện, Flexbox, CSS Grid, responsive và các biến CSS.
- Trình duyệt web hiện đại để xem trang.
- Docker và Nginx (tùy chọn): phục vụ website trong môi trường container.

## 5. Yêu cầu môi trường

### Chạy trực tiếp

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Không cần cài Node.js, npm hay thư viện bên thứ ba.

### Chạy bằng máy chủ cục bộ

- Python 3 (tùy chọn), hoặc một máy chủ tĩnh tương đương.

### Chạy bằng Docker

- Docker Engine trên Linux, hoặc Docker Desktop trên Windows/macOS.
- Kết nối Internet lần đầu để tải image `nginx:alpine`.

## 6. Cài đặt

Tải hoặc giải nén mã nguồn dự án vào một thư mục trên máy. Nếu dùng Git, thay URL mẫu bên dưới bằng URL repository thực tế:

```bash
git clone <URL-repository>
cd <ten-thu-muc-du-an>
```

Thư mục gốc của dự án là nơi chứa `index.html` và thư mục `assets/`. Hãy chạy các lệnh bên dưới từ thư mục này.

## 7. Cấu hình

Không cần file cấu hình môi trường hoặc khóa API. Có thể cá nhân hóa website như sau:

- Sửa nội dung, tiêu đề trang, email và liên kết mạng xã hội trong `index.html`.
- Thay ảnh đại diện và ảnh dự án trong `assets/img/`; giữ nguyên tên tệp đang được tham chiếu trong HTML hoặc cập nhật đường dẫn tương ứng.
- Điều chỉnh màu sắc, phông chữ, kích thước và bố cục trong `assets/css/styles.css`. Các biến CSS chính nằm trong khối `:root` ở đầu tệp.
- Trước khi phát hành, kiểm tra lại tên tác giả, nội dung bản quyền và văn bản thay thế của ảnh cho thống nhất.

**Lưu ý:** Email đang hiển thị trên trang là `dung.fvn2k7@gmail.com`. Các liên kết GitHub và LinkedIn hiện là nội dung mẫu (`#` và tên `nguyenvanan`); hãy thay bằng thông tin thật trước khi công khai website.

## 8. Chạy thử

### Mở trực tiếp trên Windows, macOS hoặc Linux

Mở `index.html` bằng trình duyệt. Cách này phù hợp để xem nhanh giao diện; một số tính năng trên trình duyệt có thể hoạt động khác khi chạy qua máy chủ HTTP.

### Windows

Mở PowerShell hoặc Command Prompt tại thư mục gốc dự án, sau đó chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có nhưng đã cài Python, dùng `python -m http.server 8000`. Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` trong cửa sổ lệnh để dừng máy chủ.

### macOS

Mở Terminal, chuyển đến thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

### Linux

Mở Terminal tại thư mục dự án rồi chạy:

```bash
python3 -m http.server 8000
```

Mở `http://localhost:8000` trên trình duyệt. Nhấn `Ctrl+C` để dừng máy chủ.

Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác, chẳng hạn `8080`, rồi truy cập đúng cổng đó.

### Docker (Nginx)

Đảm bảo Docker đang chạy và terminal đang ở thư mục gốc dự án. Lệnh sau gắn mã nguồn chỉ đọc vào Nginx và ánh xạ cổng `8080` của máy đến cổng `80` trong container.

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

Sau khi container khởi động, mở `http://localhost:8080`. Nhấn `Ctrl+C` để dừng và xóa container. Nếu cổng `8080` đã được sử dụng, đổi phần trước dấu `:` trong `-p 8080:80`, ví dụ `-p 8081:80`, rồi mở `http://localhost:8081`.

## 9. Thông tin liên hệ

- **Tác giả:** Nguyễn Tấn Dũng
- **Email:** [dung.fvn2k7@gmail.com](mailto:dung.fvn2k7@gmail.com)
- **GitHub:** cập nhật URL tài khoản GitHub thực tế trong `index.html`.
- **LinkedIn:** cập nhật URL hồ sơ LinkedIn thực tế trong `index.html`.
