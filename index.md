---
marp: false
theme: default
title: Swimming pool Heat pump control loop with solar panel
html: true
---

# Swimming pool Heat pump control loop with solar panel

    The Goal of this WEB site is to explain a Proof Of Concept regarding a swimming pool Heat pump 
    control loop with solar panel
    
    The mains power supply is measured by a Solar Panel Optimizer 
    (see https://jjdegaine.github.io/Wifi-Solar-panel-optimizer-/)
    every 5 minutes the average power supply and relay status is broadcast by bluetooth
    a small android programm collect this value and send it to an MQTT server (Mosquitto), theses value are used by Jeedom 
    
    depending on the power supply value Jeedom will modify the temperature setting

# android program

to collect the power average power supply a small android program must be used (MQTTV6.apk), please note that this .apk is not signed by google. 
You can create your own pack using appinventor.

[github](https://github.com/jjdegaine/PAC) repository

the code is available using https://appinventor.mit.edu/ (MQTTV6-2.aia)

![nomimage](https://github.com/jjdegaine/PAC/mqttV6_1.jpg)

![nomimage](https://github.com/jjdegaine/PAC/mqttV6_2.jpg)

![nomimage](https://github.com/jjdegaine/PAC/mqttV6_3.jpg)


# Jeedom

The swimmimg pool heat pump is a poolex Q line 9 which can be controlled by a Tuya APP on android.
Using the plugin wifilightV2 the pump can be controlled by Jeedom

The plugin MQTT is used to read the value sent by the android APP

![nomimage](https://github.com/jjdegaine/PAC/jeedom_scenario.jpg)




