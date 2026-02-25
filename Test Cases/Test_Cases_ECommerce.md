# CA KIỂM THỬ
## Website Swag Labs (Saucedemo.com)


---


### Mô-đun SWAG_1: Đăng nhập & Đăng xuất

#### TC_SWAG_AUTH_001: Đăng nhập thành công với tài khoản demo hợp lệ 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_001 |
| **Tiêu đề** | Đăng nhập thành công với username/password demo hợp lệ |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng truy cập trang `https://www.saucedemo.com/` |
| **Các bước thực hiện** | 1. Nhập username demo hợp lệ **`standard_user`**<br/>2. Nhập password tương ứng **`secret_sauce`**<br/>3. Click nút `Login` |
| **Kết quả mong đợi** | Hệ thống chuyển sang trang Inventory, hiển thị danh sách sản phẩm |
| **Liên quan đến** | R_SWAG_1 |

#### TC_SWAG_AUTH_002: Đăng nhập thất bại với mật khẩu sai 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_002 |
| **Tiêu đề** | Đăng nhập thất bại khi mật khẩu không chính xác |
| **Loại** | Luồng sai |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng ở trang login Swag Labs |
| **Các bước thực hiện** | 1. Nhập username demo hợp lệ **`standard_user`**<br/>2. Nhập mật khẩu sai **`secret_suace`**<br/>3. Click `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo lỗi phía trên form login, người dùng không đăng nhập được |
| **Liên quan đến** | R_SWAG_1 |

#### TC_SWAG_AUTH_003: Đăng nhập với user bị khoá 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_003 |
| **Tiêu đề** | Hệ thống xử lý đúng khi đăng nhập bằng user bị khoá |
| **Loại** | Luồng sai |
| **Mức ưu tiên** | Trung bình |
| **Điều kiện trước** | Có sẵn username demo bị khoá  |
| **Các bước thực hiện** | 1. Nhập username bị khoá **`locked_out_user`**<br/>2. Nhập password chuẩn **`secret_sauce`**<br/>3. Click `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo user bị khoá, không vào được trang Inventory |
| **Liên quan đến** | R_SWAG_2 |

#### TC_SWAG_AUTH_004: Đăng xuất thành công 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_004 |
| **Tiêu đề** | Đăng xuất hệ thống qua menu trái |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng đã login thành công vào trang Inventory |
| **Các bước thực hiện** | 1. Click nút menu (3 gạch) ở góc trái trên<br/>2. Chọn `Logout` |
| **Kết quả mong đợi** | Hệ thống quay lại trang login, session cũ không còn hiệu lực |
| **Liên quan đến** | R_SWAG_3 |

### Mô-đun SWAG_2: Danh sách & Chi tiết sản phẩm

#### TC_SWAG_INV_001: Hiển thị đúng danh sách sản phẩm sau khi login
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_001 |
| **Tiêu đề** | Kiểm tra thông tin cơ bản của danh sách sản phẩm trên trang Inventory |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng đã login thành công |
| **Các bước thực hiện** | 1. Quan sát danh sách sản phẩm trên trang Inventory<br/>2. Kiểm tra tên, giá, mô tả, hình ảnh của một vài sản phẩm đại diện ** ** |
| **Kết quả mong đợi** | Mỗi sản phẩm hiển thị đầy đủ tên, giá, mô tả ngắn, hình ảnh; không bị vỡ layout |
| **Liên quan đến** | R_SWAG_4 |

#### TC_SWAG_INV_002: Sắp xếp sản phẩm theo Name (A to Z, Z to A) 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_002 |
| **Tiêu đề** | Kiểm tra chức năng sort theo tên sản phẩm |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Trung bình |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Chọn sort `Name (A to Z)`<br/>2. Ghi nhận thứ tự một vài sản phẩm ** **<br/>3. Chọn sort `Name (Z to A)`<br/>4. So sánh thứ tự hiển thị |
| **Kết quả mong đợi** | Danh sách sắp xếp đúng theo alphabet tăng dần/giảm dần |
| **Liên quan đến** | R_SWAG_5 |

#### TC_SWAG_INV_003: Sắp xếp sản phẩm theo Price (low to high, high to low) 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_003 |
| **Tiêu đề** | Kiểm tra chức năng sort theo giá sản phẩm |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Trung bình |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Chọn sort `Price (low to high)`<br/>2. Ghi lại giá của một số sản phẩm đầu danh sách ** **<br/>3. Chọn sort `Price (high to low)`<br/>4. So sánh lại thứ tự giá |
| **Kết quả mong đợi** | Sản phẩm được sắp xếp đúng theo giá tăng dần/giảm dần |
| **Liên quan đến** | R_SWAG_5 |

#### TC_SWAG_INV_004: Xem chi tiết một sản phẩm 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_004 |
| **Tiêu đề** | Mở trang chi tiết sản phẩm từ Inventory |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Click vào tên hoặc hình của một sản phẩm bất kỳ ** **<br/>2. Quan sát trang chi tiết |
| **Kết quả mong đợi** | Trang chi tiết hiển thị đúng tên, mô tả, giá, nút Add to cart/Remove, nút Back to products |
| **Liên quan đến** | R_SWAG_6 |

### Mô-đun SWAG_3: Giỏ hàng & Checkout

#### TC_SWAG_CART_001: Thêm sản phẩm vào giỏ từ trang Inventory 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CART_001 |
| **Tiêu đề** | Thêm một sản phẩm vào giỏ và kiểm tra badge giỏ hàng |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng ở trang Inventory, giỏ hàng đang trống |
| **Các bước thực hiện** | 1. Click `Add to cart` của một sản phẩm ** **<br/>2. Quan sát badge số ở icon giỏ hàng |
| **Kết quả mong đợi** | Badge hiển thị số `1`, nút trên sản phẩm đổi thành `Remove` |
| **Liên quan đến** | R_SWAG_7 |

#### TC_SWAG_CART_002: Xem chi tiết giỏ hàng 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CART_002 |
| **Tiêu đề** | Kiểm tra thông tin sản phẩm trong giỏ |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Có ít nhất 1 sản phẩm trong giỏ |
| **Các bước thực hiện** | 1. Click icon giỏ hàng<br/>2. Đối chiếu tên, giá, số lượng sản phẩm trong giỏ với trang Inventory ** ** |
| **Kết quả mong đợi** | Thông tin sản phẩm trong giỏ khớp với sản phẩm đã chọn, tổng tiền item được hiển thị đúng |
| **Liên quan đến** | R_SWAG_7 |

#### TC_SWAG_CHECKOUT_001: Thực hiện checkout đầy đủ thông tin 
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CHECKOUT_001 |
| **Tiêu đề** | Checkout thành công với First Name, Last Name, Postal Code hợp lệ |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Trong giỏ có ít nhất 1 sản phẩm |
| **Các bước thực hiện** | 1. Từ giỏ hàng click `Checkout`<br/>2. Nhập First Name, Last Name, Postal Code hợp lệ **`Nguyen, Van A, 50000`**<br/>3. Click `Continue`<br/>4. Kiểm tra trang Overview<br/>5. Click `Finish` |
| **Kết quả mong đợi** | Hiển thị trang hoàn tất đơn hàng (THANK YOU), có nút `Back Home` |
| **Liên quan đến** | R_SWAG_8 |

#### TC_SWAG_CHECKOUT_002: Bắt buộc nhập thông tin ở bước checkout  
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CHECKOUT_002 |
| **Tiêu đề** | Kiểm tra validation khi để trống các trường checkout |
| **Loại** | Luồng sai |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng ở bước nhập thông tin checkout |
| **Các bước thực hiện** | 1. Để trống First Name và click `Continue`<br/>2. Lặp lại cho Last Name và Postal Code **`, Van A, 50000`** |
| **Kết quả mong đợi** | Hệ thống hiển thị thông báo lỗi tương ứng từng trường, không cho qua bước Overview |
| **Liên quan đến** | R_SWAG_8 |

---

## Mô-đun 2: PRODUCT & CART (20 ca kiểm thử)

### TC_PRODUCT_001: Xem chi tiết sản phẩm
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_007 |
| **Tiêu đề** | Xem chi tiết sản phẩm thành công |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng ở trang danh sách sản phẩm |
| **Các bước thực hiện** | 1. Ấn vào sản phẩm "Sauce Labs Backpack" |
| **Kết quả mong đợi** | Mở trang chi tiết với tên, giá, mô tả, hình ảnh |
| **Liên quan đến** | R9 |

### TC_CART_001: Thêm sản phẩm vào giỏ thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_001 |
| **Tiêu đề** | Thêm sản phẩm vào giỏ hàng thành công |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Người dùng đã đăng nhập, ở trang chi tiết sản phẩm |
| **Các bước thực hiện** | Ấn "Add to cart" |
| **Kết quả mong đợi** | Sản phẩm được thêm vào giỏ hàng, Nút "Add to cart" thành "Remove" |
| **Liên quan đến** | R10 |


### TC_CART_002: Xem giỏ hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_005 |
| **Tiêu đề** | Xem chi tiết giỏ hàng |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Giỏ hàng có sản phẩm |
| **Các bước thực hiện** | 1. Ấn biểu tượng "Giỏ hàng" |
| **Kết quả mong đợi** | Hiển thị danh sách sản phẩm, giá|
| **Liên quan đến** | R11 |


### TC_CART_003: Xoá sản phẩm khỏi giỏ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_007 |
| **Tiêu đề** | Xoá sản phẩm khỏi giỏ hàng |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Giỏ hàng có sản phẩm |
| **Các bước thực hiện** | 1. Mở giỏ hàng<br/>2. Ấn nút "Remove" trên sản phẩm |
| **Kết quả mong đợi** | Sản phẩm bị xoá, giỏ hàng cập nhật |
| **Liên quan đến** | R12 |

### TC_CART_004: Giỏ hàng trống
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_008 |
| **Tiêu đề** | Hiển thị giỏ hàng khi trống |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Trung bình |
| **Điều kiện trước** | Giỏ hàng không có sản phẩm |
| **Các bước thực hiện** | 1. Ấn biểu tượng "Giỏ hàng" |
| **Kết quả mong đợi** | Hiển thị giỏ hàng trống |
| **Liên quan đến** | R12 |

---

## Mô-đun 3: CHECKOUT (15 ca kiểm thử)

### TC_CHECKOUT_001: Thanh toán thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_001 |
| **Tiêu đề** | Đặt hàng thành công với phương thức |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Giỏ hàng có sản phẩm, người dùng đã đăng nhập |
| **Các bước thực hiện** | 1. Nhấn "Checkout"<br/>2. Nhập First Name: "Thanh"<br/>Last Name: "Le"<br/> Zip/Portal Code: "123456"<br/>3. Chọn "Continue"<br/>4. Ấn "Finish" |
| **Kết quả mong đợi** | Đặt hàng thành công|
| **Liên quan đến** | R13, R14, R15 |

### TC_CHECKOUT_002: Thanh toán thất bại (Zip/Postal Code trống)
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_002 |
| **Tiêu đề** | Đặt hàng thất bại khi không nhập địa chỉ |
| **Loại** | Luồng sai |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Để trống Zip/Postal Code <br/>2. Ấn "Continue" |
| **Kết quả mong đợi** | Hiển thị lỗi "Error: Postal Code is required" |
| **Liên quan đến** | R13 |

### TC_CHECKOUT_004: Zip/Postal Code hợp lệ tối thiểu
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_004 |
| **Tiêu đề** | Chấp Zip/Postal Code chỉ đúng 5 ký tự |
| **Loại** | Giá trị biên |
| **Mức ưu tiên** | Trung bình |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Nhập Zip/Postal Code: "50000" (5 ký tự)<br/>2. Ấn "Continue" |
| **Kết quả mong đợi** | Địa chỉ được chấp nhận |
| **Liên quan đến** | R13 |


### TC_CHECKOUT_003: Tính tổng tiền chính xác
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_007 |
| **Tiêu đề** | Tính tổng tiền thanh toán chính xác |
| **Loại** | Luồng đúng |
| **Mức ưu tiên** | Cao |
| **Điều kiện trước** | Giỏ hàng: Sản phẩm Sauce Labs Backpack ($29.99), Sản phẩm Sauce Labs Bike Light ($9.99) |
| **Các bước thực hiện** | 1. Ở trang thanh toán<br/>2. Kiểm tra tổng tiền |
| **Kết quả mong đợi** | Item total = $39.98|
| **Liên quan đến** | R15 |


---

## TỔNG HỢPP

| Mô-đun | Tổng số ca kiểm thử | Luồng đúng | Luồng sai | Giá trị biên |
|--------|---------|----------|----------|----------|
| Authentication | 4 | 2 | 2 | 0 |
| Product & Cart | 11 | 11 | 0 | 0 |
| Checkout | 6 | 3 | 2 | 1 |
| **TỔNG CỘNG** | **21** | **16** | **4** | **1** |


---

**KẾT THÚC CA KIỂM THỬ**





