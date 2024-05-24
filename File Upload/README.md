Link: https://portswigger.net/web-security/file-upload

# Lab: Remote code execution via web shell upload
Ta đăng nhập với account wiener:peter và thấy có phần upload ảnh 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/889794eb-3418-402b-ac36-e5f983711c96)

Tạo 1 file php cho phép đọc tệp /home/carlos/secret và upload nó lên

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9c27f630-b0d5-4b78-ad38-c72c77c0ea4a)

Sau khi upload, ta trở lại proxy http history 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b67b2847-abad-4bf7-b435-0ddc604996e5)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/32808471-890c-4be1-a4cc-52229cb1b872)

=> Đã đọc được file, giờ ta chỉ cần submit kết quả là xong.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/82c7cb3d-39e9-4373-aa08-090bc4e72d85)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4222f753-a1b3-4c60-9652-7a1fa7320141)

Nice!!

# Lab: Web shell upload via Content-Type restriction bypass
Khi tôi làm tương tự lab trên thì thấy nó bị giới hạn lại file gửi 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dc4b973d-2a2f-46fe-ad3d-b8e021dd409e)

Trong Burp Suite,

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0311fca5-8393-4ad7-936a-0707f577312d)

Tôi thay đổi Content-Type thành image/jpeg và đã upload thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/35d2ce36-dca2-43e0-80f9-1e9b265e97c1)

Tiếp đó tôi upload 1 file jpg

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c8bf72ce-aeb7-4819-9d1e-d3b51c253c1d)

Có được 1 request GET và đổi path thành exploit.php

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9ac86b0c-683a-46a1-a5e6-35f775b19c6e)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c0b479c0-1308-4f9d-953a-e82805592369)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f23a4345-b9b2-49ba-a452-d55feb8e3f54)

=> Done!! 

# Lab: Web shell upload via path traversal
Tôi vẫn thực hiện upload file như bình thường nhưng hệ thống trả về file txt nguyên bản chứ không phải nội dung tệp secret :<

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e4e349fd-6f6f-4af5-af94-c86a38a62713)

quay lại request POST /my-account/avatar và chỉnh sửa Content-Disposition: "filename:..%2fexploit.php"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/743065e1-15f8-438d-b967-5208eab51bcf)

Ta thấy dòng thông báo "The file avatars/../exploit.php has been uploaded." đã thay đổi. Mở web và quay lại trang my account

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1dba5c13-5dd3-4b7c-9e13-d9de13e87704)

Thay đổi path và nhận được đáp án. ( Vì ta đã thay đổi nơi lưu tệp rồi)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b5cec7d7-36da-4fe2-83f7-ed555e65c9ef)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7dfa43ea-4197-4a99-bcd5-8fce043ae64e)

# Lab: Web shell upload via extension blacklist bypass

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/70f5311e-c9fa-4b60-a35f-870ce422a181)

Ở request khi upload exploit.php, ta thay đổi nội dung như sau

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/aa556abe-26a2-40a0-b405-dd97f9e234ca)

=> upload thành công

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/07050299-3ca0-4d24-b258-61568aa7d81c)

Tải 1 tệp jpg và thay path thành exploit.shell => đáp án

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f751bade-69ca-45c6-ad4a-0c1e2e2bae04)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b0b7f6c3-d188-4711-af87-2160a83b629d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1c4a6819-971d-4d9e-8605-30dcd1a671a4)

# Lab: Web shell upload via obfuscated file extension
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/532efcd9-52d4-49ad-9bf3-3cc725b0a7f2)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/64013348-215b-4ad7-90a3-0b0c1cd7fc43)

Thay đổi file name thành " exploit.php%00.jpg"  %00 tương đương kí tự null để đánh lừa hệ thống

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/aa6f6291-b239-4c78-bff7-e679bbb19186)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8bc8c429-501d-42b3-bd46-858907960ec6)
