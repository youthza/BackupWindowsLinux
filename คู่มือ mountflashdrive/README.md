# MountFlashDrive auto

### 1.	ทำการเสียบ flashdrive และเช็คว่า flashdrive เข้าเครื่องรึยัง
~~~
Sudo fdisk -l 
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/1.png)
### 2.	ทำการเช็ค device ของตัวที่เสียบเพื่อเรียกมาใช้
~~~
Sudo dmesg
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/2.png)
### 3.	ทำการเช็ค uuid ของ flashdrive
~~~
Sudo blkid
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/3.png)
### 4.	ทำการติดตั้ง ntfs-3g
~~~
Sudo apt-get install ntfs-3g
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/4.png)
### 5.	ทำการสร้าง folder เพื่อ mount กับ flashdrive
~~~
Sudo mkdir /media/Flashdrive
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/5.png)
### 6.	ทำการ mount flashdrive กับ folder ที่ทำการสร้างขึ้นมา
~~~
sudo mount /dev/sda1 /media/Flashdrive/
~~~
 ![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/6.png)
### 7.	ทำการ chmod folder ให้เป็น 775
~~~
Sudo chmod 755 /media/Flashdrive/
~~~
### 8.	ทำการตั้งค่าให้เป็น Auto mount โดยการตั้งค่าใน fstab
~~~
Sudo vi /etc/fstab
~~~
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/7.png)
### 9.	จากนั้นทำการ Reboot เครื่องใหม่อีกครั้ง
~~~
Sudo reboot
~~~
### 10.	เมื่อทำการเปิดเครื่องมา จะทำการ mount auto ให้
![Editor preferences pane](https://github.com/youthza/BackupWindowsLinux/blob/main/%E0%B8%84%E0%B8%B9%E0%B9%88%E0%B8%A1%E0%B8%B7%E0%B8%AD%20mountflashdrive/8.png)
### 11.	ถ้า Reboot แล้วเครื่องไม่ mount auto ให้ใช้คำสั่ง mount -a
~~~
Sudo mount -a
~~~
