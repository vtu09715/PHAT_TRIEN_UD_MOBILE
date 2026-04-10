# E. Triển khai (level test) ứng dụng
# 1.Chuyển vào trong thư mục ~/myapp Gõ lệnh để docker compose chạy: sẽ run tất cả các service khai báo trong file docker-compose.yml
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/653ddcc3-80f1-4d89-80cf-62a64f8088af" />
# 2.Kiểm tra các container đang chạy trong docker, nếu có cái nào bị restart cần tìm lỗi rồi edit lại docker-compose.yml
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3aa2eb76-3b27-41a9-96b2-834dfa0bb717" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1e4ce1b6-387f-4018-98fe-a134207c6c86" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c13e1087-e822-425e-9589-342fd14bffae" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3586c432-3c8c-4650-842a-2f1d605f8358" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2b96c2d-7eb3-4809-9d36-f8ff1be103ad" />
# 3.Sử dụng nodered: kéo nodered http_in , http_response, function : để tạo api get đơn giản (dùng cho /api proxy_pass của nginx)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a2a879b0-5f06-46e5-9547-3f30e4ed9514" />
# 4.Sửa file ./myweb/index.html : thêm code html+js để sử dụng được api đã khai báo proxy_pass (thực ra là sử dụng nodered http_in hoặc sử dụng service myapi)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d3dddb7-e6f4-41eb-a141-284762897c90" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/92742438-9a20-4b6a-8cf4-46cac8da3234" />
