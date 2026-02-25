# BÁO CÁO LỖI
## Website Swag Labs (Saucedemo.com)

**Tổng số bug (Swag Labs):** 12  
**Ngày lập báo cáo (Swag Labs):** 25/02/2026

---

## BUG #1

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_AUTH_001 |
| **Tiêu đề** | Đăng nhập thành công với mật khẩu sai |
| **Mô tả** | Khi nhập mật khẩu sai cho user `standard_user`, hệ thống vẫn cho đăng nhập vào trang Inventory. |
| **Các bước tái hiện** | 1. Mở trang `https://www.saucedemo.com/`<br/>2. Nhập Username: `standard_user`<br/>3. Nhập Password: `secret_suace` (cố ý sai chính tả)<br/>4. Click nút `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo lỗi trên form đăng nhập, không cho vào trang Inventory. |
| **Kết quả thực tế** | Hệ thống cho phép đăng nhập, chuyển sang trang Inventory. |
| **Mức độ nghiêm trọng** | **Critical** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_AUTH_002 |

---

## BUG #2

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_AUTH_002 |
| **Tiêu đề** | Tài khoản bị khóa vẫn đăng nhập được |
| **Mô tả** | User `locked_out_user` lẽ ra phải bị chặn đăng nhập nhưng hệ thống vẫn cho vào. |
| **Các bước tái hiện** | 1. Mở trang login Swag Labs<br/>2. Nhập Username: `locked_out_user`<br/>3. Nhập Password: `secret_sauce`<br/>4. Click nút `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo user bị khóa, không truy cập được trang Inventory. |
| **Kết quả thực tế** | Hệ thống cho phép đăng nhập bình thường. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_AUTH_003 |

---

## BUG #3

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_AUTH_003 |
| **Tiêu đề** | Đăng xuất không hủy phiên làm việc (session) |
| **Mô tả** | Sau khi logout, quay lại trang bằng nút Back của trình duyệt vẫn xem được danh sách sản phẩm. |
| **Các bước tái hiện** | 1. Đăng nhập thành công bằng `standard_user`<br/>2. Từ trang Inventory, mở menu trái và chọn `Logout`<br/>3. Bấm nút Back trên trình duyệt<br/>4. Quan sát trang hiển thị |
| **Kết quả mong đợi** | Người dùng bị chuyển về trang login, không xem được dữ liệu Inventory nếu chưa đăng nhập lại. |
| **Kết quả thực tế** | Trang Inventory vẫn hiển thị danh sách sản phẩm, cho phép thao tác tiếp. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_AUTH_004 |

---

## BUG #4

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_INV_001 |
| **Tiêu đề** | Sort theo Name (A to Z) không đúng thứ tự alphabet |
| **Mô tả** | Khi chọn sort `Name (A to Z)`, thứ tự một số sản phẩm không đúng alphabet tăng dần. |
| **Các bước tái hiện** | 1. Đăng nhập thành công vào trang Inventory<br/>2. Ở dropdown sort, chọn `Name (A to Z)`<br/>3. Ghi lại thứ tự hiển thị của vài sản phẩm đầu<br/>4. So sánh với thứ tự alphabet kỳ vọng |
| **Kết quả mong đợi** | Danh sách sản phẩm sắp xếp đúng theo A → Z. |
| **Kết quả thực tế** | Một số sản phẩm bị đứng sai vị trí so với thứ tự alphabet. |
| **Mức độ nghiêm trọng** | **Minor** |
| **Mức ưu tiên** | **Trung bình** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_INV_002 |

---

## BUG #5

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_INV_002 |
| **Tiêu đề** | Sort theo Price (low to high) không đúng giá tăng dần |
| **Mô tả** | Khi chọn sort `Price (low to high)`, có sản phẩm giá cao hơn lại xuất hiện trước sản phẩm giá thấp hơn. |
| **Các bước tái hiện** | 1. Đăng nhập và vào trang Inventory<br/>2. Chọn sort `Price (low to high)`<br/>3. Ghi lại giá của 3–4 sản phẩm đầu danh sách<br/>4. So sánh với thứ tự giá kỳ vọng |
| **Kết quả mong đợi** | Giá sản phẩm sắp xếp tăng dần từ thấp đến cao. |
| **Kết quả thực tế** | Có ít nhất một cặp sản phẩm bị đảo thứ tự về giá. |
| **Mức độ nghiêm trọng** | **Minor** |
| **Mức ưu tiên** | **Trung bình** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_INV_003 |

---

## BUG #6

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_PROD_001 |
| **Tiêu đề** | Ảnh sản phẩm không hiển thị ở trang chi tiết |
| **Mô tả** | Khi mở chi tiết sản phẩm "Sauce Labs Backpack", phần hình ảnh không load, chỉ hiển thị icon lỗi. |
| **Các bước tái hiện** | 1. Từ trang Inventory, click vào tên hoặc hình "Sauce Labs Backpack"<br/>2. Quan sát khu vực ảnh sản phẩm trên trang chi tiết |
| **Kết quả mong đợi** | Ảnh sản phẩm hiển thị rõ ràng, không bị vỡ hình. |
| **Kết quả thực tế** | Hiển thị icon “broken image”, không có ảnh sản phẩm. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Trung bình** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_INV_004, TC_PRODUCT_007 |

---

## BUG #7

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CART_001 |
| **Tiêu đề** | Badge số lượng giỏ hàng không cập nhật sau khi thêm sản phẩm |
| **Mô tả** | Sau khi click `Add to cart`, badge trên icon giỏ hàng vẫn không hiện số lượng. |
| **Các bước tái hiện** | 1. Đăng nhập và vào trang Inventory<br/>2. Chọn một sản phẩm bất kỳ, click `Add to cart`<br/>3. Quan sát icon giỏ hàng ở góc phải trên |
| **Kết quả mong đợi** | Badge hiển thị số `1` tương ứng với số sản phẩm trong giỏ. |
| **Kết quả thực tế** | Badge không hiển thị hoặc hiển thị sai số lượng. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_CART_001, TC_CART_001 |

---

## BUG #8

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CART_002 |
| **Tiêu đề** | Tổng tiền sản phẩm trong giỏ không chính xác |
| **Mô tả** | Khi có nhiều sản phẩm trong giỏ, item total hiển thị không khớp với tổng cộng từng sản phẩm. |
| **Các bước tái hiện** | 1. Thêm ít nhất 2 sản phẩm khác nhau vào giỏ từ trang Inventory<br/>2. Click icon giỏ hàng để vào trang Cart<br/>3. So sánh tổng tiền hiển thị với phép cộng tay giá từng sản phẩm |
| **Kết quả mong đợi** | Tổng tiền bằng tổng giá của tất cả sản phẩm trong giỏ. |
| **Kết quả thực tế** | Tổng tiền bị lệch (thiếu hoặc thừa) so với kết quả tính toán. |
| **Mức độ nghiêm trọng** | **Critical** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_CART_002, TC_CART_005 |

---

## BUG #9

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CART_003 |
| **Tiêu đề** | Nút `Checkout` vẫn cho click khi giỏ hàng trống |
| **Mô tả** | Sau khi xóa hết sản phẩm, nút `Checkout` vẫn active và khi click sẽ chuyển sang luồng thanh toán với giỏ rỗng. |
| **Các bước tái hiện** | 1. Thêm 1–2 sản phẩm vào giỏ<br/>2. Vào trang Cart và xóa toàn bộ sản phẩm (`Remove`)<br/>3. Kiểm tra trạng thái nút `Checkout` và thử click |
| **Kết quả mong đợi** | Khi giỏ rỗng, nút `Checkout` phải bị ẩn hoặc disabled. |
| **Kết quả thực tế** | Nút `Checkout` vẫn click được dẫn tới lỗi logic. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_CART_008 |

---

## BUG #10

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CHECKOUT_001 |
| **Tiêu đề** | Không bắt buộc nhập đủ First Name / Last Name / Postal Code |
| **Mô tả** | Ở bước nhập thông tin checkout, để trống một trong các trường nhưng hệ thống vẫn cho qua trang Overview. |
| **Các bước tái hiện** | 1. Từ giỏ hàng có ít nhất 1 sản phẩm, click `Checkout`<br/>2. Để trống First Name, nhập các trường còn lại<br/>3. Click `Continue`<br/>4. Lặp lại với trường hợp trống Last Name, Postal Code |
| **Kết quả mong đợi** | Mỗi trường trống phải hiện thông báo lỗi tương ứng, không cho qua bước tiếp theo. |
| **Kết quả thực tế** | Có trường để trống nhưng hệ thống vẫn cho qua bước Overview. |
| **Mức độ nghiêm trọng** | **Major** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_SWAG_CHECKOUT_002 |

---

## BUG #11

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CHECKOUT_002 |
| **Tiêu đề** | Postal Code 4 ký tự vẫn được chấp nhận |
| **Mô tả** | Trường Zip/Postal Code cho phép nhập 4 ký tự, trong khi yêu cầu tối thiểu là 5 ký tự. |
| **Các bước tái hiện** | 1. Ở trang thông tin checkout<br/>2. Nhập Zip/Postal Code: `1000` (4 ký tự)<br/>3. Click `Continue` |
| **Kết quả mong đợi** | Hiển thị lỗi “Postal Code phải tối thiểu 5 ký tự” và không cho qua. |
| **Kết quả thực tế** | Hệ thống chấp nhận và chuyển sang bước tiếp theo. |
| **Mức độ nghiêm trọng** | **Minor** |
| **Mức ưu tiên** | **Trung bình** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_CHECKOUT_004 |

---

## BUG #12

| Trường | Chi tiết |
|--------|---------|
| **Mã lỗi** | BUG_SWAG_CHECKOUT_003 |
| **Tiêu đề** | Item total trên trang checkout hiển thị sai |
| **Mô tả** | Khi giỏ hàng gồm sản phẩm "Sauce Labs Backpack" ($29.99) và "Sauce Labs Bike Light" ($9.99), item total không bằng $39.98. |
| **Các bước tái hiện** | 1. Thêm "Sauce Labs Backpack" và "Sauce Labs Bike Light" vào giỏ<br/>2. Vào trang Cart, sau đó click `Checkout` và nhập thông tin hợp lệ<br/>3. Ở trang Overview, kiểm tra mục `Item total` |
| **Kết quả mong đợi** | Item total hiển thị đúng `$39.98`. |
| **Kết quả thực tế** | Item total hiển thị giá trị khác `$39.98`. |
| **Mức độ nghiêm trọng** | **Critical** |
| **Mức ưu tiên** | **Cao** |
| **Trạng thái** | Mới |
| **Môi trường** | Windows 10/11, Chrome 120+ |
| **Ca kiểm thử liên quan** | TC_CHECKOUT_007, TC_SWAG_CHECKOUT_001 |

---


### 3.2 Phân bố theo mô-đun

| Mô-đun | Critical | Major | Minor | Tổng |
|--------|----------|-------|-------|------|
| **Authentication** | 1 | 2 | 0 | 3 |
| **Product & Cart** | 1 | 3 | 1 | 5 |
| **Checkout** | 1 | 1 | 2 | 4 |
| **TỔNG** | **3** | **6** | **3** | **12** |

### 3.3 Phân bố theo mức ưu tiên

| Mức ưu tiên | Số lượng | % |
|----------|---------|-----|
| **Cao** | 9 | 75% |
| **Trung bình** | 3 | 25% |
| **Thấp** | 0 | 0% |

### 3.4 Phân Bố theo Loại Lỗi

| Loại | Bug ID | Số lượng |
|------|--------|---------|
| **Validation** | BUG_SWAG_CHECKOUT_001, BUG_SWAG_CHECKOUT_002 | 2 |
| **Calculation** | BUG_SWAG_CART_002, BUG_SWAG_CHECKOUT_003 | 2 |
| **Security** | BUG_SWAG_AUTH_001, BUG_SWAG_AUTH_002, BUG_SWAG_AUTH_003 | 3 |
| **UI/UX** | BUG_SWAG_INV_001, BUG_SWAG_INV_002, BUG_SWAG_PROD_001, BUG_SWAG_CART_001, BUG_SWAG_CART_003 | 5 |

---

## 4. BUG ĐƯỢC ƯU TIÊN KHẮC PHỤC TRƯỚC

### Giai đoạn 1: Critical (phải sửa ngay)
1. **BUG_SWAG_AUTH_001** – Cho phép đăng nhập với mật khẩu sai (bảo mật)  
2. **BUG_SWAG_CART_002** – Tổng tiền trong giỏ không chính xác (business)  
3. **BUG_SWAG_CHECKOUT_003** – Item total ở bước checkout sai (business)

### Giai đoạn 2: Major (nên sửa trước khi phát hành)
4. BUG_SWAG_AUTH_002 – Tài khoản bị khóa vẫn đăng nhập được  
5. BUG_SWAG_AUTH_003 – Đăng xuất không hủy session  
6. BUG_SWAG_PROD_001 – Ảnh sản phẩm không hiển thị  
7. BUG_SWAG_CART_001 – Badge giỏ hàng không cập nhật đúng  
8. BUG_SWAG_CART_003 – Vẫn cho checkout khi giỏ rỗng  
9. BUG_SWAG_CHECKOUT_001 – Không bắt buộc nhập đủ thông tin checkout

### Giai đoạn 3: Minor (có thể sửa sau)
10. BUG_SWAG_INV_001 – Sort theo Name không đúng hoàn toàn  
11. BUG_SWAG_INV_002 – Sort theo Price không đúng hoàn toàn  
12. BUG_SWAG_CHECKOUT_002 – Chấp nhận Postal Code 4 ký tự

---

## 5. KẾ HOẠCH KHẮC PHỤC

| Giai đoạn | Mục tiêu | Hạn hoàn thành | Người phụ trách |
|-------|---------|----------|-----------------|
| **Giai đoạn 1** | Sửa 3 bug Critical | 2-3 ngày | Dev Lead |
| **Giai đoạn 2** | Sửa 6 bug Major | 4-5 ngày | Dev Team |
| **Giai đoạn 3** | Sửa 3 bug Minor | Tuỳ chọn | Dev Team |
| **Kiểm thử lại** | Xác nhận bug đã được sửa | 2 ngày | QA Team |

---

## KẾT LUẬN

- **Tổng Bug:** 12 (Yêu cầu: ≥10) ✅
- **Critical bugs:** 3 (Yêu cầu: ≥2) ✅
- **Major bugs:** 6 (Yêu cầu: ≥4) ✅
- **Tất cả bug đều có thể tái hiện** ✅
- **Mức độ nghiêm trọng & mức ưu tiên hợp lý** ✅

**Quyết định phát hành:** ❌ **CHƯA PHÁT HÀNH** cho đến khi sửa hết 3 bug Critical

---

**KẾT THÚC BÁO CÁO LỖI**
