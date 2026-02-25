# Kiểm Thử Website Swag Labs (Saucedemo.com)

Dự án này chứa bộ tài liệu và kế hoạch kiểm thử thủ công được **điều chỉnh để áp dụng cho website Swag Labs** (`https://www.saucedemo.com/`).  

---

## 📋 Giới Thiệu

Tài liệu này dùng để **kiểm thử thủ công trên website Swag Labs**.  
Quá trình kiểm thử tập trung vào các chức năng thực tế đang có trên trang:
- **Đăng nhập/Đăng xuất (Authentication)**: Đăng nhập với các tài khoản demo, xử lý lỗi đăng nhập
- **Danh sách & Chi tiết sản phẩm (Inventory)**: Xem danh sách sản phẩm, sort, xem chi tiết
- **Giỏ hàng (Cart)**: Thêm/xoá sản phẩm, xem giỏ, điều hướng
- **Checkout**: Nhập thông tin khách hàng, xem lại đơn hàng, hoàn tất đặt hàng

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
- **Phạm vi kiểm thử**: Các module và tính năng của Swag Labs (login, inventory, cart, checkout)
- **Chiến lược kiểm thử**: Phương pháp và cách tiếp cận
- **Lịch trình**: Kế hoạch thực hiện kiểm thử
- **Nhân lực**: Vai trò và trách nhiệm
- **Rủi ro**: Các rủi ro tiềm ẩn và cách giảm thiểu

### 2. **Ca Kiểm Thử** ([Test_Cases_ECommerce.md](Test%20Cases/Test_Cases_ECommerce.md))
File này gồm 2 phần:
- **Phần A – Swag Labs [Thực tế]**: Các test case bạn sẽ dùng để chạy trực tiếp trên `https://www.saucedemo.com/`
- **Phần B – Demo E-Commerce**: Bộ test case mẫu cho hệ thống bán hàng online tổng quát (tham khảo kỹ thuật thiết kế)

Mỗi ca kiểm thử bao gồm:
- ID ca kiểm thử, Tiêu đề, Loại (Tích cực/Tiêu cực/Biên)
- Điều kiện trước, Các bước thực hiện, Kết quả mong đợi
- Mức độ ưu tiên, Liên quan đến yêu cầu

### 3. **Ma Trận Truy Vết Yêu Cầu** ([RTM_ECommerce.md](RTM/RTM_ECommerce.md))
File RTM gồm:
- **Phần Swag Labs [Thực tế]**: Bạn tự liệt kê yêu cầu thực tế của Swag Labs và map với test case
- **Phần Demo**: Bảng RTM mẫu cho hệ thống e-commerce giả lập (giữ lại để tham khảo cấu trúc)

### 4. **Chỉ Số Kiểm Thử** ([Test_Metrics_ECommerce.md](Test%20Metrics/Test_Metrics_ECommerce.md))
Các chỉ số kiểm thử trong file hiện tại đóng vai trò **mẫu minh hoạ**.  
Khi bạn chạy test thật trên Swag Labs, hãy:
- Cập nhật lại toàn bộ số liệu có liên quan đến kết quả thực thi với tag **`[Thực tế]`**
- Giữ lại công thức và cấu trúc bảng để tái sử dụng

### 5. **Báo Cáo Lỗi** ([Bug_Reports_ECommerce.md](Bug%20Reports/Bug_Reports_ECommerce.md))
Hiện tại file chứa **danh sách bug demo** cho hệ thống e-commerce giả lập.  
Khi test Swag Labs, bạn nên:
- Tạo thêm mục bug riêng cho Swag Labs và đánh dấu **`[Thực tế]`**
- Hoặc tạo file bug mới chỉ chuyên cho Swag Labs

### 6. **Báo Cáo Kiểm Thử** ([Test_Report_ECommerce.md](Test%20Report/Test_Report_ECommerce.md))
File report hiện tại là **báo cáo mẫu** với số liệu giả lập.  
Khi bạn hoàn thành test trên Swag Labs, hãy:
- Cập nhật lại các phần: kết quả thực thi, phân tích lỗi, quyết định release và đánh dấu **`[Thực tế]`**
- Hoặc clone file này thành báo cáo riêng cho Swag Labs

---

## 📊 Thống Kê Kiểm Thử (Mẫu)

Các thống kê dưới đây là **mẫu tham khảo**, không phản ánh kết quả thực tế trên Swag Labs.

| Chỉ Số | Giá Trị (Demo) |
|--------|----------------|
| **Tổng Ca Kiểm Thử** | 50 |
| **Tổng Yêu Cầu** | 16 |
| **Module** | 3 (Authentication, Product & Cart, Checkout) |
| **Loại Kiểm Thử** | 3 (Positive, Negative, Boundary) |
| **Mức Độ Ưu Tiên** | 3 (Cao, Trung Bình, Thấp) |

---

## 🎯 Phạm Vi Kiểm Thử Swag Labs

### ✅ Trong Phạm Vi [Thực tế]
- **Đăng nhập/Đăng xuất** với các user demo
- **Danh sách & chi tiết sản phẩm**: sort, mở chi tiết, điều hướng
- **Giỏ hàng**: thêm/xoá sản phẩm, badge số lượng, điều hướng
- **Checkout**: nhập thông tin khách, xem overview, hoàn tất đơn hàng

### ❌ Ngoài Phạm Vi
- Đăng ký tài khoản mới, quên mật khẩu (không có trên Swag Labs)
- Lịch sử đơn hàng, email xác nhận, mã giảm giá, tồn kho
- Kiểm thử hiệu suất, bảo mật nâng cao, tự động, tải, mobile

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

- **Tên Dự Án**: Kiểm Thử Website Swag Labs (Demo luyện tập)
- **Phiên bản**: 1.0 (điều chỉnh từ bộ tài liệu e-commerce tổng quát)
- **Trạng thái**: Dùng cho học tập/thực hành

---

**Cập Nhật Lần Cuối:** 24/02/2026
