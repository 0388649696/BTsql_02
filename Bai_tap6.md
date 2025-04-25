K225480106070 

Bài tập 6: Hệ quản trị CSDL
Chủ đề: Câu lệnh Select
Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

DEADLINE: 23H59:59 NGÀY 25/4/2025


### 1. Nêu ra bước để import được dữ liệu trong sv_tnut.sql là:
B1: mở SSMS
B2: Trên thanh công cụ, chọn file ---> open ---> file... Trong cửa sổ mới sẽ hiện ra. Tìm chỗ lưu file SQL đã tải và bấm open
![image](https://github.com/user-attachments/assets/68ce898b-dc41-43b4-a557-735199292558)

B3: Tạo database có tên sv_tnut để trùng với câu lệnh USE [sv_tnut] file mẫu:
![image](https://github.com/user-attachments/assets/90a32fec-82a0-4857-aac8-d7d74eb64f26)
B4: Chạy code để tạo các bảng cho database như dưới
![image](https://github.com/user-attachments/assets/cb77bf11-7a17-41ae-a8d8-22f43588f496)

### 2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên
ruy vấn ra thông tin của em (Nguyễn Đức Anh Tú) với dữ liệu đầu vào là tên, sdt, ngày tháng năm sinh:
Chọn new query để code các truy vấn
Dùng câu lenh SELECT để chọn các trường phù hợp với yêu cầu thông tin của em:
![image](https://github.com/user-attachments/assets/5c5bbd2f-f8bf-4937-9590-c25bb893e7a6)

### 3. Truy vấn những sinh viên trùng hoàn toàn ngày, tháng, năm sinh với em:
dùng câu lệnh day, month, year để lấy được ngày, tháng, năm từ cột ns có kiểu Date để so sánh:
![image](https://github.com/user-attachments/assets/4fe3568c-4367-469a-848e-6e9dad4553d5)

### 4. Truy vấn những sinh viên trùng ngày, tháng sinh với em:
![image](https://github.com/user-attachments/assets/2f62abc7-75f0-47d6-902f-e62a05ca3a5f)

### 5. Truy vấn những sinh viên trùng tháng, năm sinh với em:
![image](https://github.com/user-attachments/assets/1bf0fec8-f96d-40ba-b348-2dc89bb00b53)

### 6. Truy vấn những sinh viên trùng tên với em:
![image](https://github.com/user-attachments/assets/234c751c-c9c3-407a-9c02-aa0e9b62b418)

### 7. Truy vấn những sinh viên trùng họ và tên đệm với em:
![image](https://github.com/user-attachments/assets/c576840d-b5dd-4197-9ffb-506d65fd5884)
> Tên em là độc nhất vô nhị nên ko thấy gì

### 8. Truy vấn những sv có sđt sai khác chỉ 1 số so với sđt của em:
![image](https://github.com/user-attachments/assets/e30738d6-dfbb-4b39-923d-609820e8b8ce)

### 9. LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG VIỆT:
![image](https://github.com/user-attachments/assets/075a906b-5a2e-490c-8d34-31160d656e2e)

Chú thích:
where lop like '%KMT%': để tìm trong cột lop xem có chuỗi nào chứa chuỗi ký tự 'KMT' thì lấy ra.
collate Vietnamese_CI_AS : Sắp xêp tên và họ đệm kiểu tiếng Việt

### 10. LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV:
![image](https://github.com/user-attachments/assets/bc99eb45-5c13-40d3-8558-6e14141c7743)

Chú thích:
- Đầu tiên, e lọc ra các sinh viên thuộc nghành KMT( trong đó có cả các sinh viên KTP vì KTP cũng là sinh viên KMT)
- Tiếp theo, e lọc thủ công tên cho giới nữ (có thể)
- Tiếp theo, e đưa các tên vào code để cho ra các sinh viên có thể là nữ trong nghành KMT.
Nhược điểm: Một số bạn nam sẽ có tên giống nữ. Phải đối chiếu dữ liệu khác để sửa lại thông tin









