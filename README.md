## Tên dự án : Test Collection of APIs
## Ngày kiểm tra : 16/06/2025
## Người kiểm tra : Võ Quang Giáp
1. Mục Tiêu Kiểm Thử: Sử dụng Postman để kiểm thử một API thực tế
  Dùng Postman để gửi request tới một API thật, kiểm thử đầy đủ:

   Lấy danh sách bài viết

   Lấy chi tiết 1 bài

   Tạo bài viết (nếu API cho phép)

   Update, Xoá bài viết (nếu có quyền)

3. Môi Trường Kiểm Thử: Postman.

4. Phương Pháp Kiểm Thử: Kiểm thử tự động và thủ công trên phần mềm Postman.
# API THẬT DÙNG ĐỂ THỬ NGHIỆM: 

https://jsonplaceholder.typicode.com

# Bước 1: LẤY DANH SÁCH BÀI VIẾT (GET)
  Mở postman -> get -> nhập URl : https://jsonplaceholder.typicode.com/posts -> send 

  kết quả : Trả về danh sách bài viết 
![Ảnh chụp màn hình 2025-06-19 163704](https://github.com/user-attachments/assets/e4627425-a5be-4df0-be31-27a859e7f014)

# Bước 2: Lấy chi tiết một bài viết (GET)
  Mở postman -> get -> nhập URl : https://jsonplaceholder.typicode.com/posts/1 -> send 
  ![Ảnh chụp màn hình 2025-06-19 163704](https://github.com/user-attachments/assets/e4627425-a5be-4df0-be31-27a859e7f014)
# Bước 3: Thêm bài viết mới (POST)
  POST-> vào tab body-> chọn raw -> json
  ```
{
  "title": "Bài viết mới",
  "body": "Nội dung bài viết",
  "userId": 1
    }
```
  
  

