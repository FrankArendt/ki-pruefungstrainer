# KI-Prüfungstrainer

Lernkarten und Multiple-Choice-Quiz zur Vorbereitung auf die Prüfung „Digitalisierungsmanager für Prozessautomatisierung und Künstliche Intelligenz“.

## Funktionen

- **696 Lernkarten** in 16 Themenblöcken
- **Ausrichtung am Prüfungskatalog:** Jede Karte ist einem der zehn Kenntnisbereiche K1–K10 zugeordnet (611 Karten) oder als sonstiges Thema markiert (85 Karten)
- **Gewichtete Auswahl:** Quiz und Lernkarten ziehen Prüfungsthemen mit Gewicht 3, sonstige Themen mit Gewicht 2
- **Prüfungssimulation:** 30 gewichtet gezogene Fragen mit Auswertung je Prüfungsbereich
- **Drei Schwierigkeitsstufen:** Einfach, Mittel, Schwer
- **Lernkarten mit Wiederholungslogik:** „Gewusst“ und „Nicht gewusst“ steuern, wann eine Karte wiederkommt; nach dreimal „Gewusst“ in Folge gilt sie als sicher
- **Weiterführende Quellen** auf jeder Karte: Hochschulangebote (Elements of AI, KI-Campus, openHPI), Fachdokumentationen und Kurzvideos unter 4 Minuten
- **Quiz:** Jede Karte ist zugleich eine Multiple-Choice-Frage mit vier Antworten; wählbar nach Prüfungsbereich, Thema, Stufe und Umfang (5, 10, 20, 30, 50, 100 oder alle Fragen), mit Erklärung nach jeder Antwort, Auswertung je Prüfungsbereich und Wiederholung der falsch beantworteten Fragen
- **Fortschritt:** Lernstand je Thema und Stufe, Stand und Trefferquote je Prüfungsbereich, Quiz-Verlauf
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
| Geschäftsprozesse, Organisation & Reifegrad | Aufbau-/Ablauforganisation, Matrix, CMMI, ERP/DMS |
| Wertstrom- & Ursachenanalyse | Ishikawa, 5-Why, Pareto, Wertstromkarte, PDCA |
| No-Code-Plattformen | Trigger/Aktion, Konnektoren, Mapping, Plattformvergleich, Testkonzept, Doku |
| Dokumentenverarbeitung & Chatbots | IDP-Pipeline, Konfidenz, E-Rechnung, Intent/Entity, Fallback, Voicebot |
| Informationssicherheit & Compliance | Schutzziele, ISMS/ISO 27001, NIS-2, GoBD, TOM an Fallbeispielen |
| Entscheidungsvorlagen & Qualitätssicherung | Pyramidenprinzip, belastbare Empfehlungen, QS-Plan, Stichproben |

## Prüfungsbereiche und Gewichtung

| Bereich | Inhalt |
|---|---|
| K1 | Digitale Geschäftsprozesse, Organisation & Reifegrad |
| K2 | Prozessaufnahme & -modellierung (BPMN, Wertstrom, Ursachen) |
| K3 | Kennzahlensysteme & Automatisierungspotenzial |
| K4 | KI-Grundlagen, Grenzen & Abgrenzung |
| K5 | No-Code-Plattformen & Workflows |
| K6 | Große Sprachmodelle, Risiken & Ergebnisqualität |
| K7 | Dokumentenverarbeitung & Chatbots |
| K8 | Datenanalyse, Visualisierung & Empfehlungen |
| K9 | Datenschutz, Informationssicherheit & Compliance |
| K10 | Veränderungs- & Projektmanagement |

Die Auswahl ist gewichtet ohne Zurücklegen (Schlüssel = Zufallszahl^(1/Gewicht)). Prüfungskarten haben Gewicht 3, sonstige Karten Gewicht 2. Bei allen Karten stammen dadurch rund 91 % der gezogenen Fragen aus Prüfungsthemen. Bei den Lernkarten bleibt die Wiederholungslogik vorrangig, die Gewichtung entscheidet bei gleichem Lernstand.

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
{ id: "p12", t: "prompt", l: 2, k: "K6", q: "Frage", a: "Erklärung auf der Rückseite",
  c: "richtige Antwort", w: ["falsch 1", "falsch 2", "falsch 3"] }
```

- `t`: Themen-ID (`prompt`, `llm`, `bpmn`, `kpi`, `n8n`, `assist`, `data`, `change`, `privacy`, `strategy`, `orga`, `lean`, `nocode`, `idp`, `infosec`, `decide`)
- `k`: Prüfungsbereich `K1` bis `K10`, oder `null` für sonstige Themen (bestimmt das Gewicht 3 bzw. 2)
- `l`: Stufe (1 = einfach, 2 = mittel, 3 = schwer)
- `id`: dauerhafte Kennung – nicht ändern, sonst geht der gespeicherte Lernstand dieser Karte verloren

Die Quellen je Thema stehen im Objekt `SRC`.

## Hinweise

- Die Zuordnung zu den Prüfungsbereichen folgt den im Prüfungskatalog genannten Kenntnisbereichen und Kompetenzen. Die Karten selbst sind eigene Formulierungen, keine offiziellen Prüfungsfragen.
- Die Karten wurden auf Basis des Wissensstands Mitte 2026 erstellt und nicht einzeln mit Quellen abgeglichen. Fragen zu Recht und Datenschutz zielen auf Konzepte, nicht auf Gesetzeswortlaut; sie ersetzen keine Rechtsberatung.
- Quellen-Links und Lesezeiten sind Richtwerte. Video-Links öffnen eine YouTube-Suche, gefiltert auf Videos unter 4 Minuten.
