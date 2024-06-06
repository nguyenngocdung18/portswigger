Link: https://portswigger.net/web-security/file-path-traversal
# Lab: File path traversal, simple case
Khi mà ta chuột phải vào hình để mở nó trong tab mới 
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c9c0b3ef-47a4-4b66-9310-f755f2bb851e)

ta sẽ thấy phần image?filename=5 trong URL đáng nghi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2590fa66-c255-4b6e-836b-8e6c364f1c10)

## using Burp Suite
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/163e56a2-7fb6-44c9-96ac-db17b920d101)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c3c16c33-bf0c-478f-ac09-c7f874c14099)

# Lab: File path traversal, traversal sequences blocked with absolute path bypass
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/772d54eb-d7c1-4d1d-9a3e-a4e76c3ef719)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/47dcb1c6-9017-44c3-9089-dd72db5ef006)

# Lab: File path traversal, traversal sequences stripped non-recursively
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e988a340-2b21-49d2-9c55-5d957fa03938)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d289cea9-c058-43ff-a970-2818c55ec623)

# Lab: File path traversal, traversal sequences stripped with superfluous URL-decode
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/314ddf5d-397d-46e2-8ac0-ed6be3e35de2)

Vào tab Decoder, thử encode URl ```../../../``` 1 lần thì không được, =))) tiếp tục endcode cái đấy thì thành công. 
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0e9e5961-7297-41a0-b49f-e47727239573)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/618924c7-143a-4eb6-93e2-440544d948b9)

# Lab: File path traversal, validation of start of path
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e3017447-dba0-48fd-9bcc-7fcc940ac9fd)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a2819728-faaf-4903-a64e-9964e1bde83f)

# Lab: File path traversal, validation of file extension with null byte bypass
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4386c43b-94cf-4a5c-8db4-e6bc3b341f38)

Sử dụng kí tự %00 như một kí tự NULL. Máy chủ web có thể hiểu phần tên tệp là passwd và loại tệp là png. Khi gặp %00, máy chủ có thể kết thúc quá trình giải mã, và bất kỳ ký tự nào sau đó sẽ bị bỏ qua hoặc không được xem xét

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b3b5761d-fba5-4b53-9081-16cf8560b2e7)


