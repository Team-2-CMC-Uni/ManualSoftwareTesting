# Kiểm Thử Hệ Thống Web Bán Hàng Online

Dự án này chứa toàn bộ tài liệu và kế hoạch kiểm thử thủ công cho hệ thống website bán hàng online.

---

## 📋 Giới Thiệu

Tài liệu này bao gồm các thành phần kiểm thử chính để đảm bảo chất lượng hệ thống web bán hàng online. Quá trình kiểm thử tập trung vào các chức năng chính bao gồm:
- **Xác Thực (Authentication)**: Đăng ký, đăng nhập, quên mật khẩu, đăng xuất
- **Sản Phẩm & Giỏ Hàng (Product & Cart)**: Tìm kiếm, lọc sản phẩm, quản lý giỏ hàng
- **Thanh Toán (Checkout)**: Nhập địa chỉ, chọn phương thức thanh toán, đặt hàng, lịch sử đơn hàng

**Mục tiêu chính:**
- Xác minh các tính năng hoạt động đúng theo yêu cầu
- Phát hiện và ghi nhận các lỗi phần mềm (bugs)
- Đạt mức độ bao phủ yêu cầu ≥ 90%
- Cung cấp báo cáo chất lượng toàn diện

---

## 📁 Cấu Trúc Thư Mục

```
ManualSoftwareTesting/
├── README.md                          # Tài liệu này
├── Test Plan/
│   └── Test_Plan_ECommerce.md        # Kế hoạch kiểm thử
├── Test Cases/
│   └── Test_Cases_ECommerce.md       # 50 ca kiểm thử
├── RTM/
│   └── RTM_ECommerce.md              # Ma trận truy vết yêu cầu
├── Test Metrics/
│   └── Test_Metrics_ECommerce.md     # Chỉ số kiểm thử
├── Bug Reports/
│   └── Bug_Reports_ECommerce.md      # Báo cáo lỗi
└── Test Report/
    └── Test_Report_ECommerce.md      # Báo cáo kết quả
```

---

## 📄 Mô Tả Chi Tiết Các Tài Liệu

### 1. **Kế Hoạch Kiểm Thử** ([Test_Plan_ECommerce.md](Test%20Plan/Test_Plan_ECommerce.md))
Kế hoạch kiểm thử toàn diện bao gồm:
- **Phạm vi kiểm thử**: Các module và tính năng cần kiểm thử
- **Chiến lược kiểm thử**: Phương pháp và cách tiếp cận
- **Lịch trình**: Kế hoạch thực hiện kiểm thử
- **Nhân lực**: Vai trò và trách nhiệm
- **Rủi ro**: Các rủi ro tiềm ẩn và cách giảm thiểu

### 2. **Ca Kiểm Thử** ([Test_Cases_ECommerce.md](Test%20Cases/Test_Cases_ECommerce.md))
Bộ 50 ca kiểm thử chi tiết:
- **Xác Thực**: 15 ca kiểm thử (TC_AUTH_001 → TC_AUTH_015)
- **Sản Phẩm & Giỏ Hàng**: 20 ca kiểm thử (TC_PRODUCT_001 → TC_CART_012)
- **Thanh Toán**: 15 ca kiểm thử (TC_CHECKOUT_001 → TC_CHECKOUT_015)

Mỗi ca kiểm thử bao gồm:
- ID ca kiểm thử, Tiêu đề, Loại (Tích cực/Tiêu cực/Biên)
- Điều kiện trước, Các bước thực hiện, Kết quả mong đợi
- Mức độ ưu tiên, Liên quan đến yêu cầu

### 3. **Ma Trận Truy Vết Yêu Cầu** ([RTM_ECommerce.md](RTM/RTM_ECommerce.md))
Ma trận truy vết yêu cầu:
- **16 yêu cầu chính** (R1 → R16)
- Liên kết giữa yêu cầu và ca kiểm thử tương ứng
- Trạng thái bao phủ
- Đảm bảo mọi yêu cầu đều được kiểm thử (≥ 90%)

### 4. **Chỉ Số Kiểm Thử** ([Test_Metrics_ECommerce.md](Test%20Metrics/Test_Metrics_ECommerce.md))
Các chỉ số kiểm thử:
- Số lượng ca kiểm thử, tỷ lệ vượt qua/thất bại/bỏ qua
- Mức độ bao phủ yêu cầu
- Mức độ bao phủ module
- Mức độ bao phủ loại kiểm thử (Tích cực/Tiêu cực/Biên)
- Tốc độ phát hiện lỗi theo thời gian

### 5. **Báo Cáo Lỗi** ([Bug_Reports_ECommerce.md](Bug%20Reports/Bug_Reports_ECommerce.md))
Báo cáo các lỗi phát hiện:
- **ID lỗi, Tiêu đề, Mô tả**, Mức độ nghiêm trọng (Nghiêm Trọng/Chính/Nhỏ/Tầm thường)
- Các bước tái hiện, Kết quả thực tế, Kết quả mong đợi
- Trạng thái lỗi (Mới/Đang xử lý/Đã sửa/Đóng)
- Liên quan đến ca kiểm thử

### 6. **Báo Cáo Kiểm Thử** ([Test_Report_ECommerce.md](Test%20Report/Test_Report_ECommerce.md))
Báo cáo kết quả kiểm thử:
- **Tóm tắt kết quả**: Số ca kiểm thử vượt qua/thất bại/bỏ qua
- **Chất lượng sản phẩm**: Đánh giá toàn diện
- **Kết luận**: Khả năng phát hành sản phẩm
- **Khuyến nghị**: Hành động cần thiết trước khi phát hành

---

## 📊 Thống Kê Kiểm Thử

| Chỉ Số | Giá Trị |
|--------|--------|
| **Tổng Ca Kiểm Thử** | 50 |
| **Tổng Yêu Cầu** | 16 |
| **Module** | 3 (Xác Thực, Sản Phẩm, Thanh Toán) |
| **Loại Kiểm Thử** | 3 (Tích Cực, Tiêu Cực, Biên) |
| **Mức Độ Ưu Tiên** | 3 (Cao, Trung Bình, Thấp) |

---

## 🎯 Phạm Vi Kiểm Thử

### ✅ Trong Phạm Vi
- **Xác Thực**: Đăng ký, đăng nhập, quên mật khẩu, đăng xuất
- **Quản Lý Sản Phẩm**: Tìm kiếm, lọc, xem chi tiết sản phẩm
- **Quản Lý Giỏ Hàng**: Thêm, cập nhật, xoá sản phẩm
- **Thanh Toán**: Nhập địa chỉ, chọn phương thức thanh toán, đặt hàng, lịch sử

### ❌ Ngoài Phạm Vi
- Kiểm thử hiệu suất
- Kiểm thử bảo mật nâng cao
- Kiểm thử tự động
- Kiểm thử tải
- Kiểm thử trên thiết bị di động

---

## 🔗 Liên Kết Giữa Các Tài Liệu

```
Kế Hoạch Kiểm Thử
   ↓
Ca Kiểm Thử (50)
   ↓
Ma Trận Truy Vết (16 Yêu Cầu → Ca Kiểm Thử)
   ↓
Thực Thi Kiểm Thử → Báo Cáo Lỗi
   ↓
Chỉ Số Kiểm Thử & Báo Cáo Kiểm Thử
```

---

## 👥 Thông Tin Dự Án

- **Tên Dự Án**: Hệ Thống Web Bán Hàng Online
- **Phiên bản**: 1.2
- **Trạng thái**: Hoạt Động

---

**Cập Nhật Lần Cuối:** 29/01/2026
