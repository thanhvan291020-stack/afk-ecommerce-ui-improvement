# AI Usage Log

## 1. Công cụ AI

- **Tên công cụ:** ChatGPT.
- **Phạm vi:** Hỗ trợ thực hiện bài tập cải tiến giao diện Hành Trình AFK bằng HTML5 và CSS3.

## 2. Mục đích sử dụng

Em dùng AI để đề xuất cách trình bày danh sách sản phẩm, tạo mã HTML/CSS, giải thích mã, chỉnh giao diện theo ảnh tham khảo, sửa lỗi chữ và hỗ trợ viết tài liệu dự án.

## 3. Prompt đã sử dụng

Các prompt chính dưới đây được rút gọn từ yêu cầu em đã gửi, giữ nguyên ý chính:

1. “Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3. Có tiêu đề, khu vực sản phẩm, tối thiểu 4 sản phẩm, mỗi sản phẩm có hình ảnh, tên, giá và nút thao tác. CSS tách riêng; phù hợp máy tính và điện thoại; không dùng backend hoặc cơ sở dữ liệu.”
2. “Để hình mẫu theo hình website giúp tôi. Phần danh mục sản phẩm tôi muốn có thêm các mục như gói thể lực, sách du ký xếp theo mục riêng.”
3. “Sửa chữ ‘Tiế p bước hành trình.’; các chữ phải đúng chính tả, cách dòng đúng; sửa logo AFK; chữ ‘Chọn gói’ nằm ngay giữa.”
4. “Bỏ chữ ‘Giao diện bài tập’, ‘20 gói từ ảnh tham khảo · Giá bằng VND’ và đoạn ‘Lưu ý: Giá và phần thưởng theo ảnh bạn cung cấp…’.”
5. “Bỏ chữ ‘mẫu trong ảnh’, ‘mẫu 1’, các chữ như ‘— gói’ ở đằng sau; sửa thành ‘Gói Trưởng Thành Mùa Giải Giai Đoạn 1’ và ‘Gói Thử Thách Huyền Thoại’.”
6. “Chuẩn bị bài để đặt tên repository, đề xuất cấu trúc thư mục, viết README.md và AI_USAGE.md theo các mục giảng viên yêu cầu.”

## 4. Kết quả AI đề xuất

- Trang HTML/CSS tĩnh có 20 sản phẩm từ ảnh tham khảo, chia thành 5 nhóm.
- Mỗi thẻ gồm ảnh, tên, phần thưởng, giá, khu vực xem chi tiết và nút “Chọn gói”.
- Điều hướng đến các nhóm bằng liên kết nội trang.
- Dùng CSS Grid và media query để hiển thị 4, 2 hoặc 1 cột tùy chiều rộng màn hình.
- Dùng `details`/`summary` để mở và đóng thông tin mà không cần JavaScript.
- Dùng phông Noto lưu cục bộ để cải thiện hiển thị tiếng Việt.
- Chuẩn bị thư mục `css`, `images`, `fonts` và hai tài liệu Markdown.

## 5. Kiểm tra và điều chỉnh

Em xem các phiên bản giao diện và phát hiện các điểm cần sửa:

| Điểm em phát hiện hoặc yêu cầu | Điều chỉnh có AI hỗ trợ |
| --- | --- |
| Chữ bị lỗi khoảng cách hoặc tách dấu | Sửa văn bản tiếng Việt, dùng phông Noto và điều chỉnh `letter-spacing`, `word-spacing`, `line-height` |
| Hình minh họa chưa đúng website | Dùng ảnh chụp em cung cấp, hiển thị vùng hình tương ứng với từng sản phẩm |
| Sản phẩm chưa được nhóm rõ ràng | Chia thành Pha Lê Rồng, Gói thể lực, Sách du ký, Nguyệt San Esperia và Gói đặc biệt |
| Tên gói có chữ tạm như “mẫu 1”, “mẫu 2” | Bỏ hậu tố tạm và chỉnh tên gói theo yêu cầu |
| Phần chính có chú thích không cần thiết | Bỏ các dòng em đã chỉ ra, giữ thông tin giới hạn chức năng trong README |
| Chữ trên nút lệch và logo chưa phù hợp | Căn giữa chữ bằng Flexbox và bổ sung logo AFK |

Em không giữ toàn bộ bản AI tạo đầu tiên mà yêu cầu sửa theo những điểm trên. Trong quá trình xây dựng, AI đã hỗ trợ kiểm tra bố cục máy tính, khung mô phỏng 768 px và 390 px, cùng thao tác mở/đóng chi tiết. Đây chưa phải kiểm thử trên điện thoại thật. Việc đưa CSS sang thư mục `css` có kèm kiểm tra đường dẫn tài nguyên.

Nút “Chọn gói” chỉ là phần giao diện. Em không dùng chức năng thanh toán, đăng nhập, backend hay cơ sở dữ liệu. Giá và phần thưởng dựa trên ảnh tham khảo, không có kết nối đồng bộ dữ liệu cửa hàng.

## 6. Phần em hiểu và có thể giải thích

| Thành phần | Vai trò trong bài |
| --- | --- |
| `header`, `main`, `footer` | Chia trang thành phần đầu, nội dung chính và chân trang |
| `section`, `article` | Nhóm từng danh mục và thể hiện mỗi thẻ sản phẩm |
| `h1`, `h2`, `h3`, `p` | Tạo tiêu đề theo cấp và các đoạn thông tin sản phẩm |
| `img`, `src`, `alt` | Hiển thị ảnh và cung cấp mô tả thay thế |
| `nav`, `a href="#..."`, `id` | Tạo thanh danh mục liên kết đến đúng khu vực trong trang |
| `details`, `summary` | Mở và đóng thông tin chi tiết bằng HTML |
| `button type="button"` | Tạo nút thao tác; tự nó không thực hiện mua hàng |
| `link rel="stylesheet"` | Kết nối `index.html` với `css/style.css` |
| CSS Grid, `grid-template-columns`, `gap` | Chia cột sản phẩm và tạo khoảng cách giữa các thẻ |
| Flexbox, `justify-content`, `align-items` | Căn giữa chữ “Chọn gói” trong nút |
| `@media` | Thay đổi bố cục theo kích thước màn hình |
| `@font-face`, `font-family`, `line-height` | Nạp phông chữ và điều chỉnh cách hiển thị, khoảng cách dòng |
| `overflow: hidden`, `position`, `width`, `top`, `left` | Giới hạn vùng hiển thị của ảnh chụp để mỗi thẻ chỉ hiện hình sản phẩm tương ứng |
| Đường dẫn `../fonts/` trong CSS | Đi từ thư mục `css` lên thư mục gốc để tìm phông chữ |

Mã nguồn ban đầu và phần lớn thay đổi kỹ thuật do AI hỗ trợ tạo. Em cung cấp yêu cầu, hình tham khảo, nhận xét và quyết định những nội dung cần điều chỉnh. Trước khi trình bày bài, em cần mở mã để đối chiếu và thực hành giải thích từng thành phần trên.


### Bổ sung header và footer

Bổ sung ảnh nhân vật và banner phần thưởng từ ảnh tham khảo vào đầu trang; tạo footer nền tối gồm nhận diện, thông tin giao diện và người thực hiện. Dùng CSS để hiển thị vùng ảnh phù hợp. Footer không đưa ra cam kết thanh toán hay chứng nhận PCI DSS cho trang minh họa. Header và footer chuyển bố cục ở màn hình nhỏ.


### Cập nhật thẻ sản phẩm và nội dung khám phá

Em yêu cầu hình gói nạp cân đối theo ảnh mẫu và tham khảo các trang nạp game khác. AI tham khảo Codashop và VNGGames Shop, điều chỉnh tỷ lệ ảnh, số cột, căn giữa nội dung; bổ sung liên kết chọn gói theo nhu cầu, hướng dẫn và FAQ bằng HTML/CSS. Không thêm giá khuyến mãi, đánh giá hoặc số người mua không có dữ liệu.


### Thông tin nhân vật

Theo yêu cầu bổ sung, đầu trang có mẫu trạng thái đăng nhập thành công hiển thị nhân vật Hayate và Server S55 theo ảnh tham khảo. Dữ liệu được ghi trực tiếp trong HTML, có nhãn minh họa; chưa có đăng nhập, xác thực hay truy xuất nhân vật từ máy chủ.


### Hoàn thiện phần nhìn

Bổ sung ảnh sản phẩm thực tế vào ba thẻ khám phá, khôi phục ảnh giới thiệu trên điện thoại, điều chỉnh vùng hiển thị ảnh nhân vật trong header. Thay các ô phẳng bằng thẻ có ảnh, màu nền nhẹ, viền và hiệu ứng khi trỏ chuột. Phần hướng dẫn có biểu tượng SVG, số thứ tự và bố cục riêng. Viết lại lời giới thiệu cho hấp dẫn hơn, giữ nguyên giá và vật phẩm thưởng. Các biểu tượng SVG là mã giao diện, không dùng thư viện ngoài.
