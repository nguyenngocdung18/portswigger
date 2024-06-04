Link: https://portswigger.net/web-security/access-control

# Lab: Unprotected admin functionality
Ta tìm thấy tệp robots.txt

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/87b5c33c-6ae7-4f80-93ae-0f3bc4e79821)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a9a1fbeb-9a07-465f-ac07-ed7c6432be67)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4b9dceba-8c61-4a8c-aba0-a10e894c2bf9)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0a970ad4-bf68-408b-9a00-49bf6dbfc1f0)

# Lab: Unprotected admin functionality with unpredictable URL
Đi quanh quanh web thì ta thấy ở source-page của các trang sp thì thấy 1 đoạn mã script

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b3e1d826-489d-4d66-8ca1-081a2bbfd9ea)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3392f4a3-f69e-4583-af6e-10af3b28ee14)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/bc20ad87-e8d3-4c55-9a65-fa7ad0f02b1c)

# Lab: User role controlled by request parameter

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2c025ad3-1ec2-4cec-a454-6bfd7174b03e)

Chuyển request sang thành method POST và sửa thông số ```Admin=true```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e99b1a56-d095-420e-a99d-cacdc5f922f1)

Ta thấy đã truy cập được tới admin panel

Trong browser, ta dùng Inspect để đổi value của admin thành true và tải lại trang web

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3082b170-4ef8-470d-bd88-073abd11d9c4)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/83322677-ba9e-4217-a509-1c9be0bf5485)

=)) Otoke

# Lab: User role can be modified in user profile
Ta thấy account wiener đang có roleid=1 và ta cần phải có roleid=2 để có thể truy cập /admin

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/df9de3a5-672c-4a1a-a0cc-ce47c8282ec1)

Thêm ```"roleid":2``` vào JSON và boom!!! =)) Ta đã đặt được roleid=2

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/18135f94-e08a-45ef-a7b6-792ea9cb4f46)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a77559ce-6024-403b-a3e4-073ed2f66fdb)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/25804e78-918f-4110-b974-65da899d2234)

# Lab: User ID controlled by request parameter 
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/da0136d6-4358-43fb-9270-c316c5233c97)

Đổi thông số id=wiener thành id=carlos trên URL

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ea3c3f9f-3761-41b2-a023-d33608477be6)

=))) Oke!

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0d4d0b9c-84cb-451d-bd56-edadf6dfe6c8)
