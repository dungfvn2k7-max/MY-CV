# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Trường thông tin | Nội dung |
|---|---|
| Tên dự án | Portfolio CV cá nhân - Nguyễn Tấn Dũng |
| Phiên bản | v1.0 |
| Ngày kiểm thử | 06/11/2026 |
| Người thực hiện | Chưa cung cấp |
| Người đánh giá | Chưa cung cấp |
| Phạm vi đánh giá | Rà soát mã nguồn HTML/CSS và tài liệu trong repository |
| Môi trường kiểm thử | Chưa ghi nhận trình duyệt, hệ điều hành hoặc thiết bị thực tế |

> **Phạm vi minh chứng:** Báo cáo này dựa trên kiểm tra tĩnh `index.html`, `assets/css/styles.css` và tài liệu hiện có. Chưa thực hiện kiểm thử tương tác trên trình duyệt, đo hiệu năng, quét bảo mật hoặc chạy triển khai Docker. Trạng thái “Đạt” trong các bảng dưới đây chỉ xác nhận phần có thể kiểm chứng từ mã nguồn.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các khu vực và điều hướng chính đã có; liên kết dự án/mạng xã hội còn là placeholder. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Có quy tắc responsive và hỗ trợ focus; chưa kiểm tra trực quan trên thiết bị/trình duyệt, nội dung nhận diện chưa đồng nhất. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Website tĩnh, ít phụ thuộc; chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra lỗi tải tài nguyên. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy xử lý dữ liệu người dùng trong mã nguồn; cấu hình bảo mật ở máy chủ triển khai chưa được cung cấp/kiểm chứng. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | HTML/CSS tách riêng; cần đồng bộ nội dung và rà soát vị trí/định dạng README trước khi bàn giao. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Có thể phục vụ như website tĩnh; chưa có log kiểm thử, ảnh chụp kết quả hoặc xác nhận triển khai thực tế. |

**Quy ước trạng thái:**

- **Đạt:** Có thể xác nhận từ mã nguồn/tài liệu đã rà soát.
- **Chưa đạt:** Có lỗi hoặc yêu cầu quan trọng không đáp ứng được.
- **Cần cải thiện:** Còn rủi ro, nội dung chưa hoàn thiện hoặc chưa có đủ minh chứng để kết luận.

## 3. Chi tiết kiểm tra

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | Đạt | Các section tương ứng có trong `index.html` với ID `about`, `skills`, `projects`, `contact`. |
| Điều hướng nội bộ và nút kêu gọi hành động | Đạt | Các liên kết `#about`, `#skills`, `#projects`, `#contact` khớp với ID section; nút “Xem dự án” và “Liên hệ tôi” trỏ đến khu vực tương ứng. Chưa xác nhận bằng thao tác trình duyệt. |
| Liên kết email | Đạt | Có liên kết `mailto:dung.fvn2k7@gmail.com` trong phần Liên hệ. |
| Liên kết xem chi tiết dự án | Cần cải thiện | Cả bốn thẻ dự án đang dùng `href="#"`; chưa dẫn tới trang hoặc nội dung chi tiết. |
| Liên kết GitHub và LinkedIn | Cần cải thiện | Hai liên kết hiện dùng `href="#"`; thông tin hiển thị `nguyenvanan` chưa phải URL hồ sơ có thể xác minh. |
| Nội dung tính năng của các dự án được mô tả | Cần cải thiện | Thẻ mô tả Todo App và Weather Dashboard nhưng website hiện là trang portfolio tĩnh, không có chức năng ứng dụng tương ứng để thao tác. Cần xác nhận đây là dự án giới thiệu hay chức năng được kỳ vọng. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Bố cục responsive theo breakpoint | Đạt | `styles.css` dùng mobile-first; breakpoint tablet từ 768px và desktop từ 1280px, lưới dự án chuyển lần lượt 1, 2 và 3 cột. Chưa xác nhận ảnh chụp trên từng viewport. |
| Điều hướng và nội dung trên màn hình hẹp | Cần cải thiện | Header và danh sách điều hướng có `flex-wrap`; cần kiểm tra thực tế tại viewport nhỏ để xác nhận không tràn, chồng lấp hoặc khó thao tác. |
| Trạng thái focus và tùy chọn giảm chuyển động | Đạt | CSS có `:focus-visible` và media query `prefers-reduced-motion: reduce`. Chưa kiểm thử bằng bàn phím hoặc thiết lập hệ điều hành. |
| Tính nhất quán về danh tính tác giả | Cần cải thiện | Tiêu đề và nội dung giới thiệu dùng Nguyễn Tấn Dũng, nhưng `alt` ảnh đại diện và bản quyền chân trang ghi Nguyễn Văn An. |
| Đường dẫn tài nguyên hình ảnh | Cần cải thiện | `src` ảnh dự án đang dùng dấu gạch chéo ngược ở một số đường dẫn, trong khi các đường dẫn khác dùng dấu gạch chéo xuôi. Cần chuẩn hóa và xác nhận tải ảnh khi triển khai trên máy chủ. |
| Tương thích trình duyệt | Cần cải thiện | Chưa có kết quả kiểm thử trên Chrome, Edge, Firefox, Safari hoặc thiết bị di động thực tế. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Tải trang tĩnh và mức độ phụ thuộc | Đạt | Trang sử dụng HTML/CSS, không thấy JavaScript, backend hoặc thư viện runtime bên thứ ba trong `index.html`; cấu trúc triển khai tương đối đơn giản. Chưa chạy trên máy chủ để xác nhận. |
| Xử lý tài nguyên không tải được | Cần cải thiện | Chưa có fallback cho ảnh hoặc kiểm tra lỗi tải tài nguyên; cần kiểm tra các ảnh khi chạy qua HTTP và bổ sung phương án thay thế nếu cần. |
| Khả năng phục hồi/lỗi ứng dụng | Cần cải thiện | Không có luồng nghiệp vụ động để đánh giá; chưa kiểm tra phản hồi khi thiếu CSS/ảnh hoặc khi truy cập đường dẫn không tồn tại. |
| Hiệu năng tải trang | Cần cải thiện | Chưa đo thời gian tải, kích thước ảnh, Lighthouse hoặc Web Vitals. Cần đo trên môi trường triển khai dự kiến trước khi bàn giao. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Thu thập và lưu trữ dữ liệu người dùng | Đạt | Trong mã nguồn đã rà soát không thấy biểu mẫu gửi dữ liệu, API, cơ sở dữ liệu hoặc lưu trữ phía trình duyệt. Kết luận giới hạn ở các tệp được kiểm tra. |
| Bí mật và cấu hình nhạy cảm | Đạt | Không thấy khóa API hoặc thông tin xác thực trong `index.html`/`styles.css`; dự án hiện không yêu cầu cấu hình bí mật. |
| Cấu hình HTTPS, header bảo mật và máy chủ | Cần cải thiện | Chưa có cấu hình máy chủ hoặc môi trường triển khai để kiểm tra HTTPS, CSP, `X-Content-Type-Options` và các header phù hợp. |
| Quyền riêng tư và liên kết bên ngoài | Cần cải thiện | Trang cung cấp email và các liên kết mạng xã hội; cần xác nhận nội dung liên hệ được chủ sở hữu cho phép công khai và thay liên kết mẫu trước khi phát hành. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Tách cấu trúc và giao diện | Đạt | `index.html` tham chiếu stylesheet riêng tại `assets/css/styles.css`; ảnh được tổ chức trong `assets/img/`. |
| Ngữ nghĩa HTML và metadata cơ bản | Đạt | Có `lang="vi"`, `meta charset`, viewport, mô tả, tác giả, tiêu đề trang và các vùng `header`, `nav`, `main`, `section`, `footer`. Chưa chạy công cụ kiểm tra HTML/accessibility. |
| Đồng nhất nội dung và văn bản thay thế | Cần cải thiện | Tên tác giả trong chân trang và `alt` ảnh đại diện không khớp tên ở tiêu đề/metadata. Cần rà soát thêm tên dự án và ảnh minh họa để đảm bảo đúng nội dung. |
| README và hướng dẫn bàn giao | Cần cải thiện | README hiện nằm trong `assets/css/README.MD` thay vì thư mục gốc; cần cân nhắc đặt tài liệu hướng dẫn ở vị trí dễ tìm. Cần kiểm tra lại định dạng Markdown và lệnh theo cấu trúc repository thực tế. |
| Tài liệu release note | Đạt | Có `docs/RELEASENOTE.md` ghi phiên bản v1.0, ngày phát hành, chức năng mới và hạn chế đã biết. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng cụ thể |
|---|---|---|
| Có thể phục vụ như website tĩnh | Đạt | Dự án có `index.html` và tài nguyên tĩnh. README hướng dẫn chạy bằng máy chủ HTTP và Docker/Nginx; các hướng dẫn này chưa được thực thi để xác nhận. |
| Triển khai Docker/Nginx | Cần cải thiện | Chưa chạy container hoặc xác nhận ánh xạ volume/cổng; chưa có kết quả kiểm tra URL sau triển khai. |
| Bộ kiểm thử và kiểm thử hồi quy | Cần cải thiện | Chưa thấy test tự động hoặc kịch bản kiểm thử đã chạy. Cần bổ sung checklist chạy tay hoặc pipeline phù hợp phạm vi website tĩnh. |
| Minh chứng kiểm thử | Cần cải thiện | Chưa đính kèm ảnh chụp màn hình, log chạy, kết quả kiểm tra trình duyệt hoặc báo cáo đo hiệu năng. Thư mục `docs/screenshots/` cần được bổ sung minh chứng thực tế nếu dùng cho bàn giao. |
| Thông tin người kiểm thử và môi trường | Cần cải thiện | Chưa có tên người thực hiện/đánh giá, phiên bản trình duyệt, hệ điều hành và thiết bị kiểm thử để tái lập kết quả. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Portfolio đã có cấu trúc nội dung và nền tảng giao diện responsive phù hợp cho một website tĩnh giới thiệu cá nhân. Mã nguồn không có backend hoặc luồng xử lý dữ liệu người dùng trong phạm vi đã rà soát. Tuy nhiên, hiện chưa đủ minh chứng để xác nhận chất lượng vận hành, tương thích trình duyệt, hiệu năng và triển khai thực tế.

**Kết luận:** Chưa nên xác nhận bàn giao cuối cùng cho đến khi hoàn tất các mục cần cải thiện có ảnh hưởng trực tiếp đến trải nghiệm và tính chính xác của thông tin. Báo cáo này là rà soát mã nguồn, không thay thế cho kiểm thử chấp nhận trên môi trường bàn giao.

### Đề xuất trước khi bàn giao

1. Thay toàn bộ liên kết `#` bằng URL hợp lệ hoặc bỏ các mục chưa có đích đến; xác nhận nội dung từng dự án đúng với sản phẩm thực tế.
2. Đồng bộ tên tác giả, thông tin bản quyền và `alt` ảnh; kiểm tra quyền công khai email và hình ảnh.
3. Chuẩn hóa đường dẫn ảnh sang dấu `/`, sau đó xác nhận mọi ảnh tải thành công trên máy chủ HTTP.
4. Chạy kiểm thử giao diện ở các viewport mobile, tablet và desktop; kiểm tra điều hướng bằng chuột và bàn phím trên các trình duyệt mục tiêu.
5. Chạy triển khai thử bằng hướng dẫn HTTP và Docker/Nginx; lưu URL, log, ảnh chụp và kết quả kiểm tra vào thư mục minh chứng.
6. Đo hiệu năng cơ bản và kiểm tra cấu hình bảo mật trên môi trường triển khai dự kiến; ghi rõ môi trường và kết quả để có thể tái lập.
7. Cập nhật người thực hiện, người đánh giá, thiết bị/trình duyệt và ngày hoàn tất kiểm thử trong báo cáo.
