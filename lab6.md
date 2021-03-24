# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจหลักการทำงานของไมโครคอนโทรเลอร์เมื่อทำการสร้าง wifi

## อุปกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. USB Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม

## ศึกษาข้อมูลเบื้องต้น
* wifi คือ
  * https://th.wikipedia.org/wiki/%E0%B9%84%E0%B8%A7%E0%B9%84%E0%B8%9F
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex06/src/main.cpp
  
## วิธีการทดลอง
1. ติดตั้งอุปกรณ์ตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112203735-69c3be00-8c45-11eb-9031-35a56fbac711.png)

2. รันคำสั่ง cd pattani เพื่อเข้าไปที่โฟลเดอร์ pattani
3. รันคำสั่ง cd 06_Wifi-AP-Web-Server เพื่อใช้โปรแกรม 06_Wifi-AP-Web-Server
4. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม (กำหนดชื่อ wifi คือ TUENG-ESP-WIFI และรหัส คือ choompol)

![image](https://user-images.githubusercontent.com/80880229/112203970-b4ddd100-8c45-11eb-9acb-2aa9a776ce2d.png)
![image](https://user-images.githubusercontent.com/80880229/112204219-01c1a780-8c46-11eb-8222-dd8fdfccc92a.png)

5. กำหนดชื่อและรหัสผ่านของ wifi

![image](https://user-images.githubusercontent.com/80880229/112204167-f2425e80-8c45-11eb-887a-4653e2c4a5e0.png)

6. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์
7. กดป่มสีดำ และปุ่ม set เพื่อให้ไมโครคอนโทรเลอร์รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80880229/112204382-2ddd2880-8c46-11eb-9489-4d4bbce028e9.png)

8. รันคำสั่ง pio device monitor เพื่อดูผลลัพธ์

## ผลการทดลอง
* เมื่อทำการรันคำส่ง pio device monitor

![image](https://user-images.githubusercontent.com/80880229/112204469-477e7000-8c46-11eb-9756-116365d0ee34.png)

## อภิปราย
* เมื่อใช้โทรศัพท์ทำการค้นหา wifi ได้ผลว่า พบ wifi ชื่อ TUENG-ESP-WIFI และสามารถเข้าใช้ wifi โดยใช้รหัสผ่านคือ choompol

## คำถาม
* เราสามารถเข้าไปทำการตั้งหรือเปลี่ยนชื่อและรหัส WIFI โดยรันคำสั่งใด
  * vi src/main.cpp
