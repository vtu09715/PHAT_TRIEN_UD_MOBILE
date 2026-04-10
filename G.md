# G. Triển khai ứng dụng đến End-user
# 1.Trong Cloudflare: Tạo tunnel (đường hầm), chọn loại triển khai cho docker
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/665e3901-5d31-4e07-91b1-232b277c7858" />
# Mở đường hầm từ máy ra Internet thông qua Cloudflare
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a6e84b22-4090-4664-80b3-47d06abca4a3" />
# chạy và kiểm tra hệ thống Docker + Tunnel
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cb210eda-79d8-4b45-a7fa-777fde4b3e19" />
# Khai báo: domain sẽ trỏ vào service nào trong server
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8dcc8f1b-6509-408c-a610-6eb63cdcadd6" />
# Ứng dụng đã public ra Internet
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9e0c4a42-b37e-4b42-9cac-081aa1e5f36b" />
# tạo cấu trúc thư mục 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9bbc4425-d673-4c1d-9df8-4fabc6a8e602" />
# Tạo app.py
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5294e808-9710-4c2b-a5bc-107b4b345884" />
# Tạo requirements.txt
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a5dc4253-07c1-46cc-a805-7ce987d22dfe" />
# Tạo Tạo Dockerfile
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9c1b63f5-978b-4cd4-9d4a-9a4c970c8225" />
# Tạo index.html
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e4243fcc-f379-45b8-892e-e062617fec40" />
# Tạo nginx.conf
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a7d30546-9f32-453f-9faa-a5739fb0140a" />
# Tạo File docker-compose.yml là trung tâm của toàn sơ đồ
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4bb50071-0a00-4cae-a946-a8fc5a3205da" />
# chạy lại dooker compose 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/509becf4-2648-4fe9-9c1e-387e7fa2e0db" />
# kiểm tra container và tunnel 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3e415e10-0f36-4a4a-bd82-c218c51059fc" />
# Kiểm tra url sub-domain đã hoạt động public cho mọi end-user
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f4feea09-757c-4042-813d-4da25e0426bd" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d2e484c9-a8c8-4919-b331-0206bbe2a582" />
## đã ok 
# trả lời câu hỏi 
# 1:Tại sao dùng Nginx Reverse Proxy thay vì trỏ thẳng Tunnel vào Node-RED? 
## vì Nginx điều phối nhiều service, dễ cấu hình route, tăng bảo mật( ẩn backend). Nếu trỏ thẳng chỉ expose được 1 server, khó quản lý 
# 2: Sự khác biệt giữa việc Mount file và Mount thư mục trong Docker là gì?
## mount file: gắn 1 fil cụ thể còn mount folder: gắn cả thư mục. khác biệt: file chỉ chứa 1 file config, folder: sync toàn bộ code và data 
# 3: Nếu thay đổi file index.html ở máy Ubuntu, nội dung trên web có thay đổi ngay không? Tại sao?
## có. vì Docker đang đọc trực tiếp từ máy host, không cần rebuild container 
# 4: docker-compose.yml khai báo các services có phần restart: always hoặc restart: unless-stopped : chúng để làm gì?
## Tự động restart container khi: bị crash, reboot máy.
# 5. Cách khai báo để tất cả các services đều dùng chung 1 network? lợi ích của việc khai báo này là gì? Sửa đổi file docker-compose để tất cả các service đều dùng chung 1 network?
## dùng chung lợi ích container giao tiếp bằng tên, không cần IP, Tăng bảo mật và dễ quản lý.
# 6:Tìm cách đưa Cloudflare Token vào trong file .env rồi sau đó thêm .env vào file .gitignore trước khi push code lên github. Tại sao nói đây là điều quan trọng về bảo mật mã nguồn?
## vì token là thông tin nhạy cảm. nếu push lên githup người khác sẽ dùng được tunnel của mình và có thể chiếm quyền truy cập 
## .env giúp tách config khỏi code và giúp bảo mật.
# 7: Tại sao chúng ta nên thêm hậu tố :ro khi mount file cấu hình Nginx?
## vì nó giúp container không được sửa config tránh bị hack và lỗi ghi đè.
# 8: Khi dùng Cloudflare Tunnel: có cần thiết phải mở cổng cho các service nữa không?
## không cần vì tunnel tạo kết nối outbound, cloudflare truy cập qua tunnel giúp an toàn hơn.
