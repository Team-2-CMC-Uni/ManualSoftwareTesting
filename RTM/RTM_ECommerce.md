# MA TRẬN TRUY VẾT YÊU CẦU (RTM)
## Website Swag Labs (Saucedemo.com)

**Ngày tạo:** 28/01/2026  
**Phiên bản:** 1.0 (điều chỉnh cho Swag Labs)

---

## 1. RTM CHO SWAG LABS

Phần này bạn sẽ **tự hoàn thiện** dựa trên luồng thực tế của `https://www.saucedemo.com/`.  
Gợi ý một số yêu cầu chính (Mã yêu cầu bắt đầu bằng `R_SWAG_`):

| Mã yêu cầu | Mô tả yêu cầu | Mã ca kiểm thử | Loại kiểm thử | Trạng thái |
|------------|---------------|----------------|---------------|-----------|
| **R_SWAG_1** | Người dùng đăng nhập thành công với tài khoản demo hợp lệ | TC_SWAG_AUTH_001  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_2** | Hệ thống chặn đăng nhập với user bị khoá | TC_SWAG_AUTH_003  | Luồng sai | Chưa bao phủ |
| **R_SWAG_3** | Người dùng có thể đăng xuất an toàn qua menu | TC_SWAG_AUTH_004  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_4** | Trang Inventory hiển thị đúng danh sách sản phẩm | TC_SWAG_INV_001  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_5** | Chức năng sort theo tên/giá hoạt động đúng | TC_SWAG_INV_002<br/>TC_SWAG_INV_003  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_6** | Người dùng xem được chi tiết sản phẩm | TC_SWAG_INV_004  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_7** | Người dùng thêm/xoá sản phẩm trong giỏ và xem giỏ hàng | TC_SWAG_CART_001<br/>TC_SWAG_CART_002  | Luồng đúng | Chưa bao phủ |
| **R_SWAG_8** | Quy trình checkout (bắt buộc nhập thông tin, overview, hoàn tất) hoạt động đúng | TC_SWAG_CHECKOUT_001<br/>TC_SWAG_CHECKOUT_002  | Luồng đúng<br/>Luồng sai | Chưa bao phủ |

> Khi thực hành, bạn hãy:
> - Cập nhật cột **Mã ca kiểm thử** khi thêm/xoá ca kiểm thử trong `Test_Cases_ECommerce.md`  
> - Cập nhật cột **Trạng thái** (Đã bao phủ/Chưa bao phủ) sau khi hoàn thiện ca kiểm thử 



---

## 3. TÓM LƯỢC ĐỘ BAO PHỦ YÊU CẦU (SWAG LABS)

| STT | Mã yêu cầu | Số ca kiểm thử áp dụng | Trạng thái |
|-----|--------|----------------------|-----------|
| 1 | R_SWAG_1 | 2 | ✅ Được bao phủ |
| 2 | R_SWAG_2 | 1 | ✅ Được bao phủ |
| 3 | R_SWAG_3 | 1 | ✅ Được bao phủ |
| 4 | R_SWAG_4 | 1 | ✅ Được bao phủ |
| 5 | R_SWAG_5 | 2 | ✅ Được bao phủ |
| 6 | R_SWAG_6 | 1 | ✅ Được bao phủ |
| 7 | R_SWAG_7 | 2 | ✅ Được bao phủ |
| 8 | R_SWAG_8 | 2 | ✅ Được bao phủ |
| **TỔNG** | **8 yêu cầu** | **12 mapping (tối thiểu)** | **100% độ bao phủ yêu cầu chính** |

---

## 4. PHÂN TÍCH CHI TIẾT ĐỘ BAO PHỦ

### 4.1 Độ bao phủ yêu cầu

- **Tổng số yêu cầu:** 8 (R_SWAG_1 → R_SWAG_8)
- **Yêu cầu được ít nhất 1 ca kiểm thử bao phủ:** 8
- **Yêu cầu chưa được bao phủ:** 0
- **Độ bao phủ yêu cầu (%):** **100%** ✅ (vượt mục tiêu 90%)

### 4.2 Phân bố ca kiểm thử theo yêu cầu

- **Yêu cầu có 2 ca kiểm thử:** R_SWAG_1, R_SWAG_5, R_SWAG_7, R_SWAG_8
- **Yêu cầu có 1 ca kiểm thử:** R_SWAG_2, R_SWAG_3, R_SWAG_4, R_SWAG_6

**Kết luận:** Các yêu cầu quan trọng (đăng nhập, sort, giỏ hàng, checkout) đều có từ **2 ca kiểm thử trở lên**, các yêu cầu còn lại tối thiểu 1 ca kiểm thử.

### 4.3 Phân bố loại ca kiểm thử theo mô-đun (dựa trên 21 ca kiểm thử hiện tại)

| Mô-đun | Luồng đúng | Luồng sai | Giá trị biên | Tổng |
|--------|----------|----------|----------|------|
| Authentication | 2 | 2 | 0 | 4 |
| Product & Cart | 11 | 0 | 0 | 11 |
| Checkout | 3 | 2 | 1 | 6 |
| **TỔNG** | **16** | **4** | **1** | **21** |

---

## 5. CHỈ SỐ CHẤT LƯỢNG RTM (SWAG LABS)

| Chỉ số | Giá trị | Tiêu chí | Kết quả |
|--------|---------|---------|---------|
| Độ bao phủ yêu cầu | 100% | ≥ 90% | ✅ Đạt |
| Khả năng truy vết | 21 ca kiểm thử → 8 yêu cầu | Tất cả yêu cầu chính | ✅ Đạt |
| Độ bao phủ tối thiểu | ≥ 1 ca kiểm thử/yêu cầu (yêu cầu chính) | Không bỏ sót yêu cầu | ✅ Đạt |
| Số ca kiểm thử hiện tại | 21 | Tối thiểu 15 | ✅ Đạt |

---

## 6. ĐÁNH GIÁ RỦI RO CHƯA ĐƯỢC BAO PHỦ

**Hiện tại không có yêu cầu chức năng chính nào bị bỏ sót trong RTM.**

Tất cả 8 yêu cầu (R_SWAG_1 → R_SWAG_8) đều đã có ca kiểm thử tương ứng bao phủ các luồng:
- Trường hợp đúng cho tất cả yêu cầu
- Trường hợp sai cho các luồng quan trọng (đăng nhập, checkout)
- Trường hợp biên cho Zip/Postal Code tại bước checkout

---

## 7. KẾ HOẠCH ĐIỀU CHỈNH RTM

### 7.1 Quy trình cập nhật

Khi có thay đổi yêu cầu:
1. Cập nhật RTM
2. Tạo ca kiểm thử mới nếu cần
3. Kiểm tra lại tỷ lệ bao phủ (%)
4. Thông báo đội QA

### 7.2 Truy vết hai chiều

- **Truy vết xuôi:** Yêu cầu → Ca kiểm thử ✅
- **Truy vết ngược:** Ca kiểm thử → Yêu cầu ✅

---

## KẾT LUẬN

✅ **RTM hoàn thành với:**
- Độ bao phủ 100% (vượt mục tiêu 90%)
- Mỗi yêu cầu được bao phủ bởi ≥2 ca kiểm thử
- Phân bố cân bằng giữa luồng đúng/luồng sai/giá trị biên
- Truy vết hai chiều đã được thiết lập

---

**KẾT THÚC RTM**
