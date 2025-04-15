# Bài tập 04 của sv K225480106070 Nguyễn Đức Anh Tú
### bai tap 4: (sql server)
yêu cầu bài toán:

Tạo csdl cho hệ thống TKB (đã nghe giảng, đã xem cách làm)
Nguồn dữ liệu: TMS.tnut.edu.vn
Tạo các bảng tuỳ ý (3nf)
Tạo được query truy vấn ra thông tin gồm 4 cột: họ tên gv, môn dạy, giờ vào lớp, giờ ra.
trả lời câu hỏi: trong khoảng thời gian từ datetime1 tới datetime2 thì có những gv nào đang bận giảng dạy.
các bước thực hiện:

Tạo github repo mới: đặt tên tuỳ ý (có liên quan đến bài tập này)
tạo file readme.md, edit online nó:
paste những ảnh chụp màn hình
gõ text mô tả cho ảnh đó
Gợi ý:
sử dung tms => dữ liệu thô => tiền xử lý => dữ liệu như ý (3nf)
tạo các bảng với struct phù hợp
insert nhiều rows từ excel vào cửa sổ edit dữ liệu 1 table (quan sát thì sẽ làm đc)

## Tạo bảng GV với 2 trường là MaGV và Tên GV. Khoá chính là MaGV
![image](https://github.com/user-attachments/assets/81e24152-0cde-47ca-9f21-8961fe4b9743)

## Tạo bảng Lop gồm MaLop và TenLop
![image](https://github.com/user-attachments/assets/14a67969-5940-4215-9e4b-26384a2ed4db)

## Tạo bảng Mon
![image](https://github.com/user-attachments/assets/d0d9f36f-e400-42c4-925a-ee4892f59952)

## Tạo bảng Phong
![image](https://github.com/user-attachments/assets/0d2ab40b-0d2c-4faa-ab5b-73d6f1841195)

## Tạo bảng ThoiGian
![image](https://github.com/user-attachments/assets/74c9e2c7-5594-4342-af3a-84960de14033)

Foreign Key Relationships để quản lý và chỉnh sửa các khóa ngoại (foreign key) giữa các bảng.
![image](https://github.com/user-attachments/assets/4044bcad-3acc-4473-b372-1493d3bff866)

Nhập dữ liệu cho bảng ThoiGian
![image](https://github.com/user-attachments/assets/88ec725d-80b0-48b2-8927-3ba637cec753)

### TKB Bộ Môn - TNUT HK3 Năm học 2024-2025
![image](https://github.com/user-attachments/assets/f6bdba5e-fd4b-41a2-9f9f-77401d314591)

Lấy dữ liệu từ trang wed vào và lọc chúng
![image](https://github.com/user-attachments/assets/e2731854-1392-4126-b52b-45f6185677af)

Nhập dữ liệu cho bảng GV
![image](https://github.com/user-attachments/assets/c851bc91-272d-44ae-ba21-dca27b276925)

Nhập dữ liệu cho bảng Lop
![image](https://github.com/user-attachments/assets/d28f88a0-e2df-42a2-9b0c-8d353feb6248)

Nhập dữ liệu cho bảng Mon
![image](https://github.com/user-attachments/assets/44db7614-f688-49de-afef-437aeaa193c2)

Nhập dữ liệu cho bảng Phong
![image](https://github.com/user-attachments/assets/239c07d3-f52d-460b-b287-fcddb04b20f3)

Tạo hàm ufn_GiangVienDangDay, dùng để tra cứu thông tin giảng dạy của giảng viên trong khoảng thời gian cụ thể.
![image](https://github.com/user-attachments/assets/62421c35-7688-48f6-9481-7d86dd5efcbb)

Nhập dữ liệu cho bảng TKB
![image](https://github.com/user-attachments/assets/6fb63ba4-3f94-44e4-b17a-064b210b19a8)

Tạo sơ đồ quan hệ giữa các bảng trong csdl.
Các bảng được liên kết gồm: BangPhong, ThoiGian,BangGV,BangLop,BangMon.
Trong đó bảng trung tâm là TKB, liên kết khoá ngoại các bảng còn lại.
![image](https://github.com/user-attachments/assets/7ce83f16-9b7d-4509-b56c-2c77e5ccd086)

Thực hiện một truy vấn đến hàm người dùng định nghĩa (user-defined function) có tên ufn_GiangVienDangDay trong cơ sở dữ liệu BaiTap4
![image](https://github.com/user-attachments/assets/c09b1aad-ed0a-4dbd-bf12-f15bec7a0c76)




