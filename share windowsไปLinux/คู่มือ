 # คู่มือ Share Windows ไป Linux
## 1.	ทำการติดตั้ง Cifs 
~~~
sudo apt-get install cifs-utils
~~~
![installCifs-Utils](https://user-images.githubusercontent.com/72594670/101602041-0b752580-3a30-11eb-847b-29019c5208f3.png)

## 2.	สร้าง Folder สำหรับ mount ใน Linux ต้องสร้างทั้งใน Linux และ Windows
![Folder](https://user-images.githubusercontent.com/72594670/101602099-2778c700-3a30-11eb-8e7a-67147ec02d02.png)

## 3.	ทำการ mount ระหว่าง windows และ Linux
~~~
sudo mount.cifs "Path Windows" "Path Linux" -o user= Namewindows ,iocharset=utf8,rw,file_mode=0777,dir_mode=0777
~~~
![Mount](https://user-images.githubusercontent.com/72594670/101602167-4414ff00-3a30-11eb-9be2-847f2c9a43df.png)

## 4.	ทำการ เช็ค mount 
~~~
sudo /media/testmount 
~~~
![CheckMount](https://user-images.githubusercontent.com/72594670/101602364-97874d00-3a30-11eb-81b7-187c401988a8.png)

## 5.	สร้าง file credentials ไว้ที่ /etc/ ( สร้างเพื่อทำการ Mount auto และเพื่อความปลอดภัย )
~~~
sudo vi /etc/win-credentials
~~~
![Credential](https://user-images.githubusercontent.com/72594670/101602431-b2f25800-3a30-11eb-91c1-7aab4ad412da.png)

## 6.	ทำการเปลี่ยน chown win-credential
~~~
sudo chown root:root /etc/win-credential
~~~
## 7.	ทำการเปลี่ยน chmod win-credential
~~~
sudo chmod 600 /etc/win-credential
~~~
## 8.	ทำการกำหนดค่า fstab 
~~~
//"Path Windows" "Path Linux" cifs uid=0,credentials=/etc/win-credentials,file_mode=0755,dir_mode=0755 0 0
~~~
![AutoMount](https://user-images.githubusercontent.com/72594670/101602511-d3221700-3a30-11eb-8730-64c833d74fae.png)

## 9.	ทำการ umount
~~~
sudo umount "Path Linux"
~~~
## 10.	ทำการ test คำสั่ง mount auto
~~~
sudo mount -a
~~~
