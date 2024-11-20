## Sử dụng Cloudflare Worker Stream Google Drive

### 1. Nội dung chính
- Tạo một Web Server ( FREE ) để stream video từ Google Drive

### 2. Chuẩn bị:

- Đăng ký **Tài khoản Cloudflare** [https://dash.cloudflare.com/sign-up]. Trong quá trình đăng ký Cloudflare có yêu cầu bạn nhập website thì bạn cứ nhập tùy ý!

- **CLIENT_ID**, **CLIENT_SERECT**, **REFRESH_TOKEN** **Google Drive**. Xem hướng dẫn phía dưới.

### 3. Cách lấy **CLIENT_ID**, **CLIENT_SERECT**, **REFRESH_TOKEN**

- Truy cập [https://console.cloud.google.com] để lấy giá trị ***CLIENT_ID*** và ***CLIENT_SERECT***. Xem lại video phút 16:26 [https://www.youtube.com/watch?v=EVHgg7JM3YY] đã hướng dẫn trước đó. 

- Thêm vào Ứng dụng đã tạo URI ``https://developers.google.com/oauthplayground``

https://github.com/user-attachments/assets/89a9f76c-16ee-4601-a354-980ca5c11baf

- Truy cập vào [https://developers.google.com/oauthplayground/]

- Chọn "Drive API V3" => ``https://www.googleapis.com/auth/drive``

<img src="images/6mDUBbxaTO.png" width="400">

- Thực hiện các bước theo hình, cuối cùng chọn ``Authorize APIs``

<img src="images/X1CCVKAclZ.png" width="400">

<img src="images/Qj3SWDJBdK.png" width="400">

<img src="images/tyqbMgTq8X.png" width="400">

<img src="images/KLkMpBUvTT.png" width="400">

<img src="images/MJkBisK5WA.png" width="400">

<img src="images/CkV72JpU2h.png" width="400">

- Sau khi copy giá trị "REFRESH_TOKEN" thì đã hoàn tất bước này. 

- Vậy là bạn đã 3 giá trị **CLIENT_ID**, **CLIENT_SERECT**, **REFRESH_TOKEN** lưu lại 3 giá trị này.

### 4. TRIỂN KHAI WEB SERVER CLOUDFLARE

- Tìm đến ``scripts/worker.js`` copy script về máy rồi tiến hành chỉnh sửa giá trị ``GOOGLE_CLIENT_ID`` ``GOOGLE_CLIENT_SECRET`` ``GOOGLE_REFRESH_TOKEN``

- Tiếp theo đổi giá trị của mục ``USERNAME`` và ``PASSWORD``

- Chỉ thay đổi giá trị đoạn code phía bên dưới như

```sh
var GOOGLE_CLIENT_ID = '92048********.apps.googleusercontent.com';
var GOOGLE_CLIENT_SECRET = '**********Eq9IqDd56gKIIZId1';
var GOOGLE_REFRESH_TOKEN = '1//04LkLgjISNSQeCgYIARAAGAQSNwF-L9IronW2yMdZzc77******';

var YOUR_ACCESS = {
	USERNAME: 'admin',
	PASSWORD: 'admin',
};

```

- Lưu lại file ``workers.js``

<img src="images/5xVMa4AhVS.png" width="400">


- Truy cập tài khoản Cloudflare chọn ``Workers & Pages`` chọn ``Created`` new ``Workers``

<img src="images/Ak2Iq57JCp.png" width="400">

<img src="images/dZ9b4qwQqU.png" width="400">

<img src="images/7XMMJWKuyL.png" width="400">

<img src="images/3fhUm7Vsvp.png" width="400">

- Copy toàn bộ nội dung trong file ``worker.js`` bạn đã lưu vào và nhấn ``Deploys``

<img src="images/idCQ39yhuI.png">

- Sau khi ``Deploy`` thành công bạn copy đường dẫn website tại mục ``Preview`` địa chỉ sẽ có URL tương tự như ``https://play.xxxx.workers.dev``. Trong đó ``play`` là tên của bạn đặt.

<img src="images/cHWjyNZIcU.png" width="400">

- Truy cập vào website, lần đầu tiên bạn phải nhập tài khoản ``username`` và ``password`` giá trị bạn đã tạo trong file ``workers.js``

<img src="images/qODpeyzWKE.png" width="400">

- Giao diện website "quen thuộc" sẽ hiện ra. Bạn có thể truy cập địa chỉ website trên thiết bị di động.

<img src="images/nDKgFctCG8.png" width="400" >

### 5. SỬ DỤNG ỨNG DỤNG STREAM VIDEO

#### Laptop/PC: 
* Sử dụng các trình play stream video như Nplayer, VLC

#### Mobile/Iphone/Android:

* Chú ý: **VLC** bạn phải mở App chọn ``Copy Link 2`` để play
* Nplayer nhấn trực tiếp sẽ tự động mở.

### TỐC ĐỘ STREAMING?
- Nhanh, sẽ chậm lúc đầu để load video một chút.
- Bạn có thể tìm hiểu thêm về Cloudflare.

### DỊCH VỤ MIỄN PHÍ VÀ GIỚI HẠN?
- Dịch vụ ``Worker`` bạn sử dụng hoàn toàn miễn phí.
- Giới hạn ở số lần truy cập nhưng không đáng kể, bạn có 100k request miễn phí.
- Nên sử dụng cho riêng bạn

### ****TUYÊN BỐ MIỄN TRỪ TRÁCH NHIỆM****
- Khi sử dụng các hướng dẫn trong bài viết này, bạn cam kết rằng dữ liệu, tài khoản của bạn phải an toàn, tránh mất dữ liệu, vi phạm chính sách của nhóm...

- Cách trường hợp tài khoản của bạn bị khóa, hoặc có dấu hiệu vi phạm, vui lòng liên hệ các bên liên quan, mình KHÔNG CÓ TRÁCH NHIỆM trong việc này!

- Tất cả nội dung, mã nguồn đều công khai, bạn có thể tùy chỉnh theo ý muốn.

