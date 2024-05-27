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
