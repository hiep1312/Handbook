# 🧪 Bài Thực Hành HTML

### **Bài 1 – Form đăng nhập bảo mật**

Tạo form đăng nhập với yêu cầu:

* Gửi dữ liệu đến `/login`
* Không cho trình duyệt tự kiểm tra dữ liệu

**Tên đăng nhập:**

* Không cho trình duyệt gợi ý

**Mật khẩu:**

* Bắt buộc nhập
* Không hiển thị nội dung

**Khi submit:**

* Không reload trang hiện tại
* Mở kết quả ở **tab mới**

---

### **Bài 2 – Form đăng ký tài khoản (chuẩn UX)**

Tạo form đăng ký gồm:

**Họ tên:**

* Tự động viết hoa chữ cái đầu mỗi từ

**Email:**

* Bắt buộc đúng định dạng

**Mật khẩu:**

* Tối thiểu 8 ký tự

* Không cho trình duyệt lưu dữ liệu form

---

### **Bài 3 – Form upload ảnh đại diện**

Tạo form upload ảnh:

* Chỉ cho phép upload **ảnh**
* Có thể chọn **nhiều ảnh**
* Khi chụp ảnh bằng điện thoại:

  * Ưu tiên **camera trước**
* Dữ liệu gửi đi đúng **định dạng upload file**

---

### **Bài 4 – Form gửi phản hồi nhanh**

Tạo form phản hồi:

* Gửi dữ liệu dạng **text thuần**
* Có ô nhập nội dung **dài**
* Không cần validate dữ liệu

**Khi submit:**

* Mở kết quả trong iframe tên `result`

---

### **Bài 5 – Form đặt lịch hẹn**

Tạo form đặt lịch:

**Chọn ngày:**

* Không được nhỏ hơn **ngày hiện tại**

**Chọn giờ:**

* Chỉ cho phép **giờ tròn** (VD: 08:00, 09:00…)

* Trải nghiệm tốt trên **mobile** (bàn phím phù hợp)

---

### **Bài 6 – Form thanh toán**

Tạo form thanh toán:

**Số thẻ:**

* Chỉ cho nhập **số**
* Giới hạn độ dài

**Số tiền:**

* Có bước nhảy cố định

* Không được nhập số âm

* Một nút submit có **hành vi riêng** (khác submit mặc định)

---

### **Bài 7 – Form tìm kiếm nâng cao**

Tạo form tìm kiếm:

* Có input tìm kiếm **chuyên dụng**
* Tắt gợi ý trình duyệt

**Khi submit:**

* Gửi dữ liệu bằng **phương thức phù hợp cho tìm kiếm**

---

### **Bài 8 – Form xác nhận danh tính**

Tạo form xác nhận:

* Họ tên (**chỉ đọc**)
* Ngày sinh

**Upload giấy tờ:**

* Chỉ cho phép **PDF hoặc ảnh**
* Trình duyệt ưu tiên **camera sau** khi chụp

---

### **Bài 9 – Form khảo sát**

Tạo form khảo sát:

* Một câu hỏi: **chọn nhiều đáp án**
* Một câu hỏi: **chỉ chọn 1 đáp án**
* Một câu hỏi: **nội dung dài**
* Có nút **reset form**

---

### **Bài 10 – Form nhiều hành vi submit**

Tạo một form:

* Có **2 nút submit**

Mỗi nút:

* Gửi đến **endpoint khác nhau**

* Cách gửi dữ liệu **khác nhau**

* Một nút **bỏ qua validate**

---

### **Bài 11 – Form mobile-first**

Tạo form đăng ký nhanh:

**Số điện thoại:**

* Hiển thị bàn phím số

**Mã xác nhận:**

* Chỉ cho nhập số

* Độ dài cố định

* Tab di chuyển **đúng thứ tự**

---

### **Bài 12 – Form đăng ký sự kiện**

Tạo form đăng ký:

* Họ tên
* Email

**Ngày tham gia:**

* Chỉ cho chọn trong **tháng hiện tại**

**Số lượng người:**

* Giới hạn **min / max**

---

### **Bài 13 – Form gửi bài tập**

Tạo form nộp bài:

**Upload file:**

* Chỉ nhận **PDF**

**Tên sinh viên:**

* Bắt buộc nhập

* Cho phép gửi **nhiều file**

* Form phải có **thuộc tính name**

---

### **Bài 14 – Form cấu hình hệ thống**

Tạo form cấu hình:

* Bật / tắt tính năng
* Chọn mức độ (1 → 5)

Một số trường:

* Bị **vô hiệu hóa**
* Không cho chỉnh sửa nhưng **vẫn gửi dữ liệu**

---

### **Bài 15 – Form đăng ký newsletter**

Tạo form:

* Chỉ có **email**
* Bắt buộc nhập
* Không cho submit nếu trống
* Gửi dữ liệu đúng **encoding mặc định**

---

### **Bài 16 – Form chọn màu & thời gian**

Tạo form:

* Chọn **màu yêu thích**
* Chọn **thời gian cụ thể**
* Chọn **tuần trong năm**

---

### **Bài 17 – Form quản lý sản phẩm**

Tạo form thêm sản phẩm:

* Tên sản phẩm

**Giá:**

* Bước tăng cố định

**Trạng thái:**

* Còn hàng / Hết hàng

* Ảnh sản phẩm

---

### **Bài 18 – Form điều hướng iframe**

Tạo form:

**Khi submit:**

* Kết quả hiển thị trong **iframe**
* Không reload trang chính

---

### **Bài 19 – Form accessibility**

Tạo form:

* Mọi input đều có **label liên kết**
* Có **mô tả cho người dùng**
* Trình đọc màn hình **hiểu được nội dung**

---

### **Bài 20 – Form kiểm tra dữ liệu nâng cao**

Tạo form:

**Username:**

* Có quy tắc định dạng riêng

**Password:**

* Có yêu cầu độ dài

**Email:**

* Kiểm tra bằng **pattern**

📌 ❌ Không dùng JavaScript

---

### **Bài 21: Regular expressions**

* Chuỗi **bắt đầu bằng chữ**
* **Kết thúc bằng số**

---

### **Bài 22: Regular expressions**

* Chỉ gồm **chữ cái và số**
* Độ dài từ **6 → 12 ký tự**

---

### **Bài 23: Regular expressions**

* Số điện thoại:

  * Chỉ gồm chữ số
  * Độ dài **đúng 10 số**

---

### **Bài 24: Regular expressions**

* Username:

  * Chỉ gồm `a-z`, `0-9`, `_`
  * Không bắt đầu bằng số

---

### **Bài 25: Regular expressions**

* Mật khẩu:

  * Ít nhất 1 chữ số
  * Ít nhất 1 chữ cái
  * Độ dài tối thiểu 8

---

### **Bài 26: Regular expressions**

* Chuỗi **không chứa khoảng trắng**

---

### **Bài 27: Regular expressions**

* Mã sản phẩm:

  * Bắt đầu bằng `SP`
  * Theo sau là **4 chữ số**

---

### **Bài 28: Regular expressions**

* Chỉ chứa **chữ thường**
* Không chứa ký tự đặc biệt

---

### **Bài 29: Regular expressions**

* Bắt đầu và kết thúc bằng **cùng một chữ cái**

---

### **Bài 30: Regular expressions**

* Email đơn giản (không cần RFC)

---

### **Bài 31: Regular expressions**

* Chỉ chứa **chữ cái viết hoa**
* Độ dài **ít nhất 3 ký tự**

---

### **Bài 32: Regular expressions**

* Có ít nhất:

  * 1 chữ thường
  * 1 chữ hoa
* Không chứa chữ số

---

### **Bài 33: Regular expressions**

* Mã đơn hàng:

  * Bắt đầu bằng `ORD`
  * Theo sau **6 → 8 chữ số**

---

### **Bài 34: Regular expressions**

* Không bắt đầu bằng `_`
* Không kết thúc bằng `_`
* Chỉ gồm chữ cái, số và `_`

---

### **Bài 35: Regular expressions**

* Số nguyên dương
* Không có số 0 ở đầu

---

### **Bài 36: Regular expressions**

* Chỉ chứa chữ cái và dấu cách
* Không có **2 dấu cách liên tiếp**

---

### **Bài 37: Regular expressions**

* Mã lớp học: `WEB-XX-YYYY`

  * `WEB` cố định
  * `XX`: chữ in hoa
  * `YYYY`: 4 chữ số

---

### **Bài 38: Regular expressions**

* Bắt đầu bằng chữ
* Có thể chứa số ở giữa
* Kết thúc bằng chữ

---

### **Bài 39: Regular expressions**

* Không chứa ký tự đặc biệt
* Cho phép dấu gạch dưới `_`

---

### **Bài 40: Regular expressions**

* URL đơn giản:

  * Bắt đầu bằng `http://` hoặc `https://`
  * Có tên miền
  * Không cần xử lý query string phức tạp
  
---

📘 *Bài tập cho buổi học 2 – tập trung vào tư duy thuộc tính HTML và biểu thức chính quy.*