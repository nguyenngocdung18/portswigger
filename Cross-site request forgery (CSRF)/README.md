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
