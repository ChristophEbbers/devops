# Der zweite Weg: Die technischen Praktiken des Feedbacks
# 14 Telemetriedaten erzeugen
- Es kann nicht verhindert werden, dass Dinge schief gehen
- Vor allem bei komplexen Systemen
- Systeme so entwerfen, das kontinuierlich Telemetriedaten erzeugt werden
- Einfluss auf MTTR

## Telemetrie-Infrastruktur aufbauen
- Mitbekommen, von unerwünschtem Verhalten
- Datensammlung in Form von Events, Logs und Metriken
- auch Daten aus der Pipeline mit einbeziehen
- Daten müssen zugänglich gemacht werden

## Anwendungs-Logging-Telemetriedaten erzeugen
- Bei der täglichen Arbeit erzeugen
- Auf das Logging-Level achten
- Wenig Drucker-Toner ist kein ERROR

## Mit Telemetriedaten beim Lösen von Problemen helfen
- Kultur von Schuldzuweisung vermeiden
- Biete die Möglichkeiten Hypothesen zur Fehlerursache oder Lösen eines Problems anzuwenden
- Eine Zeile Code muss ausreichen

## Self-Service
- Jeder soll Zugriff auf Telemetriedaten haben
- Das Team hat nichts zu verbergen
- Ggf. auch an Kunden weitergeben, Vertrauen schaffen

## Telemetrielücken finden und füllen
- Aus den Ebenen: Business, Anwendung, Infrastruktur, Client, Deployment-Pipeline
- Alle Bereich abdecken, um so den Zustand zu kennen
- Sicherheitsrelevanten Vorfälle kennen
- Probleme fürher erkennen und beheben

## Anwendungs- und Business-Metriken
- Benutzer-Events/Benutzer-Interaktionen
- Entscheidung darüber welche Experimente wir nutzen können
- Transaktionszahlen über Weihnachten etc.

## Infrastruktur
- Speicherbedarf der Datenbank, der JVM

# 15 Telemetriedaten analysieren
- Berechnung des Mittelwerts und der Standardabweichung, anhand der Metriken Abweichungen erkennen
- Schwellwert zu definieren, ist manchmal nicht machbar

## Probleme
- Wenn keine Gauß-Verteilung entsteht
- Einbeziehen von Histogrammen und Schwellwert definieren

## Techniken
- Gleitenden Mittelwert bei Zeitreihen
  