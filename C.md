#### C. Cấu hình docker compose:
Tạo thư mục: ~/myapp
Chuyển vào trong thư mục ~/myapp
Tạo thư mục: ./myweb
<img width="536" height="96" alt="image" src="https://github.com/user-attachments/assets/9891bd90-da0c-4678-b5c6-2f0a5b2b73be" />

Tạo file ./myweb/index.html (với nội dung là thông tin cá nhân của em)
nano docker-compose.yml
Tạo file docker-compose.yml để nó sẽ có các dịch vụ sau:
Khai báo sử dụng nodered/node-red, cổng 1880, dữ liệu nằm tại thư mục ./nodered
Khai báo sử dụng nginx, cổng 80, cấu hình trong file ./nginx/nginx.conf
<img width="788" height="452" alt="image" src="https://github.com/user-attachments/assets/f3022aff-70a8-4d31-b39b-fda1add519fb" />
Mount thư mục ./myweb thành thư mục /myweb trong nginx
Mount file ./nginx/nginx.conf vào file /etc/nginx/nginx.conf trong nginx
Edit file ./nginx/nginx.conf để:
Cấu hình web server cổng 80
server_name là sub-domain (sub-domain tuỳ ý của em)
location / trỏ tới root là thư mục /myweb
location /api dùng proxy_pass trỏ tới 1 (hoặc nhiều) node http_in của nodered
<img width="1066" height="604" alt="image" src="https://github.com/user-attachments/assets/9ebc0fe4-3e3c-4596-9a89-8813d3a7fabe" />

Edit file ./nodered/settings.js để nodered bắt buộc đăng nhập
<img width="1094" height="618" alt="image" src="https://github.com/user-attachments/assets/5e9e149f-a88e-4ae9-b018-299e3da5cf50" />

Chạy docker-compose lần đầu để Node-RED tự sinh file cấu hình trong thư mục ./nodered, sau đó mới tiến hành sửa settings.js và restart lại container

<img width="1086" height="146" alt="image" src="https://github.com/user-attachments/assets/667b804d-c449-4440-9f63-f611c14685c0" />
<img width="924" height="337" alt="image" src="https://github.com/user-attachments/assets/000b3b6b-853c-4182-839b-6a4470cbdcfa" />
<img width="901" height="855" alt="image" src="https://github.com/user-attachments/assets/bb0d4c3c-3f4f-47bf-a830-89613d2529f3" />
