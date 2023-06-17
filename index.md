---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# Server starten: bundle exec jekyll serve --livereload
# http://192.168.104.26:4000/NodeRED/
# https://smartonosen.github.io/NodeRED/

layout: default
title: Node-RED
---

# Node-RED

In dieser Dokumentation wird die Installation von Node-RED und dem Node-RED Dashboard auf einem Raspberry Pi beschrieben.
Mithilfe dessen sollen Wetterdaten aus dem Internet und von einem DHT11-Sensor abgerufen und auf dem Dashboard dargestellt werden.

Node-RED ist ein Programmierwerkzeug, das unterschiedliche Geräte, APIs und Onlinedienste miteinander verbinden und das Zusammenspiel derer gestalten und steuern kann.

Der Aufbau von Node-RED besteht aus verschiedenen Hauptkomponenten:

1. Flow Editor: Der Flow Editor ist die Benutzeroberfläche von Node-RED, in der Sie Ihre Flows erstellen und bearbeiten. Es handelt sich um eine browserbasierte Oberfläche, die über einen Webbrowser aufgerufen wird. Im Flow Editor ziehen Sie Knoten (Nodes) aus der Palette auf die Arbeitsfläche und verbinden sie miteinander, um die gewünschte Logik und den Datenfluss zu erstellen.
<br><br>
2. Palette: Die Palette enthält eine Vielzahl von Knoten (Nodes), die in Node-RED verwendet werden können. Knoten repräsentieren verschiedene Funktionen oder Aktionen, wie beispielsweise das Lesen von Sensordaten, das Senden von E-Mails oder das Aufrufen von APIs. Die Palette ist in Kategorien organisiert, um das Finden der gewünschten Knoten zu erleichtern.
<br><br>
3. Arbeitsfläche: Die Arbeitsfläche ist der Hauptbereich im Flow Editor, in dem Sie Ihre Flows erstellen. Hier ziehen Sie Knoten aus der Palette und verbinden sie miteinander, um den Datenfluss zu definieren. Sie können auch Knoten konfigurieren und ihnen Namen geben, um ihre Funktion zu beschreiben.
<br><br>
4. Knoten (Nodes): Knoten sind die grundlegenden Bausteine in Node-RED. Jeder Knoten stellt eine bestimmte Funktion dar, beispielsweise das Empfangen von Daten, das Verarbeiten von Daten oder das Senden von Daten. Es gibt verschiedene Arten von Knoten, darunter Eingabeknoten, Ausgabeknoten, Verarbeitungsknoten und Steuerungsknoten. Knoten können miteinander verbunden werden, um den Datenfluss innerhalb des Flows zu steuern.
<br><br>
5. Flows: Flows sind die visuelle Darstellung der Logik und des Datenflusses in Node-RED. Ein Flow besteht aus einer Reihe von miteinander verbundenen Knoten, die eine bestimmte Aufgabe erfüllen. Flows können komplexe Automatisierungen und Workflows abbilden. Sie können mehrere Flows erstellen und zwischen ihnen wechseln, um verschiedene Aufgaben zu organisieren.
<br><br>
6. Debugging: Node-RED bietet integrierte Debugging-Funktionen, mit denen Sie den Datenfluss und die Ausgabe der Knoten überwachen können. Sie können Debug-Nachrichten zu bestimmten Stellen in Ihrem Flow hinzufügen, um den Inhalt von Datenobjekten anzuzeigen und Fehler zu finden.
<br><br>
7. Deploy: Sobald Sie mit der Erstellung Ihres Flows zufrieden sind, können Sie den Flow in Node-RED bereitstellen (deployen). Dies bedeutet, dass Ihre Logik und Verbindungen aktiviert und ausgeführt werden. Sie können Ihren Flow in Echtzeit testen und bei Bedarf Änderungen vornehmen.