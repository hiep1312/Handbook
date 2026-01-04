# Thẻ `<table>` trong HTML

## 📌 Menu điều hướng

* [Giới thiệu thẻ `<table>`](#giới-thiệu-thẻ-table)
* [Bảng tổng quan thuộc tính](#bảng-tổng-quan-thuộc-tính)
* [Chi tiết từng thuộc tính](#chi-tiết-từng-thuộc-tính)

    * [`align`](#align)
    * [`bgcolor`](#bgcolor)
    * [`border`](#border)
    * [`cellpadding`](#cellpadding)
    * [`cellspacing`](#cellspacing)
    * [`frame`](#frame)
    * [`rules`](#rules)
    * [`width`](#width)

---

## Giới thiệu thẻ `<table>`

Thẻ `<table>` dùng để **biểu diễn dữ liệu dạng bảng** (hàng & cột).

👉 Trong HTML5, **tất cả các thuộc tính liên quan đến tạo kiểu (style) đều đã bị <a href="#deprecated">Deprecated</a>** và phải thay thế bằng **CSS**.

Cú pháp cơ bản:

```html
<table>
  <tr>
    <td>Dữ liệu</td>
  </tr>
</table>
```

---

## Bảng tổng quan thuộc tính

| Thuộc tính                    | Trạng thái    | Mô tả                               | Thay thế bằng CSS      |
| ----------------------------- | ------------- | ----------------------------------- | ---------------------- |
| [`align`](#align)             | ⚠️ Deprecated | Căn chỉnh bảng                      | `margin`, `text-align` |
| [`bgcolor`](#bgcolor)         | ⚠️ Deprecated | Màu nền bảng                        | `background-color`     |
| [`border`](#border)           | ⚠️ Deprecated | Xác định viền bảng                  | `border`               |
| [`cellpadding`](#cellpadding) | ⚠️ Deprecated | Khoảng cách giữa nội dung và viền ô | `padding`              |
| [`cellspacing`](#cellspacing) | ⚠️ Deprecated | Khoảng cách giữa các ô              | `border-spacing`       |
| [`frame`](#frame)             | ⚠️ Deprecated | Kiểu viền ngoài bảng                | `border`, `outline`    |
| [`rules`](#rules)             | ⚠️ Deprecated | Đường kẻ giữa các ô                 | `border`               |
| [`width`](#width)             | ⚠️ Deprecated | Chiều rộng bảng                     | `width`, `max-width`   |

---

## Chi tiết từng thuộc tính

### `align`

⚠️ **<a href="#deprecated">Deprecated</a>** – dùng để căn chỉnh bảng trong HTML cũ.

#### Giá trị

* `left`: Căn bảng về bên trái
* `center`: Căn bảng ra giữa
* `right`: Căn bảng về bên phải

```html
<table align="center"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  margin: 0 auto;
}
```

---

### `bgcolor`

⚠️ **<a href="#deprecated">Deprecated</a>** – thiết lập màu nền cho bảng.

```html
<table bgcolor="#eee"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  background-color: #eee;
}
```

---

### `border`

⚠️ **<a href="#deprecated">Deprecated</a>** – xác định viền bảng.

#### Giá trị

* `1`: Có viền
* `0`: Không viền

```html
<table border="1"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  border: 1px solid #333;
}
```

---

### `cellpadding`

⚠️ **<a href="#deprecated">Deprecated</a>** – khoảng cách giữa nội dung và viền ô.

```html
<table cellpadding="10"></table>
```

✅ **Thay thế bằng CSS**:

```css
td, th {
  padding: 10px;
}
```

---

### `cellspacing`

⚠️ **<a href="#deprecated">Deprecated</a>** – khoảng cách giữa các ô.

```html
<table cellspacing="5"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  border-spacing: 5px;
}
```

---

### `frame`

⚠️ **<a href="#deprecated">Deprecated</a>** – xác định kiểu viền ngoài của bảng.

#### Giá trị

* `void`: Không viền
* `above`: Viền trên
* `below`: Viền dưới
* `hsides`: Viền trên & dưới
* `vsides`: Viền trái & phải
* `lhs`: Viền trái
* `rhs`: Viền phải
* `box`: Viền đầy đủ

```html
<table frame="box"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  border: 1px solid #333;
}
```

---

### `rules`

⚠️ **<a href="#deprecated">Deprecated</a>** – xác định đường kẻ giữa các hàng/cột.

#### Giá trị

* `none`: Không kẻ
* `rows`: Kẻ theo hàng
* `cols`: Kẻ theo cột
* `all`: Kẻ tất cả
* `groups`: Kẻ theo nhóm

```html
<table rules="all"></table>
```

✅ **Thay thế bằng CSS**:

```css
td, th {
  border: 1px solid #333;
}
```

---

### `width`

⚠️ **<a href="#deprecated">Deprecated</a>** – xác định chiều rộng bảng.

```html
<table width="600"></table>
```

✅ **Thay thế bằng CSS**:

```css
table {
  width: 600px;
}
```

## 📘 Thuật ngữ:

> <span id="deprecated"> **Deprecated** </span> là một thuật ngữ dùng để chỉ những tính năng:
>
> * ✔️ **Vẫn còn hoạt động** trong trình duyệt hiện tại
> * ⚠️ **Không còn được khuyến nghị sử dụng** trong các dự án mới
> * 🕰️ **Có thể bị loại bỏ hoàn toàn** trong các phiên bản hoặc tiêu chuẩn tương lai

## ✅ Tổng kết

* Các thuộc tính tạo kiểu của `<table>` **đã bị Deprecated hoàn toàn**
* HTML chỉ nên dùng cho **cấu trúc & ngữ nghĩa**
* CSS chịu trách nhiệm **tạo kiểu & giao diện**
* Hiểu các thuộc tính Deprecated giúp **đọc & bảo trì code cũ** tốt hơn
