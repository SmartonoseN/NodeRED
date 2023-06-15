---
# https://flows.nodered.org/node/node-red-dashboard
layout: default
title: Dashboard
nav_order: 3
---

# ![](https://github.com/node-red/node-red-dashboard/blob/master/src/icon64x64.png?raw=true) Dashboard

## Installation

Das Node-RED Dashboard ist ein Plugin für die Flow-basierte Entwicklungsplattform Node-RED, mit dem du benutzerdefinierte Benutzeroberflächen erstellen kannst. Um das Node-RED Dashboard zu installieren, müssen die folgenden Schritten gemacht werden:

1. Node-RED installieren
   Zunächst musst du sicherstellen, dass du Node-RED auf deinem System installiert hast. Node-RED kann über den Node Package Manager (npm) installiert werden. Öffne die Kommandozeile oder das Terminal und gib den folgenden Befehl ein:

   ```
   npm install -g node-red
   ```

   Dieser Befehl installiert Node-RED global auf deinem System.

2. Node-RED Dashboard installieren
   Sobald Node-RED installiert ist, kannst du das Dashboard-Plugin installieren. Öffne erneut die Kommandozeile oder das Terminal und navigiere zum Verzeichnis, in dem du Node-RED installiert hast. Führe den folgenden Befehl aus:

   ```
   npm install node-red-dashboard
   ```

   Dieser Befehl installiert das Node-RED Dashboard-Plugin in deinem Node-RED-Verzeichnis.

3. Node-RED neu starten
   Nach der Installation des Dashboards musst du Node-RED neu starten, damit das Plugin aktiviert wird. Führe den folgenden Befehl aus, um Node-RED neu zu starten:

   ```
   node-red
   ```

   Sobald Node-RED neu gestartet ist, ist das Dashboard-Plugin einsatzbereit.

4. Das Dashboard verwenden
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
