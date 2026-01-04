# Thẻ `<a>` trong HTML (Anchor Tag)

## 📌 Menu điều hướng

* [Giới thiệu thẻ `<a>`](#giới-thiệu-thẻ-a)
* [Bảng tổng quan thuộc tính](#bảng-tổng-quan-thuộc-tính)
* [Chi tiết từng thuộc tính](#chi-tiết-từng-thuộc-tính)

    * [`href`](#href)
    * [`download`](#download)
    * [`target`](#target)
    * [`referrerpolicy`](#referrerpolicy)

---

## Giới thiệu thẻ `<a>`

Thẻ `<a>` (anchor) dùng để **tạo liên kết** giữa các tài nguyên:

* Trang web khác
* File tải xuống
* Hành động hệ thống (gọi điện, gửi email, SMS)
* Điều hướng trong cùng trang

Cú pháp cơ bản:

```html
<a href="https://example.com">Đi đến Example</a>
```

---

## Bảng tổng quan thuộc tính

| Thuộc tính                          | Trạng thái  | Mô tả                                          |
| ----------------------------------- | ----------- | ---------------------------------------------- |
| [`href`](#href)                     | ✅ Standard | Xác định địa chỉ hoặc hành động của liên kết   |
| [`download`](#download)             | ✅ Standard | Yêu cầu tải tài nguyên thay vì mở              |
| [`target`](#target)                 | ✅ Standard | Xác định nơi mở liên kết                       |
| [`referrerpolicy`](#referrerpolicy) | ✅ Standard | Kiểm soát thông tin trang trước đó được gửi đi |

---

## Chi tiết từng thuộc tính

### `href`

Thuộc tính **quan trọng nhất** của thẻ `<a>`.
Xác định **đích đến** của liên kết.

#### Các dạng phổ biến

##### 1. Liên kết trang web

```html
<a href="https://google.com">Google</a>
```

**Kết quả:** Mở trang Google

---

##### 2. Gọi điện (`tel:`)

```html
<a href="tel:0123456789">Gọi ngay</a>
```

**Kết quả:**

* Trên điện thoại: mở trình gọi điện
* Trên máy tính: gọi qua ứng dụng hỗ trợ (Skype, v.v.)

---

##### 3. Gửi email (`mailto:`)

```html
<a href="mailto:test@gmail.com">Gửi email</a>
```

**Kết quả:** Mở ứng dụng email mặc định

---

##### 4. Gửi SMS (`sms:`)

```html
<a href="sms:0123456789">Gửi SMS</a>
```

**Kết quả:** Mở ứng dụng nhắn tin trên thiết bị hỗ trợ

---

### `download`

Dùng để **yêu cầu trình duyệt tải file** thay vì mở.

```html
<a href="/files/report.pdf" download>Download file</a>
```

Chỉ định tên file khi tải về:

```html
<a href="/files/report.pdf" download="BaoCao.pdf">Download</a>
```

**Lưu ý:**

* Hoạt động tốt nhất với cùng origin
* Có thể bị trình duyệt chặn với tài nguyên cross-origin

---

### `target`

Xác định **nơi mở liên kết**.

| Giá trị   | Mô tả                                        |
| --------- | -------------------------------------------- |
| `_self`   | (Mặc định) Mở trong ngữ cảnh hiện tại        |
| `_blank`  | Mở trong tab / cửa sổ mới                    |
| `_parent` | Mở trong frame(khung) cha                    |
| `_top`    | Mở trong cửa sổ trình duyệt hiện tại         |
| `name`    | Mở trong iframe hoặc tab có `name` tương ứng |

Ví dụ:

```html
<a href="https://example.com" target="_blank">Mở tab mới</a>
```

**Kết quả:** Trang được mở ở tab mới

---

### `referrerpolicy`

Kiểm soát **thông tin URL trang hiện tại** (referrer) được gửi kèm khi click link.

> [!NOTE] \
> Rất quan trọng trong **bảo mật & quyền riêng tư**.

#### Các giá trị

| Giá trị                           | Mô tả                          |
| --------------------------------- | ------------------------------ |
| `no-referrer` | Không gửi **bất kỳ thông tin referrer nào** về trang hiện tại cho trang đích. |
| `no-referrer-when-downgrade` | Không gửi **bất kỳ thông tin referrer nào** nếu trang đích không phải **https** (Tức là **http (Không bảo mật)**). |
| `origin` | Gửi thông tin referrer **giới hạn** của trang hiện tại, chỉ bao gồm: **scheme (http/https), host và port**. Không gửi path, query hay hash. |
| `origin-when-cross-origin` | Nếu **cùng origin** thì gửi **đầy đủ thông tin referrer**. Nếu **khác origin** thì chỉ gửi thông tin referrer **giới hạn (scheme + host + port)**. |
| `same-origin` | Chỉ gửi thông tin referrer khi **truy cập cùng origin**. Nếu liên kết sang website khác thì **không gửi gì cả**. |
| `strict-origin` | Chỉ gửi thông tin referrer **giới hạn (scheme + host + port)** khi **mức độ bảo mật không thay đổi**. HTTPS → HTTPS thì gửi, HTTPS → HTTP thì **không gửi**. |
| `strict-origin-when-cross-origin` | *(Mặc định)* Nếu **cùng origin** thì gửi **đầy đủ thông tin referrer**. Nếu **khác origin nhưng HTTPS → HTTPS** thì gửi thông tin referrer **giới hạn (scheme + host + port)**. Nếu **HTTPS → HTTP** thì **không gửi**. |
| `unsafe-url` | Luôn gửi **đầy đủ thông tin referrer** cho mọi trang, bất kể **không bảo mật** hay **khác origin**. (**Không an toàn**) |

Ví dụ:

```html
<a href="https://external.com" referrerpolicy="no-referrer">
  Đi ra ngoài mà không lộ nguồn
</a>
```

**Kết quả:** Trang đích **không biết** bạn đến từ đâu

---

## ✅ Tổng kết

* `<a>` không chỉ là link – mà còn là **công cụ điều hướng, bảo mật và hành động hệ thống**
* `href` quyết định hành vi
* `target` quyết định trải nghiệm người dùng
* `referrerpolicy` quyết định mức độ riêng tư
