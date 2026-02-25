# CHỈ SỐ KIỂM THỬ (TEST METRICS)
## Website Swag Labs (Saucedemo.com) – Công Thức & Mẫu Số Liệu

**Ngày lập báo cáo (Swag Labs) [Thực tế]:** …  
**Giai đoạn:** Manual QA – Swag Labs

---

## 1. CHỈ SỐ CHÍNH (Key Metrics) [Thực tế]

### 1.1 Tỷ lệ thực thi test (Test Execution Rate) [Thực tế]

**Công thức:** Execution Rate = (Test Executed / Total Test Cases) × 100%

| Metric | Giá trị |
|--------|--------|
| **Tổng số test case** | **21** *(theo `Test_Cases_ECommerce.md`)* |
| **Đã thực thi (Executed)** | … **[Thực tế]** |
| **Chưa thực thi (Not Executed)** | … **[Thực tế]** |
| **Tỷ lệ thực thi (Execution Rate)** | … **[Thực tế]** |

**Biểu đồ minh họa:**
```
Executed:      ██████████████████████████ …% (…)
Not Executed:  ░░░░░░░░░░░░░░░░░░░░░░░░░ …% (…)
```

**Gợi ý phân tích:** Điền số liệu thực tế; lý tưởng là **100% test case được thực thi**, không có test bị bỏ qua.

---

### 1.2 Tỷ lệ pass test (Test Pass Rate) [Thực tế]

**Công thức:** Pass Rate = (Test Passed / Test Executed) × 100%

| Metric | Giá trị |
|--------|--------|
| **Test Passed** | … **[Thực tế]** |
| **Test Failed** | … **[Thực tế]** |
| **Test Blocked** | … **[Thực tế]** |
| **Tổng đã thực thi (Total Executed)** | … **[Thực tế]** |
| **Tỷ lệ Pass (Pass Rate)** | … **[Thực tế]** |
| **Tỷ lệ Fail (Fail Rate)** | … **[Thực tế]** |

**Biểu đồ minh họa:**
```
Pass (…):   ██████████████████████ …%
Fail (…):   ███████ …%
Blocked (0): ░░░░░░░░░░░░░░░░░░░░░░░░░ 0%
```

**Mục tiêu:** Tỷ lệ Pass (Pass Rate) ≥ 85%  
**Kết quả:** … **[Thực tế]**  
**Nhận xét:** Điền phân tích dựa trên số lượng bug phát hiện được trong 21 test case.

---

## 2. CHỈ SỐ PHÁT TRIỂN (Defect Metrics) [Thực tế]

### 2.1 Mật độ lỗi theo module (Defect Density Per Module) [Thực tế]

**Công thức:** Defect Density = (Total Defects / Module Test Cases) × 100%

| Module | Số test case | Số lỗi (Defects) | Mật độ lỗi (Density) | Đánh giá |
|--------|--------------|------------------|----------------------|----------|
| **Authentication** | 4 | … **[Thực tế]** | … **[Thực tế]** | … |
| **Product & Cart** | 11 | … **[Thực tế]** | … **[Thực tế]** | … |
| **Checkout** | 6 | … **[Thực tế]** | … **[Thực tế]** | … |
| **TỔNG** | 21 | … | … | |

**Biểu đồ mật độ lỗi (minh họa):**
```
Auth (20%):      ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░
Product (25%):   ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
Checkout (27%):  ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
```

**Gợi ý phân tích:**  
- So sánh mật độ lỗi giữa các module Authentication / Product & Cart / Checkout  
- Tập trung kiểm thử lại module có mật độ lỗi cao nhất (thường là Product & Cart hoặc Checkout).

### 2.2 Phân bố bug theo loại (Bug Type Distribution)

| Loại bug | Số lượng | % | Ví dụ |
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

**Nhận xét:** Điều chỉnh lại số lượng theo thực tế bug trong `Bug_Reports_ECommerce.md`.

---

## 3. CHỈ SỐ MỨC ĐỘ NGHIÊM TRỌNG (Severity Distribution) [Thực tế]

### 3.1 Phân bố mức độ nghiêm trọng

| Severity | Số Lượng | % | Yêu Cầu | Status |
|----------|---------|-----|---------|--------|
| **Critical** | 3 | 25% | ≥2 | ✅ |
| **Major** | 6 | 50% | ≥4 | ✅ |
| **Minor** | 3 | 25% | - | - |
| **Trivial** | 0 | 0% | - | - |

**Biểu đồ mức độ nghiêm trọng (minh họa):**
```
Critical  ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
Major     ██████████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 50% (6)
Minor     ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
Trivial   ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 0% (0)
```

### 3.2 Chi tiết các bug Critical

| Bug ID | Tiêu Đề | Module | Impact |
|--------|---------|--------|--------|
| BUG_AUTH_002 | Mật khẩu yếu được chấp nhận | Auth | 🔴 Bảo mật |
| BUG_CART_001 | Tính tổng tiền sai | Cart | 🔴 Business |
| BUG_CHECKOUT_002 | Coupon dùng nhiều lần | Checkout | 🔴 Business |

**Ảnh hưởng:** Các bug Critical ảnh hưởng trực tiếp đến bảo mật và logic nghiệp vụ (business).

---

## 4. CHỈ SỐ ĐỘ BAO PHỦ YÊU CẦU (Requirement Coverage) [Thực tế]

### 4.1 Độ bao phủ yêu cầu

**Công thức:** Coverage % = (Requirements Covered / Total Requirements) × 100%

| Metric | Giá trị |
|--------|--------|
| **Tổng số yêu cầu (Requirements)** | **8** *(R_SWAG_1 → R_SWAG_8)* |
| **Yêu cầu đã được test case bao phủ** | … **[Thực tế]** *(thường là 8)* |
| **Yêu cầu chưa được bao phủ** | … **[Thực tế]** *(thường là 0)* |
| **Tỷ lệ bao phủ (Coverage %)** | … **[Thực tế]** |

**Mục tiêu:** ≥ 90%  
**Kết quả:** … **[Thực tế]** *(kỳ vọng 100% như RTM Swag Labs)*.

### 4.2 Phân bố test case theo requirement (tham khảo)

| Req | Mô tả (Swag Labs) | Số TC | Ghi chú |
|-----|-------------------|-------|--------|
| R_SWAG_1 | Đăng nhập với tài khoản demo hợp lệ / sai mật khẩu | 2 | TC_SWAG_AUTH_001, TC_SWAG_AUTH_002 |
| R_SWAG_2 | Đăng nhập với user bị khóa | 1 | TC_SWAG_AUTH_003 |
| R_SWAG_3 | Đăng xuất qua menu trái | 1 | TC_SWAG_AUTH_004 |
| R_SWAG_4 | Hiển thị danh sách sản phẩm Inventory | 1 | TC_SWAG_INV_001 |
| R_SWAG_5 | Sort sản phẩm theo tên / giá | 2 | TC_SWAG_INV_002, TC_SWAG_INV_003 |
| R_SWAG_6 | Xem chi tiết sản phẩm | 1 | TC_SWAG_INV_004 |
| R_SWAG_7 | Thêm/xem sản phẩm trong giỏ | 2 | TC_SWAG_CART_001, TC_SWAG_CART_002 |
| R_SWAG_8 | Checkout, nhập thông tin và validation | 2 | TC_SWAG_CHECKOUT_001, TC_SWAG_CHECKOUT_002 |
| **TỔNG** | **8 yêu cầu** | **12 test case chính** | Các test case còn lại mở rộng thêm luồng Product/Cart/Checkout |

**Biểu đồ độ bao phủ (minh họa):**
```
Coverage:      ████████████████████████████████████████████████████████████████ 100%
Min Target:    ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 90%
```

---

## 5. CÁC CHỈ SỐ BỔ SUNG (Additional Metrics) [Thực tế]

### 5.1 Tỷ lệ loại test case (Test Case Type Distribution)

| Loại | Số lượng | % | Mục tiêu | Trạng thái |
|------|---------|-----|---------|-----------|
| **Positive** | 16 | … **[Thực tế]** | - | ✅ |
| **Negative** | 4 | … **[Thực tế]** | ≥ 3 | ✅ |
| **Boundary** | 1 | … **[Thực tế]** | ≥ 1 | ✅ |

**Biểu đồ minh họa:**
```
Positive  ████████████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 56% (28)
Negative  ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 32% (16)
Boundary  ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 12% (6)
```

**Gợi ý phân tích:**  
- Positive chiếm đa số để bao phủ luồng đúng.  
- Negative và Boundary dùng để bắt lỗi validation và giá trị biên (đặc biệt ở bước checkout).

### 5.2 Tỷ lệ phát hiện bug theo giai đoạn (Bug Detection Rate) [Thực tế]

| Giai Đoạn | Ngày | Bugs Phát Hiện | Bugs/Ngày |
|-----------|------|-----------------|-----------|
| **Tuần 1** | … **[Thực tế]** | … **[Thực tế]** | … **[Thực tế]** |
| **Tuần 2** | … **[Thực tế]** | … **[Thực tế]** | … **[Thực tế]** |
| **TỔNG** | … **[Thực tế]** | … **[Thực tế]** | … **[Thực tế]** |

**Biểu đồ phát hiện bug (minh họa):**
```
Tuần 1: ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 33% (4)
Tuần 2: ████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 67% (8)
```

**Nhận xét:** Hoàn thiện dựa trên timeline test thực tế cho Swag Labs.

### 5.3 Thời gian kiểm thử

| Metric | Giá trị |
|--------|--------|
| **Thời gian bắt đầu** | 18/01/2026 |
| **Thời gian kết thúc** | 28/01/2026 |
| **Tổng thời gian** | 11 ngày |
| **Test case / Ngày** | 4.5 TC/ngày |
| **Effort (Người-ngày)** | ~22 người-giờ |

---

## 6. BẢNG ĐIỀU KHIỂN CHỈ SỐ (Metrics Dashboard) [Thực tế]

### 6.1 Tóm tắt 4 chỉ số chính

```
┌─────────────────────────────────────────────────────────────────┐
│                     METRICS DASHBOARD                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. Test Execution Rate: …%                                   │
│     ████████████████████████████████████ 100/100              │
│                                                                 │
│  2. Pass Rate: …%                                             │
│     ████████████████████░░░░░░░░░░░░░░░░░░ …/21              │
│                                                                 │
│  3. Requirement Coverage: …%                                  │
│     ████████████████████████████████████ 8/8                  │
│                                                                 │
│  4. Defect Density: …%                                        │
│     ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ …/21        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 6.2 Dashboard chi tiết

| Chỉ số | Giá trị | Tiêu chí | Trạng thái |
|-------|--------|---------|--------|
| **Execution Rate** | … | ≥ 95% | ✅ / ❌ |
| **Pass Rate** | … | ≥ 85% | ✅ / ❌ |
| **Coverage %** | … | ≥ 90% | ✅ / ❌ |
| **Critical Bugs** | … | ≈ 0 | ✅ / ❌ |
| **Major Bugs** | … | ≤ 3 | ✅ / ❌ |
| **Negative Cases** | 4 | ≥ 3 | ✅ |

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

## 10. KẾT LUẬN CHỈNUMBERING (Conclusion) [Thực tế]

### Kết Quả Tổng Hợp

| Chỉ Số | Kết Quả | Mục Tiêu | Pass/Fail |
|-------|--------|---------|-----------|
| **Execution Rate** | … **[Thực tế]** | ≥95% | ✅ / ❌ |
| **Pass Rate** | … **[Thực tế]** | ≥85% | ✅ / ❌ |
| **Coverage** | … **[Thực tế]** | ≥90% | ✅ / ❌ |
| **Critical Bugs** | … **[Thực tế]** | ≈0 | ✅ / ❌ |
| **Major Bugs** | … **[Thực tế]** | ≤3 | ✅ / ❌ |

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
