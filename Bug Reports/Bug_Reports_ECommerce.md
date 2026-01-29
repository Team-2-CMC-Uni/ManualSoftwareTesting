# BÁO CÁO LỖI (BUG REPORTS)
## Hệ Thống Web Bán Hàng Online (E-Commerce)

**Tổng số Bug:** 12  
**Ngày lập báo cáo:** 28/01/2026

---

## BUG #1

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_AUTH_001 |
| **Tiêu đề** | Email validation không chặn được định dạng sai |
| **Mô tả** | Hệ thống cho phép đăng ký với email "user@example..com" (hai dấu chấm) |
| **Các bước tái hiện** | 1. Mở trang đăng ký<br/>2. Nhập email: user@example..com<br/>3. Nhập password: Abc@12345<br/>4. Ấn "Đăng ký" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email không hợp lệ" |
| **Kết quả thực tế** | Tài khoản được tạo thành công |
| **Severity** | **Major** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_AUTH_002 |
| **Hình ảnh/Log** | Screenshot: email_validation_failed.png |

---

## BUG #2

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_AUTH_002 |
| **Tiêu đề** | Mật khẩu không yêu cầu ký tự đặc biệt |
| **Mô tả** | Mật khẩu "abcdefgh" (không có số hay ký tự đặc biệt) vẫn được chấp nhận |
| **Các bước tái hiện** | 1. Ấn "Đăng ký"<br/>2. Nhập email: test@example.com<br/>3. Nhập password: abcdefgh<br/>4. Ấn "Đăng ký" |
| **Kết quả mong đợi** | Yêu cầu mật khẩu phải có ít nhất 1 số và 1 ký tự đặc biệt |
| **Kết quả thực tế** | Đăng ký thành công |
| **Severity** | **Critical** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_AUTH_004 |
| **Ghi chú** | Đây là vấn đề bảo mật |

---

## BUG #3

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CART_001 |
| **Tiêu đề** | Giỏ hàng không cập nhật tổng tiền chính xác |
| **Mô tả** | Tổng tiền hiển thị sai khi có 2 sản phẩm cùng giá |
| **Các bước tái hiện** | 1. Thêm sản phẩm A (giá 100K) vào giỏ x2<br/>2. Thêm sản phẩm B (giá 100K) vào giỏ x1<br/>3. Kiểm tra tổng tiền |
| **Kết quả mong đợi** | Tổng tiền = 300,000đ |
| **Kết quả thực tế** | Tổng tiền = 250,000đ |
| **Severity** | **Critical** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CHECKOUT_007 |
| **Ảnh chụp** | cart_calculation_wrong.png |

---

## BUG #4

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CART_002 |
| **Tiêu đề** | Không kiểm tra tồn kho khi cập nhật số lượng |
| **Mô tả** | Cho phép cập nhật số lượng vượt quá tồn kho |
| **Các bước tái hiện** | 1. Sản phẩm có tồn kho = 5<br/>2. Thêm vào giỏ: 3<br/>3. Cập nhật lại: 10<br/>4. Kiểm tra |
| **Kết quả mong đợi** | Lỗi "Tồn kho không đủ" |
| **Kết quả thực tế** | Số lượng được cập nhật thành 10 |
| **Severity** | **Major** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CART_004 |

---

## BUG #5

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_PRODUCT_001 |
| **Tiêu đề** | Tìm kiếm không phân biệt hoa/thường |
| **Mô tả** | Tìm "LAPTOP" không hiển thị sản phẩm "laptop" |
| **Các bước tái hiện** | 1. Tìm kiếm: "LAPTOP"<br/>2. Kiểm tra kết quả |
| **Kết quả mong đợi** | Hiển thị tất cả sản phẩm có chứa "laptop" |
| **Kết quả thực tế** | Không có kết quả hoặc kết quả không đầy đủ |
| **Severity** | **Minor** |
| **Priority** | **Medium** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_PRODUCT_001 |

---

## BUG #6

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CHECKOUT_001 |
| **Tiêu đề** | Không xác nhận lại địa chỉ trước khi thanh toán |
| **Mô tả** | Dù đã nhập sai địa chỉ, vẫn cho phép đặt hàng |
| **Các bước tái hiện** | 1. Ở trang thanh toán<br/>2. Nhập địa chỉ: "ABC" (3 ký tự)<br/>3. Chọn thanh toán<br/>4. Ấn "Đặt hàng" |
| **Kết quả mong đợi** | Lỗi "Địa chỉ quá ngắn" |
| **Kết quả thực tế** | Đặt hàng thành công |
| **Severity** | **Major** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CHECKOUT_003 |

---

## BUG #7

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CHECKOUT_002 |
| **Tiêu đề** | Mã giảm giá có thể sử dụng nhiều lần |
| **Mô tả** | Cùng một mã giảm giá "SAVE50" được áp dụng cho 3 đơn hàng khác nhau |
| **Các bước tái hiện** | 1. Đặt hàng lần 1: áp dụng "SAVE50"<br/>2. Đặt hàng lần 2: áp dụng "SAVE50" lại<br/>3. Đặt hàng lần 3: áp dụng "SAVE50" lại |
| **Kết quả mong đợi** | Mã "SAVE50" chỉ được dùng 1 lần |
| **Kết quả thực tế** | Cả 3 đơn hàng đều được giảm giá |
| **Severity** | **Critical** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CHECKOUT_008 |
| **Ảnh chụp** | coupon_reused_multiple_times.png |

---

## BUG #8

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_AUTH_003 |
| **Tiêu đề** | Không gửi email xác nhận đăng ký |
| **Mô tả** | Sau khi đăng ký thành công, không nhận được email xác nhận |
| **Các bước tái hiện** | 1. Đăng ký tài khoản: user@example.com<br/>2. Chờ 5 phút<br/>3. Kiểm tra email |
| **Kết quả mong đợi** | Nhận email xác nhận từ hệ thống |
| **Kết quả thực tế** | Không nhận được email |
| **Severity** | **Major** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_AUTH_001 |

---

## BUG #9

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_PRODUCT_002 |
| **Tiêu đề** | Ảnh sản phẩm không load trong chi tiết |
| **Mô tả** | Trang chi tiết sản phẩm không hiển thị ảnh sản phẩm |
| **Các bước tái hiện** | 1. Mở trang danh sách sản phẩm<br/>2. Ấn vào sản phẩm "iPhone 14"<br/>3. Chờ trang chi tiết load |
| **Kết quả mong đợi** | Hiển thị ảnh sản phẩm rõ ràng |
| **Kết quả thực tế** | Chỉ hiển thị icon "broken image" |
| **Severity** | **Major** |
| **Priority** | **Medium** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_PRODUCT_007 |

---

## BUG #10

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CHECKOUT_003 |
| **Tiêu đề** | Email xác nhận đơn hàng chứa thông tin sai |
| **Mô tả** | Email xác nhận hiển thị sai tổng giá tiền |
| **Các bước tái hiện** | 1. Đặt hàng với tổng = 250,000đ<br/>2. Kiểm tra email xác nhận |
| **Kết quả mong đợi** | Email hiển thị tổng = 250,000đ |
| **Kết quả thực tế** | Email hiển thị tổng = 200,000đ |
| **Severity** | **Minor** |
| **Priority** | **Medium** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CHECKOUT_015 |

---

## BUG #11

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_PRODUCT_003 |
| **Tiêu đề** | Filter giá không reset khi thay đổi danh mục |
| **Mô tả** | Khi chuyển sang danh mục khác, filter giá vẫn giữ giá trị cũ |
| **Các bước tái hiện** | 1. Lọc Electronics: 500K-2M<br/>2. Chuyển sang danh mục Fashion<br/>3. Kiểm tra lại filter |
| **Kết quả mong đợi** | Filter giá được reset về mặc định |
| **Kết quả thực tế** | Filter vẫn giữ 500K-2M |
| **Severity** | **Minor** |
| **Priority** | **Low** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_PRODUCT_005, TC_PRODUCT_004 |

---

## BUG #12

| Trường | Chi Tiết |
|--------|---------|
| **Bug ID** | BUG_CART_003 |
| **Tiêu đề** | Nút "Thanh toán" vẫn hiển thị khi giỏ rỗng |
| **Mô tả** | Sau khi xoá tất cả sản phẩm, nút "Thanh toán" vẫn được click |
| **Các bước tái hiện** | 1. Xoá tất cả sản phẩm khỏi giỏ<br/>2. Kiểm tra nút "Thanh toán" |
| **Kết quả mong đợi** | Nút "Thanh toán" bị vô hiệu hóa |
| **Kết quả thực tế** | Nút vẫn hoạt động, bấm vào báo lỗi |
| **Severity** | **Major** |
| **Priority** | **High** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10, Chrome 120 |
| **Test Case Liên Quan** | TC_CART_008 |

---

## 3. PHÂN TÍCH BUG

### 3.1 Phân Bố theo Severity

| Severity | Số Lượng | % | Màu |
|----------|---------|-----|-----|
| **Critical** | 3 | 25% | 🔴 |
| **Major** | 6 | 50% | 🟠 |
| **Minor** | 3 | 25% | 🟡 |
| **Trivial** | 0 | 0% | 🟢 |

✅ **Yêu cầu:** ≥2 Critical (Có 3) ✅  
✅ **Yêu cầu:** ≥4 Major (Có 6) ✅

### 3.2 Phân Bố theo Module

| Module | Critical | Major | Minor | Tổng |
|--------|----------|-------|-------|------|
| **Authentication** | 1 | 2 | 0 | 3 |
| **Product & Cart** | 0 | 3 | 2 | 5 |
| **Checkout** | 2 | 1 | 1 | 4 |
| **TỔNG** | **3** | **6** | **3** | **12** |

### 3.3 Phân Bố theo Priority

| Priority | Số Lượng | % |
|----------|---------|-----|
| **High** | 9 | 75% |
| **Medium** | 3 | 25% |
| **Low** | 0 | 0% |

### 3.4 Phân Bố theo Loại Lỗi

| Loại | Bug ID | Số Lượng |
|------|--------|---------|
| **Validation** | BUG_AUTH_001, BUG_CHECKOUT_001 | 2 |
| **Calculation** | BUG_CART_001 | 1 |
| **Inventory** | BUG_CART_002 | 1 |
| **Security** | BUG_AUTH_002, BUG_CHECKOUT_002 | 2 |
| **Email** | BUG_AUTH_003, BUG_CHECKOUT_003 | 2 |
| **UI/UX** | BUG_PRODUCT_001, BUG_PRODUCT_002, BUG_PRODUCT_003, BUG_CART_003 | 4 |

---

## 4. BUG ĐƯỢC ƯU TIÊN KHẮC PHỤC TRƯỚC

### Giai Đoạn 1: Critical (Phải sửa ngay)
1. **BUG_AUTH_002** - Mật khẩu không yêu cầu ký tự đặc biệt (Bảo mật)
2. **BUG_CART_001** - Tính tổng tiền sai (Business logic)
3. **BUG_CHECKOUT_002** - Mã giảm giá dùng nhiều lần (Business logic)

### Giai Đoạn 2: Major (Nên sửa trước release)
4. BUG_AUTH_001 - Email validation sai
5. BUG_CART_002 - Không kiểm tra tồn kho
6. BUG_CHECKOUT_001 - Địa chỉ quá ngắn
7. BUG_AUTH_003 - Email xác nhận không gửi
8. BUG_PRODUCT_002 - Ảnh sản phẩm không load
9. BUG_CART_003 - Nút thanh toán vẫn click khi giỏ rỗng

### Giai Đoạn 3: Minor (Có thể sửa sau)
10. BUG_PRODUCT_001 - Tìm kiếm không phân biệt hoa/thường
11. BUG_CHECKOUT_003 - Email xác nhận hiển thị sai giá
12. BUG_PRODUCT_003 - Filter giá không reset

---

## 5. KẾ HOẠCH KHẮC PHỤC

| Phase | Mục Tiêu | Deadline | Người Phụ Trách |
|-------|---------|----------|-----------------|
| **Phase 1** | Sửa 3 bugs Critical | 2-3 ngày | Dev Lead |
| **Phase 2** | Sửa 6 bugs Major | 4-5 ngày | Dev Team |
| **Phase 3** | Sửa 3 bugs Minor | Tuỳ chọn | Dev Team |
| **Retesting** | Xác nhận bug được sửa | 2 ngày | QA Team |

---

## KẾT LUẬN

- **Tổng Bug:** 12 (Yêu cầu: ≥10) ✅
- **Critical bugs:** 3 (Yêu cầu: ≥2) ✅
- **Major bugs:** 6 (Yêu cầu: ≥4) ✅
- **Tất cả bug đều có thể tái hiện** ✅
- **Severity & Priority hợp lý** ✅

**Quyết định Release:** ❌ **NO-RELEASE** cho đến khi sửa hết 3 bugs Critical

---

**END OF BUG REPORTS**
