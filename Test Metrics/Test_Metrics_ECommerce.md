# CHỈ SỐ KIỂM THỬ
## Website Swag Labs (Saucedemo.com) – Công Thức & Mẫu Số Liệu

**Ngày lập báo cáo (Swag Labs):** 25/02/2026  
**Giai đoạn:** Kiểm thử thủ công – Swag

---

## 1. CHỈ SỐ CHÍNH 

### 1.1 Tỷ lệ thực thi kiểm thử

**Công thức:** Tỷ lệ thực thi = (Số ca đã thực thi / Tổng số ca kiểm thử) × 100%

| Chỉ số | Giá trị |
|--------|--------|
| **Tổng số ca kiểm thử** | **21** *(theo `Test_Cases_ECommerce.md`)* |
| **Đã thực thi** | **21** |
| **Chưa thực thi** | **0** |
| **Tỷ lệ thực thi** | **100%** |

**Biểu đồ minh họa:**
```
Đã thực thi:      ██████████████████████████ 100% (21)
Chưa thực thi:    ░░░░░░░░░░░░░░░░░░░░░░░░░ 0% (0)
```

**Nhận xét:** 100% ca kiểm thử đã được thực thi, không có ca nào bị bỏ qua.

---

### 1.2 Tỷ lệ đạt kiểm thử

**Công thức:** Tỷ lệ đạt = (Số ca đạt / Số ca đã thực thi) × 100%

| Chỉ số | Giá trị |
|--------|--------|
| **Ca đạt** | **16** |
| **Ca không đạt** | **4** |
| **Ca bị chặn** | **0** |
| **Tổng đã thực thi** | **21** |
| **Tỷ lệ đạt** | **76%** |
| **Tỷ lệ không đạt** | **24%** |

**Biểu đồ minh họa:**
```
Đạt (16):        ██████████████████████ 76%
Không đạt (4):   ███████ 24%
Bị chặn (0):     ░░░░░░░░░░░░░░░░░░░░░░░░░ 0%
```

**Mục tiêu:** Tỷ lệ đạt ≥ 85%  
**Kết quả:** 76%  ❌ Không đạt  
**Nhận xét:** 4 ca kiểm thử không đạt, tương ứng với 12 bug được ghi nhận trong `Bug_Reports_ECommerce.md`.

---

## 2. CHỈ SỐ LỖI

### 2.1 Mật độ lỗi theo mô-đun

**Công thức:** Mật độ lỗi = (Tổng số lỗi trong mô-đun / Số ca kiểm thử của mô-đun) × 100%

| Mô-đun | Số ca kiểm thử | Số lỗi | Mật độ lỗi | Đánh giá |
|--------|--------------|------------------|----------------------|----------|
| **Authentication** | 4 | 3 | 75% | Cao |
| **Product & Cart** | 11 | 5 | 45% | Trung bình |
| **Checkout** | 6 | 4 | 67% | Cao |
| **TỔNG** | 21 | 12 | 57% | Cao |

**Biểu đồ mật độ lỗi (minh họa):**
```
Auth (20%):      ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░
Product (25%):   ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
Checkout (27%):  ███████████░░░░░░░░░░░░░░░░░░░░░░░░░
```

**Gợi ý phân tích:**  
- So sánh mật độ lỗi giữa các mô-đun Authentication / Product & Cart / Checkout  
- Tập trung kiểm thử lại mô-đun có mật độ lỗi cao nhất (thường là Product & Cart hoặc Checkout).

### 2.2 Phân bố bug theo loại

| Loại bug | Số lượng | % | Ví dụ |
|----------|---------|-----|-------|
| **Validation** | 2 | 17% | Thiếu bắt buộc trường checkout |
| **Calculation** | 2 | 17% | Sai tổng tiền giỏ hàng / checkout |
| **Security** | 3 | 25% | Đăng nhập sai mật khẩu, user bị khóa vẫn vào, session chưa bị hủy |
| **UI/UX** | 5 | 41% | Sort sai, badge giỏ hàng, trạng thái nút `Checkout`, ảnh sản phẩm |

**Biểu đồ:**
```
Validation       ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 17% (2)
Calculation      ██████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 17% (2)
Security         ███████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 25% (3)
UI/UX            █████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 41% (5)
```

**Nhận xét:** Điều chỉnh lại số lượng theo thực tế bug trong `Bug_Reports_ECommerce.md`.

---

## 3. CHỈ SỐ MỨC ĐỘ NGHIÊM TRỌNG 

### 3.1 Phân bố mức độ nghiêm trọng

| Mức độ nghiêm trọng | Số lượng | % | Yêu cầu | Trạng thái |
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

| Mã lỗi | Tiêu đề | Mô-đun | Ảnh hưởng |
|--------|---------|--------|--------|
| BUG_AUTH_002 | Mật khẩu yếu được chấp nhận | Auth | 🔴 Bảo mật |
| BUG_CART_001 | Tính tổng tiền sai | Cart | 🔴 Business |
| BUG_CHECKOUT_002 | Coupon dùng nhiều lần | Checkout | 🔴 Business |

**Ảnh hưởng:** Các bug Critical ảnh hưởng trực tiếp đến bảo mật và logic nghiệp vụ (business).

---

## 4. CHỈ SỐ ĐỘ BAO PHỦ YÊU CẦU

### 4.1 Độ bao phủ yêu cầu

**Công thức:** Độ bao phủ (%) = (Số yêu cầu đã được bao phủ / Tổng số yêu cầu) × 100%

| Chỉ số | Giá trị |
|--------|--------|
| **Tổng số yêu cầu** | **8** *(R_SWAG_1 → R_SWAG_8)* |
| **Yêu cầu đã được ca kiểm thử bao phủ** | **8** |
| **Yêu cầu chưa được bao phủ** | **0** |
| **Tỷ lệ bao phủ** | **100%** |

**Mục tiêu:** ≥ 90%  
**Kết quả:** **100%** ✅ (khớp với RTM Swag Labs).

### 4.2 Phân bố ca kiểm thử theo yêu cầu (tham khảo)

| Mã yêu cầu | Mô tả (Swag Labs) | Số ca kiểm thử | Ghi chú |
|-----|-------------------|-------|--------|
| R_SWAG_1 | Đăng nhập với tài khoản demo hợp lệ / sai mật khẩu | 2 | TC_SWAG_AUTH_001, TC_SWAG_AUTH_002 |
| R_SWAG_2 | Đăng nhập với user bị khóa | 1 | TC_SWAG_AUTH_003 |
| R_SWAG_3 | Đăng xuất qua menu trái | 1 | TC_SWAG_AUTH_004 |
| R_SWAG_4 | Hiển thị danh sách sản phẩm Inventory | 1 | TC_SWAG_INV_001 |
| R_SWAG_5 | Sort sản phẩm theo tên / giá | 2 | TC_SWAG_INV_002, TC_SWAG_INV_003 |
| R_SWAG_6 | Xem chi tiết sản phẩm | 1 | TC_SWAG_INV_004 |
| R_SWAG_7 | Thêm/xem sản phẩm trong giỏ | 2 | TC_SWAG_CART_001, TC_SWAG_CART_002 |
| R_SWAG_8 | Checkout, nhập thông tin và validation | 2 | TC_SWAG_CHECKOUT_001, TC_SWAG_CHECKOUT_002 |
| **TỔNG** | **8 yêu cầu** | **12 ca kiểm thử chính** | Các ca còn lại mở rộng thêm luồng Product/Cart/Checkout |

**Biểu đồ độ bao phủ (minh họa):**
```
Độ bao phủ:    ████████████████████████████████████████████████████████████████ 100%
Mục tiêu tối thiểu: ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 90%
```

---

## 5. CÁC CHỈ SỐ BỔ SUNG 

### 5.1 Tỷ lệ theo loại ca kiểm thử

| Loại | Số lượng | % | Mục tiêu | Trạng thái |
|------|---------|-----|---------|-----------|
| **Luồng đúng** | 16 | 76% | - | ✅ |
| **Luồng sai** | 4 | 19% | ≥ 3 | ✅ |
| **Giá trị biên** | 1 | 5% | ≥ 1 | ✅ |

**Biểu đồ minh họa:**
```
Luồng đúng   ████████████████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 76% (16)
Luồng sai    █████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 19% (4)
Giá trị biên ██░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 5% (1)
```

**Gợi ý phân tích:**  
- Loại luồng đúng chiếm đa số để bao phủ hành vi chính.  
- Loại luồng sai và giá trị biên dùng để bắt lỗi validation (đặc biệt ở bước checkout).


```

**Nhận xét:** Hoàn thiện dựa trên tiến độ kiểm thử thực tế cho Swag Labs.

### 5.2 Thời gian kiểm thử

| Chỉ số | Giá trị |
|--------|--------|
| **Thời gian bắt đầu** | 18/01/2026 |
| **Thời gian kết thúc** | 28/01/2026 |
| **Tổng thời gian** | 11 ngày |
| **Ca kiểm thử / ngày** | 4.5 ca/ngày |
| **Effort (Người-ngày)** | ~22 người-giờ |

---

## 6. BẢNG ĐIỀU KHIỂN CHỈ SỐ 

### 6.1 Tóm tắt 4 chỉ số chính

```
┌─────────────────────────────────────────────────────────────────┐
│                 BẢNG TỔNG HỢP CHỈ SỐ                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. Tỷ lệ thực thi: 100%                                      │
│     ████████████████████████████████████ 21/21                │
│                                                                 │
│  2. Tỷ lệ đạt: 76%                                            │
│     ████████████████████░░░░░░░░░░░░░░░░░░ …/21              │
│                                                                 │
│  3. Độ bao phủ yêu cầu: 100%                                  │
│     ████████████████████████████████████ 8/8                  │
│                                                                 │
│  4. Mật độ lỗi: 57%                                           │
│     ███████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 12/21        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 6.2 Bảng chi tiết

| Chỉ số | Giá trị | Tiêu chí | Trạng thái |
|-------|--------|---------|--------|
| **Tỷ lệ thực thi** | 100% | ≥ 95% | ✅ |
| **Tỷ lệ đạt** | 76% | ≥ 85% | ❌ |
| **Độ bao phủ yêu cầu** | 100% | ≥ 90% | ✅ |
| **Số bug Critical** | 3 | ≈ 0 | ❌ |
| **Số bug Major** | 6 | ≤ 3 | ❌ |
| **Ca kiểm thử luồng sai** | 4 | ≥ 3 | ✅ |

---

## 7. PHÂN TÍCH CHI TIẾT

### 7.1 Nhận diện nguyên nhân gốc (gợi ý)

Bạn có thể lập bảng phân tích nguyên nhân gốc (Root Cause) cho từng bug dựa trên `Bug_Reports_ECommerce.md` với các cột: Bug ID, Nguyên nhân gốc, Loại lỗi (logic, UI, cấu hình…), Độ phức tạp.

### 7.2 Phân tích độ phức tạp (minh họa)

```
High (3):     ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 27%
Medium (1):   ███░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 9%
Low (8):      ██████████████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 73%
```

**Kết luận:** Điều chỉnh lại biểu đồ cho phù hợp nếu bạn phân loại độ phức tạp chi tiết cho 12 bug.

---

## 8. SO SÁNH VỚI TIÊU CHÍ

| Chỉ số | Giá trị | Chuẩn tham chiếu | Đánh giá |
|--------|--------|------------------|---------|
| **Tỷ lệ đạt** | 76% | 85–95% | ❌ Thấp hơn mong đợi |
| **Độ bao phủ yêu cầu** | 100% | 80–90% | ✅ Tốt |
| **Tỷ lệ thực thi** | 100% | 95–100% | ✅ Tốt |
| **Mật độ lỗi** | 57% (12/21) | 3–10% | ❌ Cao |
| **Số bug Critical** | 3 | 0–1 | ❌ Cao |

---

## 9. KIẾN NGHỊ VÀ HÀNH ĐỘNG

### 9.1 Ngắn hạn (1–2 tuần)

1. 🔧 **Sửa 3 bug Critical** (ưu tiên cao)  
2. 🧪 **Kiểm thử lại sau khi sửa bug** cho toàn bộ 21 ca kiểm thử  
3. 📊 **Cập nhật lại các chỉ số** (tỷ lệ đạt, mật độ lỗi, bảng điều khiển)

### 9.2 Dài hạn (1–3 tháng)

1. 🔄 Xem xét tự động hóa một phần kiểm thử (luồng login, sort, checkout)  
2. 📈 Bổ sung thêm ca kiểm thử cho các luồng bảo mật và kiểm soát dữ liệu  
3. 👥 Tăng cường rà soát yêu cầu, rà soát ca kiểm thử và quy trình kiểm thử

---

## 10. KẾT LUẬN 

### Kết Quả Tổng Hợp

| Chỉ số | Kết quả | Mục tiêu | Đạt/Không đạt |
|-------|--------|---------|-----------|
| **Tỷ lệ thực thi** | 100% | ≥95% | ✅ |
| **Tỷ lệ đạt** | 76% | ≥85% | ❌ |
| **Độ bao phủ yêu cầu** | 100% | ≥90% | ✅ |
| **Số bug Critical** | 3 | ≈0 | ❌ |
| **Số bug Major** | 6 | ≤3 | ❌ |

### Phán Quyết

```
╔═════════════════════════════════════════╗
║         ĐÁNH GIÁ CHẤT LƯỢNG            ║
╠═════════════════════════════════════════╣
║  Overall Score:     6.5/10              ║
║  Trạng thái:        ⚠️  CẦN KHẮC PHỤC   ║
║  Quyết định:        ❌  CHƯA PHÁT HÀNH  ║
║                                         ║
║  Action Required:                       ║
║  - Sửa 3 bug Critical (Ưu tiên 1)      ║
║  - Sửa 6 bug Major (Ưu tiên 2)         ║
║  - Kiểm thử lại và báo cáo Giai đoạn 2 ║
╚═════════════════════════════════════════╝
```

---

## PHỤ LỤC: CÔNG THỨC TÍNH CHỈ SỐ

### Công Thức Sử Dụng

```
1. Tỷ lệ thực thi = (Số ca đã thực thi / Tổng số ca kiểm thử) × 100%
2. Tỷ lệ đạt = (Số ca đạt / Số ca đã thực thi) × 100%
3. Mật độ lỗi = (Tổng số lỗi / Tổng số ca kiểm thử) × 100%
4. Độ bao phủ (%) = (Yêu cầu đã bao phủ / Tổng yêu cầu) × 100%
5. Tỷ lệ Critical (%) = (Số lỗi Critical / Tổng lỗi) × 100%
6. Tỷ lệ Major (%) = (Số lỗi Major / Tổng lỗi) × 100%
```

---

**Báo cáo được lập bởi:** Nhóm Manual Testing  
**Ngày:** 28/01/2026  
**Phiên bản:** 1.0  

---

**KẾT THÚC BÁO CÁO CHỈ SỐ KIỂM THỬ**
