# Der erste Weg
- Codebasis muss sich immer in einem deploybaren Zustand befinden
- Trunk-based entwickeln
- Verringern der Durchlaufzeit 
- Kontinuierliches Testen --> schnelles Feedback

# 9 Die Deployment-Pipeline
- Gesamte Infrastruktur lässt sich aus der Versionsverwaltung wiederherstellen
- Inkonsistent aufgesetzte Umgebungen um jeden Preis vermeiden

## Dev, Test und Prod
- Testumgebungen sind meist falsch bzw. anders konfiguriert
- Infrastruktur soll kodifiziert sein und automatisiert
- Virtuelle Umgebung
- Infrastruktur-as-code
- Container
- Cloud
- Fehler schnell reproduzierbar

## Single Repository
- Um Änderungen nachvollziehbar machen zu können
- Quell- und Konfigurationsdateien ablegen, um gewünschten Stand abbilden zu können
- Alles was für den Build-Prozess benötigt wird
- Kommunikationsmöglichkeit

## Infrastruktur einfach neu bauen
- Neu erschaffen, anstatt zu reparieren
- Immutable Infrastructure, manuelle Eingriffe sind nicht erlaubt
- Häufig Updaten, um Fehler schnell zu finden

## DONE
- Je länger die Intervalle, desto schlechter das Ergebnis
- Am Ende haben wir integrierten, getesteten, lauffähigen und potenziell auslieferbaren Code
- Nicht gegen Ende versuchen alles integrieren zu wollen
- Auch in DEV monitoren, loggen und deployen
- Deployments rechtzeitig und häufig durchführen -> Risiken reduzieren

# 10 Automatisierte Tests
- Wenn zu spät getestet wird, werden Fehler erst zu spät bemerkt
- Man kann so auch nicht mehr aus den Fehlern lernen
- Bsp.: GWS
- Angst das System nicht zu verstehen
- Angst zu wissen was passiert (Seiteneffekte)

## Continuous Build
- Automatisierte Tests geben uns schnell Feedback
- Fehler früh erkennen und beheben
- Nach dem Push wird automatisch gebaut und getestet
- Prozess kann jederzeit laufen
- Kleines Batches

## Schnelle Suite
- Wenn Ergebnis erst am nächsten Tag kommt, kann es lange dauern bis man herausgefunden hat, welche Änderung den Fehler verursacht hat
- Langsames und unregelmäßiges Feedback ist ein Problem
- Big-Bang Integration und große Batchgröße gilt es zu vermeiden
- Unit-Tests
- Akzeptanztests
- Integrationstests

## Beim Testen Fehler früh erkennen
- Unit-Tests sind prä­de­s­ti­niert um schnell Feeback zu geben
- Fehler im Integrationstest zu beseitigen sind meistens kostspieliger
- Wenn Komponenten zu eng verwoben sind, ist es schwer zu testen

## TDD
- Test schlägt fehl
- Implementierung
- Refactoring

## Manuelle Tests automatisieren
- Ermöglicht uns an den wichtigen Aufgaben zu arbeiten
- Unzuverlässige Tests mit false-positive will niemand  
- Nur auf die wichtigen Dinge fokussieren zu Testen

## Nicht funktionale Aspekte
- Verfügbarkeit, Skalierbarkeit, Kapzität, Sicherheit

## Andon-Cord ziehen
- Bei keinem erfolgreichen Durchlauf darf keine neue Arbeit ins System
- Gesamte Team informieren
- Rollback, aber wenn möglich fix forward

## Warum wir die Andon-Cord ziehen
- Problem wird immer schwieriger zu beheben
- Man dadurch nicht mehr weiß, durch was der Fehler ausgelöst ist

# 11 Continuous Integration ermöglichen
- Isolierte Branches vermeiden, da immer schwieriger auf master zu mergen
- Integrationsprobleme führen zu nacharbeiten
- Schmutzige Hacks werden gemacht, um Release-Datum zu halten

## Entwicklung in kleinen Batches und was passiert wenn man zu wenig in den master zurückführt
- Verschiedene Optionen:
  - Auf individuelle Produktivität hin optimieren
  - Auf Teamproduktivität hin optimieren
- Der Aufwand Branches wieder zusammenzuführen steigt exponentiell mit der Anzahl der Branches
- Sinkende Motivation den Code zu verbesseren bzw. zu refactoren

## Trunk-based
- Je häufiger Entwickler in Trunk integrieren, desto geringer das Risiko und kleinere Batches
- Ergebnis: Höhere Qualität und kürzer Deployment-Zeiten
- Deutlich höhere Jobzufriedenheit und niedrigere Burn-out-Raten

# 12 Releases automatisieren und Risiko reduzieren
- Code-Deployments sollten automatisiert, wiederholbar und planbar gemacht werden
- Wird ein Prod-Deployment verschoben, so werden die Unterschiede zwischen der Code-Basis immer größer
- Risiko für unerwartete Ergebnisse steigt

## Deployment-Prozess automatisieren
- Wir wollen nicht nur die Durchlaufzeit verringern, sondern
  - Anzahl der Übergaben reduzieren
  - Wissensverlust begrenzen
- In allen Umgebungen auf die gleiche Art und Weise deployen
- Sicherstellen das Umgebung konsistent ist

## Code-Deployment in Build-Pipline integrieren
- Auditing und Compliance berücksichtigen
- Schnelles Feedback liefern, ob Deployment erfolgreich war
- Deployment darf nicht lange dauern

## Deployments vom Release entkoppeln
- Installieren vs. verfügbar machen
- Umgebungsbasiert
  - Traffic umleiten
  - Blue-Green
- Anwendungsbasiert
  - Feature-Flag nutzen
  - Feature-Toggel umlegen und neue Funktion ist verfügbar
- Dark Lunches durchführen
  - Funktionalität für User noch nicht sichtbar
  - Lasttest durchführen im Hintergrund
  - Big-Bang-Release wird dadurch verhindert

## Übersicht Continuous Delivery und Continuous Deployment
- Deployments sollen ein geringes Risiko haben
- Sind leicht durchführbar
- Operations-Arbeit soll humaner werden

# 13 Architektur für risikoarme Releases
- Architektur muss sich weiterentwickeln
- Strangler-Application-Muster
- Bestehende Funktionalität hinter API verstecken
- Eng gekoppelte Architektur erfordert ein hohes Maß an Kommunikations und Koordination
- Serviceorientierte Architekturen enabled kleine Teams
- Monolith vs. Microservice
- Bsp. Amazon
  - Strikte serviceorientierte Architektur
  - Verbot von direkten Datenbankzugriffen
  - Entwicklung- und Operations-Prozess

# Strangler
- API muss sauber definiert und muss unverändert bleiben
- Teile vom Altsystem Stück für Stück abkoppeln
- Architektur entscheidet darüber wie produktiv das Team ist

