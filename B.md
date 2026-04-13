#### B. Cài đặt Ubuntu + Docker

Cài đặt hệ điều hành Ubuntu 24.04.4 LTS

Sử dụng một trong các công cụ để giả lập: HyperV (có sẵn của windows), VirutualBox (Miễn phí), VM_Ware (bản quyền)

Download file iso để cài đặt.

<img width="1479" height="884" alt="image" src="https://github.com/user-attachments/assets/ed10fe82-2eac-467f-b1f5-1d22a54a8abe" />

Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows

<img width="1108" height="624" alt="image" src="https://github.com/user-attachments/assets/a977e50f-3e3f-459e-9a85-c05ba45498a7" />

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

<img width="1112" height="631" alt="image" src="https://github.com/user-attachments/assets/f7ea36e9-3e4a-4f51-93cc-cecb95abc7e2" />

Cấu hình để docker chạy mà không cần tiền tố sudo

<img width="1113" height="628" alt="image" src="https://github.com/user-attachments/assets/f1573cf4-4194-4116-8a09-80a2eef6a320" />

Tìm hiểu tập lệnh của docker và docker compose

Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)

00<img width="1110" height="440" alt="image" src="https://github.com/user-attachments/assets/3c470ad4-69f1-47be-b6c9-25e64045f631" />
