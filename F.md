# F.Sửa lỗi 
# 1.nếu có lỗi xẩy ra trong quá trình triển khai docker compose up -d
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ac4bb740-858c-4df8-8859-ca5884770867" />
</p>

# 2.Thêm healthcheck cho myapi trong file docker-compose.yml
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4e4c3985-3bb0-48c5-acf3-d35250ef202d" />
</p>

# Cài curl trong image myapi
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b817a856-45ff-4e7e-84f4-464cc10309d2" />
</p>

# Build lại sau khi thêm healthcheck
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3bd1a011-eb03-4da3-8704-677b891ac826" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/661ac742-fff3-4f4d-980f-cc03c91310b5" />
</p>

# 3.giới hạn resource cho một service: (tránh việc 1 service chiếm quá nhiều ram)
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/775e0639-4de8-49b6-ba05-c6ed8c017a31" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e3742916-1f3e-4ef5-a753-3b0e06ffb3fc" />
</p>
