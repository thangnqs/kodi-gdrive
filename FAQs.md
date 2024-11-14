## ⚠️ Fixed "The server is temporary unavailable for this operation. Please try again later"

Một số bạn gặp phải lỗi "The server is temporary unavailable for this operation. Please try again later" khi mở Google Drive trên Kodi.

<img src="images/6dGnGystto.png" width=300>

- Sau một hồi kiểm tra mình phát hiện ra Tài khoản Upstash [https://console.upstash.com/login] đã tạo trước đó đã tự động XÓA "Database" của mình. ( XÓA DATABASE TRONG TÀI KHOẢN, CHỨ KHÔNG PHẢI XÓA TÀI KHOẢN TRUY CẬP )

- Mình có chát trực tiếp với Support và nhận được thông tin như sau:

<img src="images/UX8RMeq5jV.png" width="300">

- Tóm gọn lại là khi sử dụng gói Free Tier của nó thì mình phải kích hoạt 1 tháng / 1 lần để Database không bị tự động xóa!

- Nó sẽ gửi Email cho mình vào 1 ngày nào đó trong tháng bất kì và mình phải làm theo hướng dẫn để không bị xóa Database nhé!

<img src="images/8WxKoVWIvP.png" width="300">

- Như hình trên Unstash sẽ gửi cho bạn email để kích hoạt tiếp tục sử dụng dịch vụ của họ.

## CÁCH KHẮC PHỤC LỖI NÀY?

- OK. Bạn login vào [https://console.upstash.com/login] rồi tạo một Database mới như Video hướng dẫn trước đó nhé! [https://www.youtube.com/watch?v=EVHgg7JM3YY] Phút thứ 1:20

- Sau khi tạo "Database" mới xong rồi, thì copy đoạn code tương tự như 
`rediss://default:AdBNAAIjcDE2YmNjMTYzYiThlY2M0YTc2YmNhODY2OGx3YTwrlM2ZjNnAsMA@fine-dolphin-53325.upstash.io:6379`

- Truy cập Vercel [https://vercel.com/login] bằng tài khoản bạn đã tạo trước đó.

- Tìm đến website trên Vercel bạn đã tạo trước đó vào nhấn vào "Settings"

<img src="images/9YXuoT0etT.png" width=350>

- Chọn vào menu "Enviroment Variables"

<img src="images/ugeeCFpqot.png" width=350>

- Tìm đến chỗ "NEXT_PUBLIC_REDIS_CONNECTION" chọn Edit và nhập vào giá trị bạn mới tạo vào.

<img src="images/VCHATXCQ32.png" width=350>

- Nhấn Save lưu lại giá trị này.

<img src="images/zGZnVbsrqY.png" width=350>

- Quay trở lại đầu trang, bạn chọn vào phần "Deployments" chọn vào cái "Deployments" gần nhất. Nhấn vào dấu "..." rồi chọn "Redeloy" 

<img src="images/KQ7DdMROmF.png" width=350>

- Quá trình Redeploy sẽ mất 1-2 phút

- Sau khi Vercel thông báo Redeploy thành công. Bạn truy cập vào Kodi chọn vào tài khoản của mình xem có truy cập được Google Drive không nhé!

- Trường hợp vẫn không được thì bạn xóa cái Tài khoản Google Drive cũ trước ( nhấn giữ remote/mouses tên tài khoản ) đó đi và tiến hành "Add account" lại theo các bước như trong video đã hướng dẫn [https://www.youtube.com/watch?v=EVHgg7JM3YY] 

- Tiếp tục xem phim nhé 😆




