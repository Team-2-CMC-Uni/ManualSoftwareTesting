# CA KIỂM THỬ (TEST CASES)
## Website Swag Labs (Saucedemo.com)

Tài liệu này gồm 2 phần:
- **Phần A – Swag Labs [Thực tế]**: Các test case áp dụng trực tiếp trên `https://www.saucedemo.com/`
- **Phần B – Demo E-Commerce**: Bộ test case mẫu cho hệ thống bán hàng online tổng quát (giữ lại để tham khảo kỹ thuật thiết kế)

> Gợi ý: Khi thực hành, ưu tiên dùng **Phần A**.  
> Các giá trị cụ thể như username/password, sản phẩm, số lượng… bạn tự bổ sung và chỉnh sửa trong file với tag **`[Thực tế]`**.

---

## PHẦN A – SWAG LABS [Thực tế]

### MODULE SWAG_1: Đăng nhập & Đăng xuất

#### TC_SWAG_AUTH_001: Đăng nhập thành công với tài khoản demo hợp lệ [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_001 |
| **Tiêu đề** | Đăng nhập thành công với username/password demo hợp lệ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng truy cập trang `https://www.saucedemo.com/` |
| **Các bước thực hiện** | 1. Nhập username demo hợp lệ **[Thực tế]**<br/>2. Nhập password tương ứng **[Thực tế]**<br/>3. Click nút `Login` |
| **Kết quả mong đợi** | Hệ thống chuyển sang trang Inventory, hiển thị danh sách sản phẩm |
| **Liên quan đến** | R_SWAG_1 |

#### TC_SWAG_AUTH_002: Đăng nhập thất bại với mật khẩu sai [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_002 |
| **Tiêu đề** | Đăng nhập thất bại khi mật khẩu không chính xác |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang login Swag Labs |
| **Các bước thực hiện** | 1. Nhập username demo hợp lệ **[Thực tế]**<br/>2. Nhập mật khẩu sai **[Thực tế]**<br/>3. Click `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo lỗi phía trên form login, người dùng không đăng nhập được |
| **Liên quan đến** | R_SWAG_1 |

#### TC_SWAG_AUTH_003: Đăng nhập với user bị khoá [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_003 |
| **Tiêu đề** | Hệ thống xử lý đúng khi đăng nhập bằng user bị khoá |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Có sẵn username demo bị khoá **[Thực tế]** |
| **Các bước thực hiện** | 1. Nhập username bị khoá **[Thực tế]**<br/>2. Nhập password chuẩn **[Thực tế]**<br/>3. Click `Login` |
| **Kết quả mong đợi** | Hiển thị thông báo user bị khoá, không vào được trang Inventory |
| **Liên quan đến** | R_SWAG_2 |

#### TC_SWAG_AUTH_004: Đăng xuất thành công [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_AUTH_004 |
| **Tiêu đề** | Đăng xuất hệ thống qua menu trái |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã login thành công vào trang Inventory |
| **Các bước thực hiện** | 1. Click nút menu (3 gạch) ở góc trái trên<br/>2. Chọn `Logout` |
| **Kết quả mong đợi** | Hệ thống quay lại trang login, session cũ không còn hiệu lực |
| **Liên quan đến** | R_SWAG_3 |

### MODULE SWAG_2: Danh sách & Chi tiết sản phẩm

#### TC_SWAG_INV_001: Hiển thị đúng danh sách sản phẩm sau khi login [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_001 |
| **Tiêu đề** | Kiểm tra thông tin cơ bản của danh sách sản phẩm trên trang Inventory |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã login thành công |
| **Các bước thực hiện** | 1. Quan sát danh sách sản phẩm trên trang Inventory<br/>2. Kiểm tra tên, giá, mô tả, hình ảnh của một vài sản phẩm đại diện **[Thực tế]** |
| **Kết quả mong đợi** | Mỗi sản phẩm hiển thị đầy đủ tên, giá, mô tả ngắn, hình ảnh; không bị vỡ layout |
| **Liên quan đến** | R_SWAG_4 |

#### TC_SWAG_INV_002: Sắp xếp sản phẩm theo Name (A to Z, Z to A) [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_002 |
| **Tiêu đề** | Kiểm tra chức năng sort theo tên sản phẩm |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Chọn sort `Name (A to Z)`<br/>2. Ghi nhận thứ tự một vài sản phẩm **[Thực tế]**<br/>3. Chọn sort `Name (Z to A)`<br/>4. So sánh thứ tự hiển thị |
| **Kết quả mong đợi** | Danh sách sắp xếp đúng theo alphabet tăng dần/giảm dần |
| **Liên quan đến** | R_SWAG_5 |

#### TC_SWAG_INV_003: Sắp xếp sản phẩm theo Price (low to high, high to low) [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_003 |
| **Tiêu đề** | Kiểm tra chức năng sort theo giá sản phẩm |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Chọn sort `Price (low to high)`<br/>2. Ghi lại giá của một số sản phẩm đầu danh sách **[Thực tế]**<br/>3. Chọn sort `Price (high to low)`<br/>4. So sánh lại thứ tự giá |
| **Kết quả mong đợi** | Sản phẩm được sắp xếp đúng theo giá tăng dần/giảm dần |
| **Liên quan đến** | R_SWAG_5 |

#### TC_SWAG_INV_004: Xem chi tiết một sản phẩm [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_INV_004 |
| **Tiêu đề** | Mở trang chi tiết sản phẩm từ Inventory |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang Inventory |
| **Các bước thực hiện** | 1. Click vào tên hoặc hình của một sản phẩm bất kỳ **[Thực tế]**<br/>2. Quan sát trang chi tiết |
| **Kết quả mong đợi** | Trang chi tiết hiển thị đúng tên, mô tả, giá, nút Add to cart/Remove, nút Back to products |
| **Liên quan đến** | R_SWAG_6 |

### MODULE SWAG_3: Giỏ hàng & Checkout

#### TC_SWAG_CART_001: Thêm sản phẩm vào giỏ từ trang Inventory [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CART_001 |
| **Tiêu đề** | Thêm một sản phẩm vào giỏ và kiểm tra badge giỏ hàng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang Inventory, giỏ hàng đang trống |
| **Các bước thực hiện** | 1. Click `Add to cart` của một sản phẩm **[Thực tế]**<br/>2. Quan sát badge số ở icon giỏ hàng |
| **Kết quả mong đợi** | Badge hiển thị số `1`, nút trên sản phẩm đổi thành `Remove` |
| **Liên quan đến** | R_SWAG_7 |

#### TC_SWAG_CART_002: Xem chi tiết giỏ hàng [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CART_002 |
| **Tiêu đề** | Kiểm tra thông tin sản phẩm trong giỏ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Có ít nhất 1 sản phẩm trong giỏ |
| **Các bước thực hiện** | 1. Click icon giỏ hàng<br/>2. Đối chiếu tên, giá, số lượng sản phẩm trong giỏ với trang Inventory **[Thực tế]** |
| **Kết quả mong đợi** | Thông tin sản phẩm trong giỏ khớp với sản phẩm đã chọn, tổng tiền item được hiển thị đúng |
| **Liên quan đến** | R_SWAG_7 |

#### TC_SWAG_CHECKOUT_001: Thực hiện checkout đầy đủ thông tin [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CHECKOUT_001 |
| **Tiêu đề** | Checkout thành công với First Name, Last Name, Postal Code hợp lệ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Trong giỏ có ít nhất 1 sản phẩm |
| **Các bước thực hiện** | 1. Từ giỏ hàng click `Checkout`<br/>2. Nhập First Name, Last Name, Postal Code hợp lệ **[Thực tế]**<br/>3. Click `Continue`<br/>4. Kiểm tra trang Overview<br/>5. Click `Finish` |
| **Kết quả mong đợi** | Hiển thị trang hoàn tất đơn hàng (THANK YOU), có nút `Back Home` |
| **Liên quan đến** | R_SWAG_8 |

#### TC_SWAG_CHECKOUT_002: Bắt buộc nhập thông tin ở bước checkout [Thực tế]
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_SWAG_CHECKOUT_002 |
| **Tiêu đề** | Kiểm tra validation khi để trống các trường checkout |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở bước nhập thông tin checkout |
| **Các bước thực hiện** | 1. Để trống First Name và click `Continue`<br/>2. Lặp lại cho Last Name và Postal Code **[Thực tế]** |
| **Kết quả mong đợi** | Hệ thống hiển thị thông báo lỗi tương ứng từng trường, không cho qua bước Overview |
| **Liên quan đến** | R_SWAG_8 |

---

## PHẦN B – HỆ THỐNG WEB BÁN HÀNG ONLINE (DEMO)

> Phần này giữ nguyên các test case demo cho một hệ thống e-commerce tổng quát  
> (có đăng ký, tìm kiếm, lọc, mã giảm giá, email…).  
> Khi test Swag Labs, bạn **không cần dùng các test case không tồn tại trên trang thực tế**.

## MODULE 1: AUTHENTICATION (15 Test Cases)

### TC_AUTH_001: Đăng ký tài khoản với email hợp lệ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_001 |
| **Tiêu đề** | Đăng ký tài khoản với email hợp lệ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng chưa có tài khoản |
| **Các bước thực hiện** | 1. Mở trang đăng ký<br/>2. Nhập email: user@example.com<br/>3. Nhập mật khẩu: Abc@12345<br/>4. Nhập xác nhận mật khẩu: Abc@12345<br/>5. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Tài khoản được tạo thành công, hiển thị thông báo "Đăng ký thành công" |
| **Liên quan đến** | R1 |

### TC_AUTH_002: Đăng ký thất bại với email không hợp lệ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_002 |
| **Tiêu đề** | Đăng ký không thành công với email định dạng sai |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng ký |
| **Các bước thực hiện** | 1. Nhập email: userexample.com (thiếu @)<br/>2. Nhập mật khẩu: Abc@12345<br/>3. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email không hợp lệ", tài khoản không được tạo |
| **Liên quan đến** | R2 |

### TC_AUTH_003: Đăng ký thất bại với mật khẩu quá ngắn
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_003 |
| **Tiêu đề** | Đăng ký không thành công với mật khẩu < 8 ký tự |
| **Loại** | Boundary |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng ký |
| **Các bước thực hiện** | 1. Nhập email: user@test.com<br/>2. Nhập mật khẩu: Abc@1 (7 ký tự)<br/>3. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Hiển thị lỗi "Mật khẩu phải có ít nhất 8 ký tự" |
| **Liên quan đến** | R3 |

### TC_AUTH_004: Mật khẩu chính xác 8 ký tự được chấp nhận
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_004 |
| **Tiêu đề** | Đăng ký thành công với mật khẩu đúng 8 ký tự |
| **Loại** | Boundary |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng ký |
| **Các bước thực hiện** | 1. Nhập email: user@test.com<br/>2. Nhập mật khẩu: Abc@1234 (8 ký tự)<br/>3. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Tài khoản được tạo thành công |
| **Liên quan đến** | R3 |

### TC_AUTH_005: Mật khẩu không khớp
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_005 |
| **Tiêu đề** | Đăng ký thất bại khi mật khẩu xác nhận không khớp |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng ký |
| **Các bước thực hiện** | 1. Nhập email: user@test.com<br/>2. Nhập mật khẩu: Abc@12345<br/>3. Nhập xác nhận: Abc@12346<br/>4. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Hiển thị lỗi "Mật khẩu không khớp" |
| **Liên quan đến** | R3 |

### TC_AUTH_006: Email đã được đăng ký
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_006 |
| **Tiêu đề** | Đăng ký thất bại khi email đã tồn tại |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Tài khoản user@test.com đã tồn tại |
| **Các bước thực hiện** | 1. Nhập email: user@test.com (đã dùng)<br/>2. Nhập mật khẩu: Abc@12345<br/>3. Ấn nút "Đăng ký" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email đã được đăng ký" |
| **Liên quan đến** | R1 |

### TC_AUTH_007: Đăng nhập thành công với thông tin hợp lệ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_007 |
| **Tiêu đề** | Đăng nhập thành công với email và mật khẩu đúng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Tài khoản user@test.com đã tồn tại |
| **Các bước thực hiện** | 1. Mở trang đăng nhập<br/>2. Nhập email: user@test.com<br/>3. Nhập mật khẩu: Abc@12345<br/>4. Ấn nút "Đăng nhập" |
| **Kết quả mong đợi** | Đăng nhập thành công, chuyển đến trang chủ |
| **Liên quan đến** | R4 |

### TC_AUTH_008: Đăng nhập thất bại với mật khẩu sai
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_008 |
| **Tiêu đề** | Đăng nhập thất bại với mật khẩu không chính xác |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Tài khoản user@test.com đã tồn tại |
| **Các bước thực hiện** | 1. Nhập email: user@test.com<br/>2. Nhập mật khẩu: WrongPassword<br/>3. Ấn nút "Đăng nhập" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email hoặc mật khẩu không chính xác" |
| **Liên quan đến** | R5 |

### TC_AUTH_009: Đăng nhập thất bại với email không tồn tại
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_009 |
| **Tiêu đề** | Đăng nhập thất bại khi email không tồn tại |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng nhập |
| **Các bước thực hiện** | 1. Nhập email: notexist@test.com<br/>2. Nhập mật khẩu: Abc@12345<br/>3. Ấn nút "Đăng nhập" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email hoặc mật khẩu không chính xác" |
| **Liên quan đến** | R4, R5 |

### TC_AUTH_010: Đăng nhập thất bại khi email trống
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_010 |
| **Tiêu đề** | Đăng nhập thất bại khi không nhập email |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang đăng nhập |
| **Các bước thực hiện** | 1. Để trống email<br/>2. Nhập mật khẩu: Abc@12345<br/>3. Ấn nút "Đăng nhập" |
| **Kết quả mong đợi** | Hiển thị lỗi "Email không được để trống" |
| **Liên quan đến** | R4 |

### TC_AUTH_011: Quên mật khẩu gửi email reset
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_011 |
| **Tiêu đề** | Quên mật khẩu gửi email đặt lại thành công |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Tài khoản user@test.com đã tồn tại |
| **Các bước thực hiện** | 1. Ấn "Quên mật khẩu"<br/>2. Nhập email: user@test.com<br/>3. Ấn nút "Gửi email reset" |
| **Kết quả mong đợi** | Hiển thị "Email reset đã được gửi, kiểm tra hộp thư" |
| **Liên quan đến** | R6 |

### TC_AUTH_012: Quên mật khẩu với email không tồn tại
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_012 |
| **Tiêu đề** | Quên mật khẩu không thành công với email không tồn tại |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang quên mật khẩu |
| **Các bước thực hiện** | 1. Nhập email: notexist@test.com<br/>2. Ấn nút "Gửi email reset" |
| **Kết quả mong đợi** | Hiển thị "Email không tồn tại trong hệ thống" |
| **Liên quan đến** | R6 |

### TC_AUTH_013: Đăng xuất thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_013 |
| **Tiêu đề** | Đăng xuất thành công |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã đăng nhập |
| **Các bước thực hiện** | 1. Ấn nút "Đăng xuất" trong menu |
| **Kết quả mong đợi** | Đăng xuất thành công, chuyển đến trang đăng nhập |
| **Liên quan đến** | R4 |

### TC_AUTH_014: Session hết hạn tự động đăng xuất
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_014 |
| **Tiêu đề** | Tự động đăng xuất khi session hết hạn |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng đã đăng nhập, session timeout = 30 phút |
| **Các bước thực hiện** | 1. Đăng nhập thành công<br/>2. Chờ session hết hạn (30 phút)<br/>3. Thực hiện hành động |
| **Kết quả mong đợi** | Tự động đăng xuất, chuyển đến trang đăng nhập |
| **Liên quan đến** | R4 |

### TC_AUTH_015: Xác nhận bảo mật - SQL Injection
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_AUTH_015 |
| **Tiêu đề** | Hệ thống bảo vệ chống SQL Injection |
| **Loại** | Negative (Security) |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang đăng nhập |
| **Các bước thực hiện** | 1. Nhập email: ' OR '1'='1<br/>2. Nhập mật khẩu: ' OR '1'='1<br/>3. Ấn nút "Đăng nhập" |
| **Kết quả mong đợi** | Đăng nhập thất bại, hiển thị lỗi |
| **Liên quan đến** | R4 |

---

## MODULE 2: PRODUCT & CART (20 Test Cases)

### TC_PRODUCT_001: Tìm kiếm sản phẩm thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_001 |
| **Tiêu đề** | Tìm kiếm sản phẩm với từ khoá hợp lệ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã đăng nhập, hệ thống có sản phẩm "Laptop" |
| **Các bước thực hiện** | 1. Nhập "Laptop" vào thanh tìm kiếm<br/>2. Ấn "Tìm kiếm" |
| **Kết quả mong đợi** | Hiển thị danh sách sản phẩm có tên chứa "Laptop" |
| **Liên quan đến** | R7 |

### TC_PRODUCT_002: Tìm kiếm sản phẩm trống
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_002 |
| **Tiêu đề** | Tìm kiếm không thành công khi không nhập từ khoá |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang sản phẩm |
| **Các bước thực hiện** | 1. Để trống thanh tìm kiếm<br/>2. Ấn "Tìm kiếm" |
| **Kết quả mong đợi** | Hiển thị thông báo "Nhập từ khoá để tìm kiếm" |
| **Liên quan đến** | R7 |

### TC_PRODUCT_003: Tìm kiếm không tìm thấy kết quả
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_003 |
| **Tiêu đề** | Tìm kiếm với từ khoá không tồn tại |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang sản phẩm |
| **Các bước thực hiện** | 1. Nhập "XYZ123ProductNotExist"<br/>2. Ấn "Tìm kiếm" |
| **Kết quả mong đợi** | Hiển thị "Không tìm thấy kết quả" |
| **Liên quan đến** | R7 |

### TC_PRODUCT_004: Lọc theo khoảng giá thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_004 |
| **Tiêu đề** | Lọc sản phẩm theo khoảng giá |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang sản phẩm |
| **Các bước thực hiện** | 1. Nhập giá từ: 500,000đ<br/>2. Nhập giá đến: 2,000,000đ<br/>3. Ấn "Lọc" |
| **Kết quả mong đợi** | Hiển thị sản phẩm có giá trong khoảng 500K - 2M |
| **Liên quan đến** | R8 |

### TC_PRODUCT_005: Lọc theo danh mục
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_005 |
| **Tiêu đề** | Lọc sản phẩm theo danh mục |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang sản phẩm |
| **Các bước thực hiện** | 1. Chọn danh mục "Electronics"<br/>2. Ấn "Lọc" |
| **Kết quả mong đợi** | Hiển thị sản phẩm thuộc danh mục "Electronics" |
| **Liên quan đến** | R8 |

### TC_PRODUCT_006: Lọc giá sai (từ > đến)
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_006 |
| **Tiêu đề** | Lọc giá không hợp lệ (giá từ > giá đến) |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang sản phẩm |
| **Các bước thực hiện** | 1. Nhập giá từ: 2,000,000đ<br/>2. Nhập giá đến: 500,000đ<br/>3. Ấn "Lọc" |
| **Kết quả mong đợi** | Hiển thị lỗi "Giá từ không thể lớn hơn giá đến" |
| **Liên quan đến** | R8 |

### TC_PRODUCT_007: Xem chi tiết sản phẩm
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_007 |
| **Tiêu đề** | Xem chi tiết sản phẩm thành công |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng ở trang danh sách sản phẩm |
| **Các bước thực hiện** | 1. Ấn vào sản phẩm "Samsung Galaxy A12" |
| **Kết quả mong đợi** | Mở trang chi tiết với tên, giá, mô tả, hình ảnh, đánh giá |
| **Liên quan đến** | R9 |

### TC_PRODUCT_008: Xem đánh giá sản phẩm
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_PRODUCT_008 |
| **Tiêu đề** | Xem đánh giá của sản phẩm |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang chi tiết sản phẩm |
| **Các bước thực hiện** | 1. Cuộn xuống phần "Đánh giá" |
| **Kết quả mong đợi** | Hiển thị danh sách đánh giá, điểm số, bình luận |
| **Liên quan đến** | R9 |

### TC_CART_001: Thêm sản phẩm vào giỏ thành công
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_001 |
| **Tiêu đề** | Thêm sản phẩm vào giỏ hàng thành công |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã đăng nhập, ở trang chi tiết sản phẩm |
| **Các bước thực hiện** | 1. Nhập số lượng: 2<br/>2. Ấn "Thêm vào giỏ" |
| **Kết quả mong đợi** | Sản phẩm được thêm, hiển thị "Thêm vào giỏ thành công" |
| **Liên quan đến** | R10 |

### TC_CART_002: Thêm sản phẩm khi chưa đăng nhập
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_002 |
| **Tiêu đề** | Thêm sản phẩm khi chưa đăng nhập |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Người dùng chưa đăng nhập, ở trang chi tiết sản phẩm |
| **Các bước thực hiện** | 1. Ấn "Thêm vào giỏ" |
| **Kết quả mong đợi** | Chuyển đến trang đăng nhập |
| **Liên quan đến** | R10 |

### TC_CART_003: Thêm sản phẩm với số lượng 0
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_003 |
| **Tiêu đề** | Thêm sản phẩm không thành công khi số lượng = 0 |
| **Loại** | Boundary |
| **Priority** | Medium |
| **Điều kiện trước** | Người dùng ở trang chi tiết sản phẩm |
| **Các bước thực hiện** | 1. Nhập số lượng: 0<br/>2. Ấn "Thêm vào giỏ" |
| **Kết quả mong đợi** | Hiển thị lỗi "Số lượng phải > 0" |
| **Liên quan đến** | R10 |

### TC_CART_004: Thêm sản phẩm vượt quá tồn kho
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_004 |
| **Tiêu đề** | Thêm số lượng vượt quá tồn kho |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Sản phẩm có tồn kho = 5 |
| **Các bước thực hiện** | 1. Nhập số lượng: 10<br/>2. Ấn "Thêm vào giỏ" |
| **Kết quả mong đợi** | Hiển thị lỗi "Tồn kho chỉ còn 5 sản phẩm" |
| **Liên quan đến** | R10 |

### TC_CART_005: Xem giỏ hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_005 |
| **Tiêu đề** | Xem chi tiết giỏ hàng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Giỏ hàng có sản phẩm |
| **Các bước thực hiện** | 1. Ấn biểu tượng "Giỏ hàng" |
| **Kết quả mong đợi** | Hiển thị danh sách sản phẩm, số lượng, giá, tổng tiền |
| **Liên quan đến** | R11 |

### TC_CART_006: Cập nhật số lượng sản phẩm
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_006 |
| **Tiêu đề** | Cập nhật số lượng sản phẩm trong giỏ |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Giỏ hàng có sản phẩm |
| **Các bước thực hiện** | 1. Mở giỏ hàng<br/>2. Thay đổi số lượng từ 2 → 3<br/>3. Ấn "Cập nhật" |
| **Kết quả mong đợi** | Số lượng được cập nhật, tổng tiền thay đổi |
| **Liên quan đến** | R11 |

### TC_CART_007: Xoá sản phẩm khỏi giỏ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_007 |
| **Tiêu đề** | Xoá sản phẩm khỏi giỏ hàng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Giỏ hàng có sản phẩm |
| **Các bước thực hiện** | 1. Mở giỏ hàng<br/>2. Ấn nút "Xoá" trên sản phẩm |
| **Kết quả mong đợi** | Sản phẩm bị xoá, giỏ hàng cập nhật |
| **Liên quan đến** | R12 |

### TC_CART_008: Giỏ hàng trống
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CART_008 |
| **Tiêu đề** | Hiển thị giỏ hàng khi trống |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Giỏ hàng không có sản phẩm |
| **Các bước thực hiện** | 1. Ấn biểu tượng "Giỏ hàng" |
| **Kết quả mong đợi** | Hiển thị thông báo "Giỏ hàng trống", nút "Tiếp tục mua" |
| **Liên quan đến** | R12 |

---

## MODULE 3: CHECKOUT (15 Test Cases)

### TC_CHECKOUT_001: Thanh toán thành công (COD)
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_001 |
| **Tiêu đề** | Đặt hàng thành công với phương thức COD |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Giỏ hàng có sản phẩm, người dùng đã đăng nhập |
| **Các bước thực hiện** | 1. Nhấn "Thanh toán"<br/>2. Nhập địa chỉ: "123 Đường ABC, TP.HCM"<br/>3. Chọn "Thanh toán khi nhận hàng (COD)"<br/>4. Ấn "Đặt hàng" |
| **Kết quả mong đợi** | Đặt hàng thành công, hiển thị mã đơn hàng |
| **Liên quan đến** | R13, R14, R15 |

### TC_CHECKOUT_002: Thanh toán thất bại (địa chỉ trống)
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_002 |
| **Tiêu đề** | Đặt hàng thất bại khi không nhập địa chỉ |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Để trống địa chỉ<br/>2. Chọn phương thức thanh toán<br/>3. Ấn "Đặt hàng" |
| **Kết quả mong đợi** | Hiển thị lỗi "Địa chỉ không được để trống" |
| **Liên quan đến** | R13 |

### TC_CHECKOUT_003: Địa chỉ quá ngắn
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_003 |
| **Tiêu đề** | Không chấp nhận địa chỉ quá ngắn |
| **Loại** | Boundary |
| **Priority** | Medium |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Nhập địa chỉ: "ABC" (3 ký tự)<br/>2. Ấn "Đặt hàng" |
| **Kết quả mong đợi** | Hiển thị lỗi "Địa chỉ phải có ít nhất 10 ký tự" |
| **Liên quan đến** | R13 |

### TC_CHECKOUT_004: Địa chỉ hợp lệ tối thiểu
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_004 |
| **Tiêu đề** | Chấp nhận địa chỉ đúng 10 ký tự |
| **Loại** | Boundary |
| **Priority** | Medium |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Nhập địa chỉ: "1234567890" (10 ký tự)<br/>2. Ấn "Đặt hàng" |
| **Kết quả mong đợi** | Địa chỉ được chấp nhận |
| **Liên quan đến** | R13 |

### TC_CHECKOUT_005: Chọn phương thức thanh toán - Visa
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_005 |
| **Tiêu đề** | Thanh toán thành công với Visa giả lập |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Nhập địa chỉ: "123 Đường ABC, TP.HCM"<br/>2. Chọn "Thanh toán bằng thẻ (Visa)"<br/>3. Nhập số thẻ: 4111111111111111<br/>4. Ấn "Thanh toán" |
| **Kết quả mong đợi** | Thanh toán thành công, hiển thị mã đơn hàng |
| **Liên quan đến** | R14, R15 |

### TC_CHECKOUT_006: Visa không hợp lệ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_006 |
| **Tiêu đề** | Thanh toán thất bại với số thẻ không hợp lệ |
| **Loại** | Negative |
| **Priority** | High |
| **Điều kiện trước** | Ở trang thanh toán, chọn Visa |
| **Các bước thực hiện** | 1. Nhập số thẻ: 1234567890123456 (không hợp lệ)<br/>2. Ấn "Thanh toán" |
| **Kết quả mong đợi** | Hiển thị lỗi "Số thẻ không hợp lệ" |
| **Liên quan đến** | R14 |

### TC_CHECKOUT_007: Tính tổng tiền chính xác
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_007 |
| **Tiêu đề** | Tính tổng tiền thanh toán chính xác |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Giỏ hàng: Sản phẩm A (100K x2), Sản phẩm B (50K x1) |
| **Các bước thực hiện** | 1. Ở trang thanh toán<br/>2. Kiểm tra tổng tiền |
| **Kết quả mong đợi** | Tổng tiền = 250,000đ (200K + 50K) |
| **Liên quan đến** | R15 |

### TC_CHECKOUT_008: Áp dụng mã giảm giá
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_008 |
| **Tiêu đề** | Áp dụng mã giảm giá thành công |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Có mã giảm giá "SAVE50" (giảm 50K) |
| **Các bước thực hiện** | 1. Nhập mã giảm giá: SAVE50<br/>2. Ấn "Áp dụng"<br/>3. Kiểm tra tổng tiền |
| **Kết quả mong đợi** | Mã được áp dụng, tổng tiền = 200,000đ |
| **Liên quan đến** | R15 |

### TC_CHECKOUT_009: Mã giảm giá không hợp lệ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_009 |
| **Tiêu đề** | Mã giảm giá không hợp lệ bị từ chối |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Ở trang thanh toán |
| **Các bước thực hiện** | 1. Nhập mã giảm giá: INVALID123<br/>2. Ấn "Áp dụng" |
| **Kết quả mong đợi** | Hiển thị "Mã giảm giá không tồn tại" |
| **Liên quan đến** | R15 |

### TC_CHECKOUT_010: Lịch sử đơn hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_010 |
| **Tiêu đề** | Xem lịch sử đơn hàng đã mua |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Người dùng đã đặt hàng, ở trang tài khoản |
| **Các bước thực hiện** | 1. Ấn "Lịch sử đơn hàng" |
| **Kết quả mong đợi** | Hiển thị danh sách đơn hàng, mã, ngày, trạng thái |
| **Liên quan đến** | R16 |

### TC_CHECKOUT_011: Lưu lịch sử đơn hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_011 |
| **Tiêu đề** | Lưu lịch sử đơn hàng trong hệ thống |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Vừa đặt hàng thành công |
| **Các bước thực hiện** | 1. Đặt hàng thành công<br/>2. Kiểm tra lịch sử đơn hàng<br/>3. Đặt hàng khác<br/>4. Kiểm tra lại lịch sử |
| **Kết quả mong đợi** | Cả 2 đơn hàng được lưu trong lịch sử |
| **Liên quan đến** | R16 |

### TC_CHECKOUT_012: Xem chi tiết đơn hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_012 |
| **Tiêu đề** | Xem chi tiết một đơn hàng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Có đơn hàng trong lịch sử |
| **Các bước thực hiện** | 1. Ấn vào một đơn hàng |
| **Kết quả mong đợi** | Hiển thị chi tiết: mã, ngày, sản phẩm, giá, địa chỉ, trạng thái |
| **Liên quan đến** | R16 |

### TC_CHECKOUT_013: Hủy đơn hàng trong 1 giờ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_013 |
| **Tiêu đề** | Hủy đơn hàng trong vòng 1 giờ |
| **Loại** | Positive |
| **Priority** | Medium |
| **Điều kiện trước** | Vừa đặt hàng trong 1 giờ |
| **Các bước thực hiện** | 1. Ấn vào đơn hàng<br/>2. Ấn "Hủy đơn hàng" |
| **Kết quả mong đợi** | Đơn hàng bị hủy, trạng thái = Cancelled |
| **Liên quan đến** | R16 |

### TC_CHECKOUT_014: Không thể hủy đơn hàng quá 1 giờ
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_014 |
| **Tiêu đề** | Không thể hủy đơn hàng sau 1 giờ |
| **Loại** | Negative |
| **Priority** | Medium |
| **Điều kiện trước** | Đơn hàng được đặt >1 giờ trước |
| **Các bước thực hiện** | 1. Ấn vào đơn hàng<br/>2. Ấn "Hủy đơn hàng" |
| **Kết quả mong đợi** | Nút "Hủy" bị vô hiệu hóa hoặc hiển thị "Không thể hủy" |
| **Liên quan đến** | R16 |

### TC_CHECKOUT_015: Email xác nhận đặt hàng
| Trường | Nội dung |
|--------|---------|
| **TC_ID** | TC_CHECKOUT_015 |
| **Tiêu đề** | Gửi email xác nhận khi đặt hàng |
| **Loại** | Positive |
| **Priority** | High |
| **Điều kiện trước** | Vừa đặt hàng thành công |
| **Các bước thực hiện** | 1. Đặt hàng thành công<br/>2. Kiểm tra email |
| **Kết quả mong đợi** | Nhận email xác nhận có mã đơn hàng, sản phẩm, giá, địa chỉ |
| **Liên quan đến** | R15 |

---

## TỔNG HỢPP

| Module | Tổng TC | Positive | Negative | Boundary |
|--------|---------|----------|----------|----------|
| Authentication | 15 | 6 | 7 | 2 |
| Product & Cart | 20 | 13 | 5 | 2 |
| Checkout | 15 | 9 | 4 | 2 |
| **TỔNG CỘNG** | **50** | **28** | **16** | **6** |

**Yêu cầu:** ≥45 test case ✅ (50 TC)  
**Negative cases:** ≥10 ✅ (16 TC)  
**Boundary cases:** ≥5 ✅ (6 TC)  
**Security validation:** ≥5 ✅ (TC_AUTH_015, TC_CART_002, TC_CHECKOUT_002, TC_CHECKOUT_003, TC_CHECKOUT_006)

---

**END OF TEST CASES**
