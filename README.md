# E-commerce UI Improvement

## 1. Giới thiệu

Em thực hiện cải tiến khu vực danh sách và thẻ sản phẩm của website bán gói vật phẩm Hành Trình AFK trên Pluto Mall. Giao diện tập trung vào hình ảnh, tên gói, phần thưởng, giá bán và nút “Chọn gói”. Em chia sản phẩm thành từng nhóm để người xem dễ tìm và so sánh.

Đây là bài tập giao diện tĩnh. Nút “Chọn gói” chỉ minh họa, không thực hiện giao dịch. Dự án chưa có đăng nhập, giỏ hàng, thanh toán, backend hoặc cơ sở dữ liệu.

## 2. Website tham khảo

- **Tên website:** Pluto Mall – Hành Trình AFK.
- **URL:** https://plutomall.travelletgames.vn/hanhtrinhafk/vn
- **Khu vực đã khảo sát:** Danh sách gói vật phẩm, hình ảnh sản phẩm, tên gói, giá bán, thông tin thưởng thêm và khu vực thao tác mua gói.
- Hình ảnh và logo lấy từ ảnh chụp website được cung cấp trong quá trình làm bài, dùng để minh họa học tập. Quyền đối với các hình ảnh, logo thuộc chủ sở hữu tương ứng.
- Giá và phần thưởng được nhập theo ảnh tham khảo, không phải dữ liệu cập nhật trực tiếp từ cửa hàng.

## 3. Chức năng

- Hiển thị 20 thẻ sản phẩm với hình ảnh, tên, phần thưởng, giá bằng VND và nút “Chọn gói”.
- Chia danh mục thành 5 nhóm: Pha Lê Rồng (6 gói), Gói thể lực (2 gói), Sách du ký (4 gói), Nguyệt San Esperia (2 gói), Gói đặc biệt (6 gói).
- Nhấn vào tên danh mục để chuyển đến nhóm sản phẩm tương ứng trong cùng trang.
- Mở và đóng nội dung “Xem chi tiết” bằng HTML `details` và `summary`.
- Bố cục hỗ trợ nhiều kích thước màn hình: 5 cột từ 1400 px; 4 cột từ 1100–1399 px; 3 cột từ 800–1099 px; 2 cột từ 360–799 px; 1 cột dưới 360 px.
- Có mô tả ảnh, liên kết bỏ qua phần đầu trang và trạng thái focus hỗ trợ thao tác bằng bàn phím.

## 4. Công nghệ

- HTML5: tạo cấu trúc và nội dung trang.
- CSS3: định dạng chữ, màu sắc, thẻ sản phẩm và bố cục thích ứng.
- Phông chữ Noto được lưu trong thư mục `fonts`; thông tin giấy phép nằm trong `fonts/LICENSE.txt`.
- Không dùng JavaScript, framework, backend hoặc cơ sở dữ liệu.

### Cấu trúc thư mục

| Đường dẫn | Nội dung |
| --- | --- |
| `index.html` | Trang giao diện chính |
| `css/style.css` | Toàn bộ CSS của trang |
| `images/` | Ảnh tham khảo sản phẩm và logo AFK |
| `fonts/` | Phông chữ tiếng Việt và giấy phép |
| `README.md` | Giới thiệu dự án, hướng dẫn chạy và các cải tiến |
| `AI_USAGE.md` | Nhật ký sử dụng AI và phần em tìm hiểu |

## 5. Cách chạy

1. Tải mã nguồn và giải nén nếu tải dưới dạng ZIP.
2. Giữ nguyên cấu trúc thư mục, mở file `index.html` bằng Chrome, Edge hoặc Firefox.
3. Không cần cài thư viện hoặc chạy máy chủ.
4. Để kiểm tra giao diện nhỏ, mở DevTools và chọn chế độ thiết bị; có thể kiểm tra ở chiều rộng 390 px, 768 px và từ 1200 px.

Khi kiểm tra, cần xem ảnh và phông chữ có tải đủ không, chữ tiếng Việt có đúng dấu không, thẻ sản phẩm có tràn ngang không, liên kết danh mục có chuyển đúng nhóm không và “Xem chi tiết” có mở/đóng được không.

## 6. Cải tiến đã thực hiện

| Vấn đề ban đầu hoặc ở bản giao diện đầu tiên | Thay đổi đã thực hiện |
| --- | --- |
| Các gói khác nhau nằm chung trong danh sách, khó tìm theo nhu cầu | Tổ chức lại danh mục và tách Gói thể lực, Sách du ký thành các khu vực riêng có tiêu đề |
| Hình minh họa chưa giống sản phẩm trên website | Thay bằng ảnh chụp được cung cấp, dùng CSS để hiển thị vùng ảnh của từng sản phẩm |
| Giá bán và thao tác lựa chọn chưa được phân biệt rõ trong phương án ban đầu | Hiển thị giá thành một dòng riêng và đặt nút “Chọn gói” bên dưới |
| Chữ tiếng Việt bị giãn hoặc tách bất thường, như “Tiế p bước hành trình.” | Sửa nội dung thành “Tiếp bước hành trình.”, dùng phông Noto, điều chỉnh khoảng cách chữ và chiều cao dòng |
| Tên sản phẩm còn chứa “mẫu 1”, “mẫu 2”, “mẫu trong ảnh” hoặc hậu tố giá | Bỏ phần mô tả tạm; sửa thành “Gói Trưởng Thành Mùa Giải Giai Đoạn 1” và “Gói Thử Thách Huyền Thoại” theo nội dung em yêu cầu |
| Có các đoạn chú thích làm rối phần chính | Bỏ dòng “Giao diện bài tập”, dòng “20 gói từ ảnh tham khảo · Giá bằng VND” và đoạn lưu ý dưới danh sách; đưa thông tin phạm vi minh họa vào tài liệu dự án |
| Logo chưa phù hợp và chữ trên nút chưa cân đối | Bổ sung logo AFK, căn giữa chữ “Chọn gói” theo cả hai chiều |
| Danh sách cần phù hợp với màn hình nhỏ | Dùng CSS Grid và media query để thay đổi số cột theo chiều rộng màn hình |

**Kiểm tra trong quá trình xây dựng:** Em xem các bản giao diện và ảnh chụp, phát hiện vấn đề về chữ, hình ảnh, tên gói, danh mục và yêu cầu điều chỉnh. AI hỗ trợ kiểm tra giao diện trên trình duyệt ở bố cục máy tính và các khung mô phỏng 768 px, 390 px; kiểm tra thao tác mở/đóng chi tiết. Chưa kiểm tra trên điện thoại thật. Sau khi chuyển CSS vào thư mục riêng, đường dẫn CSS, ảnh và phông chữ được kiểm tra lại trong mã nguồn.

Nhãn “Thêm 5%” trong ảnh thể hiện vật phẩm thưởng thêm, không được dùng làm tỷ lệ giảm giá.

## 7. Hỗ trợ từ AI

Em sử dụng ChatGPT để đề xuất bố cục, tạo mã HTML/CSS, giải thích các thành phần và hỗ trợ sửa lỗi. AI cũng hỗ trợ tổ chức thư mục, soạn README và nhật ký sử dụng AI.

Em cung cấp website, ảnh sản phẩm và các yêu cầu chỉnh sửa cụ thể. Em phát hiện chữ bị lỗi khoảng cách, hình ảnh chưa phù hợp, danh mục chưa tách rõ, tên sản phẩm còn chữ “mẫu” và nút chưa căn giữa. Từ đó, em yêu cầu AI sửa lại và đối chiếu nội dung với ảnh tham khảo. Em không tự viết toàn bộ mã nguồn; các phần AI hỗ trợ được ghi trong `AI_USAGE.md`.


### Bổ sung header và footer

Bổ sung ảnh nhân vật và banner phần thưởng từ ảnh tham khảo vào đầu trang; tạo footer nền tối gồm nhận diện, thông tin giao diện và người thực hiện. Dùng CSS để hiển thị vùng ảnh phù hợp. Footer không đưa ra cam kết thanh toán hay chứng nhận PCI DSS cho trang minh họa. Header và footer chuyển bố cục ở màn hình nhỏ.


### Cân đối thẻ sản phẩm và nội dung bổ sung

Ảnh gói được thống nhất tỷ lệ 274:154; tên, phần thưởng và giá căn giữa. Thẻ hiển thị 5 cột ở màn hình rộng và giảm số cột theo màn hình. Bổ sung “Chọn gói theo nhu cầu”, hướng dẫn 3 bước và câu hỏi thường gặp. Các liên kết nhóm và FAQ hoạt động bằng HTML/CSS; không bổ sung thanh toán thật.

Nguồn tham khảo bổ sung (16/11/2026):
- [Codashop Việt Nam](https://www.codashop.com/vi-vn/): tham khảo cách phân nhóm nội dung và khu vực khám phá.
- [VNGGames Shop](https://shop.vnggames.com/vn/instruction): tham khảo việc bố trí hướng dẫn, hỗ trợ và câu hỏi thường gặp.

Đây là các ý tưởng được điều chỉnh cho bài AFK, không phải sao chép hệ thống nạp hoặc khuyến mãi của các website khác.


### Thông tin nhân vật

Theo yêu cầu bổ sung, đầu trang có mẫu trạng thái đăng nhập thành công hiển thị nhân vật Hayate và Server S55 theo ảnh tham khảo. Dữ liệu được ghi trực tiếp trong HTML, có nhãn minh họa; chưa có đăng nhập, xác thực hay truy xuất nhân vật từ máy chủ.


### Hoàn thiện phần nhìn

Bổ sung ảnh sản phẩm thực tế vào ba thẻ khám phá, khôi phục ảnh giới thiệu trên điện thoại, điều chỉnh vùng hiển thị ảnh nhân vật trong header. Thay các ô phẳng bằng thẻ có ảnh, màu nền nhẹ, viền và hiệu ứng khi trỏ chuột. Phần hướng dẫn có biểu tượng SVG, số thứ tự và bố cục riêng. Viết lại lời giới thiệu cho hấp dẫn hơn, giữ nguyên giá và vật phẩm thưởng. Các biểu tượng SVG là mã giao diện, không dùng thư viện ngoài.
