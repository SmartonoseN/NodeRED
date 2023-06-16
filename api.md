---
layout: default
title: Wetterdaten von open-meteo.com
nav_order: 5
---

# ![](https://open-meteo.com/favicon.ico) Wetterdaten von open-meteo.com

Um neben den Daten des Sensors noch einen Ausblick zu geben wie sich die Temperatur in den nächsten Tagen entwickelt wird, werden noch Daten einer öffentlichen Wetter-API in NodeRED geladen.
Wir haben uns dabei für open-meteo.com entschieden, da diese einfach zu nutzen ist und keine Anmeldung erfordert.

## Aufrufen der API in Node-RED

Um die API aufzurufen werden in NodeRED 2 Blöcke genutzt. Einen Change-Node um die benötigten Parameter in msg.payload zu schreiben und ein "http request"-Node um die eigendliche Anfrage abzuschicken.

Konkret werden im Change-Node die Koordinaten des Ortes gesetzt von dem die Daten gesucht werden sollen, welche Daten gebraucht werden (in unserem Fall die stündliche Temperatur und gefühlte Temperatur) und die Zeit (bei uns die nächsten 14 Tage). Zusätzlich wird das Zeitformat noch auf `unixtime` und ide Zeitzone auf `auto` gesetzt um die Zeiten später einfacher anzeigen zu können.

![](/img/apiChangeNode.png)

Diese Daten werden an den "http request"-Node weitergegeben. Hier muss nicht mehr viel konfiguriert werden, es muss nur die entsprechende URL von open-meteo.com eingegeben werden und darauf geauchtet werden, dass die Methode auf GET steht und als Rückgabe JSON ausgewählt ist.

![](/img/apiHttpRequestNode.png)

## Anzeige im Dashboard

Um die Daten anzuzeigen wird ein Chart mit einem Refresh-Button in der UI verwendet. In diesen Nodes muss nur wenig konfiguriert werden, nur ein paar Einstellungen wie diese genau angezeigt werden sollen (Farbe, Text, usw) und es muss eine Gruppe zur Anzeige ausgewählt werden.

Finale Anzeige:

![](/img/apiUi.png)

Um die Daten allerdings in den Chart zu bekommen müssen sie in ein bestimmtes JSON-Format gebracht werden. Dies geschied über eine function-Node, die eine JavaScript Funktion ausführt

### JavaScript Funktion
```js
let data = msg.payload.hourly
let temperature = []
let apparentTemperature = []

for (let i = 0; i < data.time.length; i++) {
    let time = data.time[i] * 1000
    temperature.push({
        x: time,
        y: data.temperature_2m[i]
    })
    apparentTemperature.push({
        x: time,
        y: data.apparent_temperature[i]
    })
}

msg.payload = [{
    "series": ["°C", "°C gefühlt"],
    "data": [temperature, apparentTemperature],
    "labels": [""]
}]

return msg;
```

### JSON von open-meteo.com
```json
{
    "latitude": 49.8,
    "longitude": 9.959999,
    "generationtime_ms": 1.3309717178344727,
    "utc_offset_seconds": 7200,
    "timezone": "Europe/Berlin",
    "timezone_abbreviation": "CEST",
    "elevation": 213,
    "hourly_units": {
        "time": "unixtime",
        "temperature_2m": "°C",
        "apparent_temperature": "°C"
    },
    "hourly": {
        "time": [1686866400, 1686870000, 1686873600, ...],
        "temperature_2m": [15.7, 15.1, 12.1, ...],
        "apparent_temperature": [14.8, 13.8, 11.3, ...]
    }
}
```

### JSON nach der function-Node
```json
[
  {
    "series": ["°C", "°C gefühlt"],
    "data": [
      [
        { "x": 1686866400000, "y": 15.7 },
        { "x": 1686870000000, "y": 15.1 },
        { "x": 1686873600000, "y": 12.1 },
        ...
      ],
      [
        { "x": 1686866400000, "y": 14.8 },
        { "x": 1686870000000, "y": 13.8 },
        { "x": 1686873600000, "y": 11.3 },
        ...
      ]
    ],
    "labels": [""]
  }
]
```

### Kompletter Flow
![](/img/apiFlow.png)

Am Ende des Flows wird noch `msg.payload` gelöscht und eine Notification angezeigt um dem Nutzer zu signalisieren das die Daten erfolgreich aktualisiert wurden.
