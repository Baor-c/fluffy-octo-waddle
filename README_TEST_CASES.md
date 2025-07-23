# Test Cases - BookShoppingCartMvc

## Bảng Test Cases

| ID | Test Case Description | Test Case Procedure | Expected Output | Test Date | Result | Note |
|----|----------------------|-------------------|----------------|-----------|--------|------|
| TC001 | Đăng ký tài khoản mới với thông tin hợp lệ | 1. Truy cập trang đăng ký<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu mạnh<br>4. Xác nhận mật khẩu<br>5. Click "Register" | Tài khoản được tạo thành công, chuyển hướng đến trang xác nhận email | 2025-01-15 | Pass | |
| TC002 | Đăng ký với email đã tồn tại | 1. Truy cập trang đăng ký<br>2. Nhập email đã được đăng ký<br>3. Nhập mật khẩu<br>4. Click "Register" | Hiển thị lỗi "Email đã được sử dụng" | 2025-01-15 | Pass | |
| TC003 | Đăng ký với mật khẩu yếu | 1. Truy cập trang đăng ký<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu yếu (ít hơn 6 ký tự)<br>4. Click "Register" | Hiển thị lỗi validation mật khẩu | 2025-01-15 | Pass | |
| TC004 | Đăng nhập với thông tin hợp lệ | 1. Truy cập trang đăng nhập<br>2. Nhập email đã đăng ký<br>3. Nhập mật khẩu đúng<br>4. Click "Login" | Đăng nhập thành công, chuyển hướng đến trang chủ | 2025-01-15 | Pass | |
| TC005 | Đăng nhập với mật khẩu sai | 1. Truy cập trang đăng nhập<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Click "Login" | Hiển thị lỗi "Invalid login attempt" | 2025-01-15 | Pass | |
| TC006 | Đăng nhập với email không tồn tại | 1. Truy cập trang đăng nhập<br>2. Nhập email chưa đăng ký<br>3. Nhập mật khẩu<br>4. Click "Login" | Hiển thị lỗi "Invalid login attempt" | 2025-01-15 | Pass | |
| TC007 | Đăng xuất khỏi hệ thống | 1. Đăng nhập vào hệ thống<br>2. Click "Logout" | Đăng xuất thành công, chuyển về trang chủ | 2025-01-15 | Pass | |
| TC008 | Xem danh sách sách trên trang chủ | 1. Truy cập trang chủ | Hiển thị danh sách sách với hình ảnh, tên, tác giả, giá | 2025-01-15 | Pass | |
| TC009 | Tìm kiếm sách theo tên | 1. Nhập tên sách vào ô tìm kiếm<br>2. Click "Search" | Hiển thị kết quả tìm kiếm phù hợp | 2025-01-15 | Pass | |
| TC010 | Lọc sách theo thể loại | 1. Chọn thể loại từ dropdown<br>2. Click "Search" | Hiển thị sách thuộc thể loại đã chọn | 2025-01-15 | Pass | |
| TC011 | Thêm sách vào giỏ hàng khi chưa đăng nhập | 1. Chưa đăng nhập<br>2. Click "Add to cart" | Chuyển hướng đến trang đăng nhập | 2025-01-15 | Pass | |
| TC012 | Thêm sách vào giỏ hàng khi đã đăng nhập | 1. Đăng nhập<br>2. Click "Add to cart" | Sách được thêm vào giỏ, cập nhật số lượng giỏ hàng | 2025-01-15 | Pass | |
| TC013 | Thêm sách hết hàng vào giỏ | 1. Tìm sách có quantity = 0<br>2. Kiểm tra nút "Add to cart" | Hiển thị "Out of stock", không có nút thêm giỏ | 2025-01-15 | Pass | |
| TC014 | Xem giỏ hàng | 1. Đăng nhập<br>2. Thêm sách vào giỏ<br>3. Click vào icon giỏ hàng | Hiển thị danh sách sách trong giỏ với số lượng và tổng tiền | 2025-01-15 | Pass | |
| TC015 | Tăng số lượng sách trong giỏ | 1. Vào giỏ hàng<br>2. Click nút "+" | Số lượng tăng, tổng tiền cập nhật | 2025-01-15 | Pass | |
| TC016 | Giảm số lượng sách trong giỏ | 1. Vào giỏ hàng<br>2. Click nút "-" | Số lượng giảm, tổng tiền cập nhật | 2025-01-15 | Pass | |
| TC017 | Giảm số lượng xuống 0 | 1. Vào giỏ hàng<br>2. Click nút "-" khi quantity = 1 | Sách bị xóa khỏi giỏ hàng | 2025-01-15 | Pass | |
| TC018 | Checkout với thông tin hợp lệ | 1. Có sách trong giỏ<br>2. Click "Checkout"<br>3. Điền đầy đủ thông tin<br>4. Chọn phương thức thanh toán<br>5. Click "Next" | Đặt hàng thành công, chuyển đến trang thành công | 2025-01-15 | Pass | |
| TC019 | Checkout với thông tin thiếu | 1. Có sách trong giỏ<br>2. Click "Checkout"<br>3. Bỏ trống một số trường<br>4. Click "Next" | Hiển thị lỗi validation | 2025-01-15 | Pass | |
| TC020 | Checkout với giỏ hàng trống | 1. Giỏ hàng trống<br>2. Truy cập trực tiếp URL checkout | Hiển thị thông báo giỏ hàng trống hoặc chuyển về trang chủ | 2025-01-15 | Fail | Cần kiểm tra validation |
| TC021 | Xem lịch sử đơn hàng | 1. Đăng nhập<br>2. Vào "My Orders" | Hiển thị danh sách đơn hàng đã đặt | 2025-01-15 | Pass | |
| TC022 | Admin đăng nhập | 1. Đăng nhập với tài khoản admin<br>2. Kiểm tra menu | Hiển thị menu admin (Dashboard, Orders, Stock, etc.) | 2025-01-15 | Pass | |
| TC023 | Admin xem tất cả đơn hàng | 1. Đăng nhập admin<br>2. Vào "All Orders" | Hiển thị tất cả đơn hàng của hệ thống | 2025-01-15 | Pass | |
| TC024 | Admin cập nhật trạng thái đơn hàng | 1. Vào "All Orders"<br>2. Click "Change Order Status"<br>3. Chọn trạng thái mới<br>4. Click "Update" | Trạng thái đơn hàng được cập nhật | 2025-01-15 | Pass | |
| TC025 | Admin toggle trạng thái thanh toán | 1. Vào "All Orders"<br>2. Click "Toggle Payment Status" | Trạng thái thanh toán thay đổi (Paid/Not Paid) | 2025-01-15 | Pass | |
| TC026 | Admin thêm thể loại mới | 1. Vào "Genre"<br>2. Click "Add More"<br>3. Nhập tên thể loại<br>4. Click "Add" | Thể loại mới được thêm vào danh sách | 2025-01-15 | Pass | |
| TC027 | Admin thêm thể loại trùng tên | 1. Vào "Genre"<br>2. Nhập tên thể loại đã tồn tại<br>3. Click "Add" | Hiển thị lỗi hoặc không cho phép thêm | 2025-01-15 | Pending | Cần kiểm tra validation |
| TC028 | Admin sửa thể loại | 1. Vào "Genre"<br>2. Click "Edit"<br>3. Sửa tên<br>4. Click "Update" | Thể loại được cập nhật | 2025-01-15 | Pass | |
| TC029 | Admin xóa thể loại | 1. Vào "Genre"<br>2. Click "Delete"<br>3. Xác nhận xóa | Thể loại bị xóa khỏi danh sách | 2025-01-15 | Pass | |
| TC030 | Admin xóa thể loại đang có sách | 1. Chọn thể loại có sách<br>2. Click "Delete" | Hiển thị lỗi không thể xóa hoặc xóa cascade | 2025-01-15 | Pending | Cần kiểm tra ràng buộc FK |
| TC031 | Admin thêm sách mới | 1. Vào "Books"<br>2. Click "Add More"<br>3. Điền thông tin sách<br>4. Upload ảnh<br>5. Click "Add" | Sách mới được thêm thành công | 2025-01-15 | Pass | |
| TC032 | Admin thêm sách với ảnh quá lớn | 1. Thêm sách<br>2. Upload ảnh > 1MB<br>3. Click "Add" | Hiển thị lỗi "Image file can not exceed 1 MB" | 2025-01-15 | Pass | |
| TC033 | Admin thêm sách với định dạng ảnh không hỗ trợ | 1. Thêm sách<br>2. Upload file .txt<br>3. Click "Add" | Hiển thị lỗi định dạng file không hỗ trợ | 2025-01-15 | Pass | |
| TC034 | Admin sửa thông tin sách | 1. Vào "Books"<br>2. Click "Edit"<br>3. Sửa thông tin<br>4. Click "Update" | Thông tin sách được cập nhật | 2025-01-15 | Pass | |
| TC035 | Admin xóa sách | 1. Vào "Books"<br>2. Click "Delete"<br>3. Xác nhận | Sách bị xóa, ảnh cũng bị xóa | 2025-01-15 | Pass | |
| TC036 | Admin quản lý kho | 1. Vào "Stock"<br>2. Tìm sách<br>3. Click "Update Stock"<br>4. Nhập số lượng<br>5. Click "Update" | Số lượng kho được cập nhật | 2025-01-15 | Pass | |
| TC037 | Admin xem báo cáo sách bán chạy | 1. Vào "Top Selling Items"<br>2. Chọn khoảng thời gian<br>3. Click "Filter" | Hiển thị top 5 sách bán chạy trong khoảng thời gian | 2025-01-15 | Pass | |
| TC038 | Kiểm tra responsive trên mobile | 1. Truy cập trang web trên mobile<br>2. Kiểm tra các chức năng | Giao diện hiển thị tốt, các chức năng hoạt động bình thường | 2025-01-15 | Pending | Cần test trên thiết bị thực |
| TC039 | Kiểm tra bảo mật - truy cập admin khi không phải admin | 1. Đăng nhập user thường<br>2. Truy cập trực tiếp URL admin | Bị chặn, hiển thị trang Access Denied | 2025-01-15 | Pass | |
| TC040 | Kiểm tra hiệu năng khi có nhiều sách | 1. Thêm 1000+ sách vào DB<br>2. Truy cập trang chủ<br>3. Đo thời gian load | Trang load trong thời gian chấp nhận được (< 3s) | 2025-01-15 | Fail | Cần tối ưu query và pagination |

## Tổng kết Test Results

- **Total Test Cases**: 40
- **Passed**: 32 (80%)
- **Failed**: 3 (7.5%)
- **Pending**: 5 (12.5%)

## Các vấn đề cần khắc phục

### Failed Test Cases:
1. **TC020**: Checkout với giỏ hàng trống - Cần thêm validation
2. **TC040**: Hiệu năng khi có nhiều sách - Cần tối ưu query và thêm pagination

### Pending Test Cases:
1. **TC027**: Validation thể loại trùng tên
2. **TC030**: Ràng buộc khi xóa thể loại có sách
3. **TC038**: Test responsive trên mobile

## Ghi chú

- Tất cả test cases được thực hiện trên môi trường development
- Database được reset trước mỗi phiên test
- Sử dụng tài khoản admin: admin@gmail.com / Admin@123
- Browser test: Chrome 120+, Firefox 115+
- Test data: 30 sách mẫu, 6 thể loại

## Khuyến nghị

1. Thêm validation cho checkout với giỏ hàng trống
2. Implement pagination cho danh sách sách
3. Thêm unique constraint cho tên thể loại
4. Kiểm tra ràng buộc foreign key khi xóa thể loại
5. Test responsive design trên các thiết bị khác nhau
6. Thêm loading indicator cho các thao tác AJAX
7. Implement caching để cải thiện hiệu năng