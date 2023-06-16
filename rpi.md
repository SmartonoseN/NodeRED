---
layout: default
title: Raspberry Pi Setup
nav_order: 1
---

# ![](https://www.raspberrypi.org/app/uploads/2012/03/raspberry-pi-logo.png) Raspberry Pi Setup

## OS Installation

Der einfachste Weg um ein OS auf dem Raspberry zu installieren ist mit dem [Raspberry Pi Imager](https://www.raspberrypi.com/software/). Nach dem Download und der Installation muss nur die SD Karte ausgewählt werden und das benötigte OS. Node-RED funktioniert auf vielen Betriebsystemen, wir benutzen hier als Beispiel Ubuntu Server in der neusten Version.

Da es sich dabei um ein OS ohne grafische Oberfläche handelt muss man in den Einstellungen des Imager noch SSH aktivieren, ein Nutzernamen und Passwort angeben und (falls kein LAN vorhanden) ein WLAN Zugang einrichten.

## Anmeldung im Raspberry Pi

Nachdem der Raspberry Pi konfiguriert wurde, muss als nächster Schritt die Anmeldung im Pi erfolgen.
Hierzu sind mehrere Schritte notwendig:
1. Zuerst müssen Sie Ihr eigenes Gerät mit dem gleichen Netzwerk verbinden, mit dem auch der Raspberry Pi verbunden ist.
2. Danach muss auf Ihrem Gerät eine Konsole geöffnet werden.
3. Wenn die IP-Adresse des Raspberry Pi bekannt ist, kann mithilfe eines Befehls die Verbindung hergestellt werden.

    Dieser Befehl lautet "ssh benutzername@IP-Adresse". Benutzername ist dabei der Name des Profils, das Sie auf dem Raspberry Pi verwenden und die IP-Adresse ist die IP des Pis.

4. Nachdem Sie das abgefragte Passwort eingegeben haben, ist die Verbindung zu Ihrem Raspberry Pi erfolgreich hergestellt.
