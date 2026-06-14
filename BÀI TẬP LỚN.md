# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419
## BÀI TẬP LỚN:
### 1. Viết phần mềm trên công cụ Mit App inventor
   (tập trung vào quy trình tạo ra phần mềm)
   app có 3 screen:
   + about về bản thân+nút gọi sang 2 screen còn lại
   + giải 1 bài toán đơn giản
   + sử dụng webview: hiển thị 1 trang web có sẵn, hỗ trợ giao diện điện thoại
   mô tả: thanh công cụ có gì? kéo thả + thay đổi thuộc tính: làm ntn, để làm gì?
          block: mô tả bản chất việc kéo thả block ntn?
                 ưu điểm gì so với viết code? nhược điểm?
                 copy paste block ? (backpack)
### 2. Viết app sử dụng Android Studio
   + Android manifest.xml  => mô tả gì? app cần quyền để do-st: khai báo ntn? để làm gì?
   + vòng đời của 1 ứng dụng android.
     code tự sinh sau khi tạo 1 project: có sẵn hàm onCreate: tại sao???
   + Code: java language. 
     app cần check xem có quyền để do-st? : code ntn? ý nghĩa?
     giao diện: (res/layout) mô tả bằng file XML + UI Design review
        + thuộc tính text, hoặc các thuộc tính khác: giá trị hardcode => lưu vào nới khác, tham chiếu tới nó:
          cú pháp của việc tham chiếu là gì?
          ưu điểm của việc tham chiếu này?
          OS hỗ trợ auto việc lấy giá trị tham chiếu theo LOCATION, LANGUAGE, THEME
          việc hỗ trợ auto này giúp app làm được điều gì?	
        + đối tượng chứa: gộp các đối tượng con lại: cùng 1 quy luật sắp xếp để hiển thị 
          các đối tượng con nằm kề nhau theo chiều dọc | hoặc ngang, gravity
     code tương tác với layout: vd hiển thị text
          mong muốn text hiển thị phù hợp với thiết lập LOCATION, LANGUAGE, THEME của người dùng
          thì làm ntn? (tránh hardcode)
     event (sự kiện) người dùng tác động vào app: CLICK vào button, click vào text,...
          với 1 sự kiện nào đó, muốn chạy 1 đoạn code để do-st
          thì LAYTOUT cần làm gì?
              CODE viết như nào (2 cách)
---------------------------
     trong app có các thư mục đặc biệt: Assets
     khi sử dụng Window Explorer để copy các files + folder vào trong Assets
     thì khi compiler: mọi file này đều đi theo app, nằm trong app
     trong app có thể truy cập được đến các file này
     cú pháp truy cập vào là gì?
     lợi ích của việc app có sẵn các files (offline cũng có)?
     ứng dụng: app hướng dẫn việc X
==> tạo app1 sử dụng cơ chế Dữ liệu chuẩn bị trước trong Assets
         format dữ liệu: tuỳ ý, nội dung tuỳ ý
         công cụ để hiển thị dữ liệu: tuỳ ý
         có cần phải tiền xử lý trước khi hiển thị ko: tuỳ ý.
         SV TỰ ĐẶT RA VẤN ĐỀ => TỰ GIẢI QUYẾT VẤN ĐỀ
         MÔ TẢ ĐƯỢC DỮ LIỆU CÓ ĐẶC THÙ GÌ
                    DÙNG THUẬT TOÁN NÀO ĐỂ XỬ LÝ DỮ LIỆU (NẾU CẦN)
                    DÙNG ĐỐI TƯỢNG NÀO ĐỂ HIỂN THỊ DỮ LIỆU.
                    (ĐỘ SÁNG TẠO LÀ KO GIỚI HẠN)
APP2 (android studio):  tạo app tương đương với Mit App inventor
  app có 3 activity
  + activity1: about: about+nút gọi sang 2 activity còn lại
  + activity2: giải toán đơn giản (tuỳ ý). mỗi khi giải xong bài toán: gọi api tại https://k58kmt.tdh.io.vn/api
    để gửi bài toán lên đó
    {app_by:mã số sv, input: {a:1,b:2,c:3,name:"hello tắc kè"},output:{ketluan:"vô nghiệm", abc:"xyz", nghiem:3.14}}
    nhận lại json: {ok:1, stt:1234}
  + activity3: 
    dùng web-view để truy cập từ 
    1 trang web https://k58kmt.tdh.io.vn?masv=mã sv của bạn
-------------------------------------------------------------------------------------------
# BÀI LÀM
# 1. Viết phần mềm trên công cụ Mit App inventor
## Quy trình xây dựng cấu trúc 3 màn hình của ứng dụng
Để hiện thực hóa yêu cầu của đề tài, ứng dụng được thiết kế gồm 3 màn hình tương tác độc lập. Quy trình cấu hình giao diện chi tiết cho từng màn hình. Trước tiên, hoàn thành việc truy cập vào Mit app Invertor:
Bước 1: Trên trình duyệt truy cập trang mit app invertor MIT App Inventor , chọn Create app! Sau đó, giao diện trình bày sẽ hiện ra:
<img width="979" height="464" alt="image" src="https://github.com/user-attachments/assets/556babac-5ef1-4444-bfcd-79e91beaa984" />
<img width="979" height="479" alt="image" src="https://github.com/user-attachments/assets/13a20cbe-b675-4c8f-8700-d00843e32025" />

Bước 2: Sau đó, sử dụng điện thoại Android tải Mit AI2 Companion, quét mã và sử dụng sau khi hoàn thành. Tiếp theo là tạo Project mới bằng cách chọn New Project, thì màn hình hình Screen 1 sẽ hiện ra.
<img width="788" height="379" alt="image" src="https://github.com/user-attachments/assets/dc669d78-8633-497e-9705-785c6923770d" />

### Screen 1: Giới thiệu bản thân (About Me) và Điều hướng
Màn hình mặc định đóng vai trò giao diện trang chủ, cung cấp thông tin tác giả và hệ thống nút bấm điều hướng.
•	Bước 1: Tạo giao diện thông tin:
-	Kéo một VerticalArrangement, chỉnh AlignHorizontal thành Center và Width thành Fill Parent.
-	Kéo linh kiện Image vào trong khung: Đặt tên là img_Avatar. Tại mục thuộc tính Picture, tải lên ảnh cá nhân dạng .jpg hoặc .png. Chỉnh Height và Width cố định (ví dụ: 150px x 150px) để tránh vỡ khung hình.
<img width="727" height="415" alt="image" src="https://github.com/user-attachments/assets/d2487197-64a2-4fc0-880e-f27cc8502716" />

-	Kéo các linh kiện Label lần lượt hiển thị: Họ và tên, Mã số sinh viên, Lớp học. Thay đổi thuộc tính FontSize thành 16 hoặc 18, chọn FontBold để làm nổi bật thông tin.
<img width="687" height="538" alt="image" src="https://github.com/user-attachments/assets/4cf373b7-416c-4003-ae1e-4f612051b833" />

•	Bước 2: Tạo hệ thống nút bấm điều hướng:
-	Kéo một HorizontalArrangement đặt phía dưới khung thông tin để chứa các nút bấm nằm ngang.
-	Kéo linh kiện Button thứ nhất, đổi tên thành bt_toan, thay đổi thuộc tính Text hiển thị thành "Giải Toán".
-	Kéo linh kiện Button thứ hai, đổi tên thành bt_web, thay đổi thuộc tính Text hiển thị thành "Xem Website".
<img width="863" height="270" alt="image" src="https://github.com/user-attachments/assets/206be5ef-1af2-4ac3-a61d-45f473899da3" />

### Screen 2: Giải bài toán phương trình bậc nhất (ax + b = 0)
Màn hình này hiện thực hóa việc nhận dữ liệu từ người dùng, xử lý toán học sơ cấp và trả kết quả. Trước tiên, blocks screen1 lại, nhìn vào thanh menu bên trái chọn nút bt_web.
<img width="979" height="682" alt="image" src="https://github.com/user-attachments/assets/39116f91-4814-44d3-bdd5-5865ac7d993e" />
<img width="773" height="385" alt="image" src="https://github.com/user-attachments/assets/296b5a56-377e-4d08-bf3c-6f81b3b9a479" />

•	Bước 1: Thiết kế khu vực nhập liệu:
-	Bấm vào nút Add Screen ở thanh công cụ trên cùng, đặt sẵn tên màn hình là Screen2, Screen3.
-	Sử dụng một HorizontalArrangement để chứa dòng nhập hệ số a: 
+ Kéo một Label (Text: "Nhập hệ số a:") và một TextBox (Đổi tên thành txt_HeSoA). 
+ Trong Properties của txt_HeSoA, tích chọn vào ô NumbersOnly để ép kiểu người dùng chỉ được nhập số, tránh lỗi Crash ứng dụng do sai định dạng dữ liệu.
-	Tương tự, tạo dòng nhập hệ số b: 
+ Gồm Label (Text: "Nhập hệ số b:") và một TextBox (Đổi tên thành txt_HeSoB, bật NumbersOnly).
•	Bước 2: Thiết kế khu vực xử lý và hiển thị:
-	Kéo linh kiện Button đặt bên dưới, đổi tên thành btn_TinhToan, đặt thuộc tính Text thành "Tính Nghiệm".
-	Kéo một Label lớn ở dưới cùng, đổi tên thành lbl_KetQua, xóa trống thuộc tính Text (Mặc định ban đầu không hiển thị gì) và chỉnh TextColor thành màu đỏ hoặc xanh để người dùng dễ quan sát kết quả sau khi tính.
<img width="973" height="504" alt="image" src="https://github.com/user-attachments/assets/cd67bb29-b578-4955-9ce0-5588fc2373ae" />
<img width="979" height="203" alt="image" src="https://github.com/user-attachments/assets/866f02f9-ca1f-4445-a15d-d65bbeaa2ad7" />

### Screen 3: Tích hợp trình duyệt hiển thị Website (WebViewer)
Màn hình này giải quyết bài toán tích hợp nội dung số từ internet vào môi trường ứng dụng di động bản địa.
•	Bước 1: Bấm Add Screen, đặt tên màn hình là Screen3.
•	Bước 2: Truy cập nhóm User Interface trong vùng Palette, kéo linh kiện WebViewer thả vào màn hình ảo.
•	Bước 3 Cấu hình tối ưu: Tại bảng thuộc tính của WebViewer, thiết lập thuộc tính Height và Width thành Fill Parent để trình duyệt con này chiếm toàn bộ không gian hiển thị của màn hình điện thoại.
-	Tại mục HomeUrl, dán đường dẫn của một trang web có cấu trúc giao diện tương thích tốt với thiết bị di động (Responsive/Mobile-friendly), ví dụ: https://google.com.
<img width="975" height="377" alt="image" src="https://github.com/user-attachments/assets/4b190806-3010-4a75-bf1a-4850a71c71c2" />

Tiếp theo, đóng gói lại toàn bộ bằng cách chọn Build , chờ đợi đóng gói apk Android. Sau đó, dùng điện thoại Android quét mã đang hiển thị trên màn hình để test.
<img width="970" height="601" alt="image" src="https://github.com/user-attachments/assets/383b6fb1-fd7b-4471-bf87-b26377695c13" />

Dùng app đã có trên điện thoại , quét mã xong rồi tải file apk về máy và cài đặt phần mềm.
<img width="232" height="523" alt="image" src="https://github.com/user-attachments/assets/dd13aaca-c52f-4b7b-b6b5-4ac186793360" />
<img width="232" height="523" alt="image" src="https://github.com/user-attachments/assets/a9f67a42-4d72-49b9-a211-550cc409d9fd" />
<img width="231" height="522" alt="image" src="https://github.com/user-attachments/assets/b02ab0ca-53f0-4d9d-a4cf-9f9846ad4691" />

# VIẾT PHẦN MỀM SỬ DỤNG ANDROID STUDIO
## Thực hành APP 1
### . Đặt vấn đề và Giải quyết vấn đề 
•	Đặt vấn đề: Xây dựng ứng dụng "Sổ tay hướng dẫn mẹo lập trình Offline". Ứng dụng cần chứa một lượng lớn dữ liệu bài viết hướng dẫn dưới dạng văn bản có cấu trúc. Nếu lưu trữ trực tiếp trong code Java sẽ gây nặng app và khó bảo trì; nếu lưu trên Server thì khi điện thoại mất mạng (Mất kết nối Internet), người dùng không thể học được.

•	Giải quyết vấn đề: Sử dụng thư mục đặc biệt Assets. Chuẩn bị trước các tệp tin chứa nội dung bài viết dưới dạng cấu trúc tệp .txt phẳng. Khi biên dịch, toàn bộ các tệp này sẽ được đóng gói đi theo App vào thiết bị người dùng.

•	Đặc thù dữ liệu: Dữ liệu dạng văn bản thô (Plain Text), mã hóa chuẩn UTF-8 để hiển thị đúng tiếng Việt.

•	Thuật toán xử lý: Sử dụng luồng đọc dữ liệu dòng BufferedReader để nạp toàn bộ nội dung từ bộ nhớ trong của App, nối chuỗi tuần tự để tái cấu trúc văn bản.

•	Đối tượng hiển thị: Sử dụng thành phần hiển thị văn bản cuộn tự do: TextView nằm bên trong ScrollView.

### Hiện thực hóa mã nguồn APP 1
<img width="979" height="520" alt="image" src="https://github.com/user-attachments/assets/038b57de-2e9d-4495-9226-830ef0f0f2b1" />

Bước 1: Khởi tạo dự án mới
1.	Mở Android Studio, tại màn hình chào mừng, chọn New Project 
2.	Một bảng danh sách các mẫu màn hình hiện ra, bạn tìm và chọn mẫu Empty Views Activity. Nhấn Next.
3.	Cấu hình các thông số dự án như sau:
-	Name: App1_Assets
-	Package name: Giữ nguyên mặc định (ví dụ: com.example.app1_assets).
-	Language: Chọn Java 
-	Minimum SDK: để mặc định 
Nhấn Finish và đợi tầm 1–2 phút để phần mềm tải cấu hình Gradle ban đầu. 
<img width="979" height="703" alt="image" src="https://github.com/user-attachments/assets/2fae6743-6eb0-4c29-94e1-4f1be85ff355" />

Bước 2: Tạo thư mục Assets và thêm file dữ liệu
1.	Click chuột phải vào thư mục app -> chọn New -> chọn Folder -> chọn Assets Folder. Nhấn Finish. Lúc này, dưới thư mục main sẽ xuất hiện một thư mục mới tên là assets.
<img width="688" height="350" alt="image" src="https://github.com/user-attachments/assets/8d620bae-4fae-44d8-b55a-702dcdc7da71" />

Bây giờ, mở phần mềm Notepad (hoặc Word) trên máy tính lên, gõ một đoạn nội dung cẩm nang hướng dẫn bất kỳ bằng tiếng Việt “CHAO MUNG DEN VOI SO TAY LAP TRINH CUA THU HIEN…”
2.	Lưu tệp đó lại với tên là huongdan.txt 
3.	Quay lại thư mục trên máy tính, nhấn Ctrl + C file huongdan.txt. Sau đó vào Android Studio, click chuột phải vào thư mục assets vừa tạo ở trên và nhấn Paste (Ctrl + V).
Bước 2 : Viết code đọc file MainActivity.java
<img width="979" height="547" alt="image" src="https://github.com/user-attachments/assets/a1682f4f-d0ce-4c45-9ae3-7e50b9bf86fa" />
<img width="979" height="258" alt="image" src="https://github.com/user-attachments/assets/e6ad392b-6fe7-4b32-a892-79e8b3e9f0cd" />

Sau đó, vào mục cài đặt của điện thoại , cài đặt cấu hình dành cho nhà phát triển , gỡ lỗi USB hoặc cũng có thể kết nối máy tính với điện thoại thông qua wifi. Bấm Run trên Android studio và trên điện thoại cũng sẽ tự động mở app. 
<img width="490" height="1105" alt="image" src="https://github.com/user-attachments/assets/6a1acd77-f02e-4384-8c58-400bd0cfcd17" />

## Thực hành APP 2
Sử dụng Project đã tạo từ APP 1 trước đó , ta triển khai APP 2. Tạo thêm file trong cấu trúc thư mục dự án bao gồm 3 màn hình giống như app của MitApp Invertor
Bước 1: VẬN HÀNH TẠI "ACTIVITY 1" - MÀN HÌNH TRANG CHỦ (ABOUT)
1. Quy trình thực hiện và Tương tác giao diện: Khi ứng dụng được cài đặt, người dùng chạm vào biểu tượng ứng dụng trên điện thoại. Hệ thống sẽ phân tích thẻ <intent-filter> trong Manifest và khởi chạy MainActivity đầu tiên.

•	Giao diện hiển thị cấu trúc thông tin sinh viên nằm trong một khối LinearLayout màu trắng có đổ bóng elevation="4dp" để tạo chiều sâu cấu trúc.

•	Thông tin sinh viên không gõ "cứng" (Hardcoded) vào XML mà được ánh xạ từ tệp quản lý tài nguyên tập trung res/values/strings.xml giúp tối ưu hóa mã nguồn theo tiêu chuẩn Google.

•	Phía dưới thông tin cá nhân là 2 nút bấm điều hướng lớn, được phân tách màu sắc (#1976D2 - Xanh dương cho Giải toán và #4CAF50 - Xanh lá cho WebView).

2. Mã nguồn Giao diện XML (activity_main.xml):

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    android:background="#FFFFFF">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/student_name"
        android:textSize="18sp"
        android:textColor="#000000"
        android:layout_gravity="center_horizontal" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/student_id"
        android:textSize="16sp"
        android:textColor="#000000"
        android:layout_gravity="center_horizontal" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/student_class"
        android:textSize="16sp"
        android:textColor="#000000"
        android:layout_gravity="center_horizontal" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/student_dob"
        android:textSize="16sp"
        android:textColor="#000000"
        android:layout_gravity="center_horizontal"
        android:layout_marginBottom="24dp" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/title_assets"
        android:textSize="20sp"
        android:textStyle="bold"
        android:textColor="#000000"
        android:layout_gravity="center_horizontal"
        android:layout_marginBottom="8dp" />

    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1">

        <TextView
            android:id="@+id/txtNoiDungAssets"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/loading_assets"
            android:textColor="#333333"
            android:textSize="18sp" />

    </ScrollView>

    <Button
        android:id="@+id/btnReload"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/btn_reload"
        android:layout_marginTop="16dp" />

</LinearLayout>

3. Mã nguồn Xử lý Logic Java (MainActivity.java):

package com.example.btl_mobile_app1;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    // 1. Khai báo đúng 2 nút bấm
    Button btnMoApp2, btnMoApp3;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // 2. Ánh xạ chính xác ID từ XML
        btnMoApp2 = findViewById(R.id.btnMoApp2);
        btnMoApp3 = findViewById(R.id.btnMoApp3);

        // 3. Thiết lập sự kiện nhảy sang Activity 2
        btnMoApp2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(MainActivity.this, MathActivity.class);
                startActivity(intent);
            }
        });

        // 4. Thiết lập sự kiện nhảy sang Activity 3
        btnMoApp3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(MainActivity.this, WebActivity.class);
                startActivity(intent);
            }
        });
    }
}

Bước 2: VẬN HÀNH VÀ KIỂM THỬ MODULE GIẢI TOÁN & GIAO TIẾP API LỒNG NHAU
1. Quy trình thực hiện thực tế trên điện thoại
1.	Từ Màn hình 1 (Trang chủ About), chạm ngón tay vào nút bấm màu xanh dương "GIẢI TOÁN & GỬI API" (btnMoApp2).
2.	Hệ thống lập tức kích hoạt MathActivity và chuyển đến giao diện giải toán.
3.	Thao tác kiểm thử kịch bản nghiệm duy nhất (Trường hợp điển hình):
-	nhập vào ô Hệ số a: 2
-	nhập vào ô Hệ số b: 2
-	Nhấn nút "GIẢI TOÁN & GỬI API".
4.	Kết quả đạt được: Có nghiệm duy nhất x = -1
-	Bên dưới đáy màn hình sẽ xuất hiện một thông báo nhanh (Toast) dạng: Server trả về -> ok: 1, STT: … (số STT sẽ tự tăng tùy thuộc vào lượt gửi trên Server của thầy). Điều này chứng minh điện thoại đã kết nối mạng và trao đổi dữ liệu 2 chiều thành công với máy chủ qua API.
<img width="301" height="680" alt="image" src="https://github.com/user-attachments/assets/c2660694-30cd-4ecd-879d-3b98b12472ac" />

Bước 3: VẬN HÀNH TẠI "ACTIVITY 3" - TRÌNH DUYỆT NHÚNG WEBVIEW ĐỊNH DANH
-	Quy trình thực hiện và Tương tác giao diện: Khi người dùng quay trở lại Màn hình 1 và nhấn nút "XEM WEBVIEW ACTIVITY 3", hệ thống lập tức gọi lớp WebActivity. Nhưng hình minh họa ở trên lại hiện thông báo lỗi kết nối API Server , lý do chưa được cấp quyền Internet. 
-	Ta cấp quyền Internet trong AndroidManifest.xml :
+ Mở file AndroidManifest.xml. Thêm dòng xin quyền truy cập Internet này nằm ngay phía trên thẻ <application>.

<uses-permission android:android:name="android.permission.INTERNET" />
    <application>
        
- Mã nguồn code MathActivity.java

package com.example.btl_mobile_app1;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
import org.json.JSONObject;
import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.net.HttpURLConnection;
import java.net.URL;
import java.nio.charset.StandardCharsets;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class MathActivity extends AppCompatActivity {
    EditText edtA, edtB;
    Button btnGiai;
    TextView txtKetQua;

    String MA_SV = "K225480106015";

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_math);

        edtA = findViewById(R.id.edtA);
        edtB = findViewById(R.id.edtB);
        btnGiai = findViewById(R.id.btnGiai);
        txtKetQua = findViewById(R.id.txtKetQua);

        btnGiai.setOnClickListener(v -> giaiPhuongTrinhBacNhat());
    }

    private void giaiPhuongTrinhBacNhat() {
        String strA = edtA.getText().toString().trim();
        String strB = edtB.getText().toString().trim();

        if (strA.isEmpty() || strB.isEmpty()) {
            Toast.makeText(this, "Vui lòng nhập đủ hệ số!", Toast.LENGTH_SHORT).show();
            return;
        }

        try {
            double a = Double.parseDouble(strA);
            double b = Double.parseDouble(strB);

            String ketLuan;
            double nghiem = 0.0;

            if (a == 0) {
                ketLuan = (b == 0) ? "Vô số nghiệm" : "Vô nghiệm";
            } else {
                nghiem = -b / a;
                ketLuan = "Có nghiệm duy nhất";
            }

            String ketQuaHienThi = ketLuan + (a != 0 ? " x = " + nghiem : "");
            txtKetQua.setText(ketQuaHienThi);

            // Gửi API bằng ExecutorService (Chuẩn Android hiện đại)
            guiDuLieuLenApi(strA, strB, ketLuan, nghiem);

        } catch (NumberFormatException e) {
            Toast.makeText(this, "Hệ số phải là số!", Toast.LENGTH_SHORT).show();
        }
    }

    private void guiDuLieuLenApi(String a, String b, String ketLuan, double nghiem) {
        ExecutorService executor = Executors.newSingleThreadExecutor();
        executor.execute(() -> {
            String result;
            try {
                URL url = new URL("https://k58kmt.tdh.io.vn/api/");
                HttpURLConnection conn = (HttpURLConnection) url.openConnection();
                conn.setRequestMethod("POST");
                conn.setRequestProperty("Content-Type", "application/json; charset=UTF-8");
                conn.setDoOutput(true);

                // Tạo JSON Body
                JSONObject jsonBody = new JSONObject();
                jsonBody.put("app_by", MA_SV);

                JSONObject jsonInput = new JSONObject();
                jsonInput.put("a", Double.parseDouble(a));
                jsonInput.put("b", Double.parseDouble(b));
                jsonInput.put("c", 0);
                jsonInput.put("name", "Nguyễn Thị Thu Hiền");
                jsonBody.put("input", jsonInput);

                JSONObject jsonOutput = new JSONObject();
                jsonOutput.put("ketluan", ketLuan);
                jsonOutput.put("nghiem", nghiem);
                jsonBody.put("output", jsonOutput);

                // Gửi dữ liệu
                try (OutputStream os = conn.getOutputStream()) {
                    os.write(jsonBody.toString().getBytes(StandardCharsets.UTF_8));
                }

                // Đọc phản hồi
                int code = conn.getResponseCode();
                if (code == 200 || code == 201) {
                    InputStream is = conn.getInputStream();
                    BufferedReader br = new BufferedReader(new InputStreamReader(is, StandardCharsets.UTF_8));
                    StringBuilder sb = new StringBuilder();
                    String line;
                    while ((line = br.readLine()) != null) sb.append(line);
                    result = sb.toString();
                } else {
                    result = "Lỗi HTTP: " + code;
                }
            } catch (Exception e) {
                result = "Lỗi kết nối: " + e.getMessage();
            }

            // Hiển thị kết quả lên UI
            String finalResult = result;
            runOnUiThread(() -> {
                if (finalResult.contains("ok\":1")) {
                    Toast.makeText(MathActivity.this, "Gửi API thành công!", Toast.LENGTH_SHORT).show();
                } else {
                    Toast.makeText(MathActivity.this, finalResult, Toast.LENGTH_LONG).show();
                }
            });
        });
    }
}
 
Sau đó ta chạy thử lại app trên điện thoại, nhập các giá trị a,b và tính toán , nếu thông báo hiện Gửi API thành công thì là hoàn thành.
<img width="422" height="951" alt="image" src="https://github.com/user-attachments/assets/22a98c82-f911-4598-8c92-0ee1499f243c" />


























