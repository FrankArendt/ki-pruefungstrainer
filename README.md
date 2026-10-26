# KI-Prüfungstrainer

Lernkarten und Multiple-Choice-Quiz zur Vorbereitung auf die Prüfung „Digitalisierungsmanager für Prozessautomatisierung und Künstliche Intelligenz“.

## Funktionen

- **611 Lernkarten** in 10 Themenblöcken, je rund 61 Karten pro Thema
- **Drei Schwierigkeitsstufen:** Einfach, Mittel, Schwer (je etwa 20 Karten pro Thema und Stufe)
- **Lernkarten mit Wiederholungslogik:** „Gewusst“ und „Nicht gewusst“ steuern, wann eine Karte wiederkommt; nach dreimal „Gewusst“ in Folge gilt sie als sicher
- **Weiterführende Quellen** auf jeder Karte: Hochschulangebote (Elements of AI, KI-Campus, openHPI), Fachdokumentationen und Kurzvideos unter 4 Minuten
- **Quiz:** Jede Karte ist zugleich eine Multiple-Choice-Frage mit vier Antworten; wählbar nach Thema, Stufe und Umfang (5, 10, 20, 50, 100 oder alle Fragen), mit Erklärung nach jeder Antwort und Wiederholung der falsch beantworteten Fragen
- **Fortschritt:** Lernstand je Thema und Stufe, Quiz-Verlauf und Durchschnitt je Thema
- **Speicherung:** im Browser, über einen privaten GitHub-Gist zwischen Geräten oder im Claude-Konto (wenn über Claude geöffnet); zusätzlich Sicherungscode zum Übertragen
- Optimiert für iPad, nutzbar auf Rechner und Smartphone, heller und dunkler Modus

## Themen

| Thema | Beispiele |
|---|---|
| Prompt Engineering | Few-Shot, Chain-of-Thought, Prompt-Ketten, Golden Set, Structured Outputs |
| KI-Grundlagen & Sprachmodelle | Token, Kontextfenster, Halluzination, RAG, Embeddings, Fine-Tuning |
| Prozessaufnahme & BPMN | Ereignisse, Gateways, Pools/Lanes, Lean, Process Mining, DMN |
| Kennzahlen, Priorisierung & ROI | ROI, Amortisation, Kapitalwert, TCO, Scoring-Modelle |
| Automatisierung mit n8n & KI | Trigger, Webhooks, Fehlerbehandlung, AI-Agent-Node, Idempotenz |
| KI-Assistenten konfigurieren | Custom GPTs, Claude-Projekte, Copilot Studio, MCP, Prompt Injection |
| Datenanalyse & Visualisierung | Diagrammwahl, Median, Perzentile, Datenqualität, Verzerrungen |
| Projekt- & Change-Management | Scrum, Kanban, Kotter, ADKAR, Stakeholder, kritischer Pfad |
| Datenschutz & KI-Compliance | DSGVO-Grundsätze, AI-Act-Risikostufen, Betreiberpflichten |
| Digitalisierungsvorhaben & Strategie | Make or Buy, PoC/Pilot, Reifegrad, Governance, Roadmap |

## Nutzung

Die App ist eine einzelne Datei (`index.html`) ohne Build-Schritt und ohne Abhängigkeiten. Sie lässt sich direkt im Browser öffnen oder über GitHub Pages bereitstellen:

1. Repository → **Settings** → **Pages**
2. Source: **Deploy from a branch**, Branch `main`, Ordner `/ (root)` → **Save**
3. Nach ein bis zwei Minuten ist die App unter `https://<benutzer>.github.io/ki-pruefungstrainer/` erreichbar.

**Auf dem iPad:** Adresse in Safari öffnen → Teilen → „Zum Home-Bildschirm“. Die App startet dann wie eine normale App.

## Synchronisierung zwischen Geräten (GitHub Gist)

Ohne Einrichtung speichert die App nur im Browser des jeweiligen Geräts. Für die Synchronisierung zwischen iPad und Rechner legt die App den Lernstand als privaten Gist (`ki-pruefungstrainer.json`) in deinem GitHub-Konto ab. Die ausführliche Anleitung mit Statusanzeige und Fehlerhilfe steht in der App im Reiter **Setup**. Kurzfassung:

1. [Zugangsschlüssel erstellen](https://github.com/settings/tokens/new?scopes=gist&description=KI-Pr%C3%BCfungstrainer) – „Personal access token (classic)“, nur Scope **gist**, Laufzeit nach Wahl.
2. In der App unter **Setup** den Schlüssel (`ghp_…`) eintragen und **Verbinden** tippen. Die App legt den Gist an oder findet einen vorhandenen.
3. Auf jedem weiteren Gerät denselben Schlüssel eintragen. Auf dem iPad in der Home-Bildschirm-App verbinden, nicht nur in Safari – beide haben getrennte Speicher.

Der Schlüssel bleibt im Browser des Geräts und wird nur an api.github.com gesendet. Er darf ausschließlich Gists lesen und schreiben. Widerrufen: GitHub → Settings → Developer settings → Personal access tokens.

Wird die App über Claude geöffnet, speichert sie im Claude-Konto. Zwischen beiden Speichern lässt sich der Stand per Sicherungscode (Reiter **Fortschritt**) übertragen.

## Aufbau der Karten

Die Karten stehen im Array `CARDS` in `index.html`. Jede Karte hat folgende Felder:

```js
{ id: "p12", t: "prompt", l: 2, q: "Frage", a: "Erklärung auf der Rückseite",
  c: "richtige Antwort", w: ["falsch 1", "falsch 2", "falsch 3"] }
```

- `t`: Themen-ID (`prompt`, `llm`, `bpmn`, `kpi`, `n8n`, `assist`, `data`, `change`, `privacy`, `strategy`)
- `l`: Stufe (1 = einfach, 2 = mittel, 3 = schwer)
- `id`: dauerhafte Kennung – nicht ändern, sonst geht der gespeicherte Lernstand dieser Karte verloren

Die Quellen je Thema stehen im Objekt `SRC`.

## Hinweise

- Die Inhalte beruhen auf den Themen des eigenen Portfolios, nicht auf dem offiziellen Prüfungskatalog von TÜV Rheinland.
- Die Karten wurden auf Basis des Wissensstands Mitte 2026 erstellt und nicht einzeln mit Quellen abgeglichen. Fragen zu Recht und Datenschutz zielen auf Konzepte, nicht auf Gesetzeswortlaut; sie ersetzen keine Rechtsberatung.
- Quellen-Links und Lesezeiten sind Richtwerte. Video-Links öffnen eine YouTube-Suche, gefiltert auf Videos unter 4 Minuten.
