

# Django REST framework

Django REST framework (DRF) là một bộ công cụ mạnh mẽ và phổ biến được sử dụng để phát triển các ứng dụng web dựa trên Django với giao diện lập trình ứng dụng (API) RESTful. Dưới đây là một số khái niệm và lý thuyết cơ bản về API và cách Django REST framework hoạt động:

**0. HTTP (Hypertext Transfer Protocol):**

- HTTP là giao thức được sử dụng trên internet để triyeenf tải dữ liệu giữa máy tính và máy chủ web. Nó dựa trên mô hình request/response và sử dụng các phương thức GET - POST - PUT - DELETE và nhiều phương thức khác.

**1. API (Application Programming Interface):**

- Một API là một tập hợp các quy tắc và giao thức mà các ứng dụng sử dụng để giao tiếp với nhau. Nó cho phép các ứng dụng khác nhau truy cập và tương tác với các tính năng và dữ liệu của ứng dụng khác.

**2. REST (Representational State Transfer):**

- REST là một kiến trúc phát triển ứng dụng web dựa trên HTTP. Nó sử dụng các phương thức HTTP như GET, POST, PUT và DELETE để quản lý tài nguyên (resource) và tương tác với chúng thông qua các URL.

**3. Django REST framework (DRF):**

- DRF là một bộ công cụ mở rộng cho Django, giúp bạn dễ dàng xây dựng các ứng dụng API RESTful một cách nhanh chóng và mạnh mẽ. DRF cung cấp các lớp và chức năng để xử lý các yêu cầu HTTP, xác thực người dùng, quản lý tài nguyên và biến đổi dữ liệu thành định dạng JSON hoặc XML.

**4. Serializer:**

- Serializer là một thành phần quan trọng trong DRF, giúp bạn chuyển đổi các đối tượng Django (như các mô hình cơ sở dữ liệu) thành định dạng dữ liệu có thể gửi qua API (ví dụ: JSON hoặc XML) và ngược lại. Serializer cho phép bạn kiểm soát cách dữ liệu được biểu diễn và phân tích.

**5. Viewsets và Routers:**

- DRF cung cấp viewsets và routers để quản lý các thao tác CRUD (Create, Read, Update, Delete) trên tài nguyên. Viewsets định nghĩa các tác vụ API, trong khi routers quản lý các URL cho các tài nguyên.

**6. Authentication và Permissions:**

- DRF có hệ thống xác thực mạnh mẽ và quyền truy cập, cho phép bạn xác định người dùng nào có quyền thực hiện các hành động cụ thể trên tài nguyên.

**7. Throttling:**

- DRF cung cấp cơ chế hạn chế tần suất yêu cầu API để ngăn chặn quá tải và bảo vệ tài nguyên của bạn.

**8. View và URL Patterns:**

- DRF sử dụng cấu hình View và URL Patterns để ánh xạ yêu cầu HTTP đến các hàm xử lý cụ thể và định dạng URL tương ứng.

**9. Đánh giá và Tài liệu:**

- DRF được cộng đồng rất hỗ trợ và có tài liệu rất tốt. Bạn có thể tìm hiểu cách sử dụng DRF thông qua các tài liệu và ví dụ thực tế trên trang web chính thức của nó.

DRF giúp bạn xây dựng các ứng dụng web dựa trên RESTful API một cách dễ dàng và hiệu quả, và nó thường được sử dụng trong việc phát triển các ứng dụng di động, ứng dụng web đơn trang (SPA), và dịch vụ web.


**10. Mã lỗi/HTTP Status Codes:**

* Mã lỗi HTTP (HTTP status codes) là các mã số được trả về bởi máy chủ HTTP để chỉ định kết quả của một yêu cầu HTTP. Ví dụ, mã 200 nghĩa là "Thành công", trong khi mã 404 nghĩa là "Không tìm thấy". Các mã lỗi giúp ứng dụng biết được trạng thái của yêu cầu và làm cho việc xử lý lỗi dễ dàng hơn.

**11. Stateless (Không lưu trạng thái):**

* Stateless là một trong các nguyên tắc của REST, nguyên tắc này đòi hỏi rằng mọi yêu cầu từ khách hàng đến máy chủ phải chứa đủ thông tin để máy chủ có thể hiểu yêu cầu mà không cần thông tin trạng thái trước đó. Điều này giúp tạo ra các hệ thống ứng dụng có khả năng mở rộng và độc lập với trạng thái.

**12. Endpoints (Điểm kết thúc):**

* Endpoints là các URL cụ thể trong ứng dụng web được sử dụng để thực hiện các thao tác cụ thể trên tài nguyên (resource). Mỗi endpoint đại diện cho một tài nguyên hoặc một loạt các tài nguyên và cho phép bạn thực hiện các phương thức HTTP như GET, POST, PUT, DELETE để thao tác với tài nguyên đó.
