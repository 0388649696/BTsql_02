# BTsql_02
K225480106070

BÀI TẬP VỀ NHÀ 02 - MÔN HỆ QUẢN TRỊ CSDL:

DEADLINE: 23H59 NGÀY 25/03/2025

ĐIỀU KIỆN: (ĐÃ LÀM XONG BÀI 1)
1. Đã cài đặt SQL Server 2022 Dev.
2. Đã cài đặt SQL Managerment Studio bản mới nhất.
3. Đã kết nối từ SQL Managerment Studio vào SQL Server.
4. Đã có tài khoản github, biết cách tạo repository(kho lưu trữ) cho phép truy cập public.

BÀI TOÁN:
- Tạo csdl quan hệ với tên QLSV gồm các bảng sau:
  + SinhVien(#masv,hoten,NgaySinh)
  + Lop(#maLop,tenLop)
  + GVCN(#@maLop,#@magv,#HK)
  + LopSV(#@maLop,#@maSV,ChucVu)
  + GiaoVien(#magv,hoten,NgaySinh,@maBM)
  + BoMon(#MaBM,tenBM,@maKhoa)
  + Khoa(#maKhoa,tenKhoa)
  + MonHoc(#mamon,Tenmon,STC)
  + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
  + DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)

YÊU CẦU:
1. Thực hiện các hành động sau trên giao diện đồ hoạ để tạo cơ sở dữ liệu cho bài toán:
  + Tạo database mới, mô tả các tham số(nếu có) trong quá trình.
  + Tạo các bảng dữ liệu với các trường như mô tả, chọn kiểu dữ liệu phù hợp với thực tế (tự tìm hiểu)
  + Mỗi bảng cần thiết lập PK, FK(s) và CK(s) nếu cần thiết. (chú ý dấu # và @: # là chỉ PK, @ chỉ FK)
2. Chuyển các thao tác đồ hoạ trên thành lệnh SQL tương đương. lưu tất cả các lệnh SQL trong file: Script_DML.sql


HÌNH THỨC LÀM BÀI:
1. Tạo repository mới, tạo file readme.md (có hướng dẫn trên zalo group)
2. Sinh viên thao tác trên máy tính cá nhân, chụp màn hình quá trình làm, chỉ cần chụp active window, thi thoảng chụp full màn hình để thấy sự cá nhân hoá.
3. Hình sau khi chụp paste trực tiếp vào file readme trên github, cần mô tả các phần trên ảnh để tỏ ra là hiểu hết!
4. upload các file liên quan: Script_DML.sql
5. Update link của repository vào cột bài tập 2 trên file excel online của thầy (đã ghim link trên zalo group)

Chú ý:
1. Được phép dùng AI và tham khảo bài của bạn, nhưng phải có sự khác biệt đáng kể.
2. Nghiêm cấm copy, clone. Tham khảo và copy là 2 việc khác hẳn nhau. Thầy có tool để check!
3. Bài làm phải có dấu ấn cá nhân (hãy sáng tạo và biết cách bảo vệ mình nếu bạn là bản chính)
4. Kết quả AI phải phù hợp với yêu cầu, nếu quá sai lệch <=> sv ko đọc => Cấm thi
5. Nên nhớ: cấm thi là ko có vùng cấm và thầy chưa bao giờ nói đùa về việc cấm thi.

## I. TẠO BẢNG VÀ THUỘC TÍNH 

![Screenshot 2025-03-24 213049](https://github.com/user-attachments/assets/775ff755-8f7e-4cee-b137-e34da8b1273e)

+ Bước 1: Chuột phải vào Databases > chọn New Database > Đặt tên là: QLSV >Save để lưu 

![Screenshot 2025-03-24 213217](https://github.com/user-attachments/assets/d929d89f-ed55-4c44-8f88-150592e24276)

+ Bước 2: Chuột phải vào Tables > chọn New > chọn Table... (cửa sổ mới sẽ hiện ra)

![bang sinh vien](https://github.com/user-attachments/assets/c15989ea-1068-4096-805b-465c887dde7f)
+ Bước 3: Nhập thông tin vào bảng mới, Cột Column điền thuộc tính, Data type đặt thuộc tính, Allow Null ( tích nếu giá trị để trống được)

![Screenshot 2025-03-24 213639](https://github.com/user-attachments/assets/c085dc60-574b-46ff-8534-8d0db2824e34)
+ Bước 4: Đặt khóa chính (Primary Key) bằng cách chuột phải vào khóa cần đặt chọn Set Primary Key.
Như ảnh ta được khóa chính:
![bang sinh vien](https://github.com/user-attachments/assets/c15989ea-1068-4096-805b-465c887dde7f)

![khóa ngoại](https://github.com/user-attachments/assets/c1f4bf01-f99b-487b-b2b9-22eb02293fbc)
+ Bước 5: Đặt khóa ngoại (Foregin key) bằng cách chuột phải trong bảng chọn Relationships

+ Bước 6: Bảng hiện ra, chọn dấu ***
  ![Screenshot 2025-03-24 222821](https://github.com/user-attachments/assets/a676cacb-412e-4960-90c7-85ba29b35956)
  Chọn Relationship name, Primarykey table (đây là bảng chứa khóa chính), Foreign key table (đây là bảng chứa khóa ngoại) Và Chọn thuộc tính maLop của hai bảng trên > chọn OK
![Screenshot 2025-03-24 223048](https://github.com/user-attachments/assets/5b8825fa-647c-4571-8449-d8cadb9ffe4c)
 LÀM TƯƠNG TỰ VỚI CÁC BẢNG KHÁC

DƯỚI ĐÂY LÀ BẢNG ĐÃ HOÀN THÀNH:
![bang sinh vien](https://github.com/user-attachments/assets/62134baa-7364-40e3-87db-cd801ba87377)
![bang lop](https://github.com/user-attachments/assets/9c54b67a-7d92-4d74-a40e-510753fbb843)
![bang gvcn](https://github.com/user-attachments/assets/9cd6ab86-fa65-47c5-8bf4-a26edeb7b232)
![bang lopsv](https://github.com/user-attachments/assets/dba807ad-1387-448d-a183-1add15fc01e2)
![bang giaovien](https://github.com/user-attachments/assets/9c478532-5f32-4934-8968-f563612ddddb)
![bang Bomon](https://github.com/user-attachments/assets/f6071b31-4842-4d21-b583-0be5d98afac7)
![bang Khoa](https://github.com/user-attachments/assets/a072554a-630a-4dd3-9bdd-cc647172608e)
![bang Monhoc](https://github.com/user-attachments/assets/fa3beebb-1aed-434a-9377-07c074da3686)
![bang Lophp](https://github.com/user-attachments/assets/a49ec324-a620-4009-9a13-dbbb02d85df7)
![bang DKMH](https://github.com/user-attachments/assets/d59fbac6-4c7d-4de7-a64b-4ef32a53a340)


## II. XUẤT CODE RA FILE Script_DML.sql

+ b1: Chọn Db QLSV > chọn Tasks> Generate Scripts... >
![Screenshot 2025-03-24 232447](https://github.com/user-attachments/assets/8eda5bbf-3dc6-437f-9494-bcfd54aac59a)
+ b2: Bảng Generate Scripts hiện ra. Chọn Choose Objects > chọn Select specific database objects >Next 
  Tùy chọn này cho phép chọn bảng theo ý. Ngoài ra có thể chọn Script entire database and all databsse để chọn toàn bộ
![Screenshot 2025-03-24 232504](https://github.com/user-attachments/assets/15bae79b-c3d2-4a89-bc34-cf91ba517907)

+ b3: Chọn Open in new query window để xem các dòng lệnh
  ![Screenshot 2025-03-24 232534](https://github.com/user-attachments/assets/1968b899-faed-4908-806b-b1b30f61c709)
  ![Screenshot 2025-03-24 232553](https://github.com/user-attachments/assets/226f9bcb-ac38-41d1-80e8-45a6cc0ea2d4)

+ b4: Lưu lại dòng lệnh với tên # Script_DML.sql
  





