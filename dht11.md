---
# https://iotstarters.com/building-node-red-dashboard-with-dht11-sensor/
layout: default
title: DHT11
nav_order: 4
---

# ![](https://williewortel.eu/wp-content/uploads/dht11.jpg) DHT11
Diese Software-Dokumentation beschreibt, wie der DHT11-Temperatursensor an einen Raspberry Pi angeschlossen und verwendet werden kann, um die Temperatur zu messen. Der DHT11 ist ein kostengünstiger und weit verbreiteter Sensor, der sowohl die Temperatur als auch die Luftfeuchtigkeit messen kann.

## Anschließen an den RPi
Führen Sie die folgenden Schritte aus, um den DHT11-Sensor mit dem Raspberry Pi zu verbinden:
<br>
1. Stecken Sie den DHT11-Sensor in das Steckbrett (Breadboard).
<br><br>
2. Verbinden Sie den 3,3V-Pin des Raspberry Pi mit dem VCC-Pin des DHT11-Sensors.
<br><br>
3. Verbinden Sie den GPIO-Pin 4 (BCM-Pin 4) des Raspberry Pi mit dem DATA-Pin des DHT11-Sensors.
<br><br>
4. Verbinden Sie den GND-Pin des Raspberry Pi mit dem GND-Pin des DHT11-Sensors.
<br><br>
5. Fügen Sie einen 10k-Ohm-Widerstand zwischen dem VCC- und dem DATA-Pin des DHT11-Sensors hinzu.
<br>

## Konfiguration in Node-RED

## Anzeige im Dashboard

![](/img/dht11Flow.png)
