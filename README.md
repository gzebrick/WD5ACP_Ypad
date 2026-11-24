<img width="700" height="350" alt="Screenshot 2026-11-14 091755" src="https://github.com/user-attachments/assets/299b5bc6-7b8d-497a-b6ab-5d72f7e14144" />

<img width="500" height="500" alt="IMG_1381" src="https://github.com/user-attachments/assets/24ca5d0d-e7da-4b32-b3a1-7c373842da07" />

<img width="350" height="400" alt="IMG_1382" src="https://github.com/user-attachments/assets/7ead76ee-9734-4bf0-8156-c6e82b62ae51" />

<img width="640" height="626" alt="CYDIO" src="https://github.com/user-attachments/assets/02beceb1-adca-4edd-969f-80e852f9e7db" />



# WD5ACP_Ypad
CYD program for touchpad macro buttons using RS232 connection for Yaesu radios

For the 991 menu item should be configured as follows:

028  GPS/232C Select = RS232C
029 232C Rate = 38400bps (recommended, but make sure the ypad host baud rate setting matches).
030 232 TOT  = 10ms  

3D case files if interested...
https://www.tinkercad.com/things/4W4bnj26UHi-cydvertcase-v2

i  recommend this one, since it matches the I/O code for the TTL port plus the display. There are lots of CYDs out there, with some variation on what ports are exposed and the I/O ports for the display, LED and touch.
 
https://a.co/d/018AxG0h
 
The TTL board just plugs into the 4-conductor cable attached to CN1 on the CYD. Something like this:

https://a.co/d/01Hyzxh7

and your 232 cable only needs 3 conductors. Ground, TX and RX. It's got to be a cross-over (pin 2 <> pin 3 / pin 3 <> pin 2)

<img width="600" height="542" alt="232" src="https://github.com/user-attachments/assets/c38e2b61-facd-4ff4-983b-6c684cf212cb" />

 
Plug the CYD into a USB port on your PC
I use the free Visual Studio program (with the added platformio extension) to compile and download. 

Just install Visual Studio. See you-tube for info on adding the platformio extension.
Download the entire ypad folder onto your pc. Unzip it if it is compressed. 
Open Visual Studio, open the added platformio extension, then within the platformio home page, select open project. Just click on the ypad folder.
Now all you need to do is open the source code main.cpp file, Visual Studio should go out and load up any library files it needs for the program.
click on the right arrow on the bottom of the screen and it should compile and download it into your ypad
 
Once it is downloaded and it starts, you'll need to open your WiFi manager on your PC and connect to the ypad portal at least once. The ypad portal  192.168.4.1 is where you tell the ypad what wifi network/password to use.  It will then reboot and connect to your assigned WiFi network
 
The ypad config page can now be accessed on your local network from ypad.local. Configure the baud rate, etc if needed, and set up the 10 button labels, text color and macro code. With luck you're connected to your radio and one-touch will perform the functions you desire.
 
There's 2 other menu screens on the ypad itself. One for setting up brightness and rebooting/recal/reconfigure wifi.. and another menu page for showing status (IP address and MAC).


