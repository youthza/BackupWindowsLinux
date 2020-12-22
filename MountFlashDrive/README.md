# MountFlashDrive auto

### 1.	ทำการเสียบ flashdrive และเช็คว่า flashdrive เข้าเครื่องรึยัง
~~~
$ sudo fdisk -l 
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/1.png)
### 2.	ทำการเช็ค device ของตัวที่เสียบเพื่อเรียกมาใช้
~~~
$ sudo dmesg
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/2.png)
### 3.	ทำการเช็ค uuid ของ flashdrive
~~~
$ sudo blkid
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/3.png)
### 4.	ทำการติดตั้ง ntfs-3g
~~~
$ sudo apt-get install ntfs-3g
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/4.png)
### 5.	ทำการสร้าง folder เพื่อ mount กับ flashdrive
~~~
$ sudo mkdir /media/Flashdrive
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/5.png)
### 6.	ทำการ mount flashdrive กับ folder ที่ทำการสร้างขึ้นมา
~~~
$ sudo mount /dev/sda1 /media/Flashdrive/
~~~
 ![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/6.png)
### 7.	ทำการ chmod folder ให้เป็น 775
~~~
$ sudo chmod 755 /media/Flashdrive/
~~~
### 8.	ทำการตั้งค่าให้เป็น Auto mount โดยการตั้งค่าใน fstab
~~~
$ sudo vi /etc/fstab
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/7.png)
### 9.	จากนั้นทำการ Reboot เครื่องใหม่อีกครั้ง
~~~
$ sudo reboot
~~~
### 10.	เมื่อทำการเปิดเครื่องมา จะทำการ mount auto ให้
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/MountFlashDrive/8.png)
### 11.	ถ้า Reboot แล้วเครื่องไม่ mount auto ให้ใช้คำสั่ง mount -a
~~~
$ sudo mount -a
~~~
