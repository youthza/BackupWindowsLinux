# Share file Linux to Windows

### 1.	ทำการ install samba
~~~
$ sudo apt-get install samba samba-common
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Share_LinuxtoWindows/1.png)
### 2.	ทำการสร้าง folder ที่ต้องการจะ share
~~~
$ sudo mkdir /mnt/winshare
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Share_LinuxtoWindows/2.png)
### 3.	เปลี่ยนความเป็นเจ้าของเพื่อให้ทุกคนเข้าใช้งานได้
~~~
$ sudo chown nobody:nogroup /mnt/winshare/
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Share_LinuxtoWindows/3.png)
### 4.	ทำการสำรองข้อมูลของ samba
~~~
$ sudo cp /etc/samba/smb.conf /etc/samba/smb.conf.org
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Share_LinuxtoWindows/4.png)
### 5.	ทำการกำหนดค่าของ samba
~~~
$ sudo vi /etc/samba/smb.conf
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/Share_LinuxtoWindows/5.png)
### 6.	ทำการ restart smbd service
~~~
$ sudo service smbd restart
~~~
### 7.  ทำการเช็ค services
~~~
$ sudo netstat
~~~
