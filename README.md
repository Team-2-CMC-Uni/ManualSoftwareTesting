# Kiểm Thử Website Swag Labs (Saucedemo.com)

Dự án này chứa bộ tài liệu và kế hoạch kiểm thử thủ công được **điều chỉnh để áp dụng cho website Swag Labs** (`https://www.saucedemo.com/`).  

---

## 📋 Giới Thiệu

Tài liệu này dùng để **kiểm thử thủ công trên website Swag Labs**.  
Quá trình kiểm thử tập trung vào các chức năng thực tế đang có trên trang:
- **Đăng nhập/Đăng xuất (Authentication)**: Đăng nhập với các tài khoản demo, xử lý lỗi đăng nhập
- **Danh sách & Chi tiết sản phẩm (Inventory)**: Xem danh sách sản phẩm, sắp xếp, xem chi tiết
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
- **Phạm vi kiểm thử**: Các mô-đun và tính năng của Swag Labs (login, inventory, cart, checkout)
- **Chiến lược kiểm thử**: Phương pháp và cách tiếp cận
- **Lịch trình**: Kế hoạch thực hiện kiểm thử
- **Nhân lực**: Vai trò và trách nhiệm
- **Rủi ro**: Các rủi ro tiềm ẩn và cách giảm thiểu

### 2. **Ca Kiểm Thử** ([Test_Cases_ECommerce.md](Test%20Cases/Test_Cases_ECommerce.md))
- Tập hợp các ca kiểm thử theo từng mô-đun: Đăng nhập/Đăng xuất, Sản phẩm & Giỏ hàng, Checkout.
- Mỗi ca kiểm thử gồm: mã ca, điều kiện trước, bước thực hiện, kết quả mong đợi và liên kết tới yêu cầu.
- Bao phủ đầy đủ luồng đúng, luồng sai và giá trị biên phục vụ đánh giá chất lượng chức năng.

### 3. **Ma Trận Truy Vết Yêu Cầu** ([RTM_ECommerce.md](RTM/RTM_ECommerce.md))
- Liên kết hai chiều giữa yêu cầu và ca kiểm thử để theo dõi mức độ bao phủ.
- Hỗ trợ kiểm soát thay đổi: khi yêu cầu cập nhật có thể xác định nhanh ca kiểm thử bị ảnh hưởng.
- Là căn cứ xác nhận tỷ lệ bao phủ yêu cầu trước khi kết luận chất lượng và phát hành.

### 4. **Chỉ Số Kiểm Thử** ([Test_Metrics_ECommerce.md](Test%20Metrics/Test_Metrics_ECommerce.md))
- Tổng hợp các chỉ số cốt lõi: tỷ lệ thực thi, tỷ lệ đạt, mật độ lỗi, độ bao phủ yêu cầu.
- Phân tích xu hướng lỗi theo mô-đun, mức độ nghiêm trọng và mức ưu tiên.
- Cung cấp dữ liệu định lượng để hỗ trợ quyết định kiểm thử lại và ưu tiên khắc phục.

### 5. **Báo Cáo Lỗi** ([Bug_Reports_ECommerce.md](Bug%20Reports/Bug_Reports_ECommerce.md))
- Ghi nhận chi tiết từng lỗi: mô tả, bước tái hiện, kết quả mong đợi/thực tế và môi trường kiểm thử.
- Phân loại lỗi theo mức độ nghiêm trọng và mức ưu tiên để lập kế hoạch xử lý.
- Liên kết lỗi với ca kiểm thử tương ứng nhằm phục vụ kiểm thử lại và xác nhận sửa lỗi.


### 6. **Báo Cáo Kiểm Thử** ([Test_Report_ECommerce.md](Test%20Report/Test_Report_ECommerce.md))
- Tóm tắt toàn bộ kết quả thực thi kiểm thử theo mô-đun và theo trạng thái đạt/không đạt.
- Tổng hợp lỗi nổi bật, rủi ro còn tồn tại và đánh giá mức sẵn sàng phát hành.
- Đưa ra kết luận cuối cùng cùng khuyến nghị hành động cho vòng kiểm thử tiếp theo.


---

## 📊 Thống Kê Kiểm Thử (Mẫu)

Các thống kê dưới đây là **mẫu tham khảo**, không phản ánh kết quả thực tế trên Swag Labs.

| Chỉ Số | Giá Trị (Demo) |
|--------|----------------|
| **Tổng Ca Kiểm Thử** | 50 |
| **Tổng Yêu Cầu** | 16 |
| **Mô-đun** | 3 (Authentication, Product & Cart, Checkout) |
| **Loại kiểm thử** | 3 (Luồng đúng, Luồng sai, Giá trị biên) |
| **Mức Độ Ưu Tiên** | 3 (Cao, Trung Bình, Thấp) |

---

## 🎯 Phạm Vi Kiểm Thử Swag Labs

### ✅ Trong Phạm Vi
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
