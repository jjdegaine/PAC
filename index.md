---
marp: false
theme: default
title: Swimming pool Heat pump control loop with solar panel
html: true
---

# Swimming pool Heat pump control loop with solar panel

    The Goal of this WEB site is to explain a Proof Of Concept regarding a wimming pool Heat pump control loop with solar panel
    
    The mains power supply is measured by a Solar Panel Optimizer (see https://jjdegaine.github.io/Wifi-Solar-panel-optimizer-/)
    every 5 minutes the average power supply is broadcast by bluetooth
    a small android programm collect this value and send it to an android automation app (Macrodroid https://www.macrodroid.com/)

    depending on the power supply value macrodroid will simulate click on the pool heat pump app (https://ismartlife.me/)

# android program

to collect the power average power supply a small android program must be used (bluetooth3.apk), please note that this .apk is not signed by google. You can creat your own pak using appinventor.

[github](https://github.com/jjdegaine/PAC)

the code is available using https://appinventor.mit.edu/ (bluetooth3.aia)

![nomimage](code bluetooth 1.jpgg)

# Macrodroid

the macrodroid automation will simulate click on the smartlife app

if power supply is < "min value" click on start Heat power pump button

if power supply is < "increase value" click on temp +
    
if power supply is > "decrease value" click on temp -

if power supply is > "max value" click on stop Heat power pump button


