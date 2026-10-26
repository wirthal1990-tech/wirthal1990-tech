# Technische Automatisierung mit nachvollziehbarer Übergabe

Ich strukturiere klar abgegrenzte technische Aufgaben und steuere ihre KI-gestützte Umsetzung: Schnittstellen (APIs, über die Programme Daten austauschen), Workflows und Qualitätssicherung. Tests, menschliche Freigaben und eine dokumentierte Übergabe gehören zur Arbeitsweise.

## Drei technische Belege

**1. Kontrollierte Agent-Freigabe — synthetische Demo, PROPOSED**

Ein kleines Offline-Beispiel bindet eine Freigabe an den SHA-256-Hash, den Inhaltsfingerabdruck genau einer Anfrage. Eine geänderte Anfrage, fehlende oder abgelaufene Zustimmung und eine wiederholte Ausführung werden verweigert. Die Aktion schreibt ausschließlich in einen virtuellen Speicher. Der Entwurf ist lokal getestet; ein öffentlicher Link folgt erst nach einer gesonderten Veröffentlichung.

**2. Evidence before go — synthetische Demo, PROPOSED**

Fehlende oder widersprüchliche Belege führen zu `NO_GO`, also einem Ausführungsstopp. Vollständige Belege erlauben zunächst nur `REVIEW_REQUIRED`, die menschliche Prüfung. Auch danach benötigt eine simulierte Freigabe eine eigene, an die Eingaben gebundene Zustimmung. Keine echten Unternehmen, Kontakte oder externen Aktionen. Der Entwurf ist lokal getestet; für diese Fassung ist noch kein öffentliches Repository bestätigt.

Die beiden Entwürfe gehören zum vorgeschlagenen Paket `controlled-automation-showcase`. Nach Erhalt einer freigegebenen Kopie laufen sie ohne Zusatzpakete mit Python 3.11 oder neuer:

```sh
python3 -B -m unittest discover -s agent-approval-demo -p 'test_*.py' -v
python3 -B -m unittest discover -s revops-evidence-demo -p 'test_*.py' -v
```

Die Befehle werden im Demo-Hauptverzeichnis ausgeführt. Tatsächlich geprüft wurde Python 3.14.8; weitere Python-Versionen sind bislang ungetestet.

**3. Ethno-API — vorhandenes öffentliches Daten-Sample**

Das öffentliche Projekt enthält ein laut seiner Dokumentation 400 Einträge umfassendes Beispiel:
[USDA Phytochemical Database JSON](https://github.com/wirthal1990-tech/USDA-Phytochemical-Database-JSON),
[JSON-Sample](https://github.com/wirthal1990-tech/USDA-Phytochemical-Database-JSON/blob/main/ethno_sample_400.json),
[Parquet-Sample](https://github.com/wirthal1990-tech/USDA-Phytochemical-Database-JSON/blob/main/ethno_sample_400.parquet).
Die [Methodik](https://github.com/wirthal1990-tech/USDA-Phytochemical-Database-JSON/blob/main/METHODOLOGY.md) und [Lizenz-/Attributionsangaben](https://github.com/wirthal1990-tech/USDA-Phytochemical-Database-JSON/blob/main/LICENSE) stehen im Originalprojekt. Dort wird für öffentliche Samples CC BY 4.0 angegeben, soweit nicht anders ausgewiesen. Hier werden ausschließlich Links gesetzt. Keine eigene Freigabe für Derivate oder weitere Drittquellen; die Eintragszahl beweist keine wissenschaftliche Validierung.

## Arbeitsweise und Grenzen

Aufgabe und Abnahmekriterien eingrenzen, kleine Umsetzung mit KI-Werkzeugen steuern, positive und negative Tests prüfen, externe Änderungen durch Menschen freigeben lassen und Ergebnisse mit Grenzen übergeben.

Die Demos zeigen eng begrenzte Kontrolllogik. Sie belegen weder produktive Agent-Systeme noch eine laufende Geschäftspipeline, Kundenresultate oder unabhängige manuelle Softwareentwicklung. Code und Texte entstanden mit KI-Unterstützung; die Verantwortung für Prüfung und Veröffentlichung bleibt beim Menschen.

Website und einziger Kontaktweg: [alex-wirth.de](https://alex-wirth.de/)
