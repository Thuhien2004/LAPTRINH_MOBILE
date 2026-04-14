
# LAPTRINH_MOBILE: Bài tập 1
### Nguyễn Thị Thu Hiền_K225480106015
### Deadline: 13/4/2026
# A. Đăng ký miền cho cá nhân
1. Đăng ký domain  của mắt bão, tên miền: thuhien04.io.vn
<img width="1918" height="1078" alt="đăngký miền" src="https://github.com/user-attachments/assets/eb7dfec1-f23f-4d63-9bd6-f4a0ac0fd9c2" />
- Tại giao diện chính trước đó của mắt bão , gõ tên miền mong muốn và thanh toán tiền :)))
2. Đăng ký tài khoản Cloudflare bằng tài khoản gmail cá nhân
<img width="1916" height="966" alt="image" src="https://github.com/user-attachments/assets/3c0a40c0-45c0-4598-aa74-42f8629d982a" />
3. Thêm domain đã đăng ký vào trong cloudflare : Nhận 2 dòng namespace
<img width="1482" height="830" alt="image" src="https://github.com/user-attachments/assets/791760c5-57cb-4acb-bcd8-19b86cb9c3bd" />
<img width="860" height="527" alt="image" src="https://github.com/user-attachments/assets/76695678-14e2-4590-9a9d-59f542e0fd47" />
4. Nhập 2 dòng namespace của cloudflare vào trong trang quản lý DNS record của tên miền đăng ký (vd trên mắt bão)
- Add 2 dòng nameserver vào mắt bão bằng cách truy cập vào trang chủ mắt bão bằng tài khaornd đã đăng ký, chọn mục quản lý tên miền.
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/c09e3216-2bb2-41fc-bb6a-09bbf2b90a3f" />
<img width="806" height="230" alt="image" src="https://github.com/user-attachments/assets/160c2522-c235-45c5-be7f-95f6046c7f47" />
<img width="555" height="301" alt="image" src="https://github.com/user-attachments/assets/0f7c4103-82ae-44b2-ae19-d4637d534535" />
- Sau đó quay trở lại phần Domains của Cloudflare để check nameservers, vui lòng chờ khoảng 1-2 tiếng, chậm nhất 24 giờ để cập nhật.
# B. Cài đặt Ubuntu + Docker
1.1. Cài đặt hệ điều hành Ubuntu 24.04.4 LTS
Sử dụng một trong các công cụ để giả lập: VMware
<img width="507" height="536" alt="image" src="https://github.com/user-attachments/assets/8d90cc92-567c-4cfd-8011-925fbf6f4b17" />
- Trước đó e đã có file sẵn tải ubuntu.iso và Vmware vậy em chỉ cần Create New Vitual Machine là được. Chọn bản iso ubuntu đã có.
<img width="617" height="566" alt="image" src="https://github.com/user-attachments/assets/eba43fc7-3bc9-4600-956c-452abc197e17" />
- nhập username và passwword
- Chọn
<img width="598" height="583" alt="image" src="https://github.com/user-attachments/assets/d6e7d0c2-50f2-4e2a-af10-fd6991d41120" />
- Chọn brige network, sau đó chọn disk 20gb
<img width="1908" height="1073" alt="image" src="https://github.com/user-attachments/assets/2c7ebf53-2415-4912-ae79-c58f2bd3076a" />
<img width="1919" height="1047" alt="image" src="https://github.com/user-attachments/assets/9311ff7d-9646-471d-b85a-b4e2a95ae425" />
- Chờ đợi Ubuntu cài đặt. Sau đó khởi động lại
- <img width="1909" height="1000" alt="image" src="https://github.com/user-attachments/assets/340a4d88-c5eb-4743-a1ea-11949ab79a34" />
1.2. Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows
- Cài SSH trên ubuntu bằng cách gõ dòng lệnh trên terminal.
<img width="1089" height="178" alt="image" src="https://github.com/user-attachments/assets/8ffe8119-5cb9-41d7-9ef8-16fe44d86d5a" />
- Vào CMD trên window gõ ssh+"tenmayao"@"ip ảo"
<img width="1887" height="1079" alt="image" src="https://github.com/user-attachments/assets/7a045156-5989-4bd2-be6f-a6375e13226b" />
2. Tìm hiểu các lệnh cơ bản ubuntu
- Liệt kê các file trong thư mục: ls
<img width="1047" height="52" alt="image" src="https://github.com/user-attachments/assets/8981461a-0036-4448-a404-2fcb2faf4fb3" />
- Tạo thư mục: mkdir nameFolder
- Chuyển thư mục làm việc: cd path
<img width="933" height="59" alt="image" src="https://github.com/user-attachments/assets/d167595c-e753-4f6d-8661-2c867c102946" />
- Tạo file mới trong thư mục: nano ten_file.txt
<img width="1108" height="58" alt="image" src="https://github.com/user-attachments/assets/1d589622-803a-429e-966d-dcca7fbdafa9" />
- Sau đó gõ nội dung file, nhấn ctril 0 để lưu -> enter -> Gõ Y để xác nhận tên file -> enter ->Xong
<img width="1771" height="1028" alt="image" src="https://github.com/user-attachments/assets/f29778f9-5fe6-40f7-a27d-d6acd4e7675e" />
- Copy file: cp file_nguồn path/file_đích
<img width="1262" height="113" alt="image" src="https://github.com/user-attachments/assets/41367dfc-126b-4fa5-97de-bf823cbf5ed3" />
- Thay đổi quyền thao tác file: sudo chmod xxx filename
<img width="1313" height="230" alt="image" src="https://github.com/user-attachments/assets/2a1b353b-17c8-48e3-9be4-09bbe31d8e51" />
- Edit file: sudo nano tenfile
<img width="1489" height="791" alt="image" src="https://github.com/user-attachments/assets/7b285902-c60e-4d91-ab52-7e91303905b3" />
<img width="1119" height="104" alt="image" src="https://github.com/user-attachments/assets/f0ff8d21-ed58-4518-8ca0-9ca4d65463d1" />
- Xem ip của máy ubuntu: ip -4 addr
<img width="1266" height="195" alt="image" src="https://github.com/user-attachments/assets/069e3f26-9321-44f5-9711-9a4dc2d225cb" />
3. Cài đặt docker cho ubuntu
- Cập nhật package: sudo apt update
<img width="1034" height="213" alt="image" src="https://github.com/user-attachments/assets/02bdc091-20a6-44f0-a459-901575e7ba79" />
- Cài các gói cần thiết: sudo apt install -y ca-certificates curl gnupg
<img width="1397" height="561" alt="image" src="https://github.com/user-attachments/assets/33981d3d-53d4-4dd0-b366-5e6a30442cbe" />
- Thêm GPG key của Docker: sudo install -m 0755 -d /etc/apt/keyringscurl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o/etc/apt/keyrings/docker.gpg
- Thêm repository Docker: echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(./etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list.
- Cài Docker: sudo apt update, sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
<img width="1692" height="906" alt="image" src="https://github.com/user-attachments/assets/ba060f73-8212-4ec2-af13-e26384522754" />
4. Kiểm tra phiên bản docker vừa cài đặt.
<img width="1247" height="94" alt="image" src="https://github.com/user-attachments/assets/d16ac843-9749-4cef-945e-4acfa837fd0a" />
- Gõ docker --version , docker compose -version
5. Cấu hình để docker chạy mà không cần tiền tố sudo
<img width="1243" height="50" alt="image" src="https://github.com/user-attachments/assets/33bb3a4d-534b-4b95-a49f-fe1840c479b4" />
- Gõ lệnh: sudo usermod -aG docker nguyenthithuhien, newgrp docker
6. Tìm hiểu tập lệnh của docker và docker compose
docker ps              # Xem container đang chạy
docker ps -a           # Xem tất cả container
docker images          # Xem danh sách image
docker pull <image>    # Tải image về
docker run <image>     # Chạy container
docker stop <id>       # Dừng container
docker rm <id>         # Xóa container
docker rmi <image>     # Xóa image
docker compose up -d      # Chạy các service
docker compose down       # Dừng các service
docker compose ps         # Xem trạng thái
docker compose logs       # Xem logs
7. Đảm bảo tường lửa trên Ubuntu đã cho phép các cổng 80, 1880, 9630 (Lệnh: sudo ufw allow ...)
<img width="1050" height="312" alt="image" src="https://github.com/user-attachments/assets/cd6d2c41-84c7-49eb-bf1c-1dcb30581e72" />
# C. Cấu hình docker compose:
1. Tạo thư mục: ~/myapp, Chuyển vào trong thư mục ~/myapp
<img width="912" height="53" alt="image" src="https://github.com/user-attachments/assets/9f2ba26e-64e9-48ed-955a-c6ecacba1316" /> 
2. Tạo thư mục: ./myweb,  Tạo file ./myweb/index.html (với nội dung là thông tin cá nhân của em)
<img width="967" height="93" alt="image" src="https://github.com/user-attachments/assets/adfd49f2-2017-46b6-9ab6-9ef88407b9e3" />
3. Tạo file docker-compose.yml để nó sẽ có các dịch vụ sau: 
- Khai báo sử dụng nodered/node-red, cổng 1880, dữ liệu nằm tại thư mục ./nodered
- Khai báo sử dụng nginx, cổng 80, cấu hình trong file ./nginx/nginx.conf
<img width="1507" height="718" alt="image" src="https://github.com/user-attachments/assets/99f4294c-5868-42c6-8b60-eb4fb11d88c4" />
<img width="1131" height="121" alt="image" src="https://github.com/user-attachments/assets/86e678c2-0356-4dfa-9978-7e3c488c702a" />
- Mount thư mục ./myweb thành thư mục /myweb trong nginx
- Mount file ./nginx/nginx.conf vào file /etc/nginx/nginx.conf trong nginx
<img width="1507" height="718" alt="image" src="https://github.com/user-attachments/assets/99f4294c-5868-42c6-8b60-eb4fb11d88c4" />
- Sau khi hoàn tất các bước, ta chạy địa chỉ localhost của web, node-red . Hiện nội dung file index.html và giao diện nodered là được.
<img width="1911" height="975" alt="image" src="https://github.com/user-attachments/assets/e62a1461-22fc-44ba-9aba-6ca465253512" />
<img width="1709" height="350" alt="image" src="https://github.com/user-attachments/assets/066e8abc-3bae-41c6-bb30-0c5e485f754b" />
6. Edit file ./nginx/nginx.conf để:
Cấu hình web server cổng 80
server_name là sub-domain (sub-domain tuỳ ý của em)
location / trỏ tới root là thư mục /myweb
location /api dùng proxy_pass trỏ tới 1 (hoặc nhiều) node http_in của nodered
<img width="1560" height="789" alt="image" src="https://github.com/user-attachments/assets/6c1d4f12-83af-403a-bf66-e39e4dc7f081" />
7. Edit file ./nodered/settings.js để nodered bắt buộc đăng nhập
Chạy docker-compose lần đầu để Node-RED tự sinh file cấu hình trong thư mục ./nodered, sau đó mới tiến hành sửa settings.js và restart lại container
- Trước tiên phải tạo mật khẩu bcrypt:
<img width="1457" height="86" alt="image" src="https://github.com/user-attachments/assets/f77dd991-9bfa-46dc-b803-ac5460d06b8d" />
- Sau đó edit phần adminAuth trong file và thay mật khẩu hash vào:
<img width="1476" height="701" alt="image" src="https://github.com/user-attachments/assets/31d0d117-c87e-403d-b5b6-b5c8ea93e42b" />
- Nếu truy cập địa chỉ cổng noded-red mà ra màn hình yêu cầu đăng nhập thì thành công:
<img width="1759" height="889" alt="image" src="https://github.com/user-attachments/assets/603ea0f7-edb1-4793-8933-2fadbe4a42d4" />
# E. Triển khai ứng dụng
1. Chuyển vào trong thư mục ~/myapp,Gõ lệnh để docker compose chạy: sẽ run tất cả các service khai báo trong file docker-compose.yml
<img width="1297" height="87" alt="image" src="https://github.com/user-attachments/assets/c2676ed7-73ce-40f1-b8ca-45cbca1f361c" />
2. Kiểm tra các container đang chạy trong docker, nếu có cái nào bị restart cần tìm lỗi rồi edit lại docker-compose.yml
<img width="1452" height="138" alt="image" src="https://github.com/user-attachments/assets/f293db32-86ca-4288-8280-1aaaf482268b" />
3. Kiểm tra kiểm thử các service đang chạy độc lập thông qua ip và port của nó: ví dụ mở trình duyệt ip_ubuntu:1880 để check nodered đã chạy chưa
   ước đó đã kiểm tra rồi, có giao diện đăng nhập nodered rồi.
4.Sử dụng nodered: kéo nodered http_in , http_response, function : để tạo api get đơn giản (dùng cho /api proxy_pass của nginx)
<img width="714" height="191" alt="image" src="https://github.com/user-attachments/assets/d2608f40-7d46-4e1b-ba9b-3a1929680871" />
- Sau đó edit các thành phần ở mỗi noded-red, xong chạy Deploy:
<img width="829" height="884" alt="image" src="https://github.com/user-attachments/assets/dba89f4f-8d70-4953-895b-45eda05fb277" />
<img width="836" height="858" alt="image" src="https://github.com/user-attachments/assets/4da2fa68-5dd2-4222-ad86-401771679b25" />
<img width="1816" height="825" alt="image" src="https://github.com/user-attachments/assets/1b72e3e5-3b32-4457-b597-d6ec410b7d81" />
- Ta test API trực tiếp bằng cách gõ trên thanh địa chỉ: http://10.170.151.31:1880/hello:
<img width="1020" height="227" alt="image" src="https://github.com/user-attachments/assets/fe58a443-20db-4678-a789-b106a1405e18" />
- Ta test nginx proxy(/api):
<img width="1547" height="366" alt="image" src="https://github.com/user-attachments/assets/e336c7a6-f14c-4f41-87e7-98e3cce2eb31" />
--> oke :))
5. Sửa file ./myweb/index.html : thêm code html+js để sử dụng được api đã khai báo proxy_pass (thực ra là sử dụng nodered http_in hoặc sử dụng service myapi)
<img width="1603" height="927" alt="image" src="https://github.com/user-attachments/assets/5f158f16-fdee-43ed-8ce4-33072d0cf0d8" />
- Sau đó ta test xem nó có gọi được API hay ko? Gõ trên thanh địa chỉ: http://10.170.151.31, hiện giao diện là được:
<img width="1815" height="897" alt="image" src="https://github.com/user-attachments/assets/681a0b59-9088-4281-aaf1-601c53a4f440" />
<img width="438" height="312" alt="image" src="https://github.com/user-attachments/assets/37cd7907-b510-4436-baa9-4c7222350d58" />
# F. Gỡ lỗi:
1. nếu có lỗi xẩy ra trong quá trình triển khai docker compose up -d
Kiểm tra nhanh: docker compose ps giúp biết container nào đang chạy xem log, ví dụ: docker logs mynginx docker logs myapi
<img width="1551" height="166" alt="image" src="https://github.com/user-attachments/assets/f05371e3-8b7f-436f-afa7-e95bb52c0070" />
2. Thêm healthcheck cho myapi trong file docker-compose.yml
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost:9630"]
giới hạn resource cho một service: (tránh việc 1 service chiếm quá nhiều ram)
deploy:
  resources:
    limits:
      memory: 512M
<img width="1523" height="784" alt="image" src="https://github.com/user-attachments/assets/8dde5ff4-b83e-42f0-9c61-fa7ca9989d20" />
- sử dụng lệnh: docker compose stats để quan sát lượng ram sử dụng bởi mỗi service
<img width="1340" height="248" alt="image" src="https://github.com/user-attachments/assets/0509f3f0-dec1-44a9-b98c-fb4eebf9f19d" />
<img width="1154" height="93" alt="image" src="https://github.com/user-attachments/assets/5f265f02-028c-4eff-b42e-833d9a79001b" />
<img width="1471" height="266" alt="image" src="https://github.com/user-attachments/assets/533206de-4d07-4fa9-9981-8a4b4942cc8b" />












