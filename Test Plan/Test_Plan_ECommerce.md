# KẾ HOẠCH KIỂM THỬ

## Website Swag Labs (Saucedemo.com)

**Phiên bản:** 1.0

**Ngày tạo:** 28/01/2026

**Nhóm:** Nhóm kiểm thử thủ công

**Trạng thái:** Đã phê duyệt

---

## 1. GIỚI THIỆU

Tài liệu này mô tả kế hoạch kiểm thử thủ công cho website Swag Labs (`https://www.saucedemo.com/`). Hệ thống demo này cung cấp các chức năng chính như: đăng nhập, xem danh sách sản phẩm, quản lý giỏ hàng và quy trình checkout.

Mục đích kiểm thử:

* Xác minh các chức năng chính hoạt động đúng theo yêu cầu
* Phát hiện và ghi nhận lỗi
* Đảm bảo độ bao phủ yêu cầu đạt từ 90% trở lên
* Cung cấp báo cáo chất lượng toàn diện trước khi phát hành

---

## 2. PHẠM VI KIỂM THỬ

### 2.1 Trong phạm vi

| Mô-đun                    | Tính năng                          | Mô tả                                                                 |
| ------------------------- | ---------------------------------- | --------------------------------------------------------------------- |
| **Xác thực**             | Đăng nhập vào hệ thống     | Đăng nhập với các tài khoản demo có sẵn, xử lý trường hợp đúng/sai   |
|                           | Đăng xuất hệ thống         | Đăng xuất qua menu bên trái, đảm bảo phiên làm việc được kết thúc    |
|                           | Thông báo lỗi đăng nhập    | Hiển thị và xử lý thông báo khi nhập sai username/password           |
| **Sản phẩm & Giỏ hàng**  | Xem danh sách sản phẩm     | Hiển thị đúng tên, giá, mô tả, hình ảnh trên trang Inventory         |
|                           | Sắp xếp sản phẩm           | Kiểm tra các tuỳ chọn sắp xếp (A to Z, Z to A, Low-High, High-Low)   |
|                           | Xem chi tiết sản phẩm      | Mở trang chi tiết sản phẩm, thông tin và nút Add to cart              |
|                           | Quản lý giỏ hàng           | Thêm/xoá sản phẩm vào/ra giỏ hàng từ nhiều vị trí khác nhau          |
| **Checkout (Thanh toán)**| Nhập thông tin khách hàng  | Nhập First Name, Last Name, Postal Code và kiểm tra tính hợp lệ      |
|                           | Xem lại đơn hàng           | Kiểm tra trang Overview: sản phẩm, số lượng, thuế, tổng tiền         |
|                           | Hoàn tất đặt hàng          | Hoàn tất checkout và hiển thị trang xác nhận đơn hàng                 |
| **Điều hướng & Menu**    | Menu bên trái              | Kiểm tra các mục All Items, About, Logout, Reset App State            |
|                           | Biểu tượng giỏ hàng        | Hiển thị số lượng sản phẩm, điều hướng đúng tới trang giỏ hàng       |

### 2.2 Ngoài phạm vi

* Đăng ký tài khoản và quên mật khẩu (không tồn tại trên website demo)
* Kiểm thử hiệu năng
* Kiểm thử bảo mật nâng cao
* Kiểm thử tự động
* Kiểm thử tải
* Kiểm thử trên thiết bị di động
* Tích hợp cổng thanh toán thực

---

## 3. PHƯƠNG PHÁP KIỂM THỬ

### 3.1 Loại kiểm thử

| Loại kiểm thử             | Mô tả                                | Trọng tâm                           |
| ------------------------- | ------------------------------------ | ----------------------------------- |
| Kiểm thử chức năng        | Kiểm tra các chức năng theo yêu cầu  | Trường hợp đúng, sai, giá trị biên  |
| Kiểm thử giao diện        | Kiểm tra hiển thị và tương tác       | Bố cục, thông báo, kiểm tra dữ liệu |
| Kiểm thử khói             | Kiểm tra nhanh các chức năng cốt lõi | Đảm bảo hệ thống hoạt động          |
| Kiểm thử xác thực dữ liệu | Kiểm tra tính hợp lệ dữ liệu nhập    | Email, mật khẩu, số tiền, địa chỉ   |

### 3.2 Kỹ thuật kiểm thử

* Phân lớp tương đương
* Phân tích giá trị biên
* Bảng quyết định
* Kiểm thử hộp đen

---

## 4. MÔI TRƯỜNG KIỂM THỬ

### 4.1 Cấu hình hệ thống

| Thành phần   | Chi tiết                           |
| ------------ | ---------------------------------- |
| Hệ điều hành | Windows 10 / Windows 11            |
| Trình duyệt  | Google Chrome (phiên bản mới nhất) |
| Độ phân giải | 1920 × 1080                        |
| Kết nối mạng | Internet ổn định                   |

### 4.2 Dữ liệu kiểm thử

| Loại dữ liệu | Chi tiết                                                                 |
| ------------ | ------------------------------------------------------------------------ |
| Tài khoản    | Danh sách tài khoản demo có sẵn trên `https://www.saucedemo.com/`   |
| Sản phẩm     | Danh sách sản phẩm hiển thị trên trang Inventory                |
| Giá cả       | Giá sản phẩm và tổng tiền đúng như hiển thị trên hệ thống       |
| Danh mục     | Không phân loại danh mục, sử dụng danh sách sản phẩm mặc định           |

### 4.3 Công cụ sử dụng

* Công cụ phát triển trình duyệt Chrome
* Google Sheets hoặc Excel để quản lý test case và lỗi
* Ảnh chụp màn hình

---

## 5. ĐIỀU KIỆN VÀO VÀ RA

### 5.1 Điều kiện vào

* Hệ thống đã được triển khai đầy đủ
* Dữ liệu kiểm thử sẵn sàng
* Kế hoạch kiểm thử được phê duyệt
* Môi trường kiểm thử hoạt động ổn định

### 5.2 Điều kiện ra

* Tất cả test case đã được thực thi
* Độ bao phủ yêu cầu đạt từ 90% trở lên
* Tất cả lỗi nghiêm trọng đã được ghi nhận
* Báo cáo kiểm thử hoàn thành
* Tài liệu kiểm thử được lưu trữ

---

## 6. RỦI RO VÀ BIỆN PHÁP GIẢM THIỂU

| Rủi ro                        | Tác động   | Biện pháp                             |
| ----------------------------- | ---------- | ------------------------------------- |
| Dữ liệu kiểm thử không đầy đủ | Cao        | Chuẩn bị trước, có danh sách kiểm tra |
| Thay đổi yêu cầu              | Trung bình | Áp dụng quy trình quản lý thay đổi    |
| Bỏ sót lỗi logic phức tạp     | Trung bình | Tăng cường kiểm thử các luồng chính   |
| Thiếu nhân sự                 | Trung bình | Chia sẻ tài liệu và kiến thức         |
| Phát hiện lỗi muộn            | Cao        | Kiểm thử sớm và thường xuyên          |

---

## 7. VAI TRÒ VÀ TRÁCH NHIỆM

| Vai trò              | Trách nhiệm                              |
| -------------------- | ---------------------------------------- |
| Trưởng nhóm kiểm thử | Quản lý tiến độ, phê duyệt tài liệu      |
| Phân tích kiểm thử   | Thiết kế test case, lập ma trận truy vết |
| Kiểm thử viên        | Thực thi test, ghi nhận lỗi              |
| Quản lý chất lượng   | Báo cáo và quyết định phát hành          |

---

## 8. LỊCH TRÌNH KIỂM THỬ

| Giai đoạn | Công việc                            | Thời gian (ngày) |
| --------- | ------------------------------------ | ---------------- |
| Chuẩn bị  | Thiết kế test case, ma trận truy vết | 3                |
| Thực thi  | Chạy test, ghi nhận lỗi              | 5                |
| Phân tích | Tổng hợp và phân tích kết quả        | 2                |
| Báo cáo   | Hoàn thành báo cáo kiểm thử          | 1                |
| **Tổng**  |                                      | **11**           |

---

## 9. TIÊU CHÍ CHẤT LƯỢNG

Hệ thống **sẵn sàng phát hành** khi:

* 100% test case được thực thi
* Tỷ lệ đạt từ 85% trở lên
* Không còn lỗi nghiêm trọng
* Độ bao phủ yêu cầu từ 90% trở lên
* Mức độ nghiêm trọng và ưu tiên được xác nhận

Hệ thống **chưa sẵn sàng phát hành** khi:

* Còn lỗi nghiêm trọng
* Tỷ lệ đạt dưới 85%
* Độ bao phủ yêu cầu dưới 90%

---

**KẾT THÚC KẾ HOẠCH KIỂM THỬ**
