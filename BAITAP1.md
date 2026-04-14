
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
1. Cài đặt hệ điều hành Ubuntu 24.04.4 LTS

Sử dụng một trong các công cụ để giả lập: VirutualBox

Download file iso để cài đặt.
Cấu hình mạng trong Ubuntu (và công cụ giả lập) để cho phép truy cập SSH vào Ubuntu từ cmd của windows
