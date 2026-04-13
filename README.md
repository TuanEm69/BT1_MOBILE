# BT1_MOBILE
## Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421
## Lớp: 58KTPM

### Bài tập 01:

### deadline : 23h59 ngày 13 tháng 4 năm 2026.
### Link gửi bài: Tại đây
A. Đăng ký tên miền xịn cho cá nhân:

Đăng ký domain xịn (có thể dùng của tenten, tên miền *.id.vn đang miễn phí cho mọi công dân việt nam <= 23 tuổi, *.io.vn : giá 30k vnđ/năm)

Đăng ký tài khoản cloudflare

Thêm domain đã đăng ký vào trong cloudflare : Nhận 2 dòng namespace

Nhập 2 dòng namespace của cloudflare vào trong trang quản lý DNS record của tên miền đăng ký (vd trên tenten)

<img width="1608" height="833" alt="image" src="https://github.com/user-attachments/assets/8c028ca7-c0e7-4f4f-a180-27cd50d88999" />

B. Cài đặt Ubuntu + Docker

Cài đặt hệ điều hành Ubuntu 24.04.4 LTS

Sử dụng một trong các công cụ để giả lập: HyperV (có sẵn của windows), VirutualBox (Miễn phí), VM_Ware (bản quyền)

Download file iso để cài đặt.

Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows

Ví dụ:

để ssh tới ubuntu ở ip 192.168.100.123, user là admin thì mở CMD trên windows,

gõ lệnh: ssh admin@192.168.100.123

hệ thống sẽ yêu cầu nhập password (chú ý : password sẽ không hiện ra)

sau khi login thành công sẽ thấy màn hình chào hỏi của ubuntu

Tìm hiểu các lệnh cơ bản của ubuntu

Các lệnh cần tìm hiểu:

Liệt kê các file trong thư mục: ls

Tạo thư mục: mkdir nameFolder

Chuyển thư mục làm việc: cd path

Copy file: cp file_nguồn path/file_đích

Thay đổi quyền thao tác file: sudo chmod xxx filename

Edit file: sudo nano tenfile

CTRL+o : lưu nội dung sau khi edit

CTRL+x : thoát edit file

Xem ip của máy ubuntu: ip -4 addr

Cài đặt docker cho Ubuntu

Kiểm tra phiên bản docker vừa cài đặt, kiểm tra phiên bản của docker compose

Cấu hình để docker chạy mà không cần tiền tố sudo

Tìm hiểu tập lệnh của docker và docker compose

Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)
