# hackathon_iot_based_wireless_water_level_sensor

IOT Based Water Level Controller Using NodeMCU 
Introduction: IOT Based Water Level Controller Using NodeMCU ESP8266


Features of this project are:-

Real-time water level updates on the Android app.
Automatically turn ON the water pump when water reaches below a minimum level.
Automatically turn OFF water pump when water reaches above a maximum level.
Manual option to control the water pump at any water level.

Requirements:-

NodeMCU ESP8266 development board
HCSR04 ultrasonic sensor
Breadboard
Single channel relay board (to control water pump)
LM7805 +5V voltage regulator IC.
Battery (9V-12V).
WiFi Router (to connect NodeMCU to internet)
Firebase (to create a database)
MIT app inventor 2 (to create Android application)

Step 1: Setup Firebase and Get Secret Key
Setup Firebase and Get Secret KeySetup Firebase and Get Secret Key
We are going to use a real-time database by Google firebase. This real-time database will act as a midway broker between Nodemcu and Android device.

First of all, navigate to firebase site and log in using your google account.
Create a new real-time database.
Get real-database URL and secret key to access the database from the app. For a detailed tutorial, you can check out how to integrate firebase with MIT app inventor.

Step 2: Create App Using MIT App Inventor 2
Create App Using MIT App Inventor.

We are going to use MIT app inventor 2 to create our Android app. Its very simple to use and easy to integrate win Google firebase.

Just follow these steps:-

Download MIT app inventor project file (.aia file) attached below.
Then go to MIT app inventor >> projects >> import project (as shown in screenshot 1). Select the file from your computer and upload it.
Open project and navigate to Screen3 (as shown in screenshot 2).
After that, go to layout window, click on firebaseDB1 (located at bottom of the workspace), enter database URL and key. Also set ProjectBucket to S_HO_C_K (as shown in screenshot 3).
At last, click on the "build" button and save app file (.apk file) to computer.  

Step 3: Configure Arduino IDE for Nodemcu Esp8266
Configure Arduino IDE for Nodemcu Esp8266
First of all, configure Arduino IDE for Nodemcu esp8266. 

Step 4: Upload Code With Some Necessary Changes
Upload Code With Some Necessary 

Download attached file (.ino file) and open it with Arduino IDE.
At line 3, enter database URL without 'https://'.
At line 4, enter database secret key.
At line 5 and 6, don't forget to update WiFi SSID and Wifi password (to which you want to connect NodeMCU ESP8266).
Scroll down a little bit and update minimum water level, maximum water level, and margins according to the depth of your own water tank.
After that, upload program to NodeMCU ESP8266.
We will be sending this code as attachment to this document. 

Step 5: Configure Hardware
We can use either a 9V or 12V battery.
Put ultrasonic sensor at the top of the water tank.
Connect water pump using a relay board (optional during testing).

We will also be sending circuit diagram as attachment. 

Step 6: Final 

Install the app (created in step 2) on your Android device.
Supply power to the setup.
Wait for NodeMCU to connect to the hotspot (you can use either router or portable hotspot)

We have already made some progress on this problem aa we have already made water flow data being send real time in Android app. We have done this previous year and will complete this once lockdown lifted. We are also sending link of youtube video made project by us. 

YouTube link https://youtu.be/1nkHMviGlOM
