Đồ án Ứng dụng quản lý lịch trình cá nhân, cho phép người dùng nhập liệu bằng ngôn ngữ tự nhiên tiếng Việt. Hệ thống tự động trích xuất thông tin, lưu trữ và nhắc nhở theo thời gian thực.

Thành viên nhóm:  

- Ngô Nguyễn Mai Nghi - 3121410343

- Đặng Ngọc Đoan Trang - 3121410515

## Cấu trúc thư mục

PersonalSchedulerVI/
├── 📄 launcher.py       # File khởi chạy tự động (Chạy file này)
├── 📄 app.py            # Mã nguồn cho main program
├── 📄 nlp.py            # Module NLP
├── 📄 requirements.txt  # Danh sách các thư viện cần thiết
├── 📄 scheduler.db      # Cơ sở dữ liệu SQLite (Có thể xóa, tự sinh ra khi chạy app)
├── 📄 test.py           # Hàm test module NLP với bộ 30 test case 
└── 📄 README.md         # Hướng dẫn sử dụng

## Hướng dẫn Cài đặt & Chạy
Đảm bảo máy tính đã cài Python (phiên bản 3.8 trở lên). Giải nén file PersonalSchedulerVI.zip

Vào cmd cd đến dir vừa giải nén, nhập **python launcher.py**

Sau khi ứng dụng kiểm tra đủ thư viện, giao diện sẽ tự động mở (có thể mất thời gian, mong thầy thông cảm ạ)

### Nếu giao diện không chạy

Chạy file test.py để kiểm tra xem NLP có hoạt động bình thường.

## Hướng dẫn Sử dụng
1. Thêm event
Nhập câu lệnh vào ô trống trên cùng và nhấn "Phân tích & Thêm".

Câu nên tuân theo cấu trúc giới từ + địa chỉ/thời gian và thứ tự thành phần câu thông dụng để đảm bảo chính xác nhất.

!Reminder chỉ hiểu được khi có cấu trúc "báo/nhắc trước/sớm X p/phút/h/giờ/tiếng"

Một số mẫu câu VD để copy:

- Nhắc t họp nhóm lúc 10 giờ sáng mai ở phòng 302, nhắc trc 15 phút

- Đi xem phim với Lan tối thứ 7 tuần sau ở CGV

- Tối nay 8 giờ đi cafe với hội bạn cũ ở Highlands

- Lịch học toán từ 18:00 tới 20:00 tối nay

- Chuyến bay đi Đà Nẵng cất cánh lúc 06:45 ngày 25/11, báo trước 2 tiếng

2. Thao tác trên bảng dữ liệu
   
Sửa/Xóa: Click chuột vào một dòng sự kiện trong bảng, sau đó nhấn nút Sửa hoặc Xóa ở góc dưới.

Làm mới: Nhấn nút Làm mới để tải lại dữ liệu từ Database.

3. Xem Lịch & Xuất File
Nhấn "Xem Lịch" để mở cửa sổ lịch tháng. Ngày có sự kiện sẽ hiện màu đỏ, hôm nay là màu xanh.

Nhấn "Xuất JSON" để sao lưu dữ liệu ra file .json.

## Troubleshooting
1. Lỗi không gõ được tiếng Việt trong ứng dụng?

Run as Administrator với các bộ gõ Unikey/EVKey.

2. Lỗi "No such column: event"

Có thể file database cũ không tương thích. Thử xóa file scheduler.db đi và chạy lại ứng dụng để tạo file .db mới.

3. Calendar không hiển thị hoặc bị lỗi

Đảm bảo cài đủ thư viện calendar và ttkbootstrap.
