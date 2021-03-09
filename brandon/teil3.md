# Kapitel 9: Die Grundlagen für unsere Deployment Pipeline legen
## Zusammenfassung
- Umgebungen auf Anforderungen erstellen können
- Single Repository
- Infrastruktur neubauen statt reparieren
- Definition des "Done" so anpassen, dass der Code in Prod läuft


## Welche Fragen sind offen geblieben?
Nichts.

## Was ist unklar?
Nichts.

## Was sind die zwei wichtigsten Punkte
1. So früh wie möglich reale Anforderungen dem Entwickler geben, um seinen Code zu testen
2. Single Source of truth "Repo" beinhaltet auch die Anforderungen

## Was hat Dich überrascht?
Die Definition von "Done", wurde nicht angepasst sondern ist jetzt umfangreicher


# Kapitel 10: Schnelles und zuverlässiges, automatisiertes Test ermöglichen
## Zusammenfassung

- Continious Build, Test und Integration von Code und Umgebung
- Eine schnelle und zuverlässige automatisierte Validierungstest-Suite aufbauen
- Bei unserem automatisierten Testen Fehler so früh wie möglich finden
- Sicherstellen, dass Test schnell laufen (auch parallel)
- Die automatisierten Test schreiben, bevor wir den Code schreiben (TDD)
- So viele manuelle Tests wie möglich automatisieren
- Performancetests in unseren Testsuit integrieren
- Nicht funktionale Anforderungen in unsere Testsuite integrieren
- Unsere Andon-Schnurr ziehen, wenn die Deployment-Pipeline unterbrochen wird
- Warum wir die Andon-Schnurr ziehen müssen

## Welche Fragen sind offen geblieben?
Auch wenn mir die unterschiedlichen Testebenen bekannt sind: Unit-Test, Akzeptanztest, Integrations- und User-Test - weiß ich nicht wie ich wieviele Umgebungen ich benötige (Performance-Umgebung, etc.)

## Was ist unklar?
Ausgangsbedingung: Entkoppelte Architektur

## Was sind die zwei wichtigsten Punkte für Dich?
1. Test-driven Development und das Verständnis, dass so früh wie möglich (Pyramide) in die Optimierung investiert werden muss
2. Das eine Andon-Schnurr per Design definiet werden muss, und somit richtig konkret beschrieben wird statt als kulturelle Pharse

## Was hat Dich überrascht?
- Das systematische Fehler und schleichende Fehler über die Historie abgefangen werden können


# Kapitel 11: Continious Intergration ermöglichen und umsetzen
## Zusammenfassung

- Entwicklung in kleinen Batchgrößen und was passiert, wenn wir zu selten Code in den Trunk committen
- Trunk-basierte Entwicklungspraktiken übernehmen

## Welche Fragen sind offen geblieben?
Nichts.

## Was ist unklar?
Nichts.

## Was sind für Dich zwei wichtigsten Punkte?
1. Trunkbasiert da stabilier
2. Trunkbasiert da höherer Durchsatz

## Was hat Dich überrascht?
Trunkbasiert führt zu höhere Zufriedenheit und niedriger Burnout-Raten

# Kapitel 12: Releases automatisieren und ihr Risiko reduzieren

## Zusammenfassung
- Unseren Deployment-Process automatisieren
- Automatisierte Self-Service-Deployment ermöglichen
- Code-Deployment in die Deployment-Pipeline einbinden
- Deployments von Releases entkoppeln
- Umgebungsbasierte Release-Muster
    - Blue-Green-Deployment
    - Canary Deployment
    - Anwendungsbasierte Muster   
## Welche Fragen sind offen geblieben?
Es gibt dennoch einen 
## Was ist unklar?
Was ist ein Self-Service
## Was snd für Dich die zwei wichtigsten Punkte?
1. Deployments müssen ebenfalls zur Routine werden
2. Schalter muss erstellt werden

## Was hat dich überrascht?
Deployment von Releases entkoppeln


# Kapitel 13: Eine Architektur für risikoarme Releases
## Zusammenfassung

- Architektonische Prototypen: Monolith vs. Mircoservices
- Mit dem Strangler-Application-Muster die Firmenarchitektur sicher weiterentwickeln

## Welche Fragen sind offen geblieben?
Wie bestimme ich die richtige Architektur?
Sind Commits und Codezeilen die richtige Metrik?
## Was ist unklar?

## Was sind für Dich die zwei wichtigsten Dinge?
1. Es gibt nicht die perfekte Architektur
2. Wie messe ich das

## Was hat Dich überrascht
Strangler-Muster - das Bild - hat mir sehr gut gefallen