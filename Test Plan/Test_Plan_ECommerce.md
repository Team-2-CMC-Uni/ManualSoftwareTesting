# KẾ HOẠCH KIỂM THỬ (TEST PLAN)
## Hệ Thống Web Bán Hàng Online (E-Commerce)

**Phiên bản:** 1.0  
**Ngày tạo:** 28/01/2026  
**Nhóm:** Manual Testing Group  
**Trạng thái:** Approved

---

## 1. GIỚI THIỆU (Introduction)

Tài liệu này mô tả kế hoạch kiểm thử thủ công (Manual QA) cho hệ thống website bán hàng online (E-Commerce). Hệ thống này cung cấp các tính năng cơ bản: xác thực người dùng, quản lý sản phẩm & giỏ hàng, và xử lý thanh toán.

Mục đích của bài kiểm thử là:
- Xác minh các tính năng chính hoạt động đúng
- Phát hiện và ghi nhận các lỗi (bug)
- Đảm bảo độ bao phủ yêu cầu ≥ 90%
- Cung cấp báo cáo chất lượng toàn diện trước khi release

---

## 2. PHẠM VI KIỂM THỬ (Scope)

### 2.1 Trong Phạm Vi (In-Scope)

| Module | Tính Năng | Mô Tả |
|--------|----------|-------|
| **Authentication** | Đăng ký tài khoản | Tạo tài khoản mới với email & mật khẩu |
| | Đăng nhập | Xác thực tên đăng nhập & mật khẩu |
| | Quên mật khẩu | Gửi email để đặt lại mật khẩu |
| | Đăng xuất | Kết thúc phiên làm việc |
| **Product & Cart** | Tìm kiếm sản phẩm | Hiển thị kết quả tìm kiếm chính xác |
| | Lọc theo giá/danh mục | Lọc sản phẩm theo điều kiện |
| | Xem chi tiết sản phẩm | Hiển thị đầy đủ thông tin sản phẩm |
| | Quản lý giỏ hàng | Thêm/cập nhật/xoá sản phẩm |
| **Checkout** | Nhập địa chỉ giao hàng | Xác thực dữ liệu địa chỉ |
| | Chọn phương thức thanh toán | COD / Visa giả lập |
| | Đặt hàng | Xử lý tạo đơn hàng |
| | Lịch sử đơn hàng | Xem danh sách đơn hàng đã mua |

### 2.2 Ngoài Phạm Vi (Out-of-Scope)

- Kiểm thử hiệu suất (Performance Testing)
- Kiểm thử bảo mật nâng cao (Advanced Security)
- Kiểm thử tự động (Automation Testing)
- Kiểm thử tải (Load Testing)
- Kiểm thử di động (Mobile Testing)
- Tích hợp với cổng thanh toán thực

---

## 3. PHƯƠNG PHÁP KIỂM THỬ (Test Approach)

### 3.1 Loại Kiểm Thử

| Loại | Mô Tả | Trọng Tâm |
|------|-------|----------|
| **Functional Testing** | Kiểm thử các chức năng cơ bản | Positive, Negative, Boundary |
| **UI Testing** | Kiểm thử giao diện người dùng | Hiển thị, tương tác, validation |
| **Smoke Testing** | Kiểm thử hồi quy cơ bản | Đảm bảo các tính năng chính hoạt động |
| **Validation Testing** | Kiểm thử kiểm định dữ liệu | Email, mật khẩu, số tiền, địa chỉ |

### 3.2 Kỹ Thuật Kiểm Thử

- **Equivalence Partitioning:** Phân chia dữ liệu vào các lớp tương đương
- **Boundary Value Analysis:** Kiểm thử giá trị biên
- **Decision Table Testing:** Kiểm thử các kết hợp điều kiện
- **BlackBox Testing:** Kiểm thử kết quả
- **WhiteBox Testing:** Kiểm thử chi tiết dòng lệnh

---

## 4. MÔI TRƯỜNG KIỂM THỬ (Test Environment)

### 4.1 Cấu Hình Hệ Thống

| Thành phần | Chi tiết |
|-----------|---------|
| **Hệ điều hành** | Windows 10/11 |
| **Trình duyệt** | Chrome (phiên bản mới nhất) |
| **Độ phân giải** | 1920 x 1080 px |
| **Kết nối mạng** | Internet bình thường |

### 4.2 Dữ Liệu Kiểm Thử

| Loại Dữ Liệu | Chi tiết |
|-------------|---------|
| **Tài khoản** | Tài khoản giả lập (10+ tài khoản test) |
| **Sản phẩm** | 50+ sản phẩm với các loại khác nhau |
| **Giá cả** | Từ 50,000đ - 5,000,000đ |
| **Danh mục** | Electronics, Fashion, Home, Food |

### 4.3 Công Cụ Sử Dụng

- Chrome DevTools (kiểm tra UI, console)
- Google Sheet hoặc Excel (quản lý test case, bug)
- Ảnh chụp màn hình (Screenshots)

---

## 5. ĐIỀU KIỆN VÀO / RA (Entry & Exit Criteria)

### 5.1 Điều Kiện Vào (Entry Criteria)

-  Hệ thống được triển khai đầy đủ
-  Dữ liệu test được chuẩn bị sẵn
-  Kế hoạch kiểm thử được phê duyệt
-  Môi trường kiểm thử sẵn sàng

### 5.2 Điều Kiện Ra (Exit Criteria)

-  Tất cả test case đã được thực thi
-  Yêu cầu (Requirements) có độ bao phủ ≥ 90%
-  Tất cả bug Critical đã được ghi nhận
-  Test report hoàn thành
-  Các biên bản kiểm thử được lưu trữ

---

## 6. RỦI RO & BIỆN PHÁP GIẢM THIỂU (Risks & Mitigation)

| Rủi Ro | Tác Động | Biện Pháp Giảm Thiểu |
|--------|----------|-------------------|
| **Dữ liệu test không chuẩn bị đầy đủ** | Cao | Chuẩn bị trước, có danh sách kiểm tra |
| **Thay đổi yêu cầu giữa kiểm thử** | Trung | Có quy trình điều khiển thay đổi |
| **Lỗi logic phức tạp bị bỏ sót** | Trung | Kiểm thử kỹ các luồng xử lý chính |
| **Thành viên nhóm bị ốm/vắng** | Trung | Lập tài liệu chi tiết, chia sẻ kiến thức |
| **Phát hiện bug quá muộn** | Cao | Kiểm thử sớm, thường xuyên |

---

## 7. VAI TRÒ & TRÁCH NHIỆM (Roles & Responsibilities)

| Vai Trò | Trách Nhiệm |
|---------|-----------|
| **Test Lead** | Giám sát tiến độ, phê duyệt tài liệu |
| **Test Analyst** | Thiết kế test case, lập RTM |
| **Tester** | Thực thi test, ghi nhận bug |
| **QA Manager** | Báo cáo tiến độ, quyết định release |

---

## 8. LỊCH TRÌNH KIỂM THỬ (Test Schedule)

| Giai Đoạn | Công Việc | Thời Gian (Ngày) |
|-----------|----------|-----------------|
| **Chuẩn bị** | Thiết kế test case, RTM | 3 |
| **Thực thi** | Chạy test case, ghi bug | 5 |
| **Phân tích** | Phân tích kết quả, viết báo cáo | 2 |
| **Báo cáo** | Hoàn thành test report, metrics | 1 |
| **Tổng** | | **11 ngày** |

---

## 9. TIÊU CHÍ CHẤT LƯỢNG (Quality Criteria)

Hệ thống được coi là **SẴN SÀNG RELEASE** khi:

- Test execution rate = 100%  
- Pass rate ≥ 85%  
- Không có bug Critical còn mở  
- RTM coverage ≥ 90%  
- Severity & Priority được xác nhận  

Hệ thống được coi là **KHÔNG SẴN SÀNG RELEASE** khi:

- Còn bug Critical  
- Pass rate < 85%  
- RTM coverage < 90%  

---

**END OF TEST PLAN**
