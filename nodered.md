---
# https://nodered.org/docs/getting-started/raspberrypi
layout: default
title: Node-RED Installation
nav_order: 2
---

# ![](https://nodered.org/about/resources/media/node-red-icon.svg) Node-RED Installation

Um Node-RED auf Ihrem Raspberry Pi zu installieren, müssen Sie folgende Schritte befolgen:

1. Node-RED installieren:
   Geben Sie den folgenden Befehl ein, um Node-RED auf Ihrem Raspberry Pi zu installieren:

   ```
   sudo apt install build-essential git curl
   bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
   ```

   Dieser Befehl wird:
   - erforderliche Abhängigkeiten installieren
   - Wenn Node.js bereits installiert ist, stellt es sicher, dass es mindestens v14 ist. Wenn es weniger als v14 ist, hält es an und überlässt dem Benutzer die Entscheidung, ob er bei Node-RED Version 1 bleiben will - oder Nodejs auf eine neuere LTS-Version aktualisieren will. Wenn nichts gefunden wird, wird es die Node.js 16 LTS Version mit dem NodeSource Paket installieren.
   - Die neueste Version von Node-RED mit npm installieren.
   - optional eine Sammlung von nützlichen Pi-spezifischen Nodes installieren.
   - Node-RED so einrichten, dass es als Dienst läuft und eine Reihe von Befehlen für die Arbeit mit dem Dienst bereitstellen.
   <br><br>
2. Node-RED starten:
   Geben Sie den Befehl `node-red` in das Terminal ein und drücken Sie die Eingabetaste. Node-RED sollte gestartet werden und Sie sollten eine Ausgabe sehen, die angibt, dass der Server auf Port 1880 läuft.

   Um Node-Red im Hintergrund laufen zu lassen können die Befehle `node-red-start`, `node-red-stop`, `node-red-restart` und `node-red-log` verwendet werden
   <br><br>
3. Um Node-RED automatisch beim Hochfahren des Pis zu starten kann dieser Befehl genutzt werden:
   ```
   sudo systemctl enable nodered.service
   ```
   Um dies wieder auzuschalten kann dieser Befehl genutzt werden:
   ```
   sudo systemctl enable nodered.service
   ```
   <br>
4. Zugriff auf die Node-RED Oberfläche:
   Öffnen Sie einen Webbrowser auf einem anderen Gerät, das mit demselben Netzwerk wie der Raspberry Pi verbunden ist, und geben Sie die IP-Adresse des Raspberry Pi gefolgt von :1880 in die Adressleiste ein. Dadurch wird die Node-RED Oberfläche geöffnet, in dem Sie Ihre Flows erstellen und bearbeiten können.

Nun haben Sie Node-RED erfolgreich auf Ihrem Raspberry Pi installiert und gestartet. Jetzt können Sie mit der Erstellung Ihrer Flows und dem Experimentieren mit den verschiedenen Node-RED-Komponenten beginnen.
