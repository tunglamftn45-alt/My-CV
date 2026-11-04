# BÁO CÁO KIỂM THỬ PHẦN MỀM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio cá nhân – Nguyễn Tùng Lâm |
| Phiên bản | v1.0.0 |
| Ngày kiểm thử | 05/11/2026 |
| Người thực hiện/đánh giá | QA/QC – rà soát mã nguồn và tài liệu |
| Phạm vi | Website portfolio tĩnh; cấu trúc HTML/CSS, tài liệu và cấu hình triển khai hiện có |
| Phương pháp | Rà soát tĩnh tài liệu, mã nguồn và cấu hình; kiểm tra trực quan ở ba viewport bằng trình duyệt tích hợp VS Code. Chưa đo hiệu năng hoặc chạy Docker trong lần đánh giá này. |
| Môi trường kiểm thử responsive | Windows; trình duyệt tích hợp VS Code (Chrome 150.0.7871.250, Electron 43.8.3); viewport giả lập 390×844, 834×1112 và 1440×900. Đây là giả lập kích thước viewport, không phải thiết bị vật lý. |

> **Quy ước trạng thái:** **Đạt** = có bằng chứng hiện có đáp ứng hạng mục; **Chưa đạt** = phát hiện không đáp ứng yêu cầu; **Cần cải thiện** = chưa có đủ bằng chứng để xác nhận hoặc cần hoàn thiện trước khi bàn giao. Đánh giá dựa trên rà soát tĩnh, không thay thế kiểm thử nghiệm thu trên môi trường chạy.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các khu vực nội dung và điều hướng nội bộ có trong HTML; liên kết dự án và mạng xã hội vẫn là placeholder. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Đã kiểm tra trực quan ở ba viewport và không phát hiện tràn ngang; chưa kiểm thử trên thiết bị vật lý hoặc các trình duyệt khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Website tĩnh, không có bước build hay phụ thuộc JavaScript; chưa chạy thử trên máy chủ, kiểm tra lỗi tải tài nguyên hoặc đo hiệu năng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy xử lý dữ liệu người dùng phía máy chủ; cần rà soát thủ công các liên kết, cấu hình máy chủ và xác nhận qua kiểm tra triển khai. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Cần cải thiện | Có cấu trúc HTML/CSS và README/Dockerfile/release note; chưa chạy validator hoặc rà soát toàn diện chất lượng mã. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã có ảnh responsive tại ba viewport; chưa xác nhận Docker build/run hoặc kiểm thử toàn diện các chức năng. |

## 3. Nội dung chi tiết

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Trang có các khu vực giới thiệu, kỹ năng, dự án và liên hệ | Đạt | Các section `about`, `skills`, `projects`, `contact` có trong `index.html`. |
| Điều hướng nội bộ tới các khu vực và quay về đầu trang | Đạt | Menu và các nút dùng anchor `#about`, `#skills`, `#projects`, `#contact`; có liên kết `#top`. Chưa xác nhận bằng thao tác trình duyệt. |
| Hiển thị thông tin liên hệ email | Đạt | Có liên kết `mailto:tunglamftn45@gmail.com` trong `index.html`. |
| Liên kết xem chi tiết dự án mở đúng đích | Chưa đạt | Các nút dự án hiện dùng `href="#"`; chưa dẫn tới trang hoặc repository dự án thực tế. |
| Liên kết hồ sơ mạng xã hội mở đúng đích | Chưa đạt | Các liên kết GitHub/Facebook hiện dùng `href="#"` trong khi hiển thị tên hồ sơ. Cần thay bằng URL chính xác và kiểm tra đích. |
| Nội dung và nhãn giao diện nhất quán, sẵn sàng xuất bản | Cần cải thiện | Một số nội dung dự án được mô tả là mẫu trong README; cần xác nhận tính chính xác, bản quyền hình ảnh/nội dung và thông tin cá nhân trước khi bàn giao. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục responsive trên mobile (390×844) | Đạt | Đã kiểm tra trực quan bằng trình duyệt tích hợp VS Code; không phát hiện tràn ngang (`scrollWidth` = `clientWidth` = 375 CSS px). Ảnh: [responsive-mobile.png](./screenshots/responsive-mobile.png). |
| Bố cục responsive trên tablet (834×1112) | Đạt | Đã kiểm tra trực quan; không phát hiện tràn ngang (`scrollWidth` = `clientWidth` = 819 CSS px). Ảnh: [responsive-tablet.png](./screenshots/responsive-tablet.png). |
| Bố cục responsive trên desktop (1440×900) | Đạt | Đã kiểm tra trực quan; không phát hiện tràn ngang (`scrollWidth` = `clientWidth` = 1425 CSS px). Ảnh: [responsive-desktop.png](./screenshots/responsive-desktop.png). |
| Quy tắc breakpoint responsive được khai báo | Đạt | `assets/css/styles.css` dùng layout một cột mặc định và breakpoint tại `768px`, `1280px`; đã đối chiếu cùng kết quả viewport ở trên. |
| Có chỉ báo focus cho thao tác bàn phím | Đạt | CSS định nghĩa `:focus-visible` với outline dễ nhận biết. Chưa kiểm thử thao tác bằng bàn phím trên trình duyệt. |
| Tôn trọng thiết lập giảm chuyển động | Đạt | CSS có media query `prefers-reduced-motion: reduce`. Chưa xác nhận hành vi trên hệ điều hành/trình duyệt thực tế. |
| Nội dung và điều hướng trong viewport đã chụp | Đạt | Đã rà soát phần đầu trang ở ba viewport. Chưa đánh giá toàn bộ nội dung dài, tương phản màu, thứ tự focus và khả năng đọc bằng công cụ chuyên dụng. |
| Tương thích trên các trình duyệt mục tiêu | Cần cải thiện | Chưa có ma trận kiểm thử Chrome, Edge, Firefox, Safari hoặc thiết bị di động. |
| Văn bản thay thế cho ảnh chính | Đạt | Ảnh đại diện có thuộc tính `alt`; ảnh dự án minh họa cũng có `alt` trong HTML. Cần đánh giá nội dung alt sau khi cập nhật ảnh thật. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có thể phục vụ dưới dạng website tĩnh, không yêu cầu backend | Đạt | README mô tả trang HTML/CSS tĩnh; Dockerfile sao chép HTML và assets vào Nginx. Đây là xác nhận theo cấu hình, chưa phải kết quả chạy. |
| Tài nguyên CSS và ảnh được tham chiếu trong trang | Cần cải thiện | HTML tham chiếu `./assets/css/styles.css` và `./assets/img/avatar.jpg`; chưa kiểm tra yêu cầu HTTP hoặc tải trang thực tế để xác nhận không có lỗi 404. |
| Hành vi khi liên kết ngoài hoặc tài nguyên không khả dụng | Cần cải thiện | Chưa có kiểm thử mất kết nối, lỗi tải ảnh, hoặc đích liên kết không tồn tại; các liên kết `#` cần được xử lý như phát hiện ở mục 3.1. |
| Có sử dụng JavaScript hoặc phụ thuộc runtime cần quản lý | Đạt | Theo README và mã nguồn được rà soát, dự án không cần JavaScript, Node.js hay gói phụ thuộc để hiển thị nội dung hiện tại. |
| Hiệu năng tải trang cơ bản | Cần cải thiện | Chưa đo thời gian tải, kích thước tài nguyên, chỉ số Lighthouse/Core Web Vitals hoặc hiệu năng trên mạng chậm/thiết bị cấu hình thấp. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có biểu mẫu hoặc xử lý dữ liệu nhạy cảm phía máy chủ | Đạt | Trong phạm vi mã nguồn tĩnh được rà soát, không thấy backend, cơ sở dữ liệu hoặc biểu mẫu gửi dữ liệu. Điều này không thay thế kiểm tra bảo mật triển khai. |
| Không đưa bí mật/credential vào cấu hình được kiểm tra | Cần cải thiện | Chưa thực hiện quét bí mật toàn repository; cần chạy công cụ phù hợp và xác nhận trước khi phát hành. |
| Liên kết ngoài và thông tin liên hệ là chính xác, an toàn | Cần cải thiện | Liên kết mạng xã hội đang dùng `href="#"`; cần cập nhật, kiểm tra URL và xác nhận thông tin được phép công khai. |
| Cấu hình máy chủ web và container | Cần cải thiện | `Dockerfile` dùng `nginx:alpine`, sao chép nội dung tĩnh và mở cổng 80. Chưa kiểm tra cấu hình header bảo mật, phiên bản image được pin, hoặc cấu hình khi triển khai thực tế. |
| Thu thập, lưu trữ dữ liệu người dùng | Đạt | Không thấy cơ chế lưu trữ dữ liệu người dùng trong trang tĩnh hiện tại. Nếu bổ sung biểu mẫu/analytics, cần đánh giá quyền riêng tư và thông báo phù hợp. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Tách cấu trúc nội dung và giao diện | Đạt | HTML nằm trong `index.html`, CSS trong `assets/css/styles.css`; ảnh nằm dưới `assets/img/`. |
| Tài liệu cài đặt, chạy và triển khai | Đạt | `README.md` có hướng dẫn chạy trực tiếp, dùng Live Server và Docker. Cần đối chiếu hướng dẫn với kết quả chạy thực tế trước bàn giao. |
| Tài liệu phiên bản và hạn chế đã biết | Đạt | Có `docs/RELEASENOTE.md`, ghi phiên bản v1.0.0, chức năng và hạn chế hiện tại. |
| Cấu trúc và chất lượng HTML/CSS được xác thực tự động | Cần cải thiện | Chưa chạy HTML/CSS validator, formatter hoặc accessibility checker; cần bổ sung kết quả nếu quy trình bàn giao yêu cầu. |
| Tính nhất quán giữa tài liệu và nội dung hiện tại | Cần cải thiện | README mô tả một số hồ sơ/dự án mẫu; nội dung liên hệ trong trang có thể thay đổi. Cần rà soát cập nhật tài liệu sau khi chốt nội dung. |
| Các thay đổi có tài liệu theo dõi | Đạt | Có `docs/AI_LOG.md` để ghi lại các thay đổi lớn; cần duy trì cập nhật cho những thay đổi tiếp theo. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có cấu hình triển khai container | Đạt | Có `Dockerfile` dùng Nginx để phục vụ trang tĩnh. Chưa chạy `docker build` hoặc container để xác nhận. |
| Có hướng dẫn chạy thử và triển khai | Đạt | `README.md` mô tả lệnh Docker và cách mở trang trực tiếp/Live Server. |
| Build và truy cập ứng dụng sau triển khai | Cần cải thiện | Chưa có log build, kết quả HTTP hoặc xác nhận trang mở thành công trên container/máy chủ. |
| Kiểm thử chức năng và giao diện trên môi trường chạy | Cần cải thiện | Đã kiểm tra responsive trên trình duyệt tích hợp; các chức năng/luồng khác và kiểm thử trên thiết bị vật lý vẫn chưa được thực thi đầy đủ. |
| Minh chứng kiểm thử responsive có thể đối chiếu | Đạt | Đã lưu ảnh chụp viewport trong `docs/screenshots/`: [mobile](./screenshots/responsive-mobile.png), [tablet](./screenshots/responsive-tablet.png), [desktop](./screenshots/responsive-desktop.png). |
| Minh chứng triển khai và kiểm thử toàn diện | Cần cải thiện | Chưa có log Docker build/run, ma trận trình duyệt hoặc kết quả kiểm thử các chức năng khác. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm có phạm vi phù hợp với một portfolio cá nhân dạng website tĩnh. Cấu trúc nội dung cơ bản, stylesheet responsive, tài liệu hướng dẫn và cấu hình Docker đã có. Tuy nhiên, kết quả báo cáo hiện dựa trên rà soát tĩnh; chưa có bằng chứng chạy thử trên trình duyệt hoặc kiểm chứng triển khai. Một số liên kết quan trọng còn là placeholder, do đó **chưa khuyến nghị bàn giao/xuất bản chính thức cho tới khi hoàn tất các việc cần làm dưới đây**.

### Vấn đề cần khắc phục trước khi bàn giao

1. Thay các `href="#"` cho liên kết dự án và mạng xã hội bằng URL thật; kiểm tra từng đích đến và cập nhật văn bản nếu cần.
2. Xác nhận nội dung, ảnh đại diện, ảnh dự án và thông tin liên hệ được phép công khai, chính xác và phù hợp mục đích sử dụng.
3. Mở rộng kiểm thử trên trình duyệt/thiết bị mục tiêu; kiểm tra menu, anchor, liên kết email, focus bằng bàn phím, giảm chuyển động, lỗi console và lỗi tải tài nguyên. Ba viewport responsive cơ bản đã được chụp minh chứng, nhưng chưa thay thế kiểm thử thiết bị vật lý.
4. Thực hiện kiểm thử tương thích trên các trình duyệt mục tiêu; ghi rõ phiên bản trình duyệt, thiết bị/viewport và kết quả.
5. Chạy thử quy trình Docker theo README (`docker build`, `docker run`), kiểm tra trang trả về đúng nội dung và không có lỗi 404.
6. Bổ sung minh chứng cho các lượt kiểm thử còn thiếu (log chạy Docker, kiểm thử chức năng và ma trận trình duyệt) bên cạnh ảnh responsive hiện có trong `docs/screenshots/`.
7. Thực hiện rà soát bảo mật và chất lượng phù hợp quy trình bàn giao, bao gồm quét bí mật, kiểm tra cấu hình triển khai, HTML/CSS và khả năng truy cập.

### Kết luận

**Trạng thái đề xuất: Cần cải thiện trước khi bàn giao chính thức.** Sau khi hoàn tất các mục ưu tiên trên, cập nhật trạng thái checklist và đính kèm minh chứng để có thể đưa ra kết luận nghiệm thu cuối cùng.