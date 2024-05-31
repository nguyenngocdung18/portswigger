Link: https://portswigger.net/web-security/csrf

# Lab: CSRF vulnerability with no defenses
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5492615f-ff53-4892-a105-3e6eeaba8a55)

Go to exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/abb4e6eb-1e28-40e4-a35e-b5572736545e)

Ấn vào view exploit 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2c3dfab3-fd32-4c13-b06b-72ab54eaf1fc)

Ta thấy email đã được thay đổi

Giờ ta quay lại , ấn store để lưu và "Deliver exploit to victim" để hoàn thành bài lab.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/caa1d239-fab1-4888-b8e6-f2aec53728f0)

# Lab: CSRF where token validation depends on request method
Lần này khi thay đổi email đã có thêm 1 thông số csrf

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7673df97-d5f7-4563-9da3-9f88c1c9fd65)

Chọn change request method

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8591249e-05af-4c88-a0f9-15af7cd00d2d)

Ta thấy mã csrf không còn được xác minh.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5b90ee1f-90f6-4f75-93d2-f90c616564f7)

Ta vẫn dùng template như lab trước nhưng thêm 1 thông số csrf 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a2daaa78-3887-4207-ab83-f7dd0fd0d991)

Thay đổi email thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b4741a39-a7a9-4246-a83e-4df7e57b2efd)

Giờ ta chỉ cần quay lại exploit server và gửi nó cho victim là xong!!

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4597703d-1c89-40a3-acc3-d4519620c6ef)

# Lab: CSRF where token validation depends on token being present

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/28b36df2-0155-4d1f-938d-06fca81403d6)

Lần này lab chỉ cho phép phương thức POST, ta thử xóa thông số csrf đi  và nhận thấy request vẫn được chấp  nhận

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a638a597-db8a-470b-bb72-3785c0faacc3)

Thực hiện thay đổi phần body trong exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4eb3409f-7210-4c93-b534-779cd5b9ddee)

Ấn view exploit và thấy email đã bị thay đổi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6fd2264a-af5f-4488-9644-de238540df03)

Giờ ta lại làm thủ tục cuối là gửi nó cho victim là xong rùi :3 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/92da9710-eb84-45e2-acdc-82c78abab8af)

# Lab: CSRF where token is not tied to user session
khi ấn send lần thứ 2 thì nó sẽ hiện thông báo lỗi => 1 csrf token chỉ dùng 1 lần

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/27b15119-4bed-4b7b-935f-2a6041582a83)

Ta phát hiện ra mỗi khi ấn vào my account thì mỗi người dùng sẽ được cấp luôn mã csrf

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/79aa3a3c-444c-4999-93b2-fe9154b22f27)

Ta sử dụng mã csrf đó và request đã được chấp nhận

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/316f9161-66bf-45eb-8729-80d61906a8c2)

Go to exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7bdc41f3-2860-4edc-85b5-82d6cf22cc95)

view exploit và thấy email đã được thay đổi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4c3dba5c-64a3-4549-ad06-ffe136073b90)

Gửi nó cho victim

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/195c870f-8116-4374-a8a1-dd5f7af6789e)
