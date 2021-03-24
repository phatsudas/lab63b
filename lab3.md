# การทดลองที่ 3 การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจหลักการทำงานของไมโครคอนโทรเลอร์เมื่อเป็นตัวส่งสัญญาณ output
3. เพื่อศึกษาการทำงานของของไมโครคอนโทรเลอร์เมื่อนำมาประยุกต์ใช้กับรีเลย์

## อุกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. USB Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม
5. Adapter
6. หลอด LED 2 หลอด
7. รีเลย์

## ศึกษาข้อมูลเบื้องต้น
* รีเลย์ คือ
  * https://th.wikipedia.org/wiki/%E0%B8%A3%E0%B8%B5%E0%B9%80%E0%B8%A5%E0%B8%A2%E0%B9%8C
* หลอดไฟ LED คือ
  * https://ra-light.com/th/%E0%B8%AB%E0%B8%A5%E0%B8%AD%E0%B8%94%E0%B9%84%E0%B8%9F-led-%E0%B8%84%E0%B8%B7%E0%B8%AD/
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* Output คือ
  * https://skjproject.wordpress.com/%E0%B8%AD%E0%B8%B8%E0%B8%9B%E0%B8%81%E0%B8%A3%E0%B8%93%E0%B9%8C%E0%B8%AD%E0%B8%B4%E0%B8%99%E0%B8%9E%E0%B8%B8%E0%B8%95input-%E0%B9%80%E0%B8%AD%E0%B9%89%E0%B8%B2%E0%B8%97%E0%B9%8C%E0%B8%9E%E0%B8%B8/%E0%B8%AA%E0%B8%B1%E0%B8%8D%E0%B8%8D%E0%B8%B2%E0%B8%93%E0%B8%97%E0%B8%B2%E0%B8%87%E0%B9%84%E0%B8%9F%E0%B8%9F%E0%B9%89%E0%B8%B2%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%AD%E0%B8%B4%E0%B8%99%E0%B8%9E%E0%B8%B8/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex03/src/main.cpp
  
## วิธีการทดลอง
ตอนที่ 1 
1. ติดตั้งอุปกรณ์ตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112192966-05e7c800-8c3a-11eb-8d21-8e4d1ae62dea.png)
![image](https://user-images.githubusercontent.com/80880229/112193098-2152d300-8c3a-11eb-8149-34c4bda6f0da.png)

2. รันคำสั่ง cd pattani เพื่อเข้าไปที่โฟลเดอร์ pattani
3. รันคำสั่ง cd 03_Output-Port เพื่อใช้โปรแกรม 03_Output-Port
4. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม

![image](https://user-images.githubusercontent.com/80880229/112194001-059bfc80-8c3b-11eb-9f42-795e01760678.png)

5. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์
6. กดป่มสีดำ และปุ่ม set เพื่อให้ไมโครคอนโทรเลอร์รับโปรแกรมใหม่เข้าไป

![image](https://user-images.githubusercontent.com/80880229/112194233-3c721280-8c3b-11eb-83cf-6961b8c857bf.png)

7. รันคำสั่ง pio device monitor เพื่อดผลลัพธ์

ตอนที่ 2

นำไมโครคอนโทรเลอร์ที่ทำการเขียนโปรแกรมตามการทดลองตอนที่ 1 และรีเลย์ มาติดตั้งตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112195348-709a0300-8c3c-11eb-8209-f9e4c0fd2983.png) 

## ผลการทดลอง
ตอนที่ 1
* เมื่อทำการรันคำส่ง pio device monitor

![image](https://user-images.githubusercontent.com/80880229/112194406-64fa0c80-8c3b-11eb-8b94-cdbaa8cec1bb.png)
![image](https://user-images.githubusercontent.com/80880229/112194466-78a57300-8c3b-11eb-8307-a0eb862d3d33.png)
![image](https://user-images.githubusercontent.com/80880229/112194503-83f89e80-8c3b-11eb-82e0-3c4609c37a50.png)

* เมื่อทำการ reset ไมโครคอนโทรเลอร์

![image](https://user-images.githubusercontent.com/80880229/112194562-970b6e80-8c3b-11eb-8620-1b1dcdaf336b.png)

ตอนที่ 2

![image](https://user-images.githubusercontent.com/80880229/112195552-ae972700-8c3c-11eb-9721-b370a13e9eb6.png)
![image](https://user-images.githubusercontent.com/80880229/112195598-bb1b7f80-8c3c-11eb-9ff0-32076cb5eb49.png)

## อภิปราย
* จากการทดลองตอนที่ 1 : ตัวแปร cnt จะทำการนับเพิ่มขึ้นทีละ 1 เมื่อ cnt เป็นจำนวนคี่ ไม่โครคอนโทรเลอร์จะส่งค่า HIGH หรือ 1 (binary) ไปที่พอต 0 และเมื่อตัวแปร cnt เป็นจำนวนคู่ ไม่โครคอนโทรเลอร์จะส่งค่า LOW หรือ 0 (binary) ไปที่พอต 0 ในกรณีที่พอต 0 เป็น 1 (binary) จะมีแรงดันส่งไปที่พอต 0 หรือเรียกว่าอยู่ในสถานะ ON ทำให้ LED สว่างขึ้น และในกรณีที่ในกรณีที่พอต 0 เป็น 0 (binary) จะไม่มีแรงดันส่งไปที่พอต 0 หรือเรียกว่าอยู่ในสถานะ OFF ทำให้ LED ดับลง เนื่องจากทำการ set ให้ตัวแปร cnt เพิ่มขึ้นทีละ 1 และ set ดีเลย์ไว้ทุกๆ 500 ms LED จึงสว่างและดับสลับกันไปทุกๆ 500 ms
* จากการทดลองตอนที่ 2 : เมื่อทำการต่อไมโครคอนโทรเลอร์กับรีเลย์และจ่ายไฟเลี้ยงให้กับรีเรย์แล้ว ไมโครคอนโทรเลอร์จะทำการควบคุมการทำงานของรีเลย์ให้เหมือนเป็นสวิตซ์เปิด-ปิด และจะทำการเปิด-ปิดสวิตซ์สลับกันทุกๆ 500 ms
  
## คำถาม
* จง
