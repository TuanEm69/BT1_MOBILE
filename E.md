#### E. Triển khai (level test) ứng dụng
Chuyển vào trong thư mục ~/myapp

Gõ lệnh để docker compose chạy: sẽ run tất cả các service khai báo trong file docker-compose.yml

<img width="1414" height="117" alt="image" src="https://github.com/user-attachments/assets/0988b177-59db-46e1-8e4f-f158ec5ebd06" />

Lợi ích: Chỉ cần docker-compose up -d là toàn bộ hệ thống (Web + Node-RED + Tunnel) tự chạy,
Kiểm tra các container đang chạy trong docker, nếu có cái nào bị restart cần tìm lỗi rồi edit lại docker-compose.yml

<img width="1399" height="99" alt="image" src="https://github.com/user-attachments/assets/6367d4ec-61eb-4bbb-bda6-76aa71547fa8" />

Kiểm tra kiểm thử các service đang chạy độc lập thông qua ip và port của nó: ví dụ mở trình duyệt ip_ubuntu:1880 để check nodered đã chạy chưa
Sử dụng nodered: kéo nodered http_in , http_response, function : để tạo api get đơn giản (dùng cho /api proxy_pass của nginx)
Sửa file ./myweb/index.html : thêm code html+js để sử dụng được api đã khai báo proxy_pass (thực ra là sử dụng nodered http_in hoặc sử dụng service myapi)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6d44b525-47d7-4cdd-a695-4a6f6f00cf14" />
