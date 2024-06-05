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

# Lab: User ID controlled by request parameter, with unpredictable user IDs 
Tìm kiếm quanh web thì tôi thấy carlos có đăng 1 bài viết

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/69e6120e-882a-4062-8904-9f6903e26666)

Trong response có lộ 1 đường dẫn nhạy cảm, khả năng cao là GUID của carlos

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/142d7228-f59d-4178-a828-a78ee8d7421b)

Về lại My account và thay đổi id

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7ade65b8-b245-44e6-8017-3ac4b6689589)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/434f1868-d1c7-4852-8cc7-1befc26d83ce)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/74f6fcff-d558-4ad2-b6f7-62a58436cb70)

# Lab: User ID controlled by request parameter with data leakage in redirect 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3331e83e-2def-4113-8f44-8672a52e7989)

Khi ta thay đổi thông số id thành carlos thì web điều hướng về trang login nhưng trước đó có vẻ như nó vẫn điều hướng tới id=carlos trước nên ta có thể xem được APIkey.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fb671084-e6fa-446d-b3be-2ac132401b67)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/df6cd4fb-a990-4417-886a-0faad397fdf3)

# Lab: User ID controlled by request parameter with password disclosure

Khi ta đổi id từ wiener thành carlos 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a1a002da-523b-48e0-8701-904e783fc62c)

Ở phần Response ta có thể lấy được mật khẩu đã bị ẩn đi.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/767ad762-566d-4f3e-8326-2a257a9c932c)

Làm tương tự với id=administrator

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/16888f8f-0a13-41eb-9a7b-f007724b514d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/68020cd6-dc24-46c6-b1d8-2aa7a64776b3)

Sử dụng mật khẩu để đăng nhập 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/90193382-2578-4f47-a90e-a09a4c543916)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/15bb58b1-1b50-407e-8998-667b8185d643)

# Lab: Insecure direct object references

Khi ta gửi tin nhắn và ấn vào view transcript thì nó sẽ tự động tải 1 tệp với tên là các số tăng dần. Nhưng vấn đề là nó lại bắt đầu từ số 2 mà không phải 1

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/814d58ef-d489-4582-addf-3ef7bd41a38b)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/17c55584-63e2-4aa3-bf95-daa19c424c25)

Sửa thành 1.txt

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/935184aa-3afa-49e9-8afe-929fc803d1d7)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8743d117-0a01-4f07-b67c-ea697df958fc)

=> Done!!!

# Lab: URL-based access control can be circumvented
Truy cập tới /admin thì hiện thông báo "Access denied"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7e114952-9531-44e1-946d-a66749d3f29a)

Sửa /admin thành / trong URL và thêm "X-Original-Url: /invalid" => thông báo trở thành "Not found". Tức là nó đã thực hiện truy vấn rồi nhưng không tìm thấy 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b98287f1-1930-4955-bb93-d6203f56845c)

Chuyển /invalid thành /admin => truy cập thành công Admin Panel

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f42889f8-8315-4ea7-8c0a-afd5146859d9)

Ta tiến hành bắt request lại và làm như trên

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9a028c4b-f36c-4c21-806e-658d5a3d11c4)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9bb12622-512d-4e89-a12c-8067fb795a7d)

Click Forward

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6cc21268-7d2d-49c5-a364-11e6ff404b77)

Xóa người dùng carlos

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8cdc8614-2a55-405b-bc2c-f3cbc17e645f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/405fb445-289e-46c4-acf2-38e1e45a0a37)

Chọn Forward để gửi đi và xong =))

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2de41ea7-3f64-4a11-908a-f62087bae7ab)

# Lab: Multi-step process with no access control on one step 
Đăng nhập vào tài khoản admin và nâng quyền carlos

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0288330d-e681-474f-a8fd-1a80fa538b6e)

Request này là xác nhận lại 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/426671b6-d423-483c-9f69-8dfe493dce49)

Ta đăng nhập vào user wiener 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b5f58803-0bfa-4e30-ac5a-df2e6369f649)

Sửa thành tên và cookie của wiener và bấm send

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ffd18145-f656-4e7e-8386-8bfe46f737de)

Sau đó tiếp tục làm tương tự với request xác thực

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/21c5a2fc-0963-4144-949e-b6a51dfc3a7c)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1a2e5162-f101-4884-ae92-768867b00d0d)

=> Done!!

# Lab: Referer-based access control 
User wiener không có quyền admin, ta thấy referer trỏ tới /login

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0a9f6f73-a1c0-4bf2-97f2-5aa291885661)

Truy cập vào account của admin và thực hiện nâng quyền cho carlos

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/30e273d4-d65c-4bb0-900f-ed65b6fc9c4c)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d4d11654-5550-4a9d-aeb9-26737ec40024)

=> Ta bắt được 1 request và quan sát referer đã từ /login thành /admin

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/eff58b90-172f-41cd-9458-a21581a7831a)

Thay dổi tên và session cookie => Done!!

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7d17738d-1e69-4c21-95be-40a41e74cf8b)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b0bc1a85-4b69-4cb5-b3de-9453111f65d9)
