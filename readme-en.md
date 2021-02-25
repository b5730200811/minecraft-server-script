# Minecraft Server Script

## Server requirements
- A Java runtime (JRE), version 8 or higher. JDK contains JRE
- OS: Windows or Linux
- Memory: >= 3 GB

> Note that these requirements are for the server only you will need to allocate more resources to the OS!

## Steps

### Linux (Ubuntu, Debian)

0. Create New Directory And Change To This
1. Download Minecraft Server.jar

   https://www.minecraft.net/en-us/download/server/ 

   *Save As* to your directory server

   OR 

   Using Command

   > Copy Link Address of Server Download 
   
   ```
   wget  [Link Address]
   ```

   **Example**

   ```
   wget https://launcher.mojang.com/v1/objects/1b557e7b033b583cd9f66746b7a9ab1ec1673ced/server.jar
   ```
   > This link is minecraft_server1.16.5.jar


2. Install JAVA (JRE) version >= 8
4. Install Screen Package *(for backgroud running)* (optional)

   ```
   sudo apt install screen
   ```

5. Run command to create server

   ```
   java -Xmx[MB_OF_MEMORY]] [-Xms[MB_OF_MEMORY]] -jar [SERVER_NAME].jar nogui
   ```

   **Example**
   
   ```
   java -Xmx1024M -Xms1024M -jar server.jar nogui
   ```

   - First time running

        need edit eula.txt for accept assignment and bababa..
     
   - Next-time running

   - Kill Process
        ```Ctrl + C ``` for kill

6. Run Backgroud Process

    Create New Screen

    ```
    screen -s [SCREEN_NAME]
    ```

    ```
    screen -list // For List of Screen which you can switch
    screen -r [SCREEN_NUMBER]
    java -Xmx1024M -Xms1024M -jar server.js nogui
    ```
    and switch back to main screen
    ```
    Ctrl + A + D 
    ```

    ```
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

## References
- https://minecraft.gamepedia.com/Server/Requirements/Dedicated

## vscode Markdown Preview
```
Ctrl + Shift + V
```


