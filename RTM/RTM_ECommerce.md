# MA TRẬN TRUY VẾT YÊU CẦU (RTM)
## Website Swag Labs (Saucedemo.com) + Demo E-Commerce

**Ngày tạo:** 28/01/2026  
**Phiên bản:** 1.0 (điều chỉnh cho Swag Labs)

---

## 1. PHẦN A – RTM CHO SWAG LABS [Thực tế]

Phần này bạn sẽ **tự hoàn thiện** dựa trên luồng thực tế của `https://www.saucedemo.com/`.  
Gợi ý một số yêu cầu chính (Req ID bắt đầu bằng `R_SWAG_`):

| Req ID | Mô Tả Yêu Cầu | Test Case ID | Loại | Trạng Thái |
|--------|---------------|--------------|------|-----------|
| **R_SWAG_1** | Người dùng đăng nhập thành công với tài khoản demo hợp lệ | TC_SWAG_AUTH_001 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_2** | Hệ thống chặn đăng nhập với user bị khoá | TC_SWAG_AUTH_003 **[Thực tế]** | Negative | To be covered |
| **R_SWAG_3** | Người dùng có thể đăng xuất an toàn qua menu | TC_SWAG_AUTH_004 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_4** | Trang Inventory hiển thị đúng danh sách sản phẩm | TC_SWAG_INV_001 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_5** | Chức năng sort theo tên/giá hoạt động đúng | TC_SWAG_INV_002<br/>TC_SWAG_INV_003 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_6** | Người dùng xem được chi tiết sản phẩm | TC_SWAG_INV_004 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_7** | Người dùng thêm/xoá sản phẩm trong giỏ và xem giỏ hàng | TC_SWAG_CART_001<br/>TC_SWAG_CART_002 **[Thực tế]** | Positive | To be covered |
| **R_SWAG_8** | Quy trình checkout (bắt buộc nhập thông tin, overview, hoàn tất) hoạt động đúng | TC_SWAG_CHECKOUT_001<br/>TC_SWAG_CHECKOUT_002 **[Thực tế]** | Positive<br/>Negative | To be covered |

> Khi thực hành, bạn hãy:
> - Cập nhật cột **Test Case ID** khi thêm/xoá test case trong `Test_Cases_ECommerce.md`  
> - Cập nhật cột **Trạng Thái** (Covered/Not Covered) sau khi hoàn thiện test case **[Thực tế]**

---

## 2. PHẦN B – BẢNG RTM DEMO CHO HỆ THỐNG E-COMMERCE (GIỮ NGUYÊN LÀM MẪU)

| Req ID | Mô Tả Yêu Cầu | Test Case ID | Loại | Trạng Thái |
|--------|---------------|--------------|------|-----------|
| **R1** | Người dùng đăng ký bằng email hợp lệ | TC_AUTH_001<br/>TC_AUTH_006 | Positive<br/>Negative | Covered |
| **R2** | Không cho đăng ký khi email sai định dạng | TC_AUTH_002<br/>TC_AUTH_004 | Negative<br/>Boundary | Covered |
| **R3** | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_003<br/>TC_AUTH_004<br/>TC_AUTH_005 | Boundary<br/>Boundary<br/>Negative | Covered |
| **R4** | Đăng nhập thành công với thông tin hợp lệ | TC_AUTH_007<br/>TC_AUTH_010<br/>TC_AUTH_015 | Positive<br/>Negative<br/>Security | Covered |
| **R5** | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_008<br/>TC_AUTH_009 | Negative<br/>Negative | Covered |
| **R6** | Quên mật khẩu gửi email đặt lại | TC_AUTH_011<br/>TC_AUTH_012 | Positive<br/>Negative | Covered |
| **R7** | Tìm kiếm hiển thị đúng kết quả | TC_PRODUCT_001<br/>TC_PRODUCT_002<br/>TC_PRODUCT_003 | Positive<br/>Negative<br/>Negative | Covered |
| **R8** | Lọc theo giá hoạt động đúng | TC_PRODUCT_004<br/>TC_PRODUCT_005<br/>TC_PRODUCT_006 | Positive<br/>Positive<br/>Negative | Covered |
| **R9** | Xem chi tiết sản phẩm | TC_PRODUCT_007<br/>TC_PRODUCT_008 | Positive<br/>Positive | Covered |
| **R10** | Thêm sản phẩm vào giỏ thành công | TC_CART_001<br/>TC_CART_002<br/>TC_CART_003<br/>TC_CART_004 | Positive<br/>Negative<br/>Boundary<br/>Negative | Covered |
| **R11** | Cập nhật số lượng trong giỏ | TC_CART_005<br/>TC_CART_006 | Positive<br/>Positive | Covered |
| **R12** | Xoá sản phẩm khỏi giỏ | TC_CART_007<br/>TC_CART_008 | Positive<br/>Positive | Covered |
| **R13** | Thanh toán bắt buộc nhập địa chỉ | TC_CHECKOUT_002<br/>TC_CHECKOUT_003<br/>TC_CHECKOUT_004 | Negative<br/>Boundary<br/>Boundary | Covered |
| **R14** | Chọn phương thức thanh toán | TC_CHECKOUT_005<br/>TC_CHECKOUT_006<br/>TC_CHECKOUT_001 | Positive<br/>Negative<br/>Positive | Covered |
| **R15** | Đặt hàng thành công | TC_CHECKOUT_001<br/>TC_CHECKOUT_007<br/>TC_CHECKOUT_008<br/>TC_CHECKOUT_009<br/>TC_CHECKOUT_015 | Positive<br/>Positive<br/>Positive<br/>Negative<br/>Positive | Covered |
| **R16** | Lưu lịch sử đơn hàng | TC_CHECKOUT_010<br/>TC_CHECKOUT_011<br/>TC_CHECKOUT_012<br/>TC_CHECKOUT_013<br/>TC_CHECKOUT_014 | Positive<br/>Positive<br/>Positive<br/>Positive<br/>Negative | Covered |

---

## 3. TÓM LƯỢC COVERAGE (PHẦN DEMO)

| Số Thứ Tự | Yêu Cầu | Số TC Áp Dụng | Trạng Thái |
|-----------|--------|--------------|-----------|
| 1 | R1 | 2 | ✅ Covered |
| 2 | R2 | 2 | ✅ Covered |
| 3 | R3 | 3 | ✅ Covered |
| 4 | R4 | 3 | ✅ Covered |
| 5 | R5 | 2 | ✅ Covered |
| 6 | R6 | 2 | ✅ Covered |
| 7 | R7 | 3 | ✅ Covered |
| 8 | R8 | 3 | ✅ Covered |
| 9 | R9 | 2 | ✅ Covered |
| 10 | R10 | 4 | ✅ Covered |
| 11 | R11 | 2 | ✅ Covered |
| 12 | R12 | 2 | ✅ Covered |
| 13 | R13 | 3 | ✅ Covered |
| 14 | R14 | 3 | ✅ Covered |
| 15 | R15 | 5 | ✅ Covered |
| 16 | R16 | 5 | ✅ Covered |
| **TỔNG** | **16 Yêu Cầu** | **42 Mapping** | **100% Coverage** |

---

## 4. PHÂN TÍCH CHI TIẾT (PHẦN DEMO)

### 3.1 Yêu Cầu Được Bao Phủ (Coverage Rate)

- **Tổng số yêu cầu:** 16
- **Yêu cầu được bao phủ:** 16
- **Yêu cầu không được bao phủ:** 0
- **Coverage %:** **100%** ✅ (Vượt quá mục tiêu 90%)

### 3.2 Phân Bố Test Case Theo Yêu Cầu

- **Yêu cầu có 2 TC:** R1, R2, R5, R6, R9, R11, R12 (7 yêu cầu)
- **Yêu cầu có 3 TC:** R4, R7, R8, R13, R14 (5 yêu cầu)
- **Yêu cầu có 4 TC:** R10 (1 yêu cầu)
- **Yêu cầu có 5 TC:** R15, R16 (2 yêu cầu)

**Kết luận:** Mỗi yêu cầu được áp dụng bởi tối thiểu 2 test case ✅

### 3.3 Loại Test Case Phân Bố Theo Module

| Module | Positive | Negative | Boundary | Total |
|--------|----------|----------|----------|-------|
| Authentication | 6 | 7 | 2 | 15 |
| Product & Cart | 13 | 5 | 2 | 20 |
| Checkout | 9 | 4 | 2 | 15 |
| **TỔNG** | **28** | **16** | **6** | **50** |

---

## 5. CHỈ SỐ CHẤT LƯỢNG RTM (PHẦN DEMO)

| Chỉ Số | Giá Trị | Tiêu Chí | Kết Quả |
|-------|--------|---------|---------|
| Coverage % | 100% | ≥ 90% | ✅ Pass |
| Traceability | 50 TC → 16 Req | Toàn bộ Req | ✅ Pass |
| Độ bao phủ tối thiểu | 2 TC/Req | ≥ 2 TC/Req | ✅ Pass |
| Số Test Case | 50 | ≥ 45 | ✅ Pass |

---

## 6. GIAO CẢNH RỦI RO KHÔNG ĐƯỢC BỌC (PHẦN DEMO)

**Không có yêu cầu nào bị bỏ sót.**

Tất cả 16 yêu cầu đều có đủ test case bao phủ cả positive, negative, và boundary case.

---

## 7. KẾ HOẠCH ĐIỀU CHỈNH RTM

### 6.1 Quy Trình Cập Nhật

Khi có thay đổi yêu cầu:
1. Cập nhật RTM
2. Tạo test case mới nếu cần
3. Kiểm tra lại coverage %
4. Thông báo đội QA

### 6.2 Traceability Bidirectional

- **Forward Traceability:** Requirement → Test Case ✅
- **Backward Traceability:** Test Case → Requirement ✅

---

## KẾT LUẬN

✅ **RTM hoàn thành với:**
- Coverage 100% (vượt mục tiêu 90%)
- Mỗi yêu cầu được bao phủ bởi ≥2 test case
- Phân bố balanced giữa Positive/Negative/Boundary
- Bidirectional traceability được thiết lập

---

**END OF RTM**
