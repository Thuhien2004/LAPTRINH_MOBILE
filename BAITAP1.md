
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


























