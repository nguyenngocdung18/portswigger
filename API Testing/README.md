Link: https://portswigger.net/web-security/api-testing
# Lab: Exploiting an API endpoint using documentation

Đăng nhập với tài khoản mật khẩu đã cho và thực hiện update email

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/afd626ac-15d4-435e-af92-46c5d6f077fd)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1599a982-73d6-4aa2-baca-fd146f5131de)

xóa "/user/winener" đi và click vào show response in browser

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e7c60c59-53a0-4fa7-aa41-ff59a861ffb0)

Ta có thể thấy được 3 options là delete, get, patch

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3959fd12-b4c6-47d1-a3b2-fdd4c97d429d)

hoặc sau khi copy link ra browser, ta có thể thấy nó trong proxy HTTP history

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6ef90987-9e68-48a7-ab50-aa49270ea9ff)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7af3ae89-663d-4e2e-bf71-15a4b45ba131)

Giờ ta chỉ cần dùng delete để hoàn thiện lab này

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/44c7d303-1092-4540-ae4f-bab2e0b0d504)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7b250df0-fd9c-45d3-9576-a89c42ea0efa)

# Lab: Finding and exploiting an unused API endpoint

Vẫn thực hiện đăng nhập và ấn vào sản phẩm "Lightweight l33t Leather Jacket"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/be63ac60-50a2-423d-8350-59eaf9ee1fd2)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/56b4a8f9-76e5-4a08-b7e2-a6ff24805285)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b2d9a7f1-36d5-4949-9e38-8a9076c45ae1)

Khi ta chuyển sang PATCH, ta thấy 1 tin nhắn

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c2066734-e401-4af3-9c56-7f5a850ddefe)

Thêm Content-type

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dd94a955-a2ec-4d96-998f-6dadd526b13f)

Thêm kí tự {}

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/bd51c809-62d9-4733-8f14-39c0b3c34c6f)

Thêm price

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dc0de7d6-5bc9-4fbc-bb06-88ee95ad2e07)

Trên browser , giá của sản phẩm đã về 0

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/aa36a8de-4326-46f0-affb-a0a96c851fda)

Thêm nó vào giỏ hàng và mua chúng với giá 0$

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/12252cd2-0d7a-49a0-873c-270ce1820121)

# Lab: Exploiting a mass assignment vulnerability
Ta thêm sản phẩm "Lightweight "l33t" Leather Jacket" vào giỏ hàng và thực hiện đặt hàng bằng cách ấn vào nút "place order" thì phát hiện ra 1 api checkout

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/16012d94-f2f3-41fa-ba36-c16d25430fa1)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d4909cde-8788-40e1-93e9-e49dc01a5d0c)

Gửi nó qua Repeater và thêm ```"chosen_discount":{"percentage":0},``` vào rồi thực hiện gửi đi thì thấy khi thêm 1 thông số nữa thì không báo lỗi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/677e07f6-b396-4d18-a81b-17d51f75ab88)

Vì thế ta chuyển mức giảm giá thành 100% để có thể mua hàng miễn phí

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e3536ed6-8e67-45d4-b4a7-e81ff01839f9)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/55c2a876-f767-4def-9a0f-b087f322de61)

=))) Done!!
