# คู่มือการ GetIp และแจ้งเตือนผ่าน Linenotify
### 1.ทำการสร้างไฟล์เป็น .sh
### 2.ทำการ chmod เป็น 775
### 3.ทำการ Set ค่าของ file .sh
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/GetIp_Linenoty/1.png)
#### 3.1.	ทำการ set time
#### -	time=$(date +%T)
#### 3.2.	ทำการ set date
#### -	datetime=$(date +'%Y%m%d')
#### 3.3.	ทำการ กำหนดค่า Ip
#### -	ip=$(netstat -anpt |grep 22 |grep ESTABLISHED | awk '{ print $5 }' | cut -d: -f1 | sort -u)
#### 3.4.	ใช้ curl เพื่อยิง Token ไปยัง Linenotify
#### 3.5.	ใส่ Token ที่ทำการ gen จาก Linenotify
#### 3.6.	ใส่ message เพื่อทำการแจ้งเตือน
#### 3.7.	ทำการเรียกใช้ ip , date , time ที่ทำการ set ไว้
### 4.ทำการเข้าไป set profile ใน home
~~~
Vi .profile
~~~
### 5.ทำการเรียกใช้ Shell Script ที่ได้ทำไว้
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/GetIp_Linenoty/2.png)
### 6.เมื่อทำการ Run จะมีการแจ้งเตือนผ่าน Linenotify
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/GetIp_Linenoty/3.png)
