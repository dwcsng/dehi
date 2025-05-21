# Du ký Barber - Booking Web App

Ứng dụng web đặt lịch cắt tóc chuyên nghiệp cho tiệm Du ký Barber.

## Tính năng

- Đăng ký, đăng nhập, đăng xuất tài khoản
- Xem danh sách dịch vụ và thợ cắt tóc
- Đặt lịch cắt tóc: chọn thợ, dịch vụ, ngày giờ, ghi chú
- Xem, lọc, chỉnh sửa, hủy lịch hẹn của bạn
- Tìm kiếm dịch vụ trên trang chủ
- Giao diện hiện đại, responsive
- Thông báo email khi lịch hẹn sắp đến hạn (cấu hình SMTP)

## Cài đặt

### 1. Clone project

```sh
git clone https://github.com/yourusername/barberproject.git
cd barberproject
```

### 2. Cài đặt môi trường Python

```sh
python -m venv venv
source venv/bin/activate  # hoặc venv\Scripts\activate trên Windows
pip install -r requirements.txt
```

### 3. Cấu hình database & media/static

- Mặc định dùng SQLite, không cần cấu hình thêm.
- Ảnh upload sẽ lưu ở thư mục `media/`.

### 4. Chạy migrate và tạo superuser

```sh
python manage.py migrate
python manage.py createsuperuser
```

### 5. Chạy server

```sh
python manage.py runserver
```

Truy cập [http://127.0.0.1:8000/](http://127.0.0.1:8000/) để sử dụng ứng dụng.

## Cấu hình gửi email (tùy chọn)

Sửa file `barberproject/settings.py`:

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your_email@gmail.com'
EMAIL_HOST_PASSWORD = 'your_app_password'
DEFAULT_FROM_EMAIL = EMAIL_HOST_USER
```

## Thư mục chính

- `main/` - Ứng dụng chính (models, views, templates, forms)
- `barberproject/` - Cấu hình project Django
- `static/` - File tĩnh (CSS, JS, ảnh)
- `media/` - Ảnh upload (dịch vụ, thợ)

## Đóng góp

Mọi đóng góp, báo lỗi hoặc ý tưởng mới đều được hoan nghênh!

---

**© 2024 Du ký Barber**
