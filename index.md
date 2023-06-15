---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# Server starten: bundle exec jekyll serve --livereload
# http://192.168.104.26:4000/
# https://iotstarters.com/building-node-red-dashboard-with-dht11-sensor/

layout: default
permalink: /
---
<style>
    h1 img {
        width: 50px;
    }
</style>

# ![](https://www.raspberrypi.org/app/uploads/2012/03/raspberry-pi-logo.png) Raspberry Pi Setup
## Anmeldung im Raspberry Pi
Nachdem der Raspberry Pi konfiguriert wurde, muss als nächster Schritt die Anmeldung im Pi erfolgen.
Hierzu sind mehrere Schritte notwendig:
Zuerst müssen Sie ihr eigenes Notebook mit dem WLAN verbinden, mit dem auch der Raspberry Pi verbunden ist.
Danach muss auf dem Notebook eine Eingabeaufforderung geöffnet werden.
Wenn nun die IP-Adresse des Raspberry Pi bekannt ist, kann mithilfe eines Befehls die Verbindung hergestellt werden.
Dieser Befehl lautet "ssh benutzername@IP-Adresse". Benutzername ist dabei der Name des Profils, dass Sie auf dem Raspberry Pi verwenden und die IP-Adresse ist die IP des Pis.
Nachdem sie dann das abgefragte Passwort eingegeben haben, ist die Verbindung zu Ihrem Raspberry Pi erfolgreich hergestellt.

# ![](https://nodered.org/about/resources/media/node-red-icon.svg) Node-RED Installation

Schritt 1: Raspbian-Image herunterladen
Laden Sie das Raspbian-Image von der offiziellen Raspberry Pi-Website herunter. Wählen Sie die Version aus, die Ihren Anforderungen entspricht (z. B. Raspbian Buster Lite für eine schlankere Installation).

Schritt 2: SD-Karte vorbereiten
Stecken Sie die SD-Karte in Ihren Computer und verwenden Sie ein geeignetes Tool wie Etcher (https://www.balena.io/etcher/), um das Raspbian-Image auf die SD-Karte zu schreiben. Befolgen Sie die Anweisungen des Tools, um den Vorgang abzuschließen.

Schritt 3: Raspberry Pi starten
Legen Sie die vorbereitete SD-Karte in den Raspberry Pi ein und schließen Sie ihn an Strom und Monitor an. Starten Sie den Raspberry Pi.

Schritt 4: Raspbian konfigurieren
Sobald der Raspberry Pi hochgefahren ist, werden Sie aufgefordert, die grundlegenden Konfigurationseinstellungen vorzunehmen. Folgen Sie den Anweisungen auf dem Bildschirm, um die Sprache, das Wi-Fi, das Passwort und andere Einstellungen festzulegen.

Schritt 5: Node.js installieren
Öffnen Sie ein Terminal auf dem Raspberry Pi und geben Sie die folgenden Befehle ein, um Node.js zu installieren:

curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -
sudo apt-get install -y nodejs

Dieser Befehl lädt die Node.js-Installationsdateien herunter und installiert Node.js auf Ihrem Raspberry Pi.

Schritt 6: Node-RED installieren
Geben Sie den folgenden Befehl ein, um Node-RED auf Ihrem Raspberry Pi zu installieren:

sudo npm install -g --unsafe-perm node-red

Dieser Befehl lädt und installiert Node-RED sowie alle erforderlichen Abhängigkeiten.

Schritt 7: Node-RED starten
Geben Sie den Befehl node-red in das Terminal ein und drücken Sie die Eingabetaste. Node-RED sollte gestartet werden und Sie sollten eine Ausgabe sehen, die angibt, dass der Server auf Port 1880 läuft.

Schritt 8: Zugriff auf Node-RED-Dashboard
Öffnen Sie einen Webbrowser auf einem anderen Gerät, das mit demselben Netzwerk wie der Raspberry Pi verbunden ist, und geben Sie die IP-Adresse des Raspberry Pi gefolgt von :1880 in die Adressleiste ein. Zum Beispiel: http://<Raspberry-Pi-IP-Adresse>:1880. Dadurch wird das Node-RED-Dashboard geöffnet, in dem Sie Ihre Flows erstellen und bearbeiten können.

Sie haben Node-RED erfolgreich auf Ihrem Raspberry Pi installiert und gestartet. Jetzt können Sie mit der Erstellung Ihrer Flows und dem Experimentieren mit den verschiedenen Node-RED-Komponenten beginnen.
# ![](https://github.com/node-red/node-red-dashboard/blob/master/src/icon64x64.png?raw=true) Dashboard
## Installation
Das Node-RED Dashboard ist ein Plugin für die Flow-basierte Entwicklungsplattform Node-RED, mit dem du benutzerdefinierte Benutzeroberflächen erstellen kannst. Um das Node-RED Dashboard zu installieren, müssen die folgenden Schritten gemacht werden:

Schritt 1: Node-RED installieren
Zunächst musst du sicherstellen, dass du Node-RED auf deinem System installiert hast. Node-RED kann über den Node Package Manager (npm) installiert werden. Öffne die Kommandozeile oder das Terminal und gib den folgenden Befehl ein:

npm install -g node-red

Dieser Befehl installiert Node-RED global auf deinem System.

Schritt 2: Node-RED Dashboard installieren
Sobald Node-RED installiert ist, kannst du das Dashboard-Plugin installieren. Öffne erneut die Kommandozeile oder das Terminal und navigiere zum Verzeichnis, in dem du Node-RED installiert hast. Führe den folgenden Befehl aus:

npm install node-red-dashboard

Dieser Befehl installiert das Node-RED Dashboard-Plugin in deinem Node-RED-Verzeichnis.

Schritt 3: Node-RED neu starten
Nach der Installation des Dashboards musst du Node-RED neu starten, damit das Plugin aktiviert wird. Führe den folgenden Befehl aus, um Node-RED neu zu starten:

node-red

Sobald Node-RED neu gestartet ist, ist das Dashboard-Plugin einsatzbereit.

Schritt 4: Das Dashboard verwenden
Öffne deinen Webbrowser und navigiere zu http://localhost:1880 (sofern du Node-RED lokal auf deinem System ausgeführt hast). Du solltest die Node-RED-Benutzeroberfläche sehen. Klicke auf das Menü-Symbol in der oberen rechten Ecke und wähle "Manage Palette" aus dem Dropdown-Menü.

Navigiere zum Tab "Install" und suche nach "node-red-dashboard". Klicke auf die Schaltfläche "Install" neben dem Dashboard-Plugin, um es in Node-RED zu aktivieren.

Sobald das Dashboard-Plugin installiert ist, kannst du im Node-RED-Editor die verfügbaren Dashboard-Komponenten finden und benutzen, um deine benutzerdefinierte Benutzeroberfläche zu erstellen.

Das waren die grundlegenden Schritte zur Installation des Node-RED Dashboards. Beachte, dass Node-RED auch auf einem Remote-Server oder einem anderen Computer installiert sein kann, und die Adresse, zu der du navigieren musst, kann sich entsprechend ändern.

## Aufbau
Ein Node-RED Dashboard besteht aus verschiedenen Elementen, die auf einer Webseite angezeigt werden. Der Aufbau eines Dashboards kann je nach Anforderungen und Zweck variieren, aber im Allgemeinen gibt es einige grundlegende Elemente, die in einem Node-RED Dashboard enthalten sind:

1. Header: Der Header ist der oberste Teil des Dashboards und enthält normalerweise den Namen des Dashboards und eine Navigationsleiste, die es dem Benutzer ermöglicht, zwischen verschiedenen Seiten oder Ansichten des Dashboards zu wechseln.

2. Widgets: Widgets sind die Hauptelemente des Dashboards und stellen die Daten dar, die der Benutzer sehen möchte. Es gibt verschiedene Arten von Widgets, wie z.B. Textfelder, Schaltflächen, Diagramme, Tabellen und mehr. Jedes Widget kann individuell konfiguriert werden, um die gewünschten Daten anzuzeigen.

3. Layout: Das Layout des Dashboards bestimmt, wie die Widgets auf der Seite angeordnet sind. Es gibt verschiedene Layout-Optionen, wie z.B. eine Spalte, eine Zeile oder ein Gitter. Das Layout kann auch responsiv sein, was bedeutet, dass es sich automatisch an die Größe des Bildschirms anpasst.

4. Footer: Der Footer ist der unterste Teil des Dashboards und enthält normalerweise Informationen wie das Datum und den Autor des Dashboards.

Zusammenfassend lässt sich sagen, dass ein Node-RED Dashboard aus Widgets besteht, die in einem bestimmten Layout angeordnet sind und von einem Header und einem Footer umgeben sind. Durch die Konfiguration der Widgets und des Layouts kann der Benutzer die gewünschten Daten auf eine übersichtliche und benutzerfreundliche Weise anzeigen.

# ![](https://williewortel.eu/wp-content/uploads/dht11.jpg) DHT11
## Anschließen an den RPi
## Konfiguration in Node-RED
## Anzeige im Dashboard
![](/img/dht11Flow.png)

# ![](https://open-meteo.com/favicon.ico) Wetterdaten von open-meteo.com
Um neben den Daten des Sensors noch einen Ausblick zu geben wie sich die Temperatur in den nächsten Tagen entwickelt wird, werden noch Daten einer öffentlichen Wetter-API in NodeRED geladen.
Wir haben uns dabei für open-meteo.com entschieden, da diese einfach zu nutzen ist und keine Anmeldung erfordert.
## Aufrufen der API in Node-RED
Um die API aufzurufen werden in NodeRED 2 Blöcke genutzt. Einen Change-Block um die benötigten Parameter in msg.payload zu schreiben und ein "http request"-Block um die eigendliche Anfrage abzuschicken.
## Anzeige im Dashboard
