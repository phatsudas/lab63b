# การทดลองที่ 5 เรื่อง การเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจหลักการทำงานของไมโครคอนโทรเลอร์เมื่อทำการเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์

## อุปกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. USB Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม

## ศึกษาข้อมูลเบื้องต้น
* Web Server คือ
  * https://techforteam.com/blog/web-server/
* Web Browser คือ
  * https://www.thaibusinesssearch.com/marketing/web-browser/
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex05/src/main.cpp
  
## วิธีการทดลอง
1. ติดตั้งอุปกรณ์ตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112354701-86243100-8cff-11eb-9406-88f276c16e56.png)

2. รันคำสั่ง cd pattani เพื่อเข้าไปที่โฟลเดอร์ pattani
3. รันคำสั่ง cd 05_Wifi-Web-Server เพื่อใช้โปรแกรม 05_Wifi-Web-Server
4. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม

![image](https://user-images.githubusercontent.com/80880229/112354937-c388be80-8cff-11eb-9985-b0f1a6d82c49.png)
![image](https://user-images.githubusercontent.com/80880229/112355043-def3c980-8cff-11eb-9aba-aff7639531c8.png)

5. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์
6. กดป่มสีดำ และปุ่ม set เพื่อให้ไมโครคอนโทรเลอร์รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80880229/112355531-5590c700-8d00-11eb-836b-d233c8577aed.png)

## ผลการทดลอง
![image](https://user-images.githubusercontent.com/80880229/112355424-34c87180-8d00-11eb-8e8f-3996febdf03b.png)

## อภิปราย
* โปรแกรมนี้เนื่องจากต้องทำการต่อ Wifi จึงต้องทำการใส่ชื่อและรหัสของ Wifiที่จะใช้งาน และเนื่องจาก set ให้ตัวแปร cnt เพิ่มทีละ 1 ในแต่ละครั้งเมื่อ Web server มีการเชื่อมต่อ จะมีการแสดงผลว่า "Hello 1" โดยตัวเลขหลังคำว่า "Hello" จะเพิ่มขึ้นทีละ 1 ตามจำนวนครั้งที่ถูกเชื่อมต่อ 

## คำถาม
* จงยกตัวอย่าง Web Browser มา 2 ตัวอย่าง
  * Google Chrome
  * Safari

