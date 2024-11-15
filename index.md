## Tài liệu cho Client NextJS
Khởi chạy dự án.

```bash
npm i --force
npm run dev
```

Mở đường dẫn dự án [http://localhost:3000](http://localhost:3000)

# Cấu trúc Thư mục Dự án Next.js

Dưới đây là cấu trúc thư mục của dự án Next.js này và mô tả vai trò của từng thư mục và file.

## Thư mục gốc

- **next.config.js**: File cấu hình cho Next.js, chứa các thiết lập đặc biệt cho dự án như các biến môi trường, cấu hình các route, và tối ưu hóa build.
- **jsconfig.json**: Cấu hình cho JavaScript, giúp IDE hiểu các alias đường dẫn và các thiết lập khác.
- **.gitignore**: File này chứa danh sách các file và thư mục sẽ bị bỏ qua khi commit vào Git.
- **package.json**: Quản lý các dependency, script, và metadata của dự án.
- **README.md**: Mô tả chung về dự án, hướng dẫn sử dụng và các thông tin cần thiết khác.
- **postcss.config.js**: Cấu hình cho PostCSS, dùng để xử lý các tệp CSS.
- **tailwind.config.js**: Cấu hình cho Tailwind CSS, nơi tùy chỉnh theme và các thiết lập Tailwind.

## Thư mục `app`
Thư mục `app` chứa các phần chính của ứng dụng, được chia thành nhiều thư mục con.

- **(auth)**: Thư mục này chứa các trang và thành phần liên quan đến xác thực người dùng.
  - **login**: Trang đăng nhập của người dùng.
  - **register**: Trang đăng ký tài khoản cho người dùng.
  - **layout.js**: File layout dùng chung cho các trang xác thực.

- **(dashboard)**: Thư mục dành cho các trang và thành phần liên quan đến bảng điều khiển.
  - **layout.js**: File layout dùng chung cho các trang trong dashboard.
- **(portal)**: Thư mục dành cho các trang và thành phần liên quan đến cổng (Trang public ra bên ngoài).
  - **layout.js**: File layout dùng chung cho các trang trong portal.

- **layout.js**: File layout chính cho toàn bộ ứng dụng.
- **loading.js**: File quản lý giao diện khi đang tải nội dung của ứng dụng.

### Các thư mục và thành phần khác

- **config**: Chứa các file cấu hình cho các phần khác nhau của ứng dụng.
- **hooks**: Chứa các custom hooks dùng để tái sử dụng logic trong ứng dụng.
- **store**: Quản lý trạng thái ứng dụng bằng @reduxjs/toolkit.
- **components**: Thư mục chứa các thành phần giao diện.
  - **partials**: Các thành phần nhỏ dùng trong nhiều nơi trong ứng dụng.
  - **ui**: Các thành phần giao diện người dùng như button, modal, và các phần tử giao diện khác.
  - **widgets**: Các widget hoặc thành phần con phức tạp được sử dụng trong ứng dụng.
- **constant**: Thư mục `constant` chứa các hằng số được sử dụng trong toàn bộ dự án. Điều này giúp tập trung quản lý các giá trị cố định để dễ dàng thay đổi và tái sử dụng khi cần thiết.
- **public**: Thư mục `public` là nơi lưu trữ các tài nguyên tĩnh cho ứng dụng Next.js. Bất kỳ file nào trong `public` đều có thể được truy cập công khai thông qua đường dẫn.
- **services**: Thư mục `services` chứa các logic liên quan đến call API, cơ sở dữ liệu, hoặc các service khác.
### Lưu ý đặt tên và chú thích liên quan đến thư mục
- **Đặt tên thư mục**: Nếu không muốn thư mục hiển thị trên đường dẫn Ví dụ: `/auth/login` thay vì `/login` thì chỉ cần thêm cặp dấu `()` vào tên thư mục thì router của NextJS sẽ không nhận tên thư mục này vào đường dẫn.
- **`[...not-found]`**: là một dạng route segment tùy chỉnh dùng để xử lý các trang không tìm thấy (404) hoặc các đường dẫn không hợp lệ. Ví dụ: thư mục not-found này đặt trong thư mục `(dashboard)` thì khi truy cập vào các đường dẫn trong thư mục này nếu không tồn tại thì sẽ router sang trang `not-found`

---
