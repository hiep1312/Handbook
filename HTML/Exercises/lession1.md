# 🧪 Bài Thực Hành HTML

## **Bài 1 – Liên kết hành động (Action Link)**

Bạn đang làm một trang **liên hệ cho trung tâm đào tạo**.

### Yêu cầu:

* Tạo **3 liên kết văn bản** với nội dung hiển thị lần lượt là:

  * Liên hệ qua điện thoại
  * Liên hệ qua email
  * Nhắn tin nhanh
* Khi người dùng nhấn:

  * Liên kết thứ nhất **gọi điện** đến số: `0909123456`
  * Liên kết thứ hai **mở trình gửi email** đến: `test@gmail.com`
  * Liên kết thứ ba **mở trình nhắn tin SMS** đến cùng số điện thoại trên
* ❌ Không được dùng JavaScript

---

## **Bài 2 – Download nâng cao**

Bạn có một file trên server:

```
/files/internal/lesson1-intro.pdf
```

### Yêu cầu:

* Tạo một liên kết với nội dung hiển thị: **Tải tài liệu buổi 1**
* Khi người dùng tải về:

  * File phải được đổi tên thành: `HTML_Buoi_1_Co_Ban.pdf`
  * **Không cho phép file mở trực tiếp trên trình duyệt**

---

## **Bài 3 – Referrer Policy**

Website hiện tại:

```
https://my-learning-site.com
```

### Yêu cầu:

* Tạo một liên kết dẫn đến **Facebook**
* Khi người dùng click:

  * Facebook **KHÔNG được biết** trang web người dùng đến từ đâu
  * **Chỉ gửi referrer khi truy cập cùng nguồn gốc**
  * Liên kết phải **mở tab mới**

📌 **Yêu cầu bắt buộc:**

* ❌ Không dùng `<meta>` tag
* ✅ Chỉ xử lý **trực tiếp trên thẻ `<a>`**

---

## **Bài 4 – Referrer Downgrade**

Giả sử:

* Trang hiện tại chạy trên **HTTPS**
* Có một link trỏ tới trang **HTTP** (không bảo mật)

### Yêu cầu:

* Tạo liên kết sao cho:

  * HTTPS → HTTPS → **Vẫn gửi referrer**
  * HTTPS → HTTP → **KHÔNG gửi referrer**

---

## **Bài 5 – Target + iframe**

Cho đoạn HTML sau:

```html
<iframe name="viewer" width="600" height="400"></iframe>
```

### Yêu cầu:

* Tạo **2 liên kết**:

  * Click → mở `page-a.html` **bên trong iframe**
  * Click → mở `page-b.html` **ở tab mới**

---

## **Bài 6 – Iframe lồng nhau**

### Cấu trúc trang:

* `index.html`

  * Chứa iframe `name="outer"`
* `outer.html`

  * Chứa iframe `name="inner"`
* `inner.html`

  * Có một liên kết `<a>`

### Yêu cầu:

* Từ liên kết trong **iframe inner**:

  * Mở một trang mới **thay thế toàn bộ trang `index.html`**
* Từ **index.html**:

  * Tạo một liên kết để mở `help.html` **bên trong iframe inner**

📌 ❌ Không dùng JavaScript

---

## **Bài 7 – Semantic Layout thực tế**

Bạn đang xây dựng trang **Blog cá nhân**.

### Yêu cầu:

* Trang phải có:

  * Khu vực **tiêu đề website**
  * **Nội dung chính**
  * Một **bài viết độc lập**
  * Một khu vực hiển thị:

    * Thông tin tác giả
    * Bài viết liên quan
  * **Phần chân trang**
* ❌ Không dùng `<div>` cho bố cục chính
* ✅ Chỉ dùng **semantic HTML**

---

## **Bài 8 – Table Logic**

Tạo bảng **thời khóa biểu học viên** với yêu cầu:

* Hàng đầu tiên là **tiêu đề**
* Cột đầu tiên là **Thứ**
* Một môn học kéo dài **2 buổi liên tiếp**
* Một ô thể hiện **giáo viên dạy nhiều lớp**

---

## **Bài 9 – Table + colgroup**

Tạo bảng **danh sách học viên** gồm:

* STT
* Họ tên
* Email
* Điểm

### Yêu cầu:

* Cột **STT**:

  * Căn giữa
* Cột **Email**:

  * Nền màu xám nhạt
* Cột **Điểm**:

  * Canh phải
* ❌ Không dùng CSS

---

## **Bài 10 – Form + Input nâng cao**

Tạo **form đăng ký tài khoản** với các yêu cầu:

### Họ tên:

* Tự động focus khi tải trang
* Tắt gợi ý trình duyệt

### Số điện thoại:

* Hiển thị **bàn phím số trên mobile**

### Email:

* Có **validate theo chuẩn email**

### Ảnh đại diện:

* Chỉ cho phép chọn **ảnh**

### Tất cả input:

* Phải liên kết với `<label>`

📌 ❌ Không dùng JavaScript, ❌ Không dùng CSS

## **Bài 11: Bảng báo cáo doanh thu**

Trang báo cáo doanh thu theo **quý** cho cửa hàng.

### Yêu cầu:

* Bảng có tiêu đề cột:

  * Quý 1, Quý 2, Quý 3, Quý 4
* Một hàng **tổng doanh thu cả năm**
* Doanh thu **Quý 2 và Quý 3 gộp chung** cho một khu vực
* Hàng **"Tổng năm"** phải hiển thị rõ ràng, tách biệt dữ liệu chính

📌 *Gợi mở:* học viên cần suy nghĩ về **gộp ô (`rowspan`, `colspan`)** và cấu trúc bảng

---

## **Bài 12: Bảng phân quyền hệ thống**

Hiển thị bảng **phân quyền người dùng** cho admin.

### Yêu cầu:

* Cột đầu tiên: **Tên chức năng**
* Các cột tiếp theo:

  * Admin
  * Editor
  * Viewer
* Một chức năng có thể được phép cho **nhiều vai trò**
* Phần tiêu đề vai trò phải **nằm riêng**, không lẫn dữ liệu

---

## **Bài 13: Bảng lịch học tuần**

Tạo bảng **lịch học tuần** với điều kiện:

* Cột đầu tiên là **Thứ**
* Mỗi ngày gồm:

  * Sáng
  * Chiều
* Một môn học kéo dài **cả sáng và chiều**
* Một giáo viên dạy **nhiều ngày liên tiếp**

---

📘 *Bài tập cho buổi học 1 – tập trung vào tư duy cấu trúc, không sử dụng JavaScript hay CSS.*