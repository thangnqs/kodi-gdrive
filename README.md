# Kodi GDrive Add-on [Updated: 11/2024 ]

### HOT NEWS 

*Phiên bản 2.0 (25/11/2024)* [https://github.com/aldacco/drive-login] đã có **UPDATE MỚI NHẤT**

- **Không còn sử dụng REDIS** 
- Thay đổi cấu hình như file ``config.txt`` 

⚠️ CÁC CẤU HÌNH TRONG VIDEO SỬ DỤNG REDIS KHÔNG CÒN GIÁ TRỊ [https://www.youtube.com/watch?v=EVHgg7JM3YY]


⚠️ GIÁ TRỊ `NEXT_PUBLIC_CLIENT_ID` THAY BẰNG ``GOOGLE_CLIENT_ID``

⚠️ GIÁ TRỊ `NEXT_PUBLIC_CLIENT_SECRET` THAY BẰNG ``GOOGLE_CLIENT_SECRET``

❌ KHÔNG CÒN SỬ DỤNG `NEXT_PUBLIC_REDIS_CONNECTION`

⚠️ PHIÊN BẢN < 2.0 VẪN SỬ DỤNG BÌNH THƯỜNG.


### [Fixed] The server is temporary unavailable? [click here](https://github.com/thangnqs/kodi-gdrive/blob/master/FAQs.md)

 
### Hướng dẫn chi tiết ( đọc từ trên xuống )

Bạn có thể xem hướng dẫn chi tiết tại [đây](https://github.com/aldacco/drive-login).

Hướng dẫn chứng thực Google Drive Stream Video trên Kodi App 

Nguồn tham khảo: [https://github.com/aldacco/drive-login]

Video hướng dẫn xem tại đây [https://www.youtube.com/watch?v=EVHgg7JM3YY]

## Các bước chuẩn bị

- Tài khoản Github [https://github.com/signup]
- Tài khoản Vercel [https://vercel.com/]
- Tài khoản Google Drive

👋 **Chú ý:** DÙNG TÀI KHOẢN GITHUB ĐỂ ĐĂNG KÝ (SIGN-UP) CÁC TÀI KHOẢN UNSTASK VÀ VERCEL

## BƯỚC 1: Đăng ký tài khoản Github

- Nếu bạn chưa có tài khoản Github thì đăng ký tại địa chỉ [https://github.com/signup]

- Đăng nhập bằng tài khoản.


## BƯỚC 2: Đăng ký tài khoản Vercel ( dùng để tạo trang web )

- Truy cập [https://vercel.com] chọn Sign-Up tài khoản Vercel bằng Github
- Fork mã nguồn từ đường dẫn [https://github.com/aldacco/drive-login]
- Tại giao diện Vercel.com, thực hiện import dự án
- Dán cấu hình như file config.txt vào mục Enviroment
- Giá trị `GOOGLE_CLIENT_ID` và `GOOGLE_CLIENT_SECRET` lấy tại **BƯỚC 2**

## BƯỚC 3: Tạo Google Certificate API
- Truy cập [https://console.cloud.google.com] để tạo API
- Xem video để lấy các giá trị `GOOGLE_CLIENT_ID` và `GOOGLE_CLIENT_SECRET`

👋 **QUAN TRỌNG**

- Sau khi triển khai web xong tại bước 4, bạn sẽ có một đường dẫn website tương tự như
  `https://xxx.vercel.app` ( đường dẫn này Vercel.com tự tạo cho bạn, không sao chép giá
  trị này)

- Quay trở lại Authencation Config bạn đã tạo trước đó, thêm
  `https://xxx.vercel.app/callback` vào mục **Authorized redirect URIs** ( nhớ có thêm chữ `callback` nhé ) và nhấn _Save_

<img src="images/N3D3L4lAng.png" width="400">

## BƯỚC 4: Cấu hình Website

- Theo hướng dẫn trong video
- Hoàn chỉnh các giá trị giống như file config.txt

## BƯỚC 5: Cài đặt Kodi, Google Drive extension

- Cài đặt Kodi và Google Drive Extension ( xem thêm video hướng dẫn)

## BƯỚC 6: Chứng thực tài khoản Google Drive trên Kodi

- Cung cấp quyền truy cập ( xem thêm video hướng dẫn )


### TUYÊN BỐ TỪ CHỐI TRÁCH NHIỆM
- Tất cả nội dung hướng dẫn trong mục đích GIÁO DỤC.
- Tôi không chịu trách nhiệm pháp lý Việt Nam nếu bạn lạm dụng nó vào mục
đích xấu.
- Vui lòng tìm hiểu kỹ trước khi sử dụng, trường hợp mất dữ liệu, tài khoản .. hoặc bất kỳ vấn đề gì trên tài khoản của bạn. Tôi không có trách nhiệm trong việc này!