Link: https://portswigger.net/web-security/logic-flaws

# Lab: Excessive trust in client-side controls
Đăng nhập với account đã cho

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2581c412-d4bd-4d14-b648-5878580efbbc)

Khi thêm "Lightweight l33t leather jacket" vào giỏ hàng, ta nhận được 1 requests POST

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fe253395-7372-44a3-850f-ad61086e7b94)

Thay đổi giá trị của price và gửi lại

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/aadc03d0-269f-40bd-afff-ea035f7978c9)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8eef6b41-ed6a-4715-bc74-5e8145204bc8)

=> Done!!

# Lab: High-level logic vulnerability
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b2200f0e-b237-46e3-9b1d-b416f71e7bae)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/672de5ff-6461-46a8-8beb-102ac6681ea9)

Kiểm tra thấy ta có thể điều chỉnh số lượng sản phẩm xuống cả số âm được nhuwgn không thể đặt mua nếu giá tiền âm nên ta mua thêm 1 sản phẩm khác và giảm số lượng nó xuống âm =))) 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e47f7676-7303-4113-9968-51c91bb9c3ac)

Sau đó ta bắt lấy request khi thêm sản phẩm có id là 2 vào giỏ hàng và chỉnh sửa thông số quantity

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5b7c8f22-0567-41b8-b891-bc1484bb1224)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0aa4edbb-2917-4505-b659-72a6a91ae0f5)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5b834567-48ad-4eb1-9469-d20ae11fee70)

=> Done!!

# Lab: Inconsistent security controls
Thử các test sqli thường gặp với login form nhưng không thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/35e89dd4-19fc-472a-9120-4d373dc1f977)

## dùng ffuf
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b2e5959d-2442-480f-9151-874fbd731608)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/378b3b51-4fa9-4685-9ea1-55126e52b2a0)

=> user: DontWannaCry

Trong phần đăng kí 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/53d3699c-de8d-4a88-8365-524cdbe254a2)

Ấn nào nút Email Client ở phía trên màn hình và dùng gmail đó để tiến hành đăng kí

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/22bb4485-80df-4166-b04b-4bf64e60a22d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a7e2c325-c65b-46d5-b95c-751d78bb40a2)

Đăng nhập và tiến hành update email

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c230b9d4-b4c6-4d8e-8116-8330f51b4bed)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8cb6e319-e019-4b34-a7b2-ae9ea8d6f763)

Click vào Admin Panel và xóa user: carlos

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c9a19d2e-b184-4aeb-ba81-a8ccb8547d0c)

# Lab: Flawed enforcement of business rules
Nhập email vào phần sign up ở dưới cùng của trang home, tôi có thêm 1 phiếu giảm giá

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a89e40d4-a51a-4e48-9703-b69377afce7d)

=))) ảo thiệt, khi nhập cùng 1 mã 2 lần liên tiếp thì nó sẽ báo đã có rồi nhưng khi dùng 2 mã luân phiên thì lại được

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e216be52-df97-4e97-98c2-aaa70f10ee51)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4f6062ef-6ecd-423a-aaa6-5ef6d93c0280)

=> Done!!

# Lab: Low-level logic flaw
Ta vẫn có thể thay đổi giá trị của thông số quantity

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a17558ef-0d33-47c2-a7ae-b946784b6c3e)

Gửi request sang Intruder thực hiện attack và phát hiện ra sau càng tăng quantity lên thì giá cả sẽ tới 1 mốc nhất định rồi nhảy về số âm và tiếp tục tăng lên.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5488f84a-9b99-4b99-bde2-443125dea120)

Vì vậy ta điều chỉnh quantity thành 99 (99 là max) và payloads như bên dưới

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ff25002a-beab-434f-a0bb-23ce5d5d71d5)

tiếp đó bên tab resources pool

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a08b4f78-7791-4e37-bbc4-afbd4d01f33f)

Tiếp theo ấn attack, Sau đó thêm 1 sản phẩm khác và tăng số lượng lên sao cho nó trên 0 và dưới 100

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e6bbdae5-49a2-4445-96f9-68bf356b670f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/cfb22e5f-8700-4333-9b6d-fdf797d26eb0)

=> Done!!

# Lab: Inconsistent handling of exceptional input

Dùng email client và tạo account như lab trước đó, lưu ý để email dài 1 chút

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9f5954ae-d0ee-484f-bbab-2813353832d5)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4c6a10b5-e519-4894-a585-f9c60e39d18f)

Sau khi tạo account thành công thì không thấy Admin Panel và xet thấy phần email chỉ hiển thị 255 kí tự và ở mục đăng kí có dòng "If you work for DontWannaCry, please use your @dontwannacry.com email address". Có thể là phải email công ty mới được.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3fdec1b8-6617-4c38-88be-f8a2ad2beccd)

Vì vậy ta đi đăng kí tài khoản mới. Nhớ là chữ "m" trong "@dontwannacry.com" đứng ở ký tự 255. Ta đếm "@dontwannacry.com" chứa 17 kí tự , vậy cần 238 kí tự trước nó nũa. Có thể dùng 1 vòng lặp for để in ra cho chính xác

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1157caa6-f069-4d08-b432-4c36f74df428)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c713290b-4127-4457-9835-80831377256e)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2a8b78b4-5b6c-4f63-8edc-a207f13133e0)

Ta đã thấy tab Admin Panel

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/34e552c8-2be9-4bf1-8eac-d912beec6c20)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8f57d037-7e44-43b6-aba6-8e7e9eb57ef5)

# Lab: Weak isolation on dual-use endpoint
Trong lab này ta thấy có phần đổi mật khẩu

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e9ab9858-3c99-42ff-8cad-a5c5e11b6bf1)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/278f351d-0044-454a-92ef-65df99720839)

Khi ta xóa bỏ thông số currentpassword thì việc đổi mật khẩu vẫn thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a233b624-748c-429f-849a-783974bad713)

Vì vậy ta đổi username thành administrator

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dd27cacb-c975-4e6d-8a4d-6ce3f92032cb)

Đổi mật khẩu thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3b5861c9-2801-41fe-8733-7b01289b2c2f)

Đăng nhập thành công administrator

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c645f72d-8b2c-4e29-9c3d-3b5ae47bca55)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a344dfa1-68b8-468f-a95e-60018c610d0c)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/16cc2a52-bbdb-435e-aeb5-eccf33698152)

# Lab: Insufficient workflow validation
Khi Mua 1 món hàng thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f628dc62-3d23-4a6e-ac8a-20866a411213)

Ta kiểm tra thấy nó hiện vị trí đích

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5d1b4f48-6136-4767-a98f-cfcba9e433d7)

Bây giờ tiến hành đặt 1 cái Lightweight "l33t" Leather Jacket

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fcbab3d9-e507-41d4-bbfa-e5fb553476f5)

Thực hiện gửi request này

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0df9ebe2-6547-4689-b82f-77cb25860f5a)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/74dbdac7-8b84-422c-a7bb-bbaea61d061a)

# Lab: Authentication bypass via flawed state machine
Đăng nhập vào ta thấy 1 chức năng 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a8a1dee2-ee44-446f-8aac-f30519027318)

Nhưng không thấy có gì khai thác được, ta tiến hành FUZZ 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/762f3a54-b81e-4fd4-886e-2821feb92671)

Mở Intercept và tiến hành bắt request

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d204dc2c-bbb7-4b43-9e3f-964a04888231)

click vào forward để gửi đi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2f7a9302-0774-4c90-849d-4c342828db5f)

Drop request này, ở browser ta sẽ thấy

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dd501015-1234-4eb0-a4fd-f0c4b9ad7dc6)

Ta tiến hành về lại trang chủ, Intercept sẽ bắt được request này

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/05460a86-b039-48da-9f17-5c946e7c198d)

Ấn forward và tada =))) Chúng ta đã bypass thành công và có tab Admin Panel

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/67cb00fd-f266-4579-a7fe-a354d17d484d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/36b005ab-4637-4718-bf42-98f68bbb4956)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ca3d16f2-7a9a-4132-8d62-d13410b4aa2f)


