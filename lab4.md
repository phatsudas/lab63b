# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล

## วัตถุประสงค์ของการทดลอง
1. เพื่อศึกษาวิธีการเขียนโปรแกรมลงบนไมโครคอนโทรเลอร์ 
2. เพื่อเข้าใจหลักการทำงานของไมโครคอนโทรเลอร์เมื่อเป็นตัวรับสัญญาณ input
3. เพื่อศึกษาการทำงานของไมโครคอนโทรเลอร์เมื่อนำมาประยุกต์ใช้กับ เซนเซอร์รับแสง (LDR)

## อุปกรณ์ที่ใช้ 
1. ไมโครคอนโทรเลอร์ (ESP-01)
2. USB
3. USB Serial
4. คอมพิวเตอร์ที่ใช้เขียนโปรแกรม
5. Adapter
6. หลอด LED 1 หลอด
7. เซนเซอร์รับแสง (LDR)
8. ตัวต้านทาน

## ศึกษาข้อมูลเบื้องต้น
* เซนเซอร์รับแสง (LDR) คือ
  * https://thiti.dev/blog/6796/
* input คือ
  * https://skjproject.wordpress.com/%E0%B8%AD%E0%B8%B8%E0%B8%9B%E0%B8%81%E0%B8%A3%E0%B8%93%E0%B9%8C%E0%B8%AD%E0%B8%B4%E0%B8%99%E0%B8%9E%E0%B8%B8%E0%B8%95input-%E0%B9%80%E0%B8%AD%E0%B9%89%E0%B8%B2%E0%B8%97%E0%B9%8C%E0%B8%9E%E0%B8%B8/%E0%B8%AA%E0%B8%B1%E0%B8%8D%E0%B8%8D%E0%B8%B2%E0%B8%93%E0%B8%97%E0%B8%B2%E0%B8%87%E0%B9%84%E0%B8%9F%E0%B8%9F%E0%B9%89%E0%B8%B2%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%AD%E0%B8%B4%E0%B8%99%E0%B8%9E%E0%B8%B8/
* ข้อมูลไมโครคอนโทรเลอร์
  * https://platformio.org/
* ข้อมูล source code
  * https://github.com/choompol-boonmee/iotset1/blob/main/examples/ex04/src/main.cpp
  
## วิธีการทดลอง
ตอนที่ 1 
1. ติดตั้งอุปกรณ์ตามรูปภาพ (ต่อ LED ที่ port 0,2 ของ Adapter)

![image](https://user-images.githubusercontent.com/80880229/112199874-32531280-8c41-11eb-9642-9446dd1870cb.png)

2. รันคำสั่ง cd pattani เพื่อเข้าไปที่โฟลเดอร์ pattani
3. รันคำสั่ง cd 04_Input-Port เพื่อใช้โปรแกรม 04_Input-Port
4. รันคำสั่ง vi src/main.cpp เพื่อดูตัวอย่างโปรแกรม (set ให้ port 0 เป็น input และ port 2 เป็น output)

![image](https://user-images.githubusercontent.com/80880229/112199969-50b90e00-8c41-11eb-8397-bd5c30f3f729.png)

5. รันคำสั่ง pio run -t upload เพื่อ upload โปรแกรมไปยังไมโครคอนโทรเลอร์

![image](https://user-images.githubusercontent.com/80880229/112200176-8c53d800-8c41-11eb-8545-0f4a612f2ca1.png)

6. รันคำสั่ง pio device monitor เพื่อดูผลลัพธ์

ตอนที่ 2

นำเซนเซอร์รับแสง (LDR) และตัวต้านทานมาติดตั้งตามรูปภาพ

![image](https://user-images.githubusercontent.com/80880229/112201176-91fded80-8c42-11eb-87c1-10c3d886ebb6.png)

## ผลการทดลอง
ตอนที่ 1
* เมื่อทำการรันคำส่ง pio device monitor

![image](https://user-images.githubusercontent.com/80880229/112200350-bad1b300-8c41-11eb-89d7-43ab2d795a31.png)
![image](https://user-images.githubusercontent.com/80880229/112200516-e5237080-8c41-11eb-85b7-b12531624072.png)
![image](https://user-images.githubusercontent.com/80880229/112200628-ff5d4e80-8c41-11eb-9740-d5fa52d00bd3.png)

* เมื่อทำการกดพอต 0

![image](https://user-images.githubusercontent.com/80880229/112200760-2287fe00-8c42-11eb-938c-8b045407e715.png)

ตอนที่ 2

![image](https://user-images.githubusercontent.com/80880229/112201347-bc4fab00-8c42-11eb-916d-9261294a5807.png)
![image](https://user-images.githubusercontent.com/80880229/112201411-cd002100-8c42-11eb-9009-1ba1ede99539.png)


## อภิปราย
* จากการทดลองตอนที่ 1 : เมื่อได้รับสัญญาณ input จาก port 0 เป็น 1 ไมโครคอนโทรเลอร์จะทำการส่งค่า LOW หรือ 0 (binary) ไปที่ port 2 ในกรณีนี้เมื่อ port 2 เป็น 0 จะไม่มีแรงดัน หรืออยู่ในสภาวะ OFF ไฟก็จะดับ แต่เมื่อได้รับสัญญาณ input จาก port 0 เป็น 0 ไมโครคอนโทรเลอร์จะทำการส่งค่า HIGH หรือ 1 (binary) ไปที่ port 2 ในกรณีนี้เมื่อ port 2 เป็น 1 จะมีแรงดัน หรืออยู่ในสภาวะ ON ไฟก็จะสว่าง
* จากการทดลองตอนที่ 2 : เมื่อไม่บังแสง port 0 จะอ่านค่าได้เป็น 0 ไมโครคอนโทรเลอร์จะทำการส่งค่า HIGH หรือ 1 (binary) ไปที่ port 2 ในกรณีนี้เมื่อ port 2 เป็น 1 จะมีแรงดัน หรืออยู่ในสภาวะ ON ไฟก็จะสว่าง เมื่อทำการบังแสง port 0 จะอ่านค่าได้เป็น 1 ไมโครคอนโทรเลอร์จะทำการส่งค่า LOW หรือ 0 (binary) ไปที่ port 2 ในกรณีนี้เมื่อ port 2 เป็น 0 จะไม่มีแรงดัน หรืออยู่ในสภาวะ OFF ไฟก็จะดับ
  
## คำถาม
* ยกตัวอย่าอุปกรณ์ input มา 2 ตัวอย่าง
  * โมดูลตรวจจับความเคลื่อนไหว
  * ตัวตรวจจับแสงสะท้อนสีแดง
