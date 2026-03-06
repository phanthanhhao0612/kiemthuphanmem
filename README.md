1. Giới thiệu

Bài kiểm thử này sử dụng công cụ Apache JMeter để đánh giá hiệu năng của website VnExpress.
Mục tiêu của kiểm thử là mô phỏng nhiều người dùng truy cập đồng thời để đo lường:
Thời gian phản hồi của website
Khả năng chịu tải
Tỷ lệ lỗi khi có nhiều người truy cập
Website được kiểm thử:
https://vnexpress.net
2. Môi trường kiểm thử
Thành phần	Mô tả
Công cụ	Apache JMeter
Hệ điều hành	Windows
Loại kiểm thử	Load Testing
Giao thức	HTTP / HTTPS
Website kiểm thử	https://vnexpress.net
3. kịch bản kiểm thử 
Thread Group 1 – Kịch bản cơ bản

Mục đích: mô phỏng lượng người dùng nhỏ truy cập trang chủ.

Thuộc tính	Giá trị
Threads (Users)	10
Ramp-up Period	5 giây
Loop Count	5

HTTP Request:

Method	Path
GET	/
Thread Group 2 – Kịch bản tải nặng

Mục đích: mô phỏng lượng truy cập lớn vào website.

Thuộc tính	Giá trị
Threads	50
Ramp-up	30 giây
Loop Count	5

HTTP Requests:

Method	Path
GET	/
GET	/the-gioi
Thread Group 3 – Kịch bản tùy chỉnh

Mục đích: mô phỏng người dùng truy cập nhiều trang khác nhau trong thời gian dài.

Thuộc tính	Giá trị
Threads	20
Duration	60 giây

HTTP Requests:

Method	Path
GET	/kinh-doanh
GET	/the-thao
Bài kiểm thử đã mô phỏng nhiều kịch bản truy cập khác nhau bằng Apache JMeter để đánh giá hiệu năng của website VnExpress.

Kết quả cho thấy website có khả năng xử lý tải tốt với nhiều người dùng truy cập đồng thời và duy trì thời gian phản hồi ổn định.
