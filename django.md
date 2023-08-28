# Django Framework

## 1.Django là gì ?

Django là một framework phát triển ứng dụng web mạnh mẽ được viết bằng Python. Nó cung cấp một nền tảng hoàn chỉnh và cấu trúc để phát triển các ứng dụng web phức tạp và hiệu quả. Dưới đây là một số đặc điểm quan trọng của Django:

1. **Cấu trúc MVC (Model-View-Controller):** Django tuân thủ mô hình MVC, nhưng được gọi là mô hình MTV (Model-Template-View). Điều này giúp tách biệt dữ liệu (Model), giao diện người dùng (Template), và logic điều khiển (View).
2. **ORM (Object-Relational Mapping):** Django cung cấp một ORM mạnh mẽ cho phép bạn tương tác với cơ sở dữ liệu mà không cần viết SQL trực tiếp. Bạn có thể định nghĩa các mô hình dữ liệu trong Python và Django sẽ tự động tạo các truy vấn SQL tương ứng.
3. **Admin Interface:** Django đi kèm với một giao diện quản trị sẵn có mà bạn có thể sử dụng để quản lý dữ liệu trang web một cách dễ dàng. Bạn có thể tùy chỉnh và mở rộng giao diện quản trị theo nhu cầu của mình.
4. **Hệ thống xác thực và phân quyền:** Django có sẵn các công cụ để quản lý xác thực người dùng và phân quyền truy cập đến các phần của ứng dụng.
5. **Hệ thống URL Mapping:** Bạn có thể định nghĩa các URL cho các chức năng khác nhau của ứng dụng và Django sẽ định tuyến các yêu cầu đến các phần của mã nguồn tương ứng.
6. **Hệ thống Template:** Django hỗ trợ hệ thống template giúp bạn tạo ra giao diện người dùng một cách dễ dàng và hiệu quả.
7. **Xử lý Form:** Django cung cấp các công cụ cho việc tạo và xử lý các biểu mẫu web một cách dễ dàng.
8. **Bảo mật:** Django có các tính năng bảo mật tích hợp để bảo vệ ứng dụng khỏi các cuộc tấn công thông qua các phương thức như bảo vệ khỏi tấn công SQL Injection, Cross-Site Scripting (XSS), và Cross-Site Request Forgery (CSRF).

Django được thiết kế để giúp phát triển ứng dụng web nhanh chóng, bảo mật và dễ bảo trì. Nó được sử dụng rộng rãi trong cộng đồng phát triển web và đã được áp dụng thành công trong nhiều dự án lớn trên toàn thế giới.


## 2. Setup project

- install python3
- Cài đặt Django 

  ```python3

  pip -m install django
  ```


## 3. App trong django

Trong Django, một ứng dụng (app) là một thành phần độc lập của dự án web của bạn, chứa các tệp mã nguồn, mô hình dữ liệu, các tập tin tĩnh, và các thành phần khác liên quan đến một phần cụ thể của trang web của bạn. Ứng dụng giúp bạn tạo ra và quản lý các phần của dự án của mình theo cách có tổ chức và dễ quản lý.

```python3

python3 manage.py startapp <tenapp>
```

Dưới đây là một số điểm quan trọng về ứng dụng trong Django:

1. **Độc lập và tái sử dụng:** Mỗi ứng dụng Django là một thành phần độc lập, bạn có thể sử dụng chúng trong nhiều dự án khác nhau hoặc tái sử dụng chúng trong cùng một dự án.
2. **Mô hình dữ liệu:** Một ứng dụng thường đi kèm với mô hình dữ liệu (models) để định nghĩa cấu trúc và quan hệ giữa các bảng trong cơ sở dữ liệu. Điều này cho phép bạn tạo, đọc, cập nhật và xóa dữ liệu từ cơ sở dữ liệu một cách dễ dàng.
3. **Views:** Ứng dụng chứa các views, là các hàm hoặc lớp xử lý các yêu cầu HTTP từ người dùng. Views xử lý logic ứng dụng và render các templates để trả về cho người dùng.
4. **Templates:** Templates là các tệp HTML hoặc các tệp mẫu khác được sử dụng để hiển thị dữ liệu cho người dùng. Django cho phép bạn tạo các template để tổ chức giao diện người dùng.
5. **Các tập tin tĩnh:** Bạn có thể lưu trữ các tệp tĩnh như hình ảnh, CSS, JavaScript trong ứng dụng để phục vụ trực tiếp cho trình duyệt của người dùng.
6. **URL patterns:** Ứng dụng xác định các URL patterns để chỉ định cách xử lý các yêu cầu HTTP từ người dùng. URL patterns quyết định nên gọi views nào để xử lý yêu cầu.
7. **Thư mục ứng dụng:** Mỗi ứng dụng có một thư mục riêng, bên trong thư mục gốc của dự án Django. Thư mục này chứa các tệp mã nguồn, mô hình, templates, và các tệp tĩnh của ứng dụng.

Để tạo một ứng dụng mới trong Django, bạn có thể sử dụng lệnh `python manage.py startapp app_name`. Sau đó, bạn cần thêm tên ứng dụng vào danh sách `INSTALLED_APPS` trong tệp cấu hình của dự án Django (`settings.py`). Sau khi đã tạo và đăng ký ứng dụng, bạn có thể bắt đầu phát triển các thành phần của nó, chẳng hạn như mô hình dữ liệu, views, và templates.

## 4. URLS & VIEW trong Django

Trong Django, URLs và views là hai thành phần quan trọng trong việc xây dựng ứng dụng web. Chúng làm cho ứng dụng có thể xác định được cách xử lý yêu cầu từ trình duyệt của người dùng. Dưới đây là giải thích về URLs và views trong Django:

**URLs (Uniform Resource Locators):**

- URLs xác định cách các yêu cầu HTTP từ trình duyệt của người dùng được định tuyến và xử lý trong ứng dụng Django. Mỗi URL được ánh xạ vào một view cụ thể.
- URLs được định nghĩa trong tệp `urls.py` của ứng dụng Django. Đây là nơi bạn liệt kê các URL patterns (mẫu URL) và ánh xạ chúng vào views.
- URL patterns có thể chứa các biến động để truyền tham số đến views, ví dụ: `/articles/<int:article_id>/` có thể đối ứng với một bài viết với `article_id` là một số nguyên.

**Views:**

- Views là các hàm Python hoặc lớp Python được sử dụng để xử lý các yêu cầu HTTP từ URLs. Views xác định nội dung cần được trả về cho trình duyệt của người dùng.
- Views có thể trả về HTML, JSON hoặc bất kỳ định dạng dữ liệu nào khác. Chúng cũng có thể tương tác với cơ sở dữ liệu để truy xuất hoặc cập nhật thông tin.
- Views có thể là các hàm thông thường hoặc được đóng gói thành lớp view sử dụng các decorators như `@csrf_exempt`, `@login_required`, vv.

Ví dụ về cách ánh xạ URLs vào views trong Django:

Trong `urls.py` của ứng dụng, bạn có thể có một đoạn mã như sau:

```python3
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
    path('about/', views.about, name='about'),
    path('articles/<int:article_id>/', views.article_detail, name='article_detail'),
]
```

Ở đây:

- `path('', views.index, name='index')` ánh xạ URL gốc vào view `index` của ứng dụng và đặt tên cho nó là 'index'.
- `path('about/', views.about, name='about')` ánh xạ URL '/about/' vào view `about` và đặt tên cho nó là 'about'.
- `path('articles/<int:article_id>/', views.article_detail, name='article_detail')` ánh xạ URL '/articles/1/' vào view `article_detail`, với `article_id` là một số nguyên và đặt tên cho nó là 'article_detail'.

Sau khi xác định URLs, bạn cần viết các views tương ứng (trong tệp `views.py`) để xử lý các yêu cầu từ các URLs này.
