# Share file Windows to Linux

### 1.	ทำการติดตั้ง Cifs 
~~~
$ sudo apt-get install cifs-utils
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20windows%E0%B9%84%E0%B8%9BLinux/1.png)
### 2.	สร้าง Folder สำหรับ mount ใน Linux
### สร้าง folder ทั้ง Linux และ windows
### 3.	ทำการ mount ระหว่าง windows และ Linux
~~~
$ sudo mount.cifs //10.25.10.81/ test1 /media/testmount -o user=Dell,iocharset=utf8,rw,file_mode=0777,dir_mode=0777
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20windows%E0%B9%84%E0%B8%9BLinux/3.png)
### 4.	ทำการ เช็ค mount 
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20windows%E0%B9%84%E0%B8%9BLinux/4.png)
### 5.	สร้าง file credentials ไว้ที่ /etc/ ( สร้างเพื่อทำการ Mount auto และเพื่อความปลอดภัย )
### ทำการใส่ User และ Password ของเครื่อง windows
~~~
$ sudo vi /etc/win-credentials
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20windows%E0%B9%84%E0%B8%9BLinux/5.png)
### 6.	ทำการเปลี่ยน chown
~~~
$ sudo chown root:root /etc/win-credential
~~~
### 7.	ทำการเปลี่ยน chmod
~~~
$ sudo chmod 600 /etc/win-credential
~~~
### 8.	ทำการกำหนดค่า fstab เมื่อมีการ restart จะทำการ mount ให้อัตโนมัติ
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20windows%E0%B9%84%E0%B8%9BLinux/6.png)
### ทำการ umount เพื่อ test fstab
~~~
$ sudo umount /media/test1	
~~~
### 10.	ทำการ test คำสั่ง mount auto
~~~
$ sudo mount -a
~~~
