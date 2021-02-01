# Teil I: Die drei Wege

## 1 - Die drei Wege
### Die Wertkette in der Herstellung
- fundamentales Konzept: Wertkette/Wertfluss
- Folge von Aktivitäten um eine Anforderung zu erfüllen
- Konstanten Fluss ermöglichen (WIP-Limit, Batch-Size)

### Die Technologie-Wertkette
- Eine Idee mit Hilfe von Technologien umzusetzen
- z.B. agiler Softwareentwicklungsprozess
- Erst Wert gestiftet, wenn in Produktion
- Einen schnellen Flow erzeugen durch Reduzierung der Batch-Size (Entwicklung und Operation parallel)
- Durchlaufzeit (gesamte Laufzeit)
- Verarbeitungszeit (wird erst gemessen, wenn mit der tatsächlichen Arbeit begonnen wird)
- Lange deployment-Zeiten gilt es zu vermeiden (Fehlerbehebung kann viel Zeit in Anspruch nehmen)
- Ziel: kurze deployment-Zeiten, umso schneller Feedback zu erhalten -> automatisieren

### Die drei Wege: Die Prinzipien als Basis von DevOps
- Arbeit sichtbar machen, Batch-Size anpassen, Deployment-Prozess automatisieren
- Feedback erhalten/einbauen
- Kultur etablieren die es möglich macht aus Erfolgen und Misserfolgen zu lernen

## 2 - Die Prinzipien des Flows
Flow wird erhöht durch:
 - Batch-Size und Intervalle verringern
 - Tests erzeugen
 - Deployment-Zeit verringern

### Wir machen unsere Arbeit sichtbar
- Fortschritt, Warten, Blockieren sichtbar machen (Kanban/Sprintboard)
- Nicht nur sichtbar dadurch, sondern kann es auch steuern (links -> rechts)
- Zeitmessung

### WIP beschränken
- Nur eine bestimmte Anzahl von Tasks
- Es darf an nichts gearbeitet werden, wofür kein Task erstellt worden ist
- Verzögerungen erkennen/sichtbar machen
