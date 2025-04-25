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











