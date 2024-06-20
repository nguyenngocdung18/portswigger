Link: https://portswigger.net/web-security/sql-injection

# Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/327800f1-dfea-47cf-97cf-8ee1ce312cb7)

# Lab: SQL injection vulnerability allowing login bypass
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/814b2e11-249d-44b6-97a2-738d26d7390d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/644e02a2-6d0c-4f41-ba27-2167e94fceed)

# Lab: SQL injection attack, querying the database type and version on Oracle
?category=Gifts'+UNION+SELECT+'abc','def'+FROM+dual--

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/22a99a6d-fc53-47e9-a624-74806107395f)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/765bc21b-86da-4e74-9f41-153523040530)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/65d7c205-d00e-44e4-8f0e-70c9008e1824)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a583ede3-705a-49ae-b83f-8fdb065c366d)

# Lab: SQL injection attack, querying the database type and version on MySQL and Microsoft
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/207d280d-2ce1-432b-ab78-70aa30174ba8)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2def5073-35ce-4511-8bfe-36b24ea1719e)

=> ta đã thấy 2 cột abc, def. giờ chỉ cần thay thành @@version để hiển thị phiên bản

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/241b1a73-d9a7-4b5d-91d7-a5c8ff7ddbad)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f5e33e95-e01b-48dc-87a1-42a187bf8f24)

# Lab: SQL injection attack, listing the database contents on non-Oracle databases

Sử dụng chức năng Inspector của BurpSuite để viết câu truy vấn tiện hơn

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0dbee7a4-5596-4e8d-8275-19a8f5bd0e15)

=> 2 cột A, b được hiển thị

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/aae6f976-8eb8-48c4-be38-cd5fa18e1279)

=> Sử dụng information_schema để xem thông tin của dbs

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6347d19f-2c0c-4a58-87ba-f21960ecdfdf)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8dfc0350-e77b-4bb7-b92b-a189b38413f4)

=> có 3 cột là username_spwono, password_mmvggl, email trong bảng users

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1e90ab00-90ee-4631-ac45-f8429592fd72)

Có 3 user là carlos:aefxfjhqso9btamwcljy, wiener:tw4jmow0pyke4yrkbb86 và administrator:wwueqldv9v3x1v16zycc

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8e843191-5473-49b2-86d9-0fd5adc5d4e6)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/451ae608-3af9-429f-9218-059c804f4b71)

=> Done!

# Lab: SQL injection attack, listing the database contents on Oracle
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/026eb5d0-1b24-4507-99fb-50832e8da6e4)


![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c7b15fe3-b834-4434-a553-2b47a4790370)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/4b450a89-05a1-4549-9818-4a4ef8c8520a)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c354e569-78f9-4498-b36d-cb8b7f404244)

=> bảng: USERS_BEGDWU

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/ef40a0e3-81d5-4339-b314-0a53b4ed4cc3)

=> 3 cột: PASSWORD_SFNPOP, EMAIL, USERNAME_CUPRTF

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/eef7d584-d062-4338-a634-929c5513b552)

=> adminstrator:83b2fgbpyht4jc9xz3q7

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a6e2ad85-4a81-448b-9ee6-7edec3b4084b)

# Lab: SQL injection UNION attack, determining the number of columns returned by the query
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/69c5e11c-4d91-4c40-b68c-edfb6af75b4b)

=> 3 NULL

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f9e69be1-782e-49d6-aac9-2283d5c6df14)

# Lab: SQL injection UNION attack, finding a column containing text

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e44829cd-48bc-4c41-850f-1d31974c42c0)

=> 3 NULL là ổn

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e2a1307b-3682-4c22-beee-3cfcbedfdf12)

=> Thay cột null thứ 2 thành text

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/642f17f2-0b52-4a2e-90f8-05e75fa65032)

Sửa text thành PwGWsK để hoàn thành lab

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2adcbd3f-9550-4dbf-9ecd-4c892ae1ad10)

# Lab: SQL injection UNION attack, retrieving multiple values in a single column

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/dd071c59-8671-434d-8d4a-34b7c13ad300)

=> 2 cột nhưng chỉ cột thứ 2 mới hiển thị thông tin được

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d8c4df17-d203-4e9e-a8a0-a395e0b1f899)

=> administrator~mvklnugg43yna6tiyj46

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5e4c8798-652a-4b3c-a33b-2d8036efe337)

# Lab: SQL injection UNION attack, retrieving data from other tables

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/84c7f391-6285-4311-947a-3b62dd8ddb25)

=> 2 cột

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/23a0ef7e-9aa1-4a60-b124-2e0ad69e8a56)

=> adminstrator:fq83f8vlie7nx75njvh0

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fd237e6b-e473-4166-9cc2-33af4f8172bb)

# Lab: Blind SQL injection with conditional responses

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/00c10237-f48c-4dd6-ab1c-7e42f5e199b8)

Thay đổi TrackId

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b5b06029-3c91-4fe1-9df0-d536af6bd128)

Ta thấy xuất hiện thông báo "Welcome back!"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2ce389c2-1453-4612-b3b4-688ca4f42598)

Khi ta sửa lại thành "AND '1' =2" thì thông báo "Welcome back!" đã mất

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/930dbf40-420b-408d-8fa5-fd429cd65cc9)

Từ đây ta có thể thấy lỗi SQl mù sẽ hiển thị thông báo "Welcome back!" nếu truy vấn là đúng còn không hiển thị gì nếu truy vấn sai

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3fda6da3-2cc4-49e5-bb1d-6604b5e0c6a4)

=> tồn tại bảng users

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2d34abc4-f0e8-41ef-a84d-e676399de3f2)

=> tồn tại user tên là administrator

Tiếp theo sử dụng ```' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>3)='a``` để check độ dài của mật khẩu và sau nhiều lần thử thì mật khẩu có độ dài là 20

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b759587e-9b46-4a74-85c8-482b91566218)

Sau đó tiến hành thử các kí tự a-z và 0-9 với Burp Intruder

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3b941668-aaf3-44cf-9586-583d87ac0f4e)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/f3619f80-45af-41fb-9e0e-11555b806356)

Vào setting và chỉnh grep-match thành "Welcome back!"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2a4fef27-e3f6-4fb0-a067-5946b1356305)

Start attack!! 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/79fc1e33-3399-4180-a456-8eb74f70d7e7)

=> ký tự đầu tiên là 'n'

Tiếp tục với kí tự thứ 2 - "SUBSTRING(password,2,1)"

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c6d61fbf-02c9-4075-85b6-d827e6c7f0e0)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e39a9a98-4e1e-4fb0-a2c9-fd95718928b4)

=> ký tự thứ 2 là 'q' . Làm tương tự tiếp tục ta sẽ được chuỗi mật khẩu của administrator là nqmztubr0kxlnymny3qy

=)))))))) Hơi nông dân nhỉ! Hoặc ta có thể dùng Attack type: Cluster bomb

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/6d4c4263-b713-494d-a9cb-5dce802f4923)

Chỉnh "Payload set" 1 và 2

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c255dc90-31ef-4278-8d76-02e473e74e11)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/007eea7a-1390-4d92-8ee6-7603ae554031)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/0c045547-d32d-47d1-af23-267213b44f65)

=> cách này thì tool nó chạy 1 lượt cho luôn nhưng mà chạy hơi lâu . chắc do máy yếu =))

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5ff236ad-2b8a-432f-ada6-0c107803e549)

# Lab: Blind SQL injection with conditional errors
Khi ta thêm 1 dấu ' vào TrackingId thì thấy thông báo lỗi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/a1853497-68d7-4809-b995-b91d96309360)

Khi thêm 2 dấu ' thì thông báo lỗi biến mất

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8cf6ce7a-39eb-46d3-952b-c3f8c6a4d82f)

Khi ta chèn câu truy vấn  ``` '||(SELECT CASE WHEN (1=1) THEN TO_CHAR(1/0) ELSE '' END FROM dual)||'``` thì có thông báo lỗi 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e5856d9f-0693-4bac-aa48-49c1d4b3c5b2)

Nhưng khi sửa thành ```'||(SELECT CASE WHEN (1=2) THEN TO_CHAR(1/0) ELSE '' END FROM dual)||'``` thì thông báo lỗi biến mất => vậy nghĩa là nếu điều kiện của câu truy vấn là false thì sẽ không có thông báo gì và khi điều kiện của câu truy vấn là true sẽ báo lỗi "Internal Server Error". Dựa vào đây ta có thể tiến thành khai thác lỗi blind sqli

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/00f1542e-1bad-469e-b9c4-65ca23f62499)

=> Khi tôi chèn truy vấn ``` '||(SELECT CASE WHEN (username='administrator') THEN TO_CHAR(1/0) ELSE '' END FROM users)||'``` thì bị báo lỗi => có tồn tại username là administrator trong bảng users

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/59f8e2a6-17d4-4ed6-a9b4-1ff750a96736)

Tiếp tục chèn ```'||(SELECT CASE WHEN LENGTH(password)>1 THEN to_char(1/0) ELSE '' END FROM users WHERE username='administrator')||'``` để kiểm tra độ dài mật khẩu => Mật khẩu có độ dài là 20 ( có thể dùng Intruder của Burp Suite )

Tiếp đó ta dùng Intruder để check mật khẩu tương tự với lab trước đó (Set payload tương tự) 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/39f59689-2e29-4527-a310-16cf3d583122)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/457c06e1-40fd-467d-95c4-1103a1a81a1a)

=> administrator:vg6i94k6u7igary2sqwb

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/3e54f65e-0edd-4e78-b071-b0f2ec645404)

# Lab: Visible error-based SQL injection

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/2f031811-3e60-46b1-b4d4-4fdf875396fd)

Khi thêm 1 dấu ' vào TrackingId ta thấy màn hình báo lỗi

Sử dụng Burp Suite bắt request đó và thêm kí tự -- vào thì thấy hết lỗi

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/86ad5997-4a56-478d-94e2-d7d0751d84b7)

Sau AND phải là kiểu boolean không phải int
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/e20db578-0c05-4d92-8850-dcbec4ded1d0)

Thêm "1=CAST..." vào thì đã không còn bị báo lỗi nữa

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/1441708c-896a-466b-b609-c73fb155e109)

Lần này câu truy vấn không được hiển thị đầy đủ. có vẻ như có 1 giới hạn kí tự nào đó

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/b06298ec-a287-48e9-b4b5-b2cc689a6198)

Xóa đi giá trị của TrackingId thì bị báo lỗi có nhiều hơn 1 hàng 

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/c0b85e55-51d0-403c-8126-f8d7e994e986)

Thêm LIMIT 1 thì thấy thông báo user administrator không thể chuyển thành kiểu int

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/52711ea5-4649-42e7-86e5-ba5487ae0857)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/965b6851-c11e-490b-8960-f7959b9a1a2b)

=> administrator:9b6r9sltacyu82v8me03

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fd2d3628-3e55-4678-ae61-48f5312bbab5)

# Lab: Blind SQL injection with time delays
Thêm dấu ' vào TrackingId nhưng không báo lỗi gì

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/acb180e9-41d5-4c65-9b22-ec4236563749)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/fbcee8e3-c74a-428e-9554-1d1b7da7e9a5)

=> Done!

# Lab: SQL injection with filter bypass via XML encoding
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/09162052-c311-4c38-bc36-c24c24aea93d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5464fdb9-a588-400e-9742-ca1a01b263c7)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d934ee16-111d-4431-9891-82a0da03c305)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/124552eb-078b-4a9a-9b59-200f337aba88)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7b03d318-8115-448a-8b31-6febf245697b)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8892e982-519e-4905-88a2-905a5c9095b8)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/951dc109-e254-450f-b90f-dd4d91b4a3bf)



