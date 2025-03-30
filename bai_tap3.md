# BÀI TẬP VỀ NHÀ 03 - MÔN HỆ QUẢN TRỊ CSDL:

DEADLINE: 23H59 NGÀY 30/03/2025

### ĐIỀU KIỆN: (ĐÃ LÀM XONG BÀI 2)

### BÀI TOÁN: Sửa bài 2 để có csdl như sau:
  + SinhVien(#masv,hoten,NgaySinh)
  + Lop(#maLop,tenLop)
  + GVCN(#@maLop,#@magv,#HK)
  + LopSV(#@maLop,#@maSV,ChucVu)
  + GiaoVien(#magv,hoten,NgaySinh,@maBM)
  + BoMon(#MaBM,tenBM,@maKhoa)
  + Khoa(#maKhoa,tenKhoa)
  + MonHoc(#mamon,Tenmon,STC)
  + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
  + DKMH(#id_dk, @maLopHP,@maSV,DiemThi,PhanTramThi)
  + Diem(#id, @id_dk, diem)

### YÊU CẦU:
1. Sửa bảng DKMH và bảng Điểm từ bài tập 2 để có các bảng như yêu cầu.
2. Nhập dữ liệu demo cho các bảng (nhập có kiểm soát từ tính năng Edit trên UI của mssm)
3. Viết lệnh truy vấn để: Tính được điểm thành phần của 1 sinh viên đang học tại 1 lớp học phần.

### HÌNH THỨC LÀM BÀI:
1. Tạo file bai_tap3.md trên cùng repository của bài tập 2:
   Nội dung chứa đề bài, và ảnh chụp quá trình thao tác các yêu cầu khác.
2. Chụp ảnh quá trình sửa bảng DKMH và quá trình thêm bảng Diem, chú ý @ là FK, và thêm CK cho trường điểm
3. Hình sau khi chụp paste trực tiếp vào file bai_tap3.md trên github, cần mô tả các phần trên ảnh để tỏ ra là hiểu hết!
4. dùng tính năng: Tasks -> Generate Scrips => sinh ra file: bai_tap_3_schema.sql  (chỉ chứa lệnh tạo cấu trúc của db)
5. dùng tính năng: Tasks -> Generate Scrips => advance => Check Data only => sinh ra file: bai_tap_3_data.sql  (chỉ chứa dữ liệu đã nhập demo vào db)
6. Tạo diagram mô tả các PK, FK của db. Chụp hình kết quả các bảng có các đường nối 1-->nhiều
7. upload 2 file  bai_tap_3_schema.sql và bai_tap_3_data.sql lên repository.
8. nhớ commit để save nội dung file bai_tap3.md

# DEADLINE: 23H59 NGÀY 30/03/2025

---------------------- hết bài tập 3-------------------------------------------
Chú ý:
1. Được phép dùng AI và tham khảo bài của bạn, nhưng phải có sự khác biệt đáng kể.
2. Nghiêm cấm copy, clone. Tham khảo và copy là 2 việc khác hẳn nhau. Thầy có tool để check!
3. Bài làm phải có dấu ấn cá nhân (hãy sáng tạo và biết cách bảo vệ mình nếu bạn là bản chính)
4. Kết quả AI phải phù hợp với yêu cầu, nếu quá sai lệch <=> sv ko đọc => Cấm thi
5. Nên nhớ: cấm thi là ko có vùng cấm và thầy chưa bao giờ nói đùa về việc cấm thi.

Nhắc lại nội quy học tập:
SV vi phạm 1 trong các lỗi sau chỉ 1 lần sẽ bị cấm thi: 🚫
1. Nghỉ ko lý do chính đáng.
2. Không làm bài tập về nhà.
3. Vắng bài kiểm tra.
4. Nói chuyện tự do trong lớp.

Bên cạnh đó, sẽ có điểm thưởng 10đ cho sv :  🎁
1. Trả lời đúng câu hỏi trên lớp.
2. Hỏi câu hỏi làm thầy khó trả lời.

# I. Sửa bảng DKMH và bảng Điểm từ bài tập 2 để có các bảng:
Sửa bảng DKMH:
![image](https://github.com/user-attachments/assets/d8a4b141-e37c-4057-87a6-d20a06d6f703)
Tạo bảng Điểm:
![image](https://github.com/user-attachments/assets/1a8d4a1e-40da-47f2-aab9-4ead5229596c)
![Screenshot 2025-03-30 204711](https://github.com/user-attachments/assets/e55540d0-5436-4bd8-9a11-59654f9247ab)
![image](https://github.com/user-attachments/assets/fc1d96b8-1c92-44e1-bdb0-91b68538df47)

## Nhập dữ liệu demo cho các bảng (nhập có kiểm soát từ tính năng Edit trên UI của mssm)
Các dữ liệu demo của các bảng như sau:
![image](https://github.com/user-attachments/assets/10f185cc-6789-4474-84c4-96274b47beef)
![image](https://github.com/user-attachments/assets/cc915113-e7ef-4ba7-8f5b-b2a78d5f3a13)
![image](https://github.com/user-attachments/assets/fbeed0b2-f73a-4062-ae40-8fa832b571e5)
![image](https://github.com/user-attachments/assets/7ce207b5-646a-478c-a8bc-03bc88568a10)
![image](https://github.com/user-attachments/assets/c8bffc9b-5bb8-4e0a-a8d9-06d1dd5a46e1)
![image](https://github.com/user-attachments/assets/d4fa519e-e6b2-4288-97fa-d063913c3397)
![image](https://github.com/user-attachments/assets/b9b56b43-f2b6-43f2-b694-47d37e36daeb)
![image](https://github.com/user-attachments/assets/ee9a30f5-d897-43bc-813f-c222eb81d75b)

# Viết lệnh truy vấn để: Tính được điểm thành phần của 1 sinh viên đang học tại 1 lớp học phần.
### Lệnh truy vấn này tính điểm thành phần của tất cả sinh viên của tất cả lớp học phần.
  SELECT 
  
      DKMH.MaSV MSSV, 
      
      LopHP.MaLopHP [Mã lớp HP], 
      
      LopHP.TenLopHP [Tên lớp HP], 
      
      DKMH.DiemThi [Điểm thi], 
      
      DKMH.PhanTramThi [Phần trăm thi], 
      
  	  COUNT(Diem.diem) AS [Số điểm thành phần],
   
      AVG(Diem.diem) AS [Điểm thành phần]

      FROM DKMH
  
      LEFT JOIN Diem ON DKMH.id_dk = Diem.id_dk
  
      JOIN LopHP ON DKMH.MaLopHP = LopHP.MaLopHP
  
      GROUP BY DKMH.MaSV, LopHP.MaLopHP, LopHP.TenLopHP, DKMH.DiemThi, DKMH.PhanTramThi
  
      ORDER BY LopHP.MaLopHP;

### Kết quả sau khi chạy lệnh truy vấn trên:
![image](https://github.com/user-attachments/assets/7ff18170-9140-485f-815c-8a46a64c41f2)

# Viết lệnh truy vấn để: Tính được điểm thành phần của 1 sinh viên đang học tại 1 lớp học phần.
### Lệnh truy vấn này tính điểm thành phần của tất cả sinh viên của tất cả lớp học phần.

  SELECT 
  
      DKMH.MaSV MSSV, 
      
      LopHP.MaLopHP [Mã lớp HP], 
      
      LopHP.TenLopHP [Tên lớp HP], 
      
      DKMH.DiemThi [Điểm thi], 
      
      DKMH.PhanTramThi [Phần trăm thi], 
      
  	  COUNT(Diem.diem) AS [Số điểm thành phần],
   
      AVG(Diem.diem) AS [Điểm thành phần]
      
  FROM DKMH
  
  LEFT JOIN Diem ON DKMH.id_dk = Diem.id_dk
  
  JOIN LopHP ON DKMH.MaLopHP = LopHP.MaLopHP
  
  GROUP BY DKMH.MaSV, LopHP.MaLopHP, LopHP.TenLopHP, DKMH.DiemThi, DKMH.PhanTramThi
  
  ORDER BY LopHP.MaLopHP;

 ### Kết quả sau khi chạy lệnh truy vấn trên:
![image](https://github.com/user-attachments/assets/5066220b-aba2-4cea-91f4-48355979b410)



