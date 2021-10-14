# Nội dung  chương trình đào tạo Clean Code v2

## Mục tiêu khoá học

Khoá học này dành cho các lập trình 6 tháng đến 18 tháng kinh nghiệm lập trình ứng dụng Java web.
Mục tiêu để cải thiện kỹ năng:
1. Kỹ thuật phân tích thiết kế ứng dụng: sản phẩm vs gia công từng phần, monolithic vs microservice,...
2. Thiết kế và kiểm tra thiết kế CSDL quan hệ: pattern (1:M, M:M, recurise, inherit) vs anti pattern
3. Cấu trúc dự án Java: cấu trúc thư mục, Maven vs Gradle. Chuyển đổi giữa Maven và Gradle.
4. Các quy tắc code sạch để dễ đọc, dễ bảo trì, cộng tác nhóm.
5. Các kỹ thuật lập trình hướng đối tượng: SOLID Pattern và 5 design patterns dễ nhớ, phổ biến.
6. Viết Unit Test
7. Lập trình JPA --> Database

Sinh viên và giảng viên sẽ thực hành qua một dự án xây dựng web site bán hàng hoặc web site đặt vé xem phim.
> Nếu sinh viên muốn thực sự hiểu, nắm vững kỹ thuật clean code thì phải lập trình bài tập, nộp bài đầy đủ

## Cách thức học và thời lượng - thời gian học
- Học trực tuyến. Mỗi buổi 2 tiếng, nghỉ giữa giờ 5 phút. 
- Số buổi học 14
- Có bài tập giao về nhà và có chấm bài tập lập trình.
- Dự án lập trình mỗi cá nhân tự làm.
- Số lượng sinh viên < 12 thì sinh viên có thể thuyết trình bài tập, dự án.
- Số lượng sinh viên > 12 giảng viên chỉ chọn 2 bài tập, dự án tốt nhất để sinh viên thuyết trình.


## Đội ngũ giảng viên - trợ giảng
- Trịnh Minh Cường
- Bùi Văn Hiên
- Lục Thanh Ngọc

## Công nghệ sử dụng
- framework: Spring Boot (sinh viên có thể chọn Quarkus)
- Front End: Thymeleaf hoặc React hoặc Vue (sinh viên tuỳ chọn)
- IDE: VSCode hoặc Intelij. Giảng viên dùng VSCode
- Database: Postgresql + Redis. công cụ DBeaver
- Docker
- API Gateway: Traefik

## Chi tiết từng buổi học

### 01. Clean Code
1. Giới thiệu khoá học học, phương pháp học, yêu cầu đầu ra. *Lãnh đạo công ty sẽ trình bày*
2. 12 quy tắc Clean Code giúp phần mềm dễ bảo trì hơn.
3. What is bad code, What is good code? Why?

**Bài tập:**
- Lập trình mô phỏng chọn đội bóng thi đấu
- Lập trình hàm tính chi phí, vay nợ khi mua trả góp chung cư.

### 02. Phân tích thiết kế nghiệp vụ
1. Những câu hỏi nên đặt ra khi khảo sát yêu cầu khách hàng - người dùng
2. Các phương pháp thu thập yêu cầu. Mẫu tài liệu thu thập yêu cầu.
3. Phân tích - phát triển yêu cầu: đối chiếu, xác nhận với khách hàng làm sao hiệu quả.
4. Vẽ User story - diagram để khách hàng hiểu được ngay họ muốn gì.

**Bài tập:**
Chọn một trong ba đề tài sau
- Thiết kế hệ thống bán vé xem phim trực tuyến như CGV
- Thiết kế hệ thống học trực tuyến
- Thiết kế shop bán hàng

### 03. Phân tích thiết kế nghiệp vụ #2
1. Nhận xét đánh giá bài tập tốt nhất buổi số 2. Những lỗi thường mắc phải
2. User Case - Activity Diagram
3. Vẽ mock up giao diện để phối hợp, kết nối giữa khách hàng và đội lập trình.
4. Tài liệu đặc tả: khi nào là đủ, khi nào là thiếu, khi nào là thừa. Làm sao đảm bảo dặc tả luôn cập nhật nhất.

### 04: Cấu trúc dữ liệu phổ biến trong Java
![](https://i2.wp.com/techvidvan.com/tutorials/wp-content/uploads/sites/2/2020/03/collection-framework-hierarchy-in-java.jpg)
1. List - Map - Set - Queue (xếp theo tần suất sử dụng, các ví dụ căn bản)
2. Phân tích thống kê tập dữ liệu 1000 người các thành phố khác nhau, nghề nghiệp, giới tính, độ tuổi khác nhau. Giảng viên chỉ ví dụ 50% các hàm.

**Bài tập**
- Sinh viên lập trình nốt 50% còn lại.

### 05. Java Stream API và Lambda Expression
1. Tại sao Java Stream và Lambda Expression giúp code clean hơn?
2. Tóm tắt các nhóm hàm chính trong Java Stream API:
   - `Stream.of` tạo stream
   - Chuyển đổi sang cấu trúc dữ liệu khác
   - `.iterate`: duyệt
   - `.collect`: chọn
   - `.map`: ánh xạ
   - `.filter`: lọc, tìm kiếm
   - `.limit`: giới hạn
   - `.groupingBy`: nhóm
   - `.skip`: bỏ qua
   - `.distict`: loại phần tử lặp lại
   - `.sorted`: các phương pháp sort chuẩn, sort theo trường, hàm sort tự viết
   - `.findAny` vs `.findFirst`: tìm
**Bài tập**
- Thực hiện lại bài tập lập trình số 4 bằng Java Stream API


### 06. Tối ưu và đánh giá tốc độ
1. Tại sao cần đo đạc, tốc độ, hiệu năng hàm trong Java?
2. Phân tích trọng số, loại bỏ yếu tố ngoại lai. Tối ưu quá sớm cùng không tốt - Premature optimization is evil
3. Sử dụng Java Microbenchmark Harness để đo tốc độ thực thi.
4. Ví dụ:
   - So sánh tốc độ các phương pháp liệt kế số nguyên tố
   - So sánh tốc độ khi không dùng và dùng Stream API
**Bài tập**

### 07. Thiết kế REST API
> Để học buổi này sinh viên đã phải biết lập trình Spring Boot căn bản

1. Tóm tắt phương thức GET, POST, PUT, DELETE
2. Request vs Response. Header vs Body
3. URL parameters vs body parameters
4. Document REST API sử dụng swagger
5. Quản lý version REST API

### 08. Báo lỗi REST API
1. Ý nghĩa HTTP Status code
2. Trả về thông điệp có ý nghĩa
3. Báo lỗi trong lúc development khác gì với báo lỗi ở production








