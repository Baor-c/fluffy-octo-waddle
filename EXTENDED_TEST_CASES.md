# Extended Test Cases - BookShoppingCartMvc

## Bảng Test Cases Mở Rộng (70 Test Cases)

| ID | Test Case Description | Test Case Procedure | Expected Output | Test Date | Result | Note |
|----|----------------------|-------------------|----------------|-----------|--------|------|
| ETC001 | Đăng ký tài khoản với email hợp lệ | 1. Truy cập /Identity/Account/Register<br>2. Nhập email: test@example.com<br>3. Nhập password: Test@123<br>4. Xác nhận password<br>5. Click Register | Tài khoản được tạo, chuyển đến trang xác nhận | 2025-01-15 | Pass | |
| ETC002 | Đăng ký với email không hợp lệ | 1. Truy cập trang đăng ký<br>2. Nhập email: invalid-email<br>3. Nhập password hợp lệ<br>4. Click Register | Hiển thị lỗi "Invalid email format" | 2025-01-15 | Pass | |
| ETC003 | Đăng ký với email trống | 1. Truy cập trang đăng ký<br>2. Để trống email<br>3. Nhập password<br>4. Click Register | Hiển thị lỗi "Email is required" | 2025-01-15 | Pass | |
| ETC004 | Đăng ký với password trống | 1. Truy cập trang đăng ký<br>2. Nhập email hợp lệ<br>3. Để trống password<br>4. Click Register | Hiển thị lỗi "Password is required" | 2025-01-15 | Pass | |
| ETC005 | Đăng ký với password ngắn hơn 6 ký tự | 1. Nhập email hợp lệ<br>2. Nhập password: 123<br>3. Click Register | Hiển thị lỗi "Password must be at least 6 characters" | 2025-01-15 | Pass | |
| ETC006 | Đăng ký với confirm password không khớp | 1. Nhập email hợp lệ<br>2. Nhập password: Test@123<br>3. Confirm password: Test@456<br>4. Click Register | Hiển thị lỗi "Passwords do not match" | 2025-01-15 | Pass | |
| ETC007 | Đăng ký với email đã tồn tại | 1. Đăng ký email: admin@gmail.com<br>2. Nhập password hợp lệ<br>3. Click Register | Hiển thị lỗi "Email already exists" | 2025-01-15 | Pass | |
| ETC008 | Đăng nhập với thông tin admin | 1. Truy cập /Identity/Account/Login<br>2. Email: admin@gmail.com<br>3. Password: Admin@123<br>4. Click Login | Đăng nhập thành công, hiển thị menu admin | 2025-01-15 | Pass | |
| ETC009 | Đăng nhập với thông tin user thường | 1. Đăng nhập với user account<br>2. Kiểm tra menu | Đăng nhập thành công, không có menu admin | 2025-01-15 | Pass | |
| ETC010 | Đăng nhập với email sai | 1. Nhập email: wrong@email.com<br>2. Nhập password bất kỳ<br>3. Click Login | Hiển thị "Invalid login attempt" | 2025-01-15 | Pass | |
| ETC011 | Đăng nhập với password sai | 1. Nhập email đúng<br>2. Nhập password sai<br>3. Click Login | Hiển thị "Invalid login attempt" | 2025-01-15 | Pass | |
| ETC012 | Đăng nhập với Remember Me | 1. Nhập thông tin đúng<br>2. Check "Remember me"<br>3. Click Login<br>4. Đóng browser, mở lại | Vẫn đăng nhập, không cần nhập lại | 2025-01-15 | Pass | |
| ETC013 | Đăng xuất khỏi hệ thống | 1. Đăng nhập thành công<br>2. Click Logout | Đăng xuất, chuyển về trang chủ | 2025-01-15 | Pass | |
| ETC014 | Quên mật khẩu với email hợp lệ | 1. Click "Forgot password"<br>2. Nhập email đã đăng ký<br>3. Click Reset | Gửi email reset password | 2025-01-15 | Pending | Cần cấu hình email |
| ETC015 | Quên mật khẩu với email không tồn tại | 1. Click "Forgot password"<br>2. Nhập email chưa đăng ký<br>3. Click Reset | Hiển thị thông báo đã gửi email (bảo mật) | 2025-01-15 | Pending | |
| ETC016 | Xem trang chủ không đăng nhập | 1. Truy cập trang chủ<br>2. Kiểm tra hiển thị | Hiển thị danh sách sách, menu Login/Register | 2025-01-15 | Pass | |
| ETC017 | Xem trang chủ khi đã đăng nhập | 1. Đăng nhập<br>2. Truy cập trang chủ | Hiển thị sách, menu user, icon giỏ hàng | 2025-01-15 | Pass | |
| ETC018 | Hiển thị sách có hình ảnh | 1. Truy cập trang chủ<br>2. Kiểm tra sách có image | Hiển thị hình ảnh sách chính xác | 2025-01-15 | Pass | |
| ETC019 | Hiển thị sách không có hình ảnh | 1. Kiểm tra sách không có image<br>2. Xem hiển thị | Hiển thị hình ảnh mặc định NoImage.png | 2025-01-15 | Pass | |
| ETC020 | Tìm kiếm sách theo tên chính xác | 1. Nhập tên sách: "Clean Code"<br>2. Click Search | Hiển thị sách "Clean Code" | 2025-01-15 | Pass | |
| ETC021 | Tìm kiếm sách theo tên một phần | 1. Nhập: "Clean"<br>2. Click Search | Hiển thị tất cả sách có chứa "Clean" | 2025-01-15 | Pass | |
| ETC022 | Tìm kiếm với từ khóa không tồn tại | 1. Nhập: "xyz123"<br>2. Click Search | Không hiển thị sách nào | 2025-01-15 | Pass | |
| ETC023 | Tìm kiếm với ký tự đặc biệt | 1. Nhập: "@#$%"<br>2. Click Search | Không hiển thị sách nào, không lỗi | 2025-01-15 | Pass | |
| ETC024 | Lọc sách theo thể loại Romance | 1. Chọn Genre: Romance<br>2. Click Search | Hiển thị chỉ sách Romance | 2025-01-15 | Pass | |
| ETC025 | Lọc sách theo thể loại Programming | 1. Chọn Genre: Programming<br>2. Click Search | Hiển thị chỉ sách Programming | 2025-01-15 | Pass | |
| ETC026 | Kết hợp tìm kiếm và lọc thể loại | 1. Nhập tên: "Code"<br>2. Chọn Genre: Programming<br>3. Click Search | Hiển thị sách Programming có chứa "Code" | 2025-01-15 | Pass | |
| ETC027 | Reset bộ lọc tìm kiếm | 1. Áp dụng filter<br>2. Click Reset | Hiển thị tất cả sách, clear filter | 2025-01-15 | Pass | |
| ETC028 | Thêm sách vào giỏ khi chưa đăng nhập | 1. Chưa đăng nhập<br>2. Click "Add to cart" | Chuyển hướng đến trang đăng nhập | 2025-01-15 | Pass | |
| ETC029 | Thêm sách có sẵn vào giỏ hàng | 1. Đăng nhập<br>2. Click "Add to cart" sách có stock > 0 | Sách được thêm, cập nhật số giỏ hàng | 2025-01-15 | Pass | |
| ETC030 | Thêm sách hết hàng vào giỏ | 1. Tìm sách có stock = 0<br>2. Kiểm tra nút Add to cart | Hiển thị "Out of stock", không có nút | 2025-01-15 | Pass | |
| ETC031 | Thêm cùng sách nhiều lần | 1. Thêm sách A vào giỏ<br>2. Thêm sách A lần nữa | Quantity tăng lên, không tạo item mới | 2025-01-15 | Pass | |
| ETC032 | Kiểm tra số lượng giỏ hàng trên header | 1. Thêm 3 sách khác nhau<br>2. Kiểm tra badge số | Hiển thị số 3 trên icon giỏ hàng | 2025-01-15 | Pass | |
| ETC033 | Xem giỏ hàng trống | 1. Đăng nhập<br>2. Chưa thêm sách nào<br>3. Click icon giỏ hàng | Hiển thị "Cart is empty" | 2025-01-15 | Pass | |
| ETC034 | Xem giỏ hàng có sách | 1. Thêm sách vào giỏ<br>2. Click icon giỏ hàng | Hiển thị danh sách sách, tổng tiền | 2025-01-15 | Pass | |
| ETC035 | Tăng số lượng sách trong giỏ | 1. Vào giỏ hàng<br>2. Click nút "+" | Quantity tăng, total price cập nhật | 2025-01-15 | Pass | |
| ETC036 | Tăng số lượng vượt quá stock | 1. Sách có stock = 5<br>2. Tăng quantity lên 6 | Nút "+" bị ẩn khi đạt max stock | 2025-01-15 | Pass | |
| ETC037 | Giảm số lượng sách trong giỏ | 1. Sách có quantity > 1<br>2. Click nút "-" | Quantity giảm, total price cập nhật | 2025-01-15 | Pass | |
| ETC038 | Giảm số lượng xuống 0 | 1. Sách có quantity = 1<br>2. Click nút "-" | Sách bị xóa khỏi giỏ hàng | 2025-01-15 | Pass | |
| ETC039 | Tính tổng tiền giỏ hàng chính xác | 1. Thêm nhiều sách với số lượng khác nhau<br>2. Kiểm tra tổng tiền | Tổng tiền = Σ(price × quantity) | 2025-01-15 | Pass | |
| ETC040 | Checkout với giỏ hàng có sách | 1. Có sách trong giỏ<br>2. Click Checkout | Chuyển đến form checkout | 2025-01-15 | Pass | |
| ETC041 | Checkout với thông tin đầy đủ | 1. Điền Name: "Nguyen Van A"<br>2. Email: "test@test.com"<br>3. Mobile: "0123456789"<br>4. Address: "123 ABC Street"<br>5. Payment: COD<br>6. Click Next | Đặt hàng thành công | 2025-01-15 | Pass | |
| ETC042 | Checkout với tên trống | 1. Để trống Name<br>2. Điền các field khác<br>3. Click Next | Hiển thị lỗi "Name is required" | 2025-01-15 | Pass | |
| ETC043 | Checkout với email không hợp lệ | 1. Email: "invalid-email"<br>2. Điền các field khác<br>3. Click Next | Hiển thị lỗi "Invalid email format" | 2025-01-15 | Pass | |
| ETC044 | Checkout với số điện thoại trống | 1. Để trống Mobile Number<br>2. Điền các field khác<br>3. Click Next | Hiển thị lỗi "Mobile number is required" | 2025-01-15 | Pass | |
| ETC045 | Checkout với địa chỉ trống | 1. Để trống Address<br>2. Điền các field khác<br>3. Click Next | Hiển thị lỗi "Address is required" | 2025-01-15 | Pass | |
| ETC046 | Checkout không chọn phương thức thanh toán | 1. Điền đầy đủ thông tin<br>2. Không chọn Payment Method<br>3. Click Next | Hiển thị lỗi "Payment method is required" | 2025-01-15 | Pass | |
| ETC047 | Checkout với giỏ hàng trống | 1. Xóa hết sách trong giỏ<br>2. Truy cập trực tiếp /Cart/Checkout | Hiển thị lỗi hoặc chuyển về trang chủ | 2025-01-15 | Fail | Cần thêm validation |
| ETC048 | Kiểm tra stock sau khi checkout | 1. Sách có stock = 10<br>2. Mua 3 cuốn<br>3. Kiểm tra stock | Stock giảm xuống 7 | 2025-01-15 | Pass | |
| ETC049 | Checkout khi stock không đủ | 1. Sách có stock = 2<br>2. Giỏ hàng có 5 cuốn<br>3. Checkout | Hiển thị lỗi "Only 2 items available" | 2025-01-15 | Pass | |
| ETC050 | Xem lịch sử đơn hàng user | 1. Đăng nhập user<br>2. Vào My Orders | Hiển thị chỉ đơn hàng của user đó | 2025-01-15 | Pass | |
| ETC051 | Xem chi tiết đơn hàng | 1. Vào My Orders<br>2. Kiểm tra thông tin đơn hàng | Hiển thị sách, số lượng, giá, tổng tiền | 2025-01-15 | Pass | |
| ETC052 | Admin đăng nhập thành công | 1. Email: admin@gmail.com<br>2. Password: Admin@123<br>3. Click Login | Đăng nhập, hiển thị menu admin | 2025-01-15 | Pass | |
| ETC053 | User thường truy cập trang admin | 1. Đăng nhập user<br>2. Truy cập /AdminOperations/Dashboard | Hiển thị Access Denied | 2025-01-15 | Pass | |
| ETC054 | Admin xem tất cả đơn hàng | 1. Đăng nhập admin<br>2. Vào All Orders | Hiển thị tất cả đơn hàng trong hệ thống | 2025-01-15 | Pass | |
| ETC055 | Admin xem chi tiết đơn hàng | 1. Vào All Orders<br>2. Click Order Detail | Hiển thị modal với chi tiết đơn hàng | 2025-01-15 | Pass | |
| ETC056 | Admin thay đổi trạng thái đơn hàng | 1. Click "Change Order Status"<br>2. Chọn "Shipped"<br>3. Click Update | Trạng thái đổi thành "Shipped" | 2025-01-15 | Pass | |
| ETC057 | Admin toggle payment status | 1. Click "Toggle Payment Status"<br>2. Kiểm tra thay đổi | Trạng thái đổi từ "Not Paid" thành "Paid" | 2025-01-15 | Pass | |
| ETC058 | Admin xem danh sách thể loại | 1. Vào Genre management<br>2. Kiểm tra danh sách | Hiển thị tất cả thể loại | 2025-01-15 | Pass | |
| ETC059 | Admin thêm thể loại mới | 1. Click Add More<br>2. Nhập "Science Fiction"<br>3. Click Add | Thể loại mới được thêm | 2025-01-15 | Pass | |
| ETC060 | Admin thêm thể loại với tên trống | 1. Click Add More<br>2. Để trống tên<br>3. Click Add | Hiển thị lỗi validation | 2025-01-15 | Pass | |
| ETC061 | Admin sửa thể loại | 1. Click Edit<br>2. Đổi tên thành "Mystery"<br>3. Click Update | Thể loại được cập nhật | 2025-01-15 | Pass | |
| ETC062 | Admin xóa thể loại không có sách | 1. Chọn thể loại trống<br>2. Click Delete<br>3. Confirm | Thể loại bị xóa | 2025-01-15 | Pass | |
| ETC063 | Admin xóa thể loại có sách | 1. Chọn thể loại có sách<br>2. Click Delete | Hiển thị lỗi hoặc xóa cascade | 2025-01-15 | Pending | Cần kiểm tra FK constraint |
| ETC064 | Admin xem danh sách sách | 1. Vào Books management<br>2. Kiểm tra danh sách | Hiển thị tất cả sách với thông tin đầy đủ | 2025-01-15 | Pass | |
| ETC065 | Admin thêm sách với thông tin đầy đủ | 1. Click Add More<br>2. Điền đầy đủ thông tin<br>3. Upload ảnh hợp lệ<br>4. Click Add | Sách mới được thêm thành công | 2025-01-15 | Pass | |
| ETC066 | Admin thêm sách thiếu thông tin bắt buộc | 1. Để trống Book Name<br>2. Điền các field khác<br>3. Click Add | Hiển thị lỗi validation | 2025-01-15 | Pass | |
| ETC067 | Admin upload ảnh quá lớn | 1. Chọn file > 1MB<br>2. Click Add | Hiển thị "Image file cannot exceed 1 MB" | 2025-01-15 | Pass | |
| ETC068 | Admin upload file không phải ảnh | 1. Chọn file .txt<br>2. Click Add | Hiển thị lỗi định dạng file | 2025-01-15 | Pass | |
| ETC069 | Admin sửa thông tin sách | 1. Click Edit<br>2. Thay đổi giá<br>3. Click Update | Thông tin sách được cập nhật | 2025-01-15 | Pass | |
| ETC070 | Admin thay đổi ảnh sách | 1. Click Edit<br>2. Upload ảnh mới<br>3. Click Update | Ảnh cũ bị xóa, ảnh mới được lưu | 2025-01-15 | Pass | |

## Tổng kết Extended Test Results

- **Total Test Cases**: 70
- **Passed**: 65 (92.9%)
- **Failed**: 2 (2.9%)
- **Pending**: 3 (4.2%)

## Phân loại Test Cases

### Authentication & Authorization (14 cases)
- Đăng ký, đăng nhập, đăng xuất
- Validation form
- Phân quyền admin/user

### Book Management - User Side (13 cases)  
- Xem danh sách sách
- Tìm kiếm và lọc
- Hiển thị thông tin sách

### Shopping Cart (12 cases)
- Thêm/xóa sách
- Quản lý số lượng
- Tính toán giá

### Checkout & Orders (10 cases)
- Quy trình đặt hàng
- Validation thông tin
- Quản lý stock

### Admin - Order Management (5 cases)
- Xem và quản lý đơn hàng
- Thay đổi trạng thái

### Admin - Genre Management (6 cases)
- CRUD thể loại sách

### Admin - Book Management (10 cases)
- CRUD sách và upload ảnh

## Các vấn đề cần khắc phục

### Failed Cases:
1. **ETC047**: Checkout với giỏ hàng trống - Cần validation
2. **ETC063**: Xóa thể loại có sách - Cần kiểm tra FK constraint

### Pending Cases:
1. **ETC014**: Reset password - Cần cấu hình email
2. **ETC015**: Reset password với email không tồn tại
3. **ETC063**: Ràng buộc foreign key

## Khuyến nghị cải thiện

1. **Bảo mật**: Thêm CSRF protection, rate limiting
2. **UX**: Thêm loading indicators, confirmation dialogs
3. **Performance**: Implement pagination, caching
4. **Validation**: Tăng cường client-side validation
5. **Error Handling**: Cải thiện thông báo lỗi
6. **Testing**: Thêm unit tests, integration tests
7. **Monitoring**: Thêm logging và monitoring

## Test Environment
- **Framework**: ASP.NET Core 9.0
- **Database**: SQL Server
- **Browser**: Chrome 120+, Firefox 115+
- **Test Data**: 30 sách, 6 thể loại
- **Admin Account**: admin@gmail.com / Admin@123