# Câu lệnh Select
Bài tập 06 của sinh viên: K225480106057 - Phạm Mạnh Quỳnh - môn Hệ Quản Trị CSDL
- Bài tập 6: Hệ quản trị CSDL
- Chủ đề: Câu lệnh Select
- Yêu cầu bài tập: 
- Cho file sv_tnut.sql (1.6MB)
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
------------------------------------------------------------------------------------------------------------------------------
1. Các bước để import được dữ liệu trong sv_tnut.sql vào sql:
- Bước 1: mở SSMS và kết nối tới SQL Server
- Bước 2: Sau khi kết nối thành công, trên thanh công cụ, chọn _file ---> open ---> file..._
![Screenshot 2025-04-25 152138](https://github.com/user-attachments/assets/a80fd6ee-7ef2-4737-aace-cd684305982d)
- Một cửa sổ mới sẽ hiện ra. Trong cửa sổ đó, tìm nơi lưu file SQL đã tải và bấm _open_
![Screenshot 2025-04-25 152504](https://github.com/user-attachments/assets/c3245884-6e74-4c87-b92b-b70b230667c9)

- Bước 3: Tạo database có tên _sv_tnut_ để phủ hợp với câu lệnh _USE [sv_tnut]_ của thầy( _USE [sv_tnut]_ là lệnh sử dụng Database ):
![Screenshot 2025-04-25 152856](https://github.com/user-attachments/assets/5230dfe9-fc42-4864-8bbb-9d4f16253ed0)
- Bước 4: Bôi đen đoạn tạo các bảng trong code để tạo các bảng cho database:
![Screenshot 2025-04-25 153038](https://github.com/user-attachments/assets/4c4aefd5-ce1e-4b61-9d3e-af924397051d)

- Chúng ta thu được một bảng có tên SV:
  
![Screenshot 2025-04-25 153308](https://github.com/user-attachments/assets/d5022aa1-4d97-482c-80db-39d3390e05f2)

- Bước 5: chọn toàn bộ các đoạn code còn lại, là đoạn code để thêm dữ liệu vào bảng, và chạy chúng:
![Screenshot 2025-04-25 153623](https://github.com/user-attachments/assets/199ef66c-56da-48be-9948-82b2825e05df)

- Kết quả được bảng có dữ liệu như sau:
![Screenshot 2025-04-25 153725](https://github.com/user-attachments/assets/fd341da1-7c66-4322-8328-8ad29570870a)

2. Truy vấn ra thông tin của em (Phạm Mạnh Quỳnh) với dữ liệu đầu vào là tên, sdt, ngày tháng năm sinh:
- Chọn _new query_ để code các truy vấn
- Dùng câu lenh SELECT để chọn các trường phù hợp với yêu cầu thông tin của em:
![Screenshot 2025-04-25 154724](https://github.com/user-attachments/assets/277cb376-bcec-4953-b5d5-a234fe0b4595)

3. Truy vấn những sinh viên trùng hoàn toàn ngày, tháng, năm sinh với em:
- dùng câu lệnh day, month, year để lấy được ngày, tháng, năm từ cột ns có kiểu Date để so sánh:
![Screenshot 2025-04-25 160035](https://github.com/user-attachments/assets/ba0fc388-27b8-4558-b485-ffbf7bd32ffc)

4. Truy vấn những sinh viên trùng ngày, tháng sinh với em:
![Screenshot 2025-04-25 161216](https://github.com/user-attachments/assets/2fc19a44-8de7-48ec-aeb2-f88bd733eee0)

5. Truy vấn những sinh viên trùng tháng, năm sinh với em:
![Screenshot 2025-04-25 161327](https://github.com/user-attachments/assets/965a9ece-1097-48fa-a225-4f3e32d82121)

6. Truy vấn những sinh viên trùng tên với em:
![Screenshot 2025-04-25 161535](https://github.com/user-attachments/assets/6cf3375a-da7b-41b6-80ac-c5d0c4c8fe20)

7. Truy vấn những sinh viên trùng họ và tên đệm với em:
![Screenshot 2025-04-25 161732](https://github.com/user-attachments/assets/8c304db2-652d-44e2-8ea8-1e352d85cac4)

8. Truy vấn những sv có sđt sai khác chỉ 1 số so với sđt của em:
![Screenshot 2025-04-25 162940](https://github.com/user-attachments/assets/433c18cf-2351-4ba1-a624-61f2ae2130c6)
- trong bảng không có ai khác chỉ 1 số trong sdt so với em.
9. LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG VIỆT:
![Screenshot 2025-04-25 163537](https://github.com/user-attachments/assets/a6d8699f-c2f6-4afb-a08c-55bbfe7abaa0)
- Giải thích:
  + where lop like '%KMT%': tìm trong cột _lop_ xem có chuỗi string nào chứa chuỗi ký tự 'KMT' thì lấy ra.
  + collate Vietnamese_CI_AS : Sắp xêp tên và họ đệm kiểu tiếng Việt theo thứ tự từ A-->Z.
10. LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV:
![Screenshot 2025-04-25 165337](https://github.com/user-attachments/assets/77979cc3-de66-4411-b7b1-c6af05fd6b9e)
- Giải thích:
  + Đầu tiên, e lọc ra các sinh viên thuộc nghành KMT( trong đó có cả các sinh viên KTP vì KTP cũng là sinh viên KMT)
  + Tiếp theo, e nhờ chat lọc ra các sinh viên có tên là nữ trong danh sách( có thể có sai sót vì cũng có một số sinh viên có tên giống nữ như em =)) )
  + Tiếp theo, e đưa các tên vào code để lọc ra các sinh viên có thể là nữ trong nghành KMT.
  + Vì có thể có sai sót về tên nên sau đó em có thể loại bỏ những sinh viên là nam, ví dụ như em :)
![Screenshot 2025-04-25 170447](https://github.com/user-attachments/assets/c9201281-d056-49a4-a53e-06a4c98265a9)
- em vẫn còn giữ lại đoạn code xắp xếp tên để nhìn cho đẹp mắt.
