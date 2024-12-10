# sensor
การใช้ esp32 เพื่อใช้ในการรับค่าอนาล็อกมาจากเซ็นเซอร์วัดความชื่นในดินจำนวน 2 ตัวแล้วทำการส่งข้อมูลขึ้น Google Sheet และ Node-red แล้วยังสั้งการให้บอร์ด esp32 เข้าสู้โหมด Sleep เพื่อประหยัดพลังงาน

## <a name="content"></a> สารบัญ  
1. [อุปกรที่ใช้ทั้งหมด](#อุปกร)
2. [ไลบรารี่ที่ใช้ในโค้ดทั้งหมด](#libra)
3. [วงจรในการต่อใช้งาน](#ต่ออุปกร)
4. [ลักษการทำงาน(โฟลว์ชาร์ต)](โฟลว์ชาร์ต)

<br/>

## <a name="อุปกร"></a> อุปกรที่ใช้ทั้งหมด
1. บอร์ด esp32 x 10
2. เซนเซอร์วัดความชื่นในดิน x 20
3. แบทเตอร์รี่ 12 V x 10
4. โมดูลแปลงแรงดัน DC 12V เป็น usb 5V x 10
5. หน้าจอ LCD x 10
6. กล่องที่นำไปติดตั้งบอร์ด esp32 x 10
7. กล่องกันน้ำ(กล่องเก็บรองเท้า) x 10
8. ขาตั้งเพื่อมใช้ในการยึดกล่อง x 10

[กลับสู่สารบัญ](#content)
<br/>

## <a name="libra"></a> ไลบรารี่ที่ใช้ในโค้ดทั้งหมด
1. Wire : ใช้ในการวนลูป
2. WiFi : ใช้ในการเชื่อมต่อ WiFi
3. PubSubClient : ใช้ในการรับส่งข้อมูลด้วยโปรโตคอล MQTT
4. HTTPClient : ใช้ในการส่งข้อมูลขึ้น Google Sheet
5. LiquidCrystal : ใช้ในการแสดงข้อความขึ้น LCD
6. esp_sleep : ใช้ในการให้บอร์ด ESP32 สามารถเข้าสู้โหมด Sleep ได้

[กลับสู่สารบัญ](#content)

<br/>

## <a name="ต่ออุปกร"></a> วงจรในการต่อใช้งาน
การต่อวงจรในการใช้งานจะนำ esp32 ต่อเข้ากับเซนเซอร์วัดค่าในดิน 2 ตัวและต่อกับหน้าจอLCD ซึ่งการต่อเซนเซอร์วัดความชื่นในดินจะทำการต่อที่ขา 34 และ 36
<p align="center">
<img src=https://github.com/user-attachments/assets/a1acf8f4-98cc-477c-8488-59b5196341ee>
  
[กลับสู่สารบัญ](#content)
<br/>

## <a name="โฟลว์ชาร์ต"></a> ลักษการทำงาน(โฟลว์ชาร์ต)
<p align="center">
<img src=https://github.com/user-attachments/assets/29281371-dafa-43ee-8580-880e2b413e7a>

<br/>
