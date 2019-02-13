# PM2.5

In this setup, you will use your NodeMCU to read PM1, PM2.5 and PM10 level from PMS5003, and display them on ThingSpeak in 20-second intervals. 

You will need:

- NodeMCU v2 cp2102 (~$3)
- PMS5003 (~$14)
- Power supply module 
- Breadboard
- MicroUSB
- Jumper wires

<b>1. Set up NodeMCU:</b><br>
Please follow the instructions available at the bottom of this page https://github.com/ICECapstone/Blink to set up your NodeMCU. 

<b>2. Physical connections: </b><br>
PMS5003 Vcc -> 5V of the power supply module <br>
PMS5003 Ground -> Ground of the power supply module -> NodeMCU ground <br>
PMS5003 TX -> GPIO2 of NodeMCU <br>

![screen shot 2019-02-13 at 9 57 37 am](https://user-images.githubusercontent.com/11530521/52683656-15ce5180-2f76-11e9-92f8-c4107b32d5bb.png)

<b>3. Set up ThingSpeak: </b><br>
If you would like to see PM readings online, please set up your ThingsSpeak channel on www.thingspeak.com.  Gather your 'API key' and 'Channel ID' for use in the code.  Under Channel setting, enable three fields for data gathering (field 1: PM2.5; field 2: PM1.0; field3: PM10).

![thingspeak](https://user-images.githubusercontent.com/11530521/52684231-2253a980-2f78-11e9-8c2a-095cd966f92f.png)

<b>4. Upload the code to your NodeMCU: </b><br>
Note: I slightly modified the original code (https://learn.adafruit.com/pm25-air-quality-sensor) to allow displaying data online via ThingSpeak. The code is available in this repository as 'PM25a.ino'.  You will need to replace:
- ssid with your ssid
- password with your Wi-Fi password
- myWriteAPIKey with your ThingSpeak's writeAPI 
- myChannelNumber with your ThingSpeak's channel number

<b>5. Enjoy: </b></br>
Once you upload the code, your NodeMCU starts gathering data from PMS5003, and data are displayed on ThingsSpeak.  

![data](https://user-images.githubusercontent.com/11530521/52684414-c63d5500-2f78-11e9-9d23-03794f51702d.png)

