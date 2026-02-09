# KẾ HOẠCH KIỂM THỬ

## Hệ Thống Web Bán Hàng Online (Thương mại điện tử)

**Phiên bản:** 1.0
**Ngày tạo:** 28/01/2026
**Nhóm:** Nhóm kiểm thử thủ công
**Trạng thái:** Đã phê duyệt

---

## 1. GIỚI THIỆU

Tài liệu này mô tả kế hoạch kiểm thử thủ công cho hệ thống website bán hàng online. Hệ thống cung cấp các chức năng chính như: xác thực người dùng, quản lý sản phẩm và giỏ hàng, xử lý thanh toán.

Mục đích kiểm thử:

* Xác minh các chức năng chính hoạt động đúng theo yêu cầu
* Phát hiện và ghi nhận lỗi
* Đảm bảo độ bao phủ yêu cầu đạt từ 90% trở lên
* Cung cấp báo cáo chất lượng toàn diện trước khi phát hành

---

## 2. PHẠM VI KIỂM THỬ

### 2.1 Trong phạm vi

| Mô-đun                  | Tính năng                   | Mô tả                                        |
| ----------------------- | --------------------------- | -------------------------------------------- |
| **Xác thực**            | Đăng ký tài khoản           | Tạo tài khoản mới bằng email và mật khẩu     |
|                         | Đăng nhập                   | Xác thực thông tin đăng nhập                 |
|                         | Quên mật khẩu               | Gửi email đặt lại mật khẩu                   |
|                         | Đăng xuất                   | Kết thúc phiên làm việc                      |
| **Sản phẩm & Giỏ hàng** | Tìm kiếm sản phẩm           | Hiển thị kết quả tìm kiếm chính xác          |
|                         | Lọc theo giá/danh mục       | Lọc sản phẩm theo điều kiện                  |
|                         | Xem chi tiết sản phẩm       | Hiển thị đầy đủ thông tin                    |
|                         | Quản lý giỏ hàng            | Thêm, cập nhật, xoá sản phẩm                 |
| **Thanh toán**          | Nhập địa chỉ giao hàng      | Kiểm tra và xác thực dữ liệu địa chỉ         |
|                         | Chọn phương thức thanh toán | Thanh toán khi nhận hàng / Thẻ Visa mô phỏng |
|                         | Đặt hàng                    | Tạo đơn hàng thành công                      |
|                         | Lịch sử đơn hàng            | Xem danh sách đơn hàng đã mua                |

### 2.2 Ngoài phạm vi

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
* Kiểm thử hộp trắng

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

| Loại dữ liệu | Chi tiết                                 |
| ------------ | ---------------------------------------- |
| Tài khoản    | 10 tài khoản kiểm thử                    |
| Sản phẩm     | Trên 50 sản phẩm                         |
| Giá cả       | Từ 50.000đ đến 5.000.000đ                |
| Danh mục     | Điện tử, Thời trang, Gia dụng, Thực phẩm |

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
