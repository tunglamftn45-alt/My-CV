# Portfolio cá nhân – Nguyễn Tùng Lâm

Trang portfolio/CV cá nhân giới thiệu thông tin, kỹ năng, một số dự án tiêu biểu và thông tin liên hệ của Nguyễn Tùng Lâm, Frontend Developer.

## Mô tả

Đây là website tĩnh được xây dựng bằng HTML và CSS thuần. Giao diện hỗ trợ nhiều kích thước màn hình, có thể mở trực tiếp bằng trình duyệt hoặc phục vụ bằng máy chủ web tĩnh. Dự án không có backend, cơ sở dữ liệu hay bước biên dịch.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Trình bày các kỹ năng: HTML5, CSS3, Flexbox, Grid, JavaScript ES6+ và Git/GitHub.
- Trưng bày các dự án mẫu: Landing Page, Todo List, Weather Dashboard và blog cá nhân.
- Hiển thị email và các hồ sơ mạng xã hội.
- Điều hướng nhanh đến từng khu vực trên trang và quay lại đầu trang.
- Bố cục responsive, hỗ trợ thao tác bàn phím và thiết lập giảm chuyển động của hệ điều hành.

> Các thẻ dự án và liên kết hồ sơ trong trang hiện là nội dung giới thiệu mẫu; hãy cập nhật nội dung và đích liên kết trong `index.html` cho phù hợp trước khi xuất bản.

## Công nghệ sử dụng

- **HTML5**: cấu trúc và nội dung trang.
- **CSS3**: giao diện, bố cục Flexbox/Grid, responsive và hiệu ứng.
- **Docker + Nginx** (tùy chọn): phục vụ website tĩnh trong container.

Trang hiện không cần thư viện JavaScript, Node.js, trình quản lý gói hay dịch vụ bên ngoài để chạy.

## Yêu cầu môi trường

### Chạy trực tiếp hoặc dùng máy chủ phát triển

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Trình soạn thảo mã nguồn (khuyến nghị Visual Studio Code) nếu muốn chỉnh sửa.
- Git (tùy chọn, chỉ cần khi clone mã nguồn).
- Nếu chạy bằng Live Server: Visual Studio Code và tiện ích mở rộng **Live Server**.

### Chạy bằng Docker

- Docker Desktop trên Windows/macOS, hoặc Docker Engine trên Linux.
- Docker CLI khả dụng trong terminal.

Không cần cài Node.js hoặc cấu hình biến môi trường cho dự án này.

## Cài đặt

### Windows (PowerShell)

Clone mã nguồn:

```powershell
git clone https://github.com/tunglamftn45-alt/My-CV.git
Set-Location My-CV
```

Hoặc tải và giải nén mã nguồn, sau đó mở thư mục dự án trong File Explorer hoặc Visual Studio Code.

### macOS

```bash
git clone https://github.com/tunglamftn45-alt/My-CV.git
cd My-CV
```

Hoặc tải và giải nén mã nguồn bằng Finder.

### Linux

```bash
git clone https://github.com/tunglamftn45-alt/My-CV.git
cd My-CV
```

Hoặc tải và giải nén mã nguồn bằng trình quản lý tệp của môi trường desktop.

Sau khi có mã nguồn, không cần cài thêm gói phụ thuộc. Kiểm tra thư mục có các tệp `index.html`, `assets/css/styles.css` và `assets/img/avatar.jpg`.

## Cấu hình và tùy chỉnh

- **Nội dung trang, dự án và thông tin liên hệ:** chỉnh sửa `index.html`.
- **Màu sắc, phông chữ, khoảng cách và breakpoint responsive:** chỉnh sửa các biến CSS ở đầu `assets/css/styles.css`.
- **Ảnh đại diện:** thay `assets/img/avatar.jpg` hoặc cập nhật đường dẫn ảnh trong `index.html`.
- **Cổng Live Server:** workspace hiện cấu hình cổng `5501` trong `.vscode/settings.json`; có thể đổi trong thiết lập Live Server của VS Code.
- **Docker:** không cần tệp `.env` hay cấu hình riêng. Cổng web trong container là `80`; có thể đổi cổng phía máy tính khi chạy container.

## Chạy thử

### Mở trực tiếp trong trình duyệt

Không cần máy chủ phát triển; mở tệp `index.html` bằng trình duyệt:

- **Windows:** nhấp đúp `index.html` trong File Explorer, hoặc chạy `Start-Process .\index.html` trong PowerShell từ thư mục dự án.
- **macOS:** chạy `open index.html` từ thư mục dự án.
- **Linux:** chạy `xdg-open index.html` từ thư mục dự án.

### Chạy bằng Visual Studio Code Live Server

1. Mở thư mục dự án trong VS Code.
2. Cài tiện ích **Live Server** nếu máy chưa có.
3. Nhấp chuột phải vào `index.html` và chọn **Open with Live Server**.
4. Mở địa chỉ mà tiện ích hiển thị. Với thiết lập workspace hiện tại, địa chỉ thường là `http://127.0.0.1:5501`.

Sau khi chỉnh sửa và lưu HTML/CSS, trình duyệt sẽ tải lại trang. Có thể kiểm tra hiển thị ở các kích thước màn hình khác nhau và thử các liên kết điều hướng, email, cũng như liên kết dự án.

## Chạy bằng Docker

Dockerfile của dự án dùng Nginx để phục vụ trang tĩnh. Lệnh dưới đây dùng được trong PowerShell, Command Prompt, Terminal macOS và Linux:

```bash
docker build -t tung-lam-portfolio .
docker run --rm --name tung-lam-portfolio -p 8080:80 tung-lam-portfolio
```

Mở [http://localhost:8080](http://localhost:8080) để xem trang. Nhấn `Ctrl+C` để dừng container. Nếu cổng `8080` đã được sử dụng, thay `8080` ở phía trái của `-p` bằng một cổng trống khác, ví dụ `8081:80`.

## Thông tin liên hệ

- **Email:** [tunglamftn45@gmail.com](mailto:tunglamftn45@gmail.com)
- **GitHub:** [github.com/tunglamftn45-alt](https://github.com/tunglamftn45-alt)
- **LinkedIn:** linkedin.com/in/nguyentunglam

Portfolio: **Nguyễn Tùng Lâm** · Frontend Developer.
