# KI-Prüfungstrainer

Lernkarten und Multiple-Choice-Quiz zur Vorbereitung auf die Prüfung „Digitalisierungsmanager für Prozessautomatisierung und Künstliche Intelligenz“.

- 61 Lernkarten in 10 Themenblöcken (Prompt Engineering, KI-Grundlagen, BPMN, Kennzahlen/ROI, n8n, KI-Assistenten, Datenanalyse, Change-Management, Datenschutz/AI Act, Strategie)
- Schwierigkeitsstufen: Einfach, Mittel, Schwer
- Quiz aus den Lernkarten mit Erklärung nach jeder Antwort
- Lernstand und Quiz-Ergebnisse werden gespeichert (im Browser bzw. im Claude-Konto, wenn über Claude geöffnet)
- Sicherungscode zum Übertragen des Fortschritts zwischen Geräten

## Nutzung

Die App ist eine einzelne Datei (`index.html`) ohne Build-Schritt. Einfach im Browser öffnen oder über GitHub Pages bereitstellen:
Settings → Pages → Branch `main`, Ordner `/ (root)`.

Auf dem iPad: Seite in Safari öffnen → Teilen → „Zum Home-Bildschirm“.

## Synchronisierung zwischen Geräten (GitHub Gist)

Ohne Einrichtung speichert die App nur im Browser des jeweiligen Geräts. Für die Synchronisierung zwischen iPad und Rechner legt die App den Lernstand als privaten Gist (`ki-pruefungstrainer.json`) in deinem GitHub-Konto ab. Die ausführliche Anleitung steht in der App im Reiter **Setup**. Kurzfassung:

1. [Zugangsschlüssel erstellen](https://github.com/settings/tokens/new?scopes=gist&description=KI-Pr%C3%BCfungstrainer) – „Personal access token (classic)“, nur Scope **gist**, Laufzeit nach Wahl.
2. In der App unter **Setup** den Schlüssel (`ghp_…`) eintragen und **Verbinden** tippen. Die App legt den Gist an oder findet einen vorhandenen.
3. Auf jedem weiteren Gerät denselben Schlüssel eintragen. Auf dem iPad in der Home-Bildschirm-App verbinden, nicht nur in Safari.

Der Schlüssel bleibt im Browser des Geräts und wird nur an api.github.com gesendet. Er darf ausschließlich Gists lesen und schreiben. Widerrufen: GitHub → Settings → Developer settings → Personal access tokens.

Wird die App über Claude geöffnet, speichert sie im Claude-Konto. Zwischen beiden Speichern lässt sich der Stand per Sicherungscode übertragen.

## Hinweise

Die Inhalte beruhen auf den Themen des eigenen Portfolios, nicht auf dem offiziellen Prüfungskatalog. Quellen-Links und Lesezeiten sind Richtwerte.
