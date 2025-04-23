BÀI TẬP VỀ NHÀ 05, Môn Hệ quản trị csdl. K225480106070

SUBJECT: Trigger on ssmsql 

A. Trình bày lại đầu bài của đồ án PT&TKHT:
1. Mô tả bài toán của đồ án PT&TKHT, 
   đưa ra yêu cầu của bài toán đó
2. Cơ sở dữ liệu của Đồ án PT&TKHT :
   Có database với các bảng dữ liệu cần thiết (3nf),
   Các bảng này đã có PK, FK, CK cần thiết
 
B. Nội dung Bài tập 05:
1. Dựa trên cơ sở là csdl của Đồ án
2. Tìm cách bổ xung thêm 1 (hoặc vài) trường phi chuẩn
   (là trường tính toán đc, nhưng thêm vào thì ok hơn,
    ok hơn theo 1 logic nào đó, vd ok hơn về speed)
   => Nêu rõ logic này!
3. Viết trigger cho 1 bảng nào đó, 
   mà có sử dụng trường phi chuẩn này,
   nhằm đạt được 1 vài mục tiêu nào đó.
   => Nêu rõ các mục tiêu 
4. Nhập dữ liệu có kiểm soát, 
   nhằm để test sự hiệu quả của việc trigger auto run.
5. Kết luận về Trigger đã giúp gì cho đồ án của em.

HƯỚNG DẪN CÁCH LÀM:

Hướng dẫn làm phần A: 
 - Chỉ cần nêu ra y/c của đồ án.
 - Không cần chụp quá trình làm ra db, tables.
 - Chỉ cần đưa ra db gồm các bảng nào,
   mỗi bảng có các trường nào, kiểu dữ liệu nào,
   và pk, fk, ck của các bảng.

Hướng dẫn làm phần B:
1. Sv tạo repo mới trên github, cho phép truy cập public.
2. Tạo file Readme.md, đầu file để thông tin cá nhân sv.
3. Tiếp theo đưa phần A vào file Reame.md .
3. Các thao tác làm trên csdl bằng phần mềm ssms.
4. Chụp ảnh màn hình quá trình làm.
5. Paste ngay vào Readme.md, 
   rồi gõ mô tả ảnh này làm gì, nhập gì, hay đạt được điều gì...
6. Có thể thêm những nhận xét hoặc kết luận
   cho việc bản thân đã hiểu rõ thêm về 1 vấn đề gì đó.
7. Lặp lại các step 4 5 6 cho đến khi hoàn thành yêu cầu của phần B.
8. Xuất các file sql chứa cấu trúc và data, up lên cùng repo.
9. Link đến repo cần mở được trực tiếp nội dung, 
   Paste link này vào file excel online ghim trên nhóm.
   Thầy sẽ dùng tool để check các link này.

DEADLINE: 23H59:59 NGÀY 23/04/2025

p/s:
 - Sv được phép tham khảo mọi nguồn, nhưng phải tự làm lại.
 - Đọc thêm nội quy học tập để biết các chế tài.
 - Đã đến lúc khẳng định bản thân và toả sáng!
 - Chỗ nào vướng mắc cứ share lên nhóm để cùng tháo gỡ.

========================================
# Đồ Án: PHÂN TÍCH VÀ THIẾT KẾ HỆ THỐNG QUẢN LÝ TRUNG TÂM TIẾNG ANH

## 1. Mô tả bài toán của đồ án PT&TKHT

### Khảo sát, phân tích hiện trạng của hệ thống:

Tiến hành khảo sát chi tiết quy trình hoạt động hiện tại của trung tâm tiếng Anh (bao gồm quản lý học viên, giáo viên, khóa học, lớp học, lịch học, điểm danh, điểm số, thu chi học phí, báo cáo...) dù đang thực hiện thủ công hay bằng phần mềm cũ.
Xác định các vấn đề tồn tại, hạn chế và điểm nghẽn trong hệ thống hiện tại (ví dụ: tốn thời gian, dễ sai sót, khó tổng hợp báo cáo, thiếu đồng bộ dữ liệu).
Thu thập các dữ liệu định lượng (số lượng học viên, giáo viên, lớp học, tần suất giao dịch...) làm cơ sở cho việc phân tích yêu cầu và đánh giá hiệu quả.
Phân tích hệ thống thông tin:

### Phân tích các yêu cầu nghiệp vụ chi tiết cho hệ thống mới từ các bên liên quan (ban quản lý, nhân viên, giáo viên).
Xác định các chức năng cần thiết của hệ thống mới (quản lý tuyển sinh, quản lý đào tạo, quản lý tài chính, quản lý nhân sự, chức năng báo cáo...).
Phân tích các yêu cầu phi chức năng (hiệu năng, bảo mật, khả năng mở rộng...).
Xây dựng các Use Case hoặc User Story mô tả các tương tác giữa người dùng và hệ thống.
Thiết kế hệ thống Quản lý Trung tâm Tiếng Anh:

### Thiết kế kiến trúc tổng thể của hệ thống (ví dụ: kiến trúc 3 lớp, web-based).
Thiết kế cơ sở dữ liệu (xây dựng mô hình thực thể - kết hợp ERD, xác định cấu trúc chi tiết các bảng dữ liệu).
Thiết kế các module/phân hệ chính của hệ thống và mối quan hệ giữa chúng.
Thiết kế luồng xử lý dữ liệu cho các nghiệp vụ quan trọng.
Thiết kế giao diện người dùng (UI/UX) cho các màn hình chính.
Xây dựng các tệp cơ sở dữ liệu:

### Triển khai thiết kế cơ sở dữ liệu đã hoàn thiện (tạo cấu trúc bảng, định nghĩa khóa chính, khóa ngoại, kiểu dữ liệu, ràng buộc toàn vẹn) trên một hệ quản trị cơ sở dữ liệu (ví dụ: SQL Server, MySQL).
Thực hiện chuẩn hóa dữ liệu để đảm bảo tính nhất quán và giảm dư thừa.
Thiết kế chương trình:

### Thiết kế chi tiết cấu trúc bên trong từng module chức năng (các lớp, phương thức...).
Thiết kế các thuật toán xử lý logic nghiệp vụ phức tạp (ví dụ: thuật toán xếp lịch, tính toán học phí/công nợ...).
Xây dựng mã nguồn (coding) cho các chức năng đã thiết kế.
Thiết kế và triển khai giao diện người dùng theo mẫu đã tạo.
Thiết kế và xây dựng các báo cáo theo yêu cầu.
Lập kế hoạch kiểm thử và thực hiện kiểm thử các chức năng của chương trình.

 # 2. Cơ sở dữ liệu của Đồ án PT&TKHT 
 
Sơ đồ thực thể liên kết:
![image](https://github.com/user-attachments/assets/e5ece73a-235f-4f72-94fc-941271fb37d2)

#B. Nội dung Bài tập











