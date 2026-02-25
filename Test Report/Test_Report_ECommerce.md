# BÁO CÁO KIỂM THỬ
## Website Swag Labs (Saucedemo.com) 


---

## 1. TỔNG QUAN KIỂM THỬ 

### 1.1 Thông Tin Chung 

| Thông Tin | Chi Tiết |
|-----------|---------|
| **Hệ thống** | Website Swag Labs (`https://www.saucedemo.com/`) |
| **Phiên bản kiểm thử** | v1.0 (luyện tập) |
| **Ngày bắt đầu** |  **20/02/2026** |
| **Ngày kết thúc** |  **22/02/2026** |
| **Tổng thời gian** |  **2 ngày** |
| **Kiểm thử viên** | Toàn thể nhóm 2 |
| **Trình duyệt** | Chrome, Brave |
| **Hệ điều hành** | Windows 10/11 |

### 1.2 Mục Tiêu Kiểm Thử

✅ Xác minh tất cả chức năng chính hoạt động đúng  
✅ Phát hiện lỗi (bug) trong hệ thống  
✅ Đảm bảo độ bao phủ yêu cầu ≥ 90%  
✅ Cung cấp báo cáo chất lượng để quyết định phát hành

---

## 2. KẾT QUẢ KIỂM THỬ TỔNG THỂ 

### 2.1 Thống kê thực thi kiểm thử

| Chỉ số | Giá trị |
|--------|--------|
| **Tổng số ca kiểm thử** | **21** *(theo `Test_Cases_ECommerce.md`)* |
| **Đã thực thi** |  **21** |
| **Tỷ lệ thực thi** |  **100%** |

### 2.2 Kết quả chi tiết 

| Trạng Thái | Số Lượng | % | Biểu Tượng |
|-----------|---------|------|-----------|
| **Đạt** |  **16** | 76% | ✅ |
| **Không đạt** |  **4** | 24% | ❌ |
| **Bị chặn** | 0 | 0% | 🚫 |
| **Bỏ qua** | 0 | 0% | ⏭️ |

**Tỷ lệ đạt:**  **76%** (Mục tiêu: ≥85%)  
**Tỷ lệ không đạt:**  **24%**

### 2.3 Kết quả theo mô-đun

| Mô-đun | Tổng số ca kiểm thử | Đạt | Không đạt | Tỷ lệ đạt | Tỷ lệ không đạt |
|--------|---------|------|------|--------|--------|
| **Authentication (Đăng nhập/Đăng xuất)** | 4 |  **2** |  **2** | 50% | 50% |
| **Product & Cart (Sản phẩm & Giỏ hàng)** | 11 |  **11** |  **0** | 100% | 0% |
| **Checkout (Thanh toán)** | 6 |  **3** |  **2** | 60% | 40% |
| **TỔNG** | 21 |  **16** |  **4** | 76% | 24% |

---

## 3. CHI TIẾT KẾT QUẢ THEO MÔ-ĐUN (SWAG LABS – KHUNG ĐIỀN SỐ LIỆU)

Phần này dùng để điền kết quả thực tế dựa trên **21 ca kiểm thử** trong `Test_Cases_ECommerce.md`.

### 3.1 Mô-đun: Authentication (4 ca kiểm thử)

| TC_ID | Tiêu đề | Kết quả | Bug ID (nếu có) |
|-------|---------|---------|-----------------|
| **TC_SWAG_AUTH_001** | Đăng nhập thành công với tài khoản demo hợp lệ | ✅ / ❌ | - |
| **TC_SWAG_AUTH_002** | Đăng nhập thất bại khi mật khẩu không chính xác | ✅ / ❌ | BUG_SWAG_AUTH_001 |
| **TC_SWAG_AUTH_003** | Đăng nhập với user bị khóa | ✅ / ❌ | BUG_SWAG_AUTH_002 |
| **TC_SWAG_AUTH_004** | Đăng xuất hệ thống qua menu trái | ✅ / ❌ | BUG_SWAG_AUTH_003 |

**Tóm tắt mô-đun Authentication:** điền nhận xét thực tế sau khi kiểm thử.

### 3.2 Mô-đun: Product & Cart (11 ca kiểm thử)

| TC_ID | Tiêu đề | Kết quả | Bug ID (nếu có) |
|-------|---------|---------|-----------------|
| **TC_SWAG_INV_001** | Hiển thị đúng danh sách sản phẩm sau khi login | ✅ / ❌ | - |
| **TC_SWAG_INV_002** | Sort theo Name (A→Z, Z→A) | ✅ / ❌ | BUG_SWAG_INV_001 |
| **TC_SWAG_INV_003** | Sort theo Price (low to high, high to low) | ✅ / ❌ | BUG_SWAG_INV_002 |
| **TC_SWAG_INV_004** | Xem chi tiết một sản phẩm từ Inventory | ✅ / ❌ | BUG_SWAG_PROD_001 |
| **TC_SWAG_CART_001** | Thêm sản phẩm vào giỏ từ trang Inventory | ✅ / ❌ | BUG_SWAG_CART_001 |
| **TC_SWAG_CART_002** | Xem chi tiết giỏ hàng | ✅ / ❌ | BUG_SWAG_CART_002 |
| **TC_PRODUCT_007** | Xem chi tiết sản phẩm (Mô-đun 2) | ✅ / ❌ | BUG_SWAG_PROD_001 |
| **TC_CART_001** | Thêm sản phẩm vào giỏ thành công (Mô-đun 2) | ✅ / ❌ | BUG_SWAG_CART_001 |
| **TC_CART_005** | Xem giỏ hàng (Mô-đun 2) | ✅ / ❌ | BUG_SWAG_CART_002 |
| **TC_CART_007** | Xóa sản phẩm khỏi giỏ (Mô-đun 2) | ✅ / ❌ | BUG_SWAG_CART_003 |
| **TC_CART_008** | Giỏ hàng trống (Mô-đun 2) | ✅ / ❌ | BUG_SWAG_CART_003 |

**Tóm tắt mô-đun Product & Cart:** điền nhận xét thực tế sau khi kiểm thử.

### 3.3 Mô-đun: Checkout (6 ca kiểm thử)

| TC_ID | Tiêu đề | Kết quả | Bug ID (nếu có) |
|-------|---------|---------|-----------------|
| **TC_SWAG_CHECKOUT_001** | Checkout thành công với thông tin hợp lệ | ✅ / ❌ | BUG_SWAG_CHECKOUT_003 |
| **TC_SWAG_CHECKOUT_002** | Validation khi để trống thông tin checkout | ✅ / ❌ | BUG_SWAG_CHECKOUT_001 |
| **TC_CHECKOUT_001** | Thanh toán thành công | ✅ / ❌ | - |
| **TC_CHECKOUT_002** | Thanh toán thất bại (Postal Code trống) | ✅ / ❌ | - |
| **TC_CHECKOUT_004** | Zip/Postal Code hợp lệ tối thiểu (5 ký tự) | ✅ / ❌ | BUG_SWAG_CHECKOUT_002 |
| **TC_CHECKOUT_007** | Tính tổng tiền chính xác | ✅ / ❌ | BUG_SWAG_CHECKOUT_003 |

**Tóm tắt mô-đun Checkout:** điền nhận xét thực tế sau khi kiểm thử.

---

## 4. TOP LỖI NGHIÊM TRỌNG NHẤT

### 🔴 Lỗi Critical

| # | Mã lỗi | Tiêu đề | Mức độ nghiêm trọng | Ảnh hưởng |
|---|--------|---------|----------|--------|
| 1 | **BUG_AUTH_002** | Mật khẩu không yêu cầu ký tự đặc biệt | Critical | **Bảo mật cao** |
| 2 | **BUG_CART_001** | Giỏ hàng không cập nhật tổng tiền chính xác | Critical | **Mất tiền** |
| 3 | **BUG_CHECKOUT_002** | Mã giảm giá dùng nhiều lần | Critical | **Mất doanh thu** |

### 🟠 Lỗi Major

| # | Mã lỗi | Tiêu đề | Mức độ nghiêm trọng | Ảnh hưởng |
|---|--------|---------|----------|--------|
| 4 | **BUG_CART_002** | Không kiểm tra tồn kho khi cập nhật số lượng | Major | **Overselling** |
| 5 | **BUG_CHECKOUT_001** | Dù đã nhập sai địa chỉ, vẫn cho phép đặt hàng | Major | **Giao hàng sai địa chỉ** |

---

## 5. PHÂN TÍCH LỖI THEO MỨC ĐỘ NGHIÊM TRỌNG

### Biểu đồ phân bố mức độ nghiêm trọng

| Mức độ nghiêm trọng | Số lỗi | % | Màu |
|----------|--------|-----|-----|
| **Critical** | 3 | 25% | 🔴 |
| **Major** | 6 | 50% | 🟠 |
| **Minor** | 3 | 25% | 🟡 |
| **Trivial** | 0 | 0% | 🟢 |

```
Critical  ████████████████████░░░░░░░░░░░░░░░░░░ 25% (3)
Major     ████████████████████████████░░░░░░░░░░░░ 50% (6)
Minor     ████████████████░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
```

### Phân tích

- **25% bugs Critical:** Nguy hiểm, ảnh hưởng đến bảo mật & logic business
- **50% bug Major:** Cần sửa trước khi phát hành
- **25% bugs Minor:** Có thể sửa sau

---

## 6. NHẬN XÉT CHẤT LƯỢNG HỆ THỐNG

### 6.1 Điểm mạnh

✅ **Các tính năng cơ bản hoạt động** - 76% ca kiểm thử đạt  
✅ **Validation cơ bản có** - Email, mật khẩu được check  
✅ **Giỏ hàng & checkout khác nhau - các tính năng chính có**  
✅ **Lịch sử đơn hàng hoạt động** - Lưu trữ dữ liệu tốt

### 6.2 Điểm yếu

❌ **3 bugs Critical** - Cần sửa ngay  
❌ **Validation không chặt** - Email, mật khẩu, địa chỉ  
❌ **Tính toán sai tiền** - Bug Critical trong logic thanh toán  
❌ **Không kiểm tra tồn kho** - Có thể overselling  
❌ **Mã giảm giá không có limit** - Dùng nhiều lần được  
❌ **Xử lý error chưa tốt** - Một số form vẫn submit khi lỗi

### 6.3 Rủi ro lớn

| Rủi Ro | Độ Lớn | Mô Tả |
|--------|--------|-------|
| **Bảo mật mật khẩu** | 🔴 Cao | Mật khẩu yếu được chấp nhận |
| **Tính toán tiền** | 🔴 Cao | Sai số tiền = mất doanh thu |
| **Overselling** | 🟠 Trung | Tồn kho không được check |
| **Giao hàng** | 🟠 Trung | Địa chỉ validation yếu |

---

## 7. ĐỘ BAO PHỦ YÊU CẦU

| Chỉ số | Giá trị | Mục tiêu | Kết quả |
|--------|--------|---------|---------|
| **Độ bao phủ (%)** | **100%** | ≥ 90% | ✅ |
| **Tổng số ca kiểm thử** | **21** | ≥ 15 | ✅ |
| **Ca kiểm thử luồng sai** | **4** | ≥ 3 | ✅ |
| **Ca kiểm thử giá trị biên** | **1** | ≥ 1 | ✅ |

---

## 8. QUYẾT ĐỊNH PHÁT HÀNH

### 📊 Tiêu chí quyết định

| Tiêu chí | Yêu cầu | Kết quả | Trạng thái |
|----------|---------|---------|-----------|
| **Tỷ lệ đạt** | ≥85% | 76% | ❌ |
| **Số bug Critical** | 0 | 3 | ❌ |
| **Độ bao phủ yêu cầu** | ≥90% | 100% | ✅ |
| **Hồi quy** | Không còn lỗi nghiêm trọng mới | Không còn lỗi nghiêm trọng mới | ✅ / ❌ |

### 🎯 Quyết định cuối cùng

> Phần dưới là mẫu, bạn thay thế bằng kết luận thực tế sau khi kiểm thử Swag Labs.

## ❌/**✅** **QUYẾT ĐỊNH PHÁT HÀNH**

**Lý Do:**  
- Ghi rõ dựa trên số liệu tỷ lệ đạt, số bug Critical/Major,… 

**Khuyến Nghị :**
- Các hạng mục cần sửa/kiểm thử lại cụ thể cho Swag Labs

---

## 9. KHO LƯU TRỮ TÀI LIỆU

| Loại | Tập Tin | Vị Trí |
|------|---------|--------|
| **Test Plan** | Test_Plan_ECommerce.md | `/Test Plan/` |
| **Ca kiểm thử** | Test_Cases_ECommerce.md | `/Test Cases/` |
| **RTM** | RTM_ECommerce.md | `/RTM/` |
| **Bug Report** | Bug_Reports_ECommerce.md | `/Bug Reports/` |
| **Test Report** | Test_Report_ECommerce.md | `/Test Report/` |
| **Test Metrics** | Test_Metrics_ECommerce.md | `/Test Metrics/` |

---

## 10. PHỤ LỤC

### Phụ Lục A: Danh sách ca kiểm thử không đạt

```
BUG_AUTH_001     TC_AUTH_002   ❌
BUG_AUTH_002     TC_AUTH_015   ❌
BUG_PRODUCT_001  TC_PRODUCT_001 ❌
BUG_PRODUCT_002  TC_PRODUCT_007 ❌
BUG_PRODUCT_003  TC_PRODUCT_005 ❌
BUG_CART_001     TC_CART_006    ❌
BUG_CART_002     TC_CART_004    ❌
BUG_CART_003     TC_CART_008    ❌
BUG_CHECKOUT_001 TC_CHECKOUT_002 ❌
BUG_CHECKOUT_002 TC_CHECKOUT_008 ❌
BUG_CHECKOUT_003 TC_CHECKOUT_015 ❌
(Liên quan có thể trùng)
```

### Phụ Lục B: Kỳ Hạn Sửa

| Giai đoạn | Mã lỗi | Ngày mục tiêu | Nhóm phụ trách |
|-------|---------|-------------|----------|
| **Giai đoạn 1** | BUG_AUTH_002, BUG_CART_001, BUG_CHECKOUT_002 | 03/02 | Dev Lead |
| **Giai đoạn 2** | BUG_AUTH_001, BUG_CART_002, BUG_CHECKOUT_001, BUG_AUTH_003, BUG_PRODUCT_002, BUG_CART_003 | 07/02 | Dev Team |
| **Giai đoạn 3** | BUG_PRODUCT_001, BUG_CHECKOUT_003, BUG_PRODUCT_003 | Tuỳ chọn | Dev Team |

---

## KẾT LUẬN

**Hệ thống cần cải thiện đáng kể trước khi phát hành.**

Có 12 lỗi phát hiện được, trong đó 3 bugs Critical cần sửa ngay lập tức. 
Tỷ lệ đạt hiện tại 76% chưa đạt mục tiêu 85%. 
Sau khi sửa bug Critical và Major, dự kiến Giai đoạn 2 sẽ đạt tiêu chí phát hành.

---

**Lập báo cáo bởi:** Nhóm Manual Testing   
**Ngày:** 25/02/2026  

---

**KẾT THÚC BÁO CÁO KIỂM THỬ**
