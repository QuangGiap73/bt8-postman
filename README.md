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

# BƯỚC 2 : LẤY CHI TIẾT BÀI VIẾT (GET)
  Mở postman -> get -> nhập URl : https://jsonplaceholder.typicode.com/posts/1 -> send 
  
  ![Ảnh chụp màn hình 2025-06-19 163704](https://github.com/user-attachments/assets/e4627425-a5be-4df0-be31-27a859e7f014)
#BƯỚC 3: THÊM BÀI VIẾT MỚI (POST)
  POST-> vào tab body-> chọn raw -> json -> bấm send để xem kết quả
  ```
{
  "title": "Bài viết mới",
  "body": "Nội dung bài viết",
  "userId": 1
    }
```
![image](https://github.com/user-attachments/assets/f844a934-e79c-482f-a761-a6fdad8bad34)

# BƯỚC 4: CẬP NHẬT BÀI VIẾT (PUT)
  Pust -> body(json)
   ```
{
  "id": 1,
  "title": "Bài viết cập nhật",
  "body": "Nội dung mới",
  "userId": 1
}
```
  ![Ảnh chụp màn hình 2025-06-19 163933](https://github.com/user-attachments/assets/4c301a54-f30d-4dc6-b466-62ccc559234f)
# BƯỚC 5: XOÁ BÀI VIẾT (DELETE)
  DELETE->send
  ![Ảnh chụp màn hình 2025-06-19 164014](https://github.com/user-attachments/assets/95bcda73-361b-47c6-9f75-dd9666c3012e)
# BƯỚC 6: TEST TỰ ĐỘNG (tab "Tests")
  Post-> scripts -> json
  ```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response must be JSON", function () {
    pm.response.to.be.json;
});

pm.test("Check response has id", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property("id");
});

  

  

