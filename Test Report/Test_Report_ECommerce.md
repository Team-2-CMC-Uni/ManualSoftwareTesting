# BÁO CÁO KIỂM THỬ (TEST REPORT)
## Hệ Thống Web Bán Hàng Online (E-Commerce)

**Ngày báo cáo:** 28/01/2026  
**Giai đoạn kiểm thử:** Manual QA - Phase 1  
**Trạng thái báo cáo:** Final

---

## 1. TỔNG QUAN KIỂM THỬ

### 1.1 Thông Tin Chung

| Thông Tin | Chi Tiết |
|-----------|---------|
| **Hệ thống** | Website Bán Hàng Online (E-Commerce) |
| **Phiên bản test** | v1.0 |
| **Ngày bắt đầu** | 18/01/2026 |
| **Ngày kết thúc** | 28/01/2026 |
| **Tổng thời gian** | 11 ngày |
| **Tester** | Nhóm Manual Testing |
| **Trình duyệt** | Chrome 120 |
| **OS** | Windows 10/11 |

### 1.2 Mục Tiêu Kiểm Thử

✅ Xác minh tất cả chức năng chính hoạt động đúng  
✅ Phát hiện lỗi (bug) trong hệ thống  
✅ Đảm bảo coverage requirement ≥ 90%  
✅ Cung cấp báo cáo chất lượng để quyết định release

---

## 2. KẾT QUẢ KIỂM THỬ TỔNG THỂ

### 2.1 Thống Kê Thực Thi Test

| Metric | Giá Trị |
|--------|--------|
| **Tổng Test Case** | 50 |
| **Đã Thực Thi** | 50 |
| **Execution Rate** | **100%** ✅ |

### 2.2 Kết Quả Chi Tiết

| Trạng Thái | Số Lượng | % | Biểu Tượng |
|-----------|---------|------|-----------|
| **Pass** | 38 | 76% | ✅ |
| **Fail** | 12 | 24% | ❌ |
| **Blocked** | 0 | 0% | 🚫 |
| **Skipped** | 0 | 0% | ⏭️ |

**Pass Rate:** 76% (Mục tiêu: ≥85%)  
**Fail Rate:** 24% (Có 12 bug)

### 2.3 Kết Quả theo Module

| Module | Total | Pass | Fail | Pass % | Fail % |
|--------|-------|------|------|--------|--------|
| **Authentication** | 15 | 12 | 3 | 80% | 20% |
| **Product & Cart** | 20 | 15 | 5 | 75% | 25% |
| **Checkout** | 15 | 11 | 4 | 73% | 27% |
| **TỔNG** | **50** | **38** | **12** | **76%** | **24%** |

---

## 3. CHI TIẾT KẾT QUẢ THEO MODULE

### 3.1 Module: Authentication (15 Test Cases)

| TC_ID | Tiêu Đề | Kết Quả | Bug ID |
|-------|---------|---------|--------|
| TC_AUTH_001 | Đăng ký email hợp lệ | ✅ Pass | - |
| TC_AUTH_002 | Email sai định dạng | ❌ Fail | BUG_AUTH_001 |
| TC_AUTH_003 | Mật khẩu < 8 ký tự | ✅ Pass | - |
| TC_AUTH_004 | Mật khẩu = 8 ký tự | ✅ Pass | - |
| TC_AUTH_005 | Mật khẩu không khớp | ✅ Pass | - |
| TC_AUTH_006 | Email đã đăng ký | ✅ Pass | - |
| TC_AUTH_007 | Đăng nhập thành công | ✅ Pass | - |
| TC_AUTH_008 | Sai mật khẩu | ✅ Pass | - |
| TC_AUTH_009 | Email không tồn tại | ✅ Pass | - |
| TC_AUTH_010 | Email trống | ✅ Pass | - |
| TC_AUTH_011 | Quên mật khẩu | ✅ Pass | - |
| TC_AUTH_012 | Quên mật khẩu email không tồn tại | ✅ Pass | - |
| TC_AUTH_013 | Đăng xuất | ✅ Pass | - |
| TC_AUTH_014 | Session timeout | ✅ Pass | - |
| TC_AUTH_015 | SQL Injection | ❌ Fail | BUG_AUTH_002 |

**Kết quả:** 12 Pass / 3 Fail = 80% ✅

### 3.2 Module: Product & Cart (20 Test Cases)

| TC_ID | Tiêu Đề | Kết Quả | Bug ID |
|-------|---------|---------|--------|
| TC_PRODUCT_001 | Tìm kiếm thành công | ❌ Fail | BUG_PRODUCT_001 |
| TC_PRODUCT_002 | Tìm kiếm trống | ✅ Pass | - |
| TC_PRODUCT_003 | Tìm kiếm không tìm thấy | ✅ Pass | - |
| TC_PRODUCT_004 | Lọc theo giá | ✅ Pass | - |
| TC_PRODUCT_005 | Lọc theo danh mục | ❌ Fail | BUG_PRODUCT_003 |
| TC_PRODUCT_006 | Lọc giá sai | ✅ Pass | - |
| TC_PRODUCT_007 | Xem chi tiết sản phẩm | ❌ Fail | BUG_PRODUCT_002 |
| TC_PRODUCT_008 | Xem đánh giá | ✅ Pass | - |
| TC_CART_001 | Thêm vào giỏ thành công | ✅ Pass | - |
| TC_CART_002 | Thêm khi chưa đăng nhập | ✅ Pass | - |
| TC_CART_003 | Thêm số lượng 0 | ✅ Pass | - |
| TC_CART_004 | Vượt tồn kho | ❌ Fail | BUG_CART_002 |
| TC_CART_005 | Xem giỏ hàng | ✅ Pass | - |
| TC_CART_006 | Cập nhật số lượng | ❌ Fail | BUG_CART_001 |
| TC_CART_007 | Xoá sản phẩm | ✅ Pass | - |
| TC_CART_008 | Giỏ rỗng | ❌ Fail | BUG_CART_003 |
| TC_PRODUCT_001 | Tìm kiếm thành công | (Xem lại) | - |
| TC_PRODUCT_009 | Tìm kiếm phân biệt hoa/thường | ❌ Fail | BUG_PRODUCT_001 |
| TC_CART_009 | Cập nhật giỏ sai | ✅ Pass | - |
| TC_CART_010 | Xoá giỏ hàng | ✅ Pass | - |

**Kết quả:** 15 Pass / 5 Fail = 75% ⚠️

### 3.3 Module: Checkout (15 Test Cases)

| TC_ID | Tiêu Đề | Kết Quả | Bug ID |
|-------|---------|---------|--------|
| TC_CHECKOUT_001 | Thanh toán COD | ✅ Pass | - |
| TC_CHECKOUT_002 | Địa chỉ trống | ❌ Fail | BUG_CHECKOUT_001 |
| TC_CHECKOUT_003 | Địa chỉ quá ngắn | ❌ Fail | BUG_CHECKOUT_001 |
| TC_CHECKOUT_004 | Địa chỉ 10 ký tự | ✅ Pass | - |
| TC_CHECKOUT_005 | Visa giả lập | ✅ Pass | - |
| TC_CHECKOUT_006 | Visa không hợp lệ | ✅ Pass | - |
| TC_CHECKOUT_007 | Tính tổng tiền | ❌ Fail | BUG_CART_001 |
| TC_CHECKOUT_008 | Mã giảm giá | ❌ Fail | BUG_CHECKOUT_002 |
| TC_CHECKOUT_009 | Mã giảm không hợp lệ | ✅ Pass | - |
| TC_CHECKOUT_010 | Lịch sử đơn hàng | ✅ Pass | - |
| TC_CHECKOUT_011 | Lưu lịch sử | ✅ Pass | - |
| TC_CHECKOUT_012 | Chi tiết đơn hàng | ✅ Pass | - |
| TC_CHECKOUT_013 | Hủy trong 1 giờ | ✅ Pass | - |
| TC_CHECKOUT_014 | Không hủy sau 1 giờ | ✅ Pass | - |
| TC_CHECKOUT_015 | Email xác nhận | ❌ Fail | BUG_CHECKOUT_003 |

**Kết quả:** 11 Pass / 4 Fail = 73% ⚠️

---

## 4. TOP 5 LỖI NGHIÊM TRỌNG NHẤT

### 🔴 Lỗi Critical

| # | Bug ID | Tiêu Đề | Severity | Impact |
|---|--------|---------|----------|--------|
| 1 | **BUG_AUTH_002** | Mật khẩu không yêu cầu ký tự đặc biệt | Critical | **Bảo mật cao** |
| 2 | **BUG_CART_001** | Tính tổng tiền sai | Critical | **Mất tiền** |
| 3 | **BUG_CHECKOUT_002** | Mã giảm giá dùng nhiều lần | Critical | **Mất doanh thu** |

### 🟠 Lỗi Major

| # | Bug ID | Tiêu Đề | Severity | Impact |
|---|--------|---------|----------|--------|
| 4 | **BUG_CART_002** | Không kiểm tra tồn kho | Major | **Overselling** |
| 5 | **BUG_CHECKOUT_001** | Địa chỉ quá ngắn bị chấp nhận | Major | **Giao hàng sai địa chỉ** |

---

## 5. PHÂN TÍCH LỖI THEO SEVERITY

### Biểu Đồ Severity Distribution

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

### Phân Tích

- **25% bugs Critical:** Nguy hiểm, ảnh hưởng đến bảo mật & logic business
- **50% bugs Major:** Cần sửa trước release
- **25% bugs Minor:** Có thể sửa sau

---

## 6. NHẬN XÉT CHẤT LƯỢNG HỆ THỐNG

### 6.1 Điểm Mạnh

✅ **Các tính năng cơ bản hoạt động** - 76% test pass  
✅ **Validation cơ bản có** - Email, mật khẩu được check  
✅ **Giỏ hàng & checkout khác nhau - các tính năng chính có**  
✅ **Lịch sử đơn hàng hoạt động** - Lưu trữ dữ liệu tốt

### 6.2 Điểm Yếu

❌ **3 bugs Critical** - Cần sửa ngay  
❌ **Validation không chặt** - Email, mật khẩu, địa chỉ  
❌ **Tính toán sai tiền** - Bug Critical trong logic thanh toán  
❌ **Không kiểm tra tồn kho** - Có thể overselling  
❌ **Mã giảm giá không có limit** - Dùng nhiều lần được  
❌ **Xử lý error chưa tốt** - Một số form vẫn submit khi lỗi

### 6.3 Rủi Ro Lớn

| Rủi Ro | Độ Lớn | Mô Tả |
|--------|--------|-------|
| **Bảo mật mật khẩu** | 🔴 Cao | Mật khẩu yếu được chấp nhận |
| **Tính toán tiền** | 🔴 Cao | Sai số tiền = mất doanh thu |
| **Overselling** | 🟠 Trung | Tồn kho không được check |
| **Giao hàng** | 🟠 Trung | Địa chỉ validation yếu |

---

## 7. COVERAGE REQUIREMENT

| Metric | Giá Trị | Mục Tiêu | Kết Quả |
|--------|--------|---------|---------|
| **Coverage %** | 100% | ≥90% | ✅ Pass |
| **Test Case** | 50 | ≥45 | ✅ Pass |
| **Negative Cases** | 16 | ≥10 | ✅ Pass |
| **Boundary Cases** | 6 | ≥5 | ✅ Pass |

---

## 8. QUYẾT ĐỊNH RELEASE

### 📊 Tiêu Chí Quyết Định

| Tiêu Chí | Yêu Cầu | Kết Quả | Status |
|----------|---------|---------|--------|
| **Pass Rate** | ≥85% | 76% | ❌ FAIL |
| **Bugs Critical** | 0 | 3 | ❌ FAIL |
| **Coverage** | ≥90% | 100% | ✅ PASS |
| **Regression** | ✅ OK | ✅ OK | ✅ PASS |

### 🎯 QUYẾT ĐỊNH CUỐI CÙNG

## ❌ **NO-RELEASE**

**Lý Do:**
1. ❌ **3 bugs Critical còn mở** - Cần sửa ngay
2. ❌ **Pass rate 76% < 85%** - Chưa đủ chất lượng
3. ❌ **Lỗi bảo mật** - Mật khẩu weak không bị chặn
4. ❌ **Lỗi tính tiền** - Sai kết quả thanh toán

**Khuyến Nghị:**
- 🔧 Sửa 3 bugs Critical (2-3 ngày)
- 🔧 Sửa 6 bugs Major (4-5 ngày)
- ✅ Re-test sau khi sửa
- 📋 Cập nhật báo cáo

---

## 9. KHO LƯỚI TRỮ TÀILIỆU

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
