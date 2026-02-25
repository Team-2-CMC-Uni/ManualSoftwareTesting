# BÁO CÁO KIỂM THỬ (TEST REPORT)
## Website Swag Labs (Saucedemo.com) 


---

## 1. TỔNG QUAN KIỂM THỬ 

### 1.1 Thông Tin Chung 

| Thông Tin | Chi Tiết |
|-----------|---------|
| **Hệ thống** | Website Swag Labs (`https://www.saucedemo.com/`) |
| **Phiên bản test** | v1.0 (luyện tập) |
| **Ngày bắt đầu** |  **20/02/2026** |
| **Ngày kết thúc** |  **22/02/2026** |
| **Tổng thời gian** |  **2 ngày** |
| **Tester** | Toàn thể nhóm 2 |
| **Trình duyệt** | Chrome, Brave |
| **OS** | Windows 10/11 |

### 1.2 Mục Tiêu Kiểm Thử

✅ Xác minh tất cả chức năng chính hoạt động đúng  
✅ Phát hiện lỗi (bug) trong hệ thống  
✅ Đảm bảo coverage requirement ≥ 90%  
✅ Cung cấp báo cáo chất lượng để quyết định release

---

## 2. KẾT QUẢ KIỂM THỬ TỔNG THỂ [Thực tế]

### 2.1 Thống kê thực thi test [Thực tế]

| Metric | Giá trị |
|--------|--------|
| **Tổng số test case** | **21** *(theo `Test_Cases_ECommerce.md`)* |
| **Đã thực thi (Executed)** |  **21** |
| **Tỷ lệ thực thi (Execution Rate)** |  **100%** |

### 2.2 Kết quả chi tiết [Thực tế]

| Trạng Thái | Số Lượng | % | Biểu Tượng |
|-----------|---------|------|-----------|
| **Pass** |  **16** | … | ✅ / ❌ |
| **Fail** |  **4** | … | ❌  |
| **Blocked** | 0 | 0% | 🚫 |
| **Skipped** | 0 | 0% | ⏭️ |

**Pass Rate:**  **76%** (Mục tiêu: ≥85%)  
**Fail Rate:**  **24%**

### 2.3 Kết quả theo module [Thực tế]

| Module | Tổng TC | Pass | Fail | Pass % | Fail % |
|--------|---------|------|------|--------|--------|
| **Authentication (Đăng nhập/Đăng xuất)** | 4 |  **2** |  **2** | … | … |
| **Product & Cart (Sản phẩm & Giỏ hàng)** | 11 |  **11** |  **0** | … | … |
| **Checkout (Thanh toán)** | 6 |  **3** |  **2** | … | … |
| **TỔNG** | 21 |  **16** |  **4** | … | … |

---

## 3. CHI TIẾT KẾT QUẢ THEO MODULE (SWAG LABS – KHUNG ĐIỀN SỐ LIỆU)

Phần này dùng để điền kết quả thực tế dựa trên **21 test case** trong `Test_Cases_ECommerce.md`.

### 3.1 Module: Authentication (4 Test Case)

| TC_ID | Tiêu đề | Kết quả | Bug ID |
|-------|---------|---------|--------|
| **TC_SWAG_AUTH_001** | Đăng nhập thành công với tài khoản demo hợp lệ | ✅ / ❌ |  **BUG_AUTH_001** |
| **TC_SWAG_AUTH_002** | Đăng nhập thất bại khi mật khẩu không chính xác | ✅ / ❌ |  **BUG_AUTH_002** |
| **TC_SWAG_AUTH_003** | Đăng nhập với user bị khóa | ✅ / ❌ |  **BUG_AUTH_003** |
| **TC_SWAG_AUTH_004** | Đăng xuất hệ thống qua menu trái | ✅ / ❌ |  **BUG_AUTH_004** |

**Tóm tắt module Authentication:**  **Authentication (Đăng nhập/Đăng xuất)**

### 3.2 Module: Product & Cart (11 Test Case)

| TC_ID | Tiêu đề | Kết quả | Bug ID |
|-------|---------|---------|--------|
| **TC_SWAG_INV_001** | Hiển thị đúng danh sách sản phẩm sau khi login | ✅ / ❌ |  **BUG_PRODUCT_001** |
| **TC_SWAG_INV_002** | Sort theo Name (A→Z, Z→A) | ✅ / ❌ |  **BUG_PRODUCT_002** |
| **TC_SWAG_INV_003** | Sort theo Price
| **TC_SWAG_INV_004** | Xem chi tiết một sản phẩm từ Inventory | ✅ / ❌ |  **BUG_PRODUCT_003** |
| **TC_SWAG_CART_001** | Thêm sản phẩm vào giỏ từ trang Inventory | ✅ / ❌ |  **BUG_CART_001** |
| **TC_SWAG_CART_002** | Xem chi tiết giỏ hàng | ✅ / ❌ |  **BUG_CART_002** |
| **TC_PRODUCT_007** | Xem chi tiết sản phẩm (Module 2) | ✅ / ❌ |  **BUG_PRODUCT_004** |
| **TC_CART_001** | Thêm sản phẩm vào giỏ thành công (Module 2) | ✅ / ❌ |  **BUG_CART_003** |
| **TC_CART_005** | Xem giỏ hàng (Module 2) | ✅ / ❌ |  **BUG_CART_004** |
| **TC_CART_007** | Xóa sản phẩm khỏi giỏ (Module 2) | ✅ / ❌ |  **BUG_CART_005** |
| **TC_CART_008** | Giỏ hàng trống (Module 2) | ✅ / ❌ |  **BUG_CART_006** |

**Tóm tắt module Product & Cart:**  **Product & Cart (Sản phẩm & Giỏ hàng)**

### 3.3 Module: Checkout (6 Test Case)

| TC_ID | Tiêu đề | Kết quả | Bug ID |
|-------|---------|---------|--------|
| **TC_SWAG_CHECKOUT_001** | Checkout thành công với thông tin hợp lệ | ✅ / ❌ |  **BUG_CHECKOUT_001** |
| **TC_SWAG_CHECKOUT_002** | Validation khi để trống thông tin checkout | ✅ / ❌ |  **BUG_CHECKOUT_002** |
| **TC_CHECKOUT_001** | Thanh toán thành công | ✅ / ❌ |  **BUG_CHECKOUT_003** |
| **TC_CHECKOUT_002** | Thanh toán thất bại (Postal Code trống) | ✅ / ❌ |  **BUG_CHECKOUT_004** |
| **TC_CHECKOUT_004** | Zip/Postal Code hợp lệ tối thiểu (5 ký tự) | ✅ / 

---

## 4. TOP LỖI NGHIÊM TRỌNG NHẤT

### 🔴 Lỗi Critical

| # | Bug ID | Tiêu Đề | Severity | Impact |
|---|--------|---------|----------|--------|
| 1 | **BUG_AUTH_002** | Mật khẩu không yêu cầu ký tự đặc biệt | Critical | **Bảo mật cao** |
| 2 | **BUG_CART_001** | Giỏ hàng không cập nhật tổng tiền chính xác | Critical | **Mất tiền** |
| 3 | **BUG_CHECKOUT_002** | Mã giảm giá dùng nhiều lần | Critical | **Mất doanh thu** |

### 🟠 Lỗi Major

| # | Bug ID | Tiêu Đề | Severity | Impact |
|---|--------|---------|----------|--------|
| 4 | **BUG_CART_002** | Không kiểm tra tồn kho khi cập nhật số lượng | Major | **Overselling** |
| 5 | **BUG_CHECKOUT_001** | Dù đã nhập sai địa chỉ, vẫn cho phép đặt hàng | Major | **Giao hàng sai địa chỉ** |

---

## 5. PHÂN TÍCH LỖI THEO SEVERITY

### Biểu đồ phân bố Severity

| Severity | Số Bugs | % | Màu |
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
- **50% bugs Major:** Cần sửa trước release
- **25% bugs Minor:** Có thể sửa sau

---

## 6. NHẬN XÉT CHẤT LƯỢNG HỆ THỐNG

### 6.1 Điểm mạnh

✅ **Các tính năng cơ bản hoạt động** - 76% test pass  
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

## 7. ĐỘ BAO PHỦ YÊU CẦU (Coverage Requirement)

| Metric | Giá trị | Mục tiêu | Kết quả |
|--------|--------|---------|---------|
| **Coverage %** | … **[Thực tế]** | ≥ 90% | ✅ / ❌ |
| **Tổng số test case** | **21** | ≥ 15 | ✅ |
| **Negative Cases** | **4** | ≥ 3 | ✅ |
| **Boundary Cases** | **1** | ≥ 1 | ✅ |

---

## 8. QUYẾT ĐỊNH RELEASE [Thực tế]

### 📊 Tiêu chí quyết định

| Tiêu chí | Yêu cầu | Kết quả | Trạng thái |
|----------|---------|---------|--------|
| **Pass Rate** | ≥85% | … **[Thực tế]** | ✅ / ❌ |
| **Bugs Critical** | 0 | … **[Thực tế]** | ✅ / ❌ |
| **Coverage** | ≥90% | … **[Thực tế]** | ✅ / ❌ |
| **Regression** | ✅ OK | … **[Thực tế]** | ✅ / ❌ |

### 🎯 Quyết định cuối cùng

> Phần dưới là mẫu, bạn thay thế bằng kết luận thực tế sau khi test Swag Labs.

## ❌/**✅** **QUYẾT ĐỊNH RELEASE [Thực tế]**

**Lý Do:**  
- Ghi rõ dựa trên số liệu Pass Rate, số bug Critical/Major,… **[Thực tế]**

**Khuyến Nghị [Thực tế]:**
- Các hạng mục cần sửa/retet cụ thể cho Swag Labs

---

## 9. KHO LƯU TRỮ TÀI LIỆU

| Loại | Tập Tin | Vị Trí |
|------|---------|--------|
| **Test Plan** | Test_Plan_ECommerce.md | `/Test Plan/` |
| **Test Cases** | Test_Cases_ECommerce.md | `/Test Cases/` |
| **RTM** | RTM_ECommerce.md | `/RTM/` |
| **Bug Report** | Bug_Reports_ECommerce.md | `/Bug Reports/` |
| **Test Report** | Test_Report_ECommerce.md | `/Test Report/` |
| **Test Metrics** | Test_Metrics_ECommerce.md | `/Test Metrics/` |

---

## 10. KHUYẾN NGHỊ HỖ TRỢ

### Giai Đoạn Tiếp Theo (Next Steps)

**Tuần 1 (01/02 - 07/02):**
- [ ] Phát triển sửa bugs Critical (Dev team)
- [ ] Chuẩn bị dữ liệu test cho Phase 2

**Tuần 2 (08/02 - 14/02):**
- [ ] Re-test bugs Critical
- [ ] Sửa bugs Major
- [ ] Kiểm thử Regression

**Tuần 3 (15/02 - 21/02):**
- [ ] Re-test toàn bộ hệ thống (50 TC)
- [ ] Cập nhật báo cáo cuối cùng
- [ ] Quyết định release lần 2

### SLA Re-testing

- **Critical bugs:** Re-test sau 1 ngày sửa
- **Major bugs:** Re-test trong 2 ngày
- **Minor bugs:** Re-test sau release

---

## 11. PHỤ LỤC

### Phụ Lục A: Danh Sách Test Case Fail

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

| Phase | Bug Ids | Target Date | Dev Lead |
|-------|---------|-------------|----------|
| **Phase 1** | BUG_AUTH_002, BUG_CART_001, BUG_CHECKOUT_002 | 03/02 | Dev Lead |
| **Phase 2** | BUG_AUTH_001, BUG_CART_002, BUG_CHECKOUT_001, BUG_AUTH_003, BUG_PRODUCT_002, BUG_CART_003 | 07/02 | Dev Team |
| **Phase 3** | BUG_PRODUCT_001, BUG_CHECKOUT_003, BUG_PRODUCT_003 | Tuỳ chọn | Dev Team |

---

## KẾT LUẬN

**Hệ thống cần cải thiện đáng kể trước khi release.**

Có 12 lỗi phát hiện được, trong đó 3 bugs Critical cần sửa ngay lập tức. 
Pass rate hiện tại 76% chưa đạt mục tiêu 85%. 
Sau khi sửa bugs Critical và Major, dự kiến Phase 2 sẽ đạt tiêu chí release.

---

**Lập báo cáo bởi:** Nhóm Manual Testing  
**Phê duyệt bởi:** QA Manager  
**Ngày:** 28/01/2026  

---

**END OF TEST REPORT**
