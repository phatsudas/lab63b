# การทดลองที่ 2 การเขียนโปรแกรมค้นหาไวไฟ

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจหลักการทำงานของไมโครคอนโทรเลอร์เมื่อทำการแสกนหา wifi

## อุกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม

## ศึกษาข้อมูลเบื้องต้น
* wifi คือ
  * https://th.wikipedia.org/wiki/%E0%B9%84%E0%B8%A7%E0%B9%84%E0%B8%9F
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex02/src/main.cpp
  
## วิธีการทดลอง
1. ติดตั้งอุปกรณ์ตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112186010-50197b00-8c33-11eb-9379-9357a75876c7.png)


2. รันคำสั่ง cd 02_Scan-wifi เพื่อใช้โปรแกรม 02_Scan-wifi
3. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม

![image](https://user-images.githubusercontent.com/80880229/112186303-91aa2600-8c33-11eb-9f0b-7b25a6529258.png)
![image](https://user-images.githubusercontent.com/80880229/112186441-b8685c80-8c33-11eb-8d35-16f12e7d83b7.png)

4. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์
5. กดป่มสีดำ และปุ่ม set เพื่อให้ไมโครคอนโทรเลอร์รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80880229/112187226-7e4b8a80-8c34-11eb-9caa-64f1d7d645ae.png)

6. รันคำสั่ง pio device monitor เพื่อดผลลัพธ์

## ผลการทดลอง
* เมื่อทำการรันคำส่ง pio device monitor

![image](https://user-images.githubusercontent.com/80880229/112187441-b05cec80-8c34-11eb-9cd8-4068a98aeb75.png)
![image](https://user-images.githubusercontent.com/80880229/112187563-c8cd0700-8c34-11eb-947b-600ad85490ad.png)

* เมื่อทำการ reset ไมโครคอนโทรเลอร์

![image](https://user-images.githubusercontent.com/80880229/112187633-da161380-8c34-11eb-811c-0aab2f6b9a9f.png)

## อภิปราย
* เมื่อไมโครคอนโทรเลอร์ทำการแสกนเจอไวไฟ บนคอมพิวเตอร์จะแสดงผลว่า ไมโครคอนโทรเลอร์เจอไวไฟกี่ตัว ไวไฟแต่ละตัวชื่ออะไรบ้าง และจะแสดงผลใหม่ทุกครั้งเมื่อเจอสัญญาณไวไฟใหม่ หรือมีการเปลี่ยนแปลงของสัญญาณที่พบ การแสกนเจอไวไฟขึ้นอยู่กับความแรงของสัญญาณไวไฟนั้นๆ เมื่อทำการกดปุ่ม reset ไมโครคอนโทรเลอร์ก็จำทำการแสกนหาสัญญาณไวไฟใหม่

## คำถาม
* จง
