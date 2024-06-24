Link: https://portswigger.net/web-security/cross-site-scripting

# Lab: Reflected XSS into HTML context with nothing encoded
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/886b8e2f-6adb-45d9-aa4c-a73a90fb4de5)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/24f11ed2-7422-4367-878c-6154bb15f1bc)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1ca2b307-3e61-48db-bcf6-f4e67871bae0)

# Lab: Stored XSS into HTML context with nothing encoded
Vào post bất kì comment ```<script>alert(1)</script>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d40e60a6-511b-4284-a74c-2bf3547c518f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ba73bcfa-4fa6-43b6-8e1c-f2f0a1ce36cc)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/96037e45-bbe6-4304-a5eb-93ce80e39c56)

=> Done!

# Lab: DOM XSS in document.write sink using source location.search
Ta thấy searchterm đang được để trong 1 thẻ <img>

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6b7ae5f8-5d9a-49ae-89ad-0bd89da7220c)

break out thẻ img

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1ab1cf37-d697-4971-b59f-789736f2dd1c)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/075b103c-b179-45ce-bd96-dde213cc6641)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f943f52f-74a1-4360-b5c3-6ffbdec0f24d)

# Lab: DOM XSS in innerHTML sink using source location.search
Khi thực hiện tìm kiếm thì ta thấy nội dung sẽ nằm trong thẻ <span id=....> </span> 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/31782be8-a1b5-4e9d-9a7a-476cdbfcccf0)

Sử dụng câu lệnh ```<img src=1 onerror=alert(1)>``` 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d7df665e-56e6-433e-86f9-b88a76e7d2b6)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/633e0d17-2876-478b-b050-18c968714f34)

# Lab: DOM XSS in jQuery anchor href attribute sink using location.search source
Khi ta thêm vào URL 1 giá trị bất kỳ ví dụ là "12a" vào sao tham số "returnPath=/". Ta thấy phần /12a được để trong 1 thẻ là ```<a href=...>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0386194b-ac21-4d80-a378-c355512427da)

Ta sử dụng ```javascript:alert(document.cookie)```.  Khi trình duyệt gặp URL bắt đầu bằng "javascript:", nó hiểu rằng phần còn lại của URL là một đoạn mã JavaScript cần được thực thi thay vì điều hướng đến một trang web mới.

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4f665964-b69c-4f82-a0aa-17c08c006a7d)

Ấn Back để hoàn thành lab!

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/90f53d88-b068-451a-b795-f6e9d76a487f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c8a724c6-0eaf-46af-ac8c-8fcd3f7fcc75)

# Lab: DOM XSS in jQuery selector sink using a hashchange event
Go to exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fcd68966-9341-4b05-b0a4-0430452d4465)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/da0afb6d-1ac6-4e0a-b688-6516bb375d88)

Store -> View exploit
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f47972d1-194a-4498-a1c6-b3bd71479f0b)

hàm print() đã được thực hiện. Quay lại exploit server để gửi tới victim

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8240103b-33e6-478d-8767-501e097ec085)

# Lab: Reflected XSS into attribute with angle brackets HTML-encoded
Khi search kí tự "h" , ta thấy kí tự "h" được đặc trong 1 thuộc tính là ```value ="h"```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/72fb2144-0b29-4710-bb19-aa5bf2ec2b09)

Sử dụng ```"onmouseover="alert(1)``` 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/baae49af-f773-4e5a-bfbb-f97690353b0f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/10646459-6ffd-4432-8331-547617dd7e6b)

# Lab: Stored XSS into anchor href attribute with double quotes HTML-encoded
Chọn 1 post bất kì và thực hiện bình luận

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/002d7b49-be7c-470c-89f8-ec0dfe21782f)

Ta thấy khi ta điền thông tin vào mục website thì sẽ được lưu vào thẻ ```<a href=...>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/776c89e1-269b-478d-8162-2797e8639429)

Tạo 1 comment

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/27d71fff-8501-47be-958d-432a88977b20)

Khi kick vào tên của mình sẽ hiện thông báo alert(1)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0155cd13-173b-44d6-95a5-136f328f524d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4a230de8-e831-4420-b082-882c420c79a5)

# Lab: Reflected XSS into a JavaScript string with angle brackets HTML encoded
Ta thấy kí tự ta tìm kiếm được gán vào giá trị của searchterm 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7af1b06d-aac8-4921-8dc5-da163a096420)

Sử dụng ```'-alert(1)-'```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8f2b3be4-91b5-43fb-8fb1-1f563e50ba11)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/00311f9c-c92f-48c1-947b-c0c1eb36ef5a)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/84e4dfe9-f31e-4979-9c04-0792efbcb4ab)

# Lab: DOM XSS in document.write sink using source location.search inside a select element

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e120a550-286f-4264-8981-8fb8784d2ef9)

Ta thấy biến "store" lấy giá trị từ tham số storeId trong URL. Hàm document.write sau đó viết một phần tử ```<select>``` chứa các phần tử ```<option>```, trong đó có thể có một ```<option>``` với giá trị của store từ URL nếu tham số storeId tồn tại.

Ta thực hiện chèn đoạn mã ```&storeId="></select><img src=1 onerror=alert(1)>``` vào trong URL và dùng inspect để xem
Mã JavaScript sẽ xử lý giá trị của storeId là ```"></select><img src=1 onerror=alert(1)>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/087cb6d9-043c-40ea-976a-c7506a59712f)

=> Trong thẻ select đã có thêm 1 option ```<img..>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4d03fa4a-29af-433a-ac05-cd037107dcc9)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c236a2ec-0261-4bea-ae5f-771e7ad26dfb)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ed9ce263-ed2c-4919-8c49-97f7949d6d9f)

# Lab: DOM XSS in AngularJS expression with angle brackets and double quotes HTML-encoded

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c5fdbb63-544b-4d67-92f8-394bd7052830)

Sử dụng ```{{$on.constructor('alert(1)')()}}```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0a7d9028-a766-4a30-a622-7b2cd6941df3)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/522cc85b-0325-4a1a-b962-82ce04ce3f0f)

# Lab: Reflected DOM XSS
Ta thấy web sẽ nhận input bằng "searchResults.js" và máy chủ sẽ phản hồi lại kết quả tìm kiếm

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d93096c2-f923-47ef-a958-39803ebdaebf)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c4e51369-0acf-4093-b2d2-57426b1c275a)

Ta thấy mã script đã thoát dấu ngoặc đơn ngoặc kép nhưng dấu "\" thì chưa. Vì vậy ta sử dụng ```\"-alert(1)}//```

kết quả trả về:

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a827700e-c528-4919-9ddc-f841a0a707ca)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/31874586-25bc-4334-b48c-a96cc6172a74)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/be937639-3a13-46fe-93e3-f2f230587510)

# Lab: Stored DOM XSS

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4bcfe8ac-fe4b-4517-a7e2-9d4c7c152efc)

Để ngăn chặn XSS, trang web sử dụng hàm JavaScript replace() để mã hóa dấu ngoặc nhọn. Tuy nhiên, khi đối số đầu tiên là một chuỗi thì hàm chỉ thay thế lần xuất hiện đầu tiên

Sử dụng ```<><img src=1 onerror=alert(1)>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0adbbc8e-6571-4aa6-8c9c-afba3e338048)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7853533d-49ea-4087-b4d7-d00cd4706f26)

# Lab: Reflected XSS into HTML context with most tags and attributes blocked

