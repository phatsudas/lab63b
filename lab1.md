# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจวิธีการใช้งานและวิธีการทำงานของไมโครคอนโทรเลอร์

## อุกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม

## ศึกษาข้อมูลเบื้องต้น
* ไมโครคอนโทรเลอร์คือ
  * https://th.wikipedia.org/wiki/%E0%B9%84%E0%B8%A1%E0%B9%82%E0%B8%84%E0%B8%A3%E0%B8%84%E0%B8%AD%E0%B8%99%E0%B9%82%E0%B8%97%E0%B8%A3%E0%B8%A5%E0%B9%80%E0%B8%A5%E0%B8%AD%E0%B8%A3%E0%B9%8C
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex01/src/main.cpp
  
## วิธีการทดลอง
1. ติดตั้งอุปกรณ์ตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112181077-ad5efd80-8c2e-11eb-953c-3aede21064e0.png)
![image](https://user-images.githubusercontent.com/80880229/112181371-f8791080-8c2e-11eb-829a-b508ed763684.png)

2. รันคำสั่ง cd pattani เพื่อเข้าไปที่โฟลเดอร์ pattani
3. รันคำสั่ง cd 01_Serial-Monitor เพื่อใช้โปรแกรม 01_Serial-Monitor
4. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม

![image](https://user-images.githubusercontent.com/80880229/112182271-b8665d80-8c2f-11eb-8543-62be30a7e54a.png)

5. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์
6. กดป่มสีดำ และปุ่ม set เพื่อให้ไมโครคอนโทรเลอร์รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80880229/112182617-054a3400-8c30-11eb-8fde-a662d14c320c.png)

7. รันคำสั่ง pio device monitor เพื่อดูผลลัพธ์

## ผลการทดลอง
* เมื่อทำการรันคำส่ง pio device monitor

![image](https://user-images.githubusercontent.com/80880229/112183501-e5674000-8c30-11eb-97d6-b2ca4674bcd1.png)

* เมื่อทำการ reset ไมโครคอนโทรเลอร์

![image](https://user-images.githubusercontent.com/80880229/112183704-16477500-8c31-11eb-87df-53ea74cf4857.png)

## อภิปราย
* เมื่อทำการรันคำส่ง pio device monitor ตัวแปร cnt จะนับเพิ่มขึ้นทีละ 1 โดยเริ่มนับตั้งแต่ 0 และแสดงผลทุกๆ 1 วินาที เมื่อทำการกดปุ่ม reset ที่ไมโครคอนโทรเลอร์ ตัวแปร cnt จะทำการเริ่มนับใหม่ ตั้งแต่ 0 เป็นต้นไป

## คำถาม
* จง
