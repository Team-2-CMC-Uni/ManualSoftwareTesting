# CHỈ SỐ KIỂM THỬ (TEST METRICS)
## Hệ Thống Web Bán Hàng Online (E-Commerce)

**Ngày lập báo cáo:** 28/01/2026  
**Giai đoạn:** Phase 1 - Manual QA Testing

---

## 1. CHỈ SỐ CHÍNH (Key Metrics)

### 1.1 Tỷ Lệ Thực Thi Test (Test Execution Rate)

**Công thức:** Execution Rate = (Test Executed / Total Test Cases) × 100%

| Metric | Giá Trị |
|--------|--------|
| **Tổng Test Case** | 50 |
| **Test Executed** | 50 |
| **Test Not Executed** | 0 |
| **Execution Rate** | **100%** ✅ |

**Biểu Đồ:**
```
Executed:      ██████████████████████████ 100% (50)
Not Executed:  ░░░░░░░░░░░░░░░░░░░░░░░░░ 0%   (0)
```

**Phân Tích:** Tất cả test case đã được thực thi, không có test bị skipped.

---

### 1.2 Tỷ Lệ Vượt Qua Test (Test Pass Rate)

**Công thức:** Pass Rate = (Test Passed / Test Executed) × 100%

| Metric | Giá Trị |
|--------|--------|
| **Test Passed** | 38 |
| **Test Failed** | 12 |
| **Test Blocked** | 0 |
| **Total Executed** | 50 |
| **Pass Rate** | **76%** ⚠️ |
| **Fail Rate** | **24%** |

**Biểu Đồ:**
```
Pass (38):   ██████████████████████ 76%
Fail (12):   ███████ 24%
Blocked (0): ░░░░░░░░░░░░░░░░░░░░░░░░░ 0%
```

**Mục Tiêu:** Pass Rate ≥ 85%  
**Kết Quả:** 76% < 85% ❌ **KHÔNG ĐẠT**

**Nguyên Nhân:** 12 bug phát hiện được, cần sửa trước release

---

## 2. CHỈ SỐ PHÁT TRIỂN (Defect Metrics)

### 2.1 Mật Độ Lỗi Theo Module (Defect Density Per Module)

**Công thức:** Defect Density = (Total Defects / Module Test Cases) × 100%

| Module | Test Cases | Defects | Density | Status |
|--------|-----------|---------|---------|--------|
| **Authentication** | 15 | 3 | **20%** | ⚠️ |
| **Product & Cart** | 20 | 5 | **25%** | 🔴 Cao |
| **Checkout** | 15 | 4 | **27%** | 🔴 Cao |
| **TỔNG** | **50** | **12** | **24%** | |

**Biểu Đồ Defect Density:**
```
Auth (20%):      ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░
Product (25%):   ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
Checkout (27%):  ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
```

**Phân Tích:**
- **Module Product & Cart** có density cao nhất (25%) → Cần kiểm thử kỹ hơn
- **Module Checkout** cũng cao (27%) → Bugs liên quan tới tiền, thanh toán
- **Module Auth** tốt hơn (20%) nhưng vẫn có bugs bảo mật

### 2.2 Phân Bố Bug Theo Loại (Bug Type Distribution)

| Loại Bug | Số Lượng | % | Ví Dụ |
|----------|---------|-----|-------|
| **Validation** | 2 | 17% | Email, Địa chỉ |
| **Calculation** | 1 | 8% | Tính tổng tiền |
| **Inventory** | 1 | 8% | Tồn kho |
| **Security** | 2 | 17% | Mật khẩu, Coupon |
| **Email/Notification** | 2 | 17% | Email không gửi |
| **UI/UX** | 4 | 33% | Hiển thị, Button |

**Biểu Đồ:**
```
Validation       ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 17% (2)
Calculation      ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 8% (1)
Inventory        ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 8% (1)
Security         ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 17% (2)
Email/Notif      ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 17% (2)
UI/UX            ███████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 33% (4)
```

**Kết Luận:** UI/UX bugs chiếm 33% → Giao diện cần chỉnh sửa nhiều

---

## 3. CHỈ SỐ SEVERITY (Severity Distribution)

### 3.1 Phân Bố Mức Độ Nghiêm Trọng

| Severity | Số Lượng | % | Yêu Cầu | Status |
|----------|---------|-----|---------|--------|
| **Critical** | 3 | 25% | ≥2 | ✅ |
| **Major** | 6 | 50% | ≥4 | ✅ |
| **Minor** | 3 | 25% | - | - |
| **Trivial** | 0 | 0% | - | - |

**Biểu Đồ Severity:**
```
Critical  ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
Major     ██████████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 50% (6)
Minor     ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
Trivial   ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 0% (0)
```

### 3.2 Chi Tiết Critical Bugs

| Bug ID | Tiêu Đề | Module | Impact |
|--------|---------|--------|--------|
| BUG_AUTH_002 | Mật khẩu yếu được chấp nhận | Auth | 🔴 Bảo mật |
| BUG_CART_001 | Tính tổng tiền sai | Cart | 🔴 Business |
| BUG_CHECKOUT_002 | Coupon dùng nhiều lần | Checkout | 🔴 Business |

**Ảnh hưởng:** Critical bugs ảnh hưởng trực tiếp đến bảo mật & doanh thu

---

## 4. CHỈ SỐ COVERAGE REQUIREMENT (Requirement Coverage)

### 4.1 Độ Bao Phủ Yêu Cầu

**Công thức:** Coverage % = (Requirements Covered / Total Requirements) × 100%

| Metric | Giá Trị |
|--------|--------|
| **Tổng Requirements** | 16 |
| **Requirements Covered** | 16 |
| **Requirements Not Covered** | 0 |
| **Coverage %** | **100%** ✅ |

**Mục Tiêu:** ≥90%  
**Kết Quả:** 100% ✅ **VƯỢT QUAMỤC TIÊU**

### 4.2 Phân Bố Test Case Theo Requirement

| Req | Mô Tả | Số TC | Min Yêu Cầu | Status |
|-----|-------|-------|------------|--------|
| R1  | Đăng ký email hợp lệ | 2 | ≥2 | ✅ |
| R2  | Email sai định dạng | 2 | ≥2 | ✅ |
| R3  | Mật khẩu tối thiểu 8 ký tự | 3 | ≥2 | ✅ |
| R4  | Đăng nhập thành công | 3 | ≥2 | ✅ |
| R5  | Sai mật khẩu | 2 | ≥2 | ✅ |
| R6  | Quên mật khẩu | 2 | ≥2 | ✅ |
| R7  | Tìm kiếm | 3 | ≥2 | ✅ |
| R8  | Lọc theo giá | 3 | ≥2 | ✅ |
| R9  | Chi tiết sản phẩm | 2 | ≥2 | ✅ |
| R10 | Thêm vào giỏ | 4 | ≥2 | ✅ |
| R11 | Cập nhật giỏ | 2 | ≥2 | ✅ |
| R12 | Xoá khỏi giỏ | 2 | ≥2 | ✅ |
| R13 | Thanh toán - Địa chỉ | 3 | ≥2 | ✅ |
| R14 | Chọn phương thức | 3 | ≥2 | ✅ |
| R15 | Đặt hàng thành công | 5 | ≥2 | ✅ |
| R16 | Lịch sử đơn hàng | 5 | ≥2 | ✅ |
| **TỔNG** | **16 Req** | **42 TC** | **≥32** | **✅ PASS** |

**Biểu Đồ Coverage:**
```
Coverage:      ████████████████████████████████████████████████████████████████ 100%
Min Target:    ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 90%
```

---

## 5. CHỈ SỐ GHI CHÚ THÊM (Additional Metrics)

### 5.1 Tỷ Lệ Test Case Loại (Test Case Type Distribution)

| Loại | Số Lượng | % | Mục Tiêu | Status |
|------|---------|-----|---------|--------|
| **Positive** | 28 | 56% | - | ✅ |
| **Negative** | 16 | 32% | ≥10 | ✅ |
| **Boundary** | 6 | 12% | ≥5 | ✅ |

**Biểu Đồ:**
```
Positive  ████████████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 56% (28)
Negative  ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 32% (16)
Boundary  ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 12% (6)
```

**Phân Tích:**
- **56% Positive cases:** Kiểm thử tính năng chính ✅
- **32% Negative cases:** Vượt quá 10 ✅
- **12% Boundary cases:** Vượt quá 5 ✅

### 5.2 Tỷ Lệ Phát Hiện Bug Theo Giai Đoạn (Bug Detection Rate)

| Giai Đoạn | Ngày | Bugs Phát Hiện | Bugs/Ngày |
|-----------|------|-----------------|-----------|
| **Tuần 1** | 18-24/01 | 4 | 0.67 |
| **Tuần 2** | 25-28/01 | 8 | 2.00 |
| **TỔNG** | 11 ngày | **12 bugs** | **1.09 bugs/ngày** |

**Biểu Đồ Phát Hiện:**
```
Tuần 1: ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 33% (4)
Tuần 2: ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 67% (8)
```

**Trend:** Bugs phát hiện tăng ở tuần 2 → Testing kỹ hơn

### 5.3 Thời Gian Kiểm Thử

| Metric | Giá Trị |
|--------|--------|
| **Thời gian bắt đầu** | 18/01/2026 |
| **Thời gian kết thúc** | 28/01/2026 |
| **Tổng thời gian** | 11 ngày |
| **Test case / Ngày** | 4.5 TC/ngày |
| **Effort (Người-ngày)** | ~22 người-giờ |

---

## 6. BIỂU ĐỒ CHỈ SỐ (Metrics Dashboard)

### 6.1 Tóm Tắt 4 Chỉ Số Chính

```
┌─────────────────────────────────────────────────────────────────┐
│                     METRICS DASHBOARD                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. Test Execution Rate: 100% ✅                               │
│     ████████████████████████████████████ 100/100              │
│                                                                 │
│  2. Pass Rate: 76% ⚠️                                          │
│     ████████████████████░░░░░░░░░░░░░░░░░░ 38/50              │
│                                                                 │
│  3. Requirement Coverage: 100% ✅                              │
│     ████████████████████████████████████ 16/16                │
│                                                                 │
│  4. Defect Density: 24% ⚠️                                     │
│     ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 12/50       │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 6.2 Dashboard Chi Tiết

| Chỉ Số | Giá Trị | Tiêu Chí | Status |
|-------|--------|---------|--------|
| **Execution Rate** | 100% | ≥95% | ✅ |
| **Pass Rate** | 76% | ≥85% | ❌ |
| **Coverage %** | 100% | ≥90% | ✅ |
| **Critical Bugs** | 3 | ≈0 | ❌ |
| **Major Bugs** | 6 | ≤3 | ❌ |
| **Negative Cases** | 16 | ≥10 | ✅ |

---

## 7. PHÂN TÍCH CHI TIẾT (In-Depth Analysis)

### 7.1 Root Cause Analysis Cho Fail Cases

| Bug | Root Cause | Loại Lỗi | Độ Phức Tạp |
|-----|-----------|---------|-----------|
| BUG_AUTH_001 | Regex validation sai | Code Bug | Low |
| BUG_AUTH_002 | Yêu cầu mật khẩu không đủ | Design Flaw | High |
| BUG_PRODUCT_001 | Case-sensitive search | Code Bug | Low |
| BUG_PRODUCT_002 | Image path sai | Config Issue | Low |
| BUG_PRODUCT_003 | Filter state không reset | Code Bug | Low |
| BUG_CART_001 | Formula tính sai | Logic Bug | High |
| BUG_CART_002 | Missing inventory check | Code Bug | Medium |
| BUG_CART_003 | Button state không update | UI Bug | Low |
| BUG_CHECKOUT_001 | Validation missing | Code Bug | Low |
| BUG_CHECKOUT_002 | Coupon limit không check | Logic Bug | High |
| BUG_CHECKOUT_003 | Email template sai data | Code Bug | Low |

### 7.2 Phân Tích Độ Phức Tạp

```
High (3):     ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 27%
Medium (1):   ███░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 9%
Low (8):      ██████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 73%
```

**Kết Luận:** Phần lớn bugs là Low complexity (73%) nhưng 3 bugs High complexity cần chú ý.

---

## 8. SO SÁNH VỚI TIÊU CHÍ (Benchmarking)

### 8.1 So Sánh Với Industry Standard

| Metric | Giá Trị | Chuẩn Ngành | Vị Trí |
|--------|--------|-----------|--------|
| **Pass Rate** | 76% | 85-95% | ❌ Dưới |
| **Coverage** | 100% | 80-90% | ✅ Trên |
| **Execution Rate** | 100% | 95-100% | ✅ Trên |
| **Bug Density** | 24% | 3-10% | ❌ Cao |
| **Critical Bugs** | 3 | 0-1 | ❌ Cao |

**Kết Luận:** Hệ thống cần cải thiện bug quality trước release.

---

## 9. DUYÊN KIẾN ĐỀ XUẤT (Recommendations)

### 9.1 Ngắn Hạn (1-2 Tuần)

1. 🔧 **Sửa 3 bugs Critical** (Ưu tiên cao)
   - BUG_AUTH_002: Cộng thêm validation mật khẩu
   - BUG_CART_001: Kiểm tra lại formula tính tiền
   - BUG_CHECKOUT_002: Thêm coupon usage limit

2. 🧪 **Re-test sau sửa**
   - Chạy lại 50 test case
   - Lập báo cáo Phase 2

3. 📊 **Cập nhật Metrics**
   - Expected Pass Rate sau sửa: 88-90%

### 9.2 Dài Hạn (1-3 Tháng)

1. 🔄 **Kiểm thử Automation**
   - Tự động hóa 30% test cases
   - Reduce manual effort

2. 📈 **Cải thiện Coverage**
   - Thêm test security nâng cao
   - Performance testing

3. 👥 **Đào tạo & Process**
   - Huấn luyện dev về secure coding
   - Code review trước commit

---

## 10. KẾT LUẬN CHỈNUMBERING (Conclusion)

### Kết Quả Tổng Hợp

| Chỉ Số | Kết Quả | Mục Tiêu | Pass/Fail |
|-------|--------|---------|-----------|
| **Execution Rate** | 100% | ≥95% | ✅ PASS |
| **Pass Rate** | 76% | ≥85% | ❌ FAIL |
| **Coverage** | 100% | ≥90% | ✅ PASS |
| **Critical Bugs** | 3 | ≈0 | ❌ FAIL |
| **Major Bugs** | 6 | ≤3 | ❌ FAIL |

### Phán Quyết

```
╔═════════════════════════════════════════╗
║         QUALITY ASSESSMENT             ║
╠═════════════════════════════════════════╣
║  Overall Score:     6.5/10              ║
║  Status:            ⚠️  NEEDS FIXING    ║
║  Release Decision:  ❌  NO-RELEASE      ║
║                                         ║
║  Action Required:                       ║
║  - Sửa 3 bugs Critical (Priority 1)    ║
║  - Sửa 6 bugs Major (Priority 2)       ║
║  - Re-test và báo cáo Phase 2          ║
╚═════════════════════════════════════════╝
```

---

## PHỤ LỤC: CÔNG THỨC TÍNH CHỈ SỐ

### Công Thức Sử Dụng

```
1. Execution Rate = (Executed TC / Total TC) × 100%
2. Pass Rate = (Passed TC / Executed TC) × 100%
3. Defect Density = (Total Defects / Total TC) × 100%
4. Coverage % = (Covered Req / Total Req) × 100%
5. Critical Severity % = (Critical / Total Defects) × 100%
6. Major Severity % = (Major / Total Defects) × 100%
```

---

**Báo cáo được lập bởi:** Nhóm Manual Testing  
**Ngày:** 28/01/2026  
**Phiên bản:** 1.0  

---

**END OF TEST METRICS**
