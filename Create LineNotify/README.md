# คูมือ Line Notify
### 1.  https://notify-bot.line.me/th/  เข้าเว็บไซต์เพื่อ Login เข้า Line Notify
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/1.png)
### 2.	 ทำการ Login เข้า Line Notify
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/2.png)
### 3.	ทำการเข้าไปใน My Page
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/3.png)
### 4.	ทำการ Generate token ของ LineNotify
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/4.png)
### 5.	ขั้นตอนที่ 1 ทำการตั้งชื่อ Line Notify
### ขั้นตอนที่ 2 ทำการเลือก Group Line ที่ต้องการจะ connect กับ Line Notify
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/5.png)
### 6.	Line จะทำการ Generate Token Code ขึ้นมาให้ ทำการ copy Token Code
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/6.png)
### 7.	Line Notify จะทำการ Connect ระหว่าง Line Notify กับ Group Line 
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/7.png)
### 8.	ขั้นตอนที่ 1 Curl คือเครื่องมือที่ใช้ยิงเข้าไปยัง server โดยผ่าน Protocol ต่างๆที่เราต้องการจะใช้
###     ขั้นตอนที่ 2 Token Code ที่ทำการ connect Token ระหว่าง Line Notify และ Group Line
###     ขั้นตอนที่ 3 Message Box เป็นคำสั่งที่ต้องการให้แจ้งเตือนใน Group Line
###     ขั้นตอนที่ 4 เป็น Server ของ Line Notify ที่ทำการยิงขึ้นไป
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/8.1.png)
### 9.	ทำการ Save Line Notify ที่ทำเสร็จแล้วเป็น Batch file หรือ .bat เพื่อทำการ Run ผ่าน Command Prompt
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/9.png)
### 10.	ทำการ Add Line Notify เข้า Group Line ที่ทำการ Connect Token ไว้
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/10.png)
### 11.	เมื่อทำการ Run Batch file ที่ทำการสร้างขึ้น Curl จะทำการส่ง Message ไปยัง Server ของ Line Notify และทำการส่ง Massage นั้นกลับมาที่ Group Line ที่ทำการ Connect Token 
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Create%20LineNotify/11.png)
