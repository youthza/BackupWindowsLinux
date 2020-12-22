# Create Keygen 
## เพื่อส่งไฟล์จาก Linux to Linux โดยไม่ติด Password

### 1.	ทำการ create key-gen
~~~
~$ ssh-keygen
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20Linux%E0%B9%84%E0%B8%9BLinux/1.png)
### เช็คว่าทำการสร้าง keygen แล้ว
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20Linux%E0%B9%84%E0%B8%9BLinux/1.1.png)
### 2.	ทำการ copy keygen เพื่อส่งไปยังเครื่องปลายทาง
~~~
~$ ssh-copy-id USER@HOST
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20Linux%E0%B9%84%E0%B8%9BLinux/2.png)
### เช็ค key ที่เครื่องปลายทาง
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20Linux%E0%B9%84%E0%B8%9BLinux/2-1.png)
### 3.	ทำการทดลองส่งข้อมูลไปยังเครื่องปลายทาง
~~~
~$ scp -i .ssh/id_rsa SOURCE_PATH USER@HOST:DESTINATION_PATH
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/share%20Linux%E0%B9%84%E0%B8%9BLinux/3.png)

