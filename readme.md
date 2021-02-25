# สคริปต์สร้าง Minecraft Server: Java Edition

## ความต้องการของเซิร์ฟเวอร์ 
- Java runtime (JRE) เวอร์ชัน 8 ขึ้นไป
- หน่วยความจำ: 1 GB ขึ้นไป

> **หมายเหตุ** ความต้องการเหล่านี้มีไว้สำหรับเซิร์ฟเวอร์เท่านั้น คุณต้องจัดสรรทรัพยากรเพิ่มเติมให้กับระบบปฏิบัติการเอง!


## ระบบปฏิบัติการที่ต้องการติดตั้ง
- [Windows](#windows-10)
- [Linux](#linux-(Ubuntu,-Debian))



## ขั้นตอน

## Windows 10
1. สร้างโฟลเดอร์ไว้สำหรับเซิรฟ์เวอร์

2. ดาวน์โหลดไฟล์เซิร์ฟเวอร์

   https://www.minecraft.net/en-us/download/server/ 
   
   เลือก *Save As* ไปยังโฟลเดอร์ที่สร้าง

3. รันไฟล์ server.jar

   > **กรณีรันครั้งแรก**
   >
   > เซิร์ฟเวอร์จะรันได้แปป
   >
   > จำเป็นต้องเข้าไปแก้ไขไฟล์ eula.txt ก่อน
   >
   > แก้ไขจาก `eula=false` เป็น `eula=true`

### Linux (Ubuntu, Debian)

0. สร้างโฟลเดอร์ว่าง ๆ แล้วเข้าไปที่โฟลเดอร์นั้น

1. ดาวน์โหลดไฟล์ Minecraft Server.jar

   https://www.minecraft.net/en-us/download/server/ 
   
   *Save As* ไปที่โฟลเดอร์เซิร์ฟเวอร์

   หรือ ใช้คำสั่ง

   ```bat
   cd \
   copy a b
   ping 192.168.0.1
   ```

   ```console
   foo@bar:~$ whoami
   foo
   ```

   ```shell
   git clone http://github.com/garden/tree
   ```

   **ตัวอย่าง**

   ```shell
   $ wget https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar
   ```
   > ลิงค์ข้างต้นเป็นของ minecraft_server_1.16.5.jar

2. ติดตั้ง Java runtime

4. ติดตั้ง Screen Package *(สำหรับรัน Background Process)* (แนะนำ)

   ```shell
   $ sudo apt install screen
   ```

5. รันคำสั่งเพื่อสร้างเซิร์ฟเวอร์

   ```shell
   $ java [-Xmx<ขนาดแรมสูงสุดที่ต้องการ หน่วย M หรือ G>] [-Xms<ขนาดแรมเริ่มต้นที่ต้องการ หน่วย M หรือ G>] -jar <ชื่อไฟล์ที่ดาวน์โหลดจากขั้นตอนที่ 1>.jar nogui
   ```

   **ตัวอย่าง**
   
   ```shell
   $ java -Xmx1024M -Xms1024M -jar server.jar nogui
   ```

   - **กรณีรันครั้งแรก** 
      
      ต้องไปแก้ไขไฟล์ eula.txt เพื่อยอมรับข้อกำหนดของ Minecraft
      
      ```shell
      $ nano eula.txt
      ```
      
      แก้เป็น
      eula = true
      แล้วกด `Ctrl + S` เพื่อบันทึกและ `Ctrl + X` เพื่อกลับสู่ Shell Script

   - **กรณีรันครั้งถัดไป**

   - **หยุดรันเซิร์ฟเวอร์**
      กด `Ctrl + C `

6. รัน Backgroud Process

    Create New Screen

    ```shell
    screen -s [SCREEN_NAME]
    ```

    ```shell
    screen -list // For List of Screen which you can switch
    screen -r [SCREEN_NUMBER]
    java -Xmx1024M -Xms1024M -jar server.js nogui
    ```
    and switch back to main screen
    ```shell
    Ctrl + A + D 
    ```

    ```shell
    apt install openjdk-8-jre-headless curl screen nano bash grep
    ```

7. Open External Connection Port 25565

### Linux (CentOS)

> #### The quarterly results look great!
> 
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.


## Checking Connection Port

https://portchecker.co/

external-ip: [ipv4]

port: 25565

## TL; DR
```shell
$ sudo apt update
$ sudo apt upgrade
$ sudo install screen
```

## References
- https://minecraft.gamepedia.com/Server/Requirements/Dedicated
- http://www.dla.go.th/upload/document/type14/2017/12/19204_1_1512617352720.pdf?time=1527460904987

## VS Code Markdown Preview
```
Ctrl + Shift + V
```


