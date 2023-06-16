---
# https://flows.nodered.org/node/node-red-dashboard
layout: default
title: Dashboard
nav_order: 3
---

# ![](https://github.com/node-red/node-red-dashboard/blob/master/src/icon64x64.png?raw=true) Dashboard

Das Node-RED Dashboard ist ein Plugin für die Flow-basierte Entwicklungsplattform Node-RED, mit dem Sie benutzerdefinierte Benutzeroberflächen erstellen können. Um das Node-RED Dashboard zu installieren, müssen die folgenden Schritten befolgt werden:

## Installation

Öffnen Sie Ihren Webbrowser und navigieren Sie zu http://IP-des-Raspberry:1880 (sofern Sie Node-RED lokal auf Ihrem System ausgeführt haben). Sie sollten die Node-RED-Benutzeroberfläche sehen. Klicken Sie auf das Menü-Symbol in der oberen rechten Ecke und wählen Sie "Manage Palette" aus dem Dropdown-Menü.

Navigieren Sie zum Tab "Install" und suchen Sie nach "node-red-dashboard". Klicken Sie auf die Schaltfläche "Install" neben dem Dashboard-Plugin, um es in Node-RED zu aktivieren.
![](/img/dashboardInstall.webp)

Sobald das Dashboard-Plugin installiert ist, können Sie im Node-RED-Editor die verfügbaren Dashboard-Komponenten finden und benutzen, um Ihre benutzerdefinierte Benutzeroberfläche zu erstellen. Die Oberfläche finden Sie dann unter http://IP-des-Raspberry:1880/ui

## Aufbau

Ein Node-RED Dashboard besteht aus verschiedenen Elementen, die auf einer Webseite angezeigt werden. Der Aufbau eines Dashboards kann je nach Anforderungen und Zweck variieren, aber im Allgemeinen gibt es einige grundlegende Elemente, die in einem Node-RED Dashboard enthalten sind:

1. Header: Der Header ist der oberste Teil des Dashboards und enthält normalerweise den Namen des Dashboards und eine Navigationsleiste, die es dem Benutzer ermöglicht, zwischen verschiedenen Seiten oder Ansichten des Dashboards zu wechseln.
<br><br>
2. Widgets: Widgets sind die Hauptelemente des Dashboards und stellen die Daten dar, die der Benutzer sehen möchte. Es gibt verschiedene Arten von Widgets, wie z.B. Textfelder, Schaltflächen, Diagramme, Tabellen und mehr. Jedes Widget kann individuell konfiguriert werden, um die gewünschten Daten anzuzeigen.
<br><br>
3. Layout: Das Layout des Dashboards bestimmt, wie die Widgets auf der Seite angeordnet sind. Es gibt verschiedene Layout-Optionen, wie z.B. eine Spalte, eine Zeile oder ein Gitter. Das Layout kann auch responsiv sein, was bedeutet, dass es sich automatisch an die Größe des Bildschirms anpasst.
<br><br>
4. Footer: Der Footer ist der unterste Teil des Dashboards und enthält normalerweise Informationen wie das Datum und den Autor des Dashboards.

Zusammenfassend lässt sich sagen, dass ein Node-RED Dashboard aus Widgets besteht, die in einem bestimmten Layout angeordnet sind und von einem Header und einem Footer umgeben sind. Durch die Konfiguration der Widgets und des Layouts kann der Benutzer die gewünschten Daten auf eine übersichtliche und benutzerfreundliche Weise anzeigen.
