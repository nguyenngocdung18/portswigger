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













# Lab: SQL injection with filter bypass via XML encoding
![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/09162052-c311-4c38-bc36-c24c24aea93d)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/5464fdb9-a588-400e-9742-ca1a01b263c7)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/d934ee16-111d-4431-9891-82a0da03c305)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/124552eb-078b-4a9a-9b59-200f337aba88)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/7b03d318-8115-448a-8b31-6febf245697b)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/8892e982-519e-4905-88a2-905a5c9095b8)

![image](https://github.com/nguyenngocdung18/portswigger/assets/134156226/951dc109-e254-450f-b90f-dd4d91b4a3bf)



