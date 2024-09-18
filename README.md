# Hệ thống quản lý dự án
Một hệ thống quản lý dự án được tạo bằng:
- Node.js và Express cho phần phụ trợ.
- Máy chủ MS SQL cho cơ sở dữ liệu.
- React.js cho phần giao diện.
- Redux để quản lý trạng thái ở phần giao diện.

## Mô-đun
### 1. Người dùng
- Bcrypt để băm mật khẩu trước khi lưu trữ vào cơ sở dữ liệu và giải mã khi đăng nhập.
- Mã thông báo web Json (JWT) để ủy quyền, tức là tạo mã thông báo khi người dùng đăng nhập để họ có thể thực hiện các chức năng riêng tư như cập nhật hồ sơ của mình
và cũng để xem các tuyến riêng tư.
- Người dùng được giao các dự án cũng chứa các nhiệm vụ.
### 2. Dự án
- Người dùng có thể làm việc trên một Dự án duy nhất
- Một dự án có nhiều tác vụ

### 3. Nhiệm vụ
- Một tác vụ có thể thuộc về một dự án duy nhất
- Người dùng có thể được chỉ định nhiều dự án

### Cơ sở dữ liệu

Tạo cơ sở dữ liệu máy chủ MS SQL và đặt tên tùy ý và thêm ba bảng
- Người dùng
- Dự án
- Nhiệm vụ

### Biến Env

Tạo tệp .env trong thư mục gốc và thêm nội dung sau
```
DB_HOST= localhost
DB_USER= tên người dùng máy chủ ms sql
DB_NAME= tên cơ sở dữ liệu của bạn
DB_PASSWORD= mật khẩu máy chủ sql của bạn
SECRET_KEY= khóa bí mật của bạn

```

### Cài đặt các phụ thuộc (root, client & server)

```
# cài đặt đồng thời trong thư mục gốc
npm install

cd server
npm install

cd client
npm install
```

### Chạy

```
# Chạy máy khách (:3000) & máy chủ (:8001)
npm chạy dev