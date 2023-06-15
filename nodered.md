---
# https://nodered.org/docs/getting-started/raspberrypi
layout: default
title: Node-RED Installation
nav_order: 2
---

# ![](https://nodered.org/about/resources/media/node-red-icon.svg) Node-RED Installation

1. Raspbian-Image herunterladen
   Laden Sie das Raspbian-Image von der offiziellen Raspberry Pi-Website herunter. Wählen Sie die Version aus, die Ihren Anforderungen entspricht (z. B. Raspbian Buster Lite für eine schlankere Installation).

2. SD-Karte vorbereiten
   Stecken Sie die SD-Karte in Ihren Computer und verwenden Sie ein geeignetes Tool wie Etcher (https://www.balena.io/etcher/), um das Raspbian-Image auf die SD-Karte zu schreiben. Befolgen Sie die Anweisungen des Tools, um den Vorgang abzuschließen.

3. Raspberry Pi starten
   Legen Sie die vorbereitete SD-Karte in den Raspberry Pi ein und schließen Sie ihn an Strom und Monitor an. Starten Sie den Raspberry Pi.

4. Raspbian konfigurieren
   Sobald der Raspberry Pi hochgefahren ist, werden Sie aufgefordert, die grundlegenden Konfigurationseinstellungen vorzunehmen. Folgen Sie den Anweisungen auf dem Bildschirm, um die Sprache, das Wi-Fi, das Passwort und andere Einstellungen festzulegen.

5. Node.js installieren
   Öffnen Sie ein Terminal auf dem Raspberry Pi und geben Sie die folgenden Befehle ein, um Node.js zu installieren:

   ```
   curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -
   sudo apt-get install -y nodejs
   ```

   Dieser Befehl lädt die Node.js-Installationsdateien herunter und installiert Node.js auf Ihrem Raspberry Pi.

6. Node-RED installieren
   Geben Sie den folgenden Befehl ein, um Node-RED auf Ihrem Raspberry Pi zu installieren:

   ```
   sudo npm install -g --unsafe-perm node-red
   ```

   Dieser Befehl lädt und installiert Node-RED sowie alle erforderlichen Abhängigkeiten.

7. Node-RED starten
   Geben Sie den Befehl node-red in das Terminal ein und drücken Sie die Eingabetaste. Node-RED sollte gestartet werden und Sie sollten eine Ausgabe sehen, die angibt, dass der Server auf Port 1880 läuft.

8. Zugriff auf Node-RED-Dashboard
   Öffnen Sie einen Webbrowser auf einem anderen Gerät, das mit demselben Netzwerk wie der Raspberry Pi verbunden ist, und geben Sie die IP-Adresse des Raspberry Pi gefolgt von :1880 in die Adressleiste ein. Zum Beispiel: http://<Raspberry-Pi-IP-Adresse>:1880. Dadurch wird das Node-RED-Dashboard geöffnet, in dem Sie Ihre Flows erstellen und bearbeiten können.

Sie haben Node-RED erfolgreich auf Ihrem Raspberry Pi installiert und gestartet. Jetzt können Sie mit der Erstellung Ihrer Flows und dem Experimentieren mit den verschiedenen Node-RED-Komponenten beginnen.
