---
layout: default
title: Wetterdaten von open-meteo.com
nav_order: 5
---

# ![](https://open-meteo.com/favicon.ico) Wetterdaten von open-meteo.com

Um neben den Daten des Sensors noch einen Ausblick zu geben wie sich die Temperatur in den nächsten Tagen entwickelt wird, werden noch Daten einer öffentlichen Wetter-API in NodeRED geladen.
Wir haben uns dabei für open-meteo.com entschieden, da diese einfach zu nutzen ist und keine Anmeldung erfordert.

## Aufrufen der API in Node-RED

Um die API aufzurufen werden in NodeRED 2 Blöcke genutzt. Einen Change-Block um die benötigten Parameter in msg.payload zu schreiben und ein "http request"-Block um die eigendliche Anfrage abzuschicken.

## Anzeige im Dashboard
