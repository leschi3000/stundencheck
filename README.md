# StundenCheck

**Vor der Stunde in 30 Sekunden ausfüllen – passende Unterrichtsanpassungen erhalten.**

Die Lehrkraft tippt an, was heute los ist (z. B. *sehr unruhig, drei Kinder krank, Sprachbarrieren, Praktikantin dabei*) – die App schlägt didaktisch begründete Anpassungen vor (z. B. *Partnerarbeit statt Gruppenarbeit, Visualisierung ergänzen, Audioversion bereitstellen, Bewegungsphase nach 15 Minuten*).

> **Keine Diagnostik, sondern adaptive Unterrichtsplanung.** Die Vorschläge sind Impulse – die pädagogische Entscheidung bleibt bei der Lehrkraft.

## Funktionen

- ✅ **30-Sekunden-Check**: Faktoren antippen (Klasse, einzelne Kinder, Lernvoraussetzungen, Rahmenbedingungen, Stundenplanung)
- ✅ **Regelbasierte Vorschläge** mit Begründung („weil: sehr unruhig + Gruppenarbeit geplant“), gruppiert nach Sozialform, Aufgaben, Material, Rhythmus, Klima, Organisation
- ✅ **Klassenstufe 1–13 einstellbar** – Formulierungen und Zeitangaben passen sich an (Grundschule / Sek I / Sek II)
- ✅ **Eigene Faktoren + eigene Vorschläge** anlegbar
- ✅ **Verlauf** der Checks, Kopieren & JSON-Export
- ✅ **Optionale KI-Verfeinerung** mit eigenem Anthropic-API-Key (Claude) – die App funktioniert aber komplett ohne
- ✅ **Datenschutzfreundlich**: eine einzige HTML-Datei, keine Server, kein Konto, kein Tracking; alle Daten bleiben im Browser (localStorage)
- ✅ Hell-/Dunkelmodus, mobil optimiert

## Nutzung – drei Möglichkeiten

### 1. Datenschutzkonform ohne Hosting (empfohlen für die Schule)
Die Datei [`index.html`](index.html) herunterladen und direkt im Browser öffnen (Doppelklick) – funktioniert offline, auch auf dem Dienst-iPad (z. B. über „Dateien“). Es verlässt nichts das Gerät.

### 2. GitHub Pages (sofort online)
Dieses Repository wird automatisch über GitHub Pages ausgeliefert:
**https://leschi3000.github.io/stundencheck/**

### 3. Vercel (eigenes Hosting)
1. Auf [vercel.com](https://vercel.com) mit GitHub anmelden
2. „Add New → Project“ → dieses Repository `stundencheck` importieren
3. Keine Einstellungen nötig (statische Seite) → **Deploy**
4. Fertig – Vercel deployt bei jedem Push automatisch neu

## KI-Verfeinerung (optional)

In den Einstellungen kann ein eigener [Anthropic-API-Key](https://console.anthropic.com/) hinterlegt werden. Dann kann Claude die regelbasierten Vorschläge auf die konkrete Faktor-Kombination zuschneiden.

**Datenschutz-Hinweise:**
- Der Key wird ausschließlich lokal im Browser gespeichert
- Gesendet werden nur die angetippten Faktoren und die Klassenstufe – niemals Namen oder Daten einzelner Kinder eingeben
- Die Anfrage geht direkt an die Anthropic-API (USA)

## Technik

Eine einzige `index.html` – Vanilla JS, kein Build, keine Abhängigkeiten. Der Vorschlags-Kern ist eine transparente Regelbasis (`RULES`, `COMBOS` im Quelltext) und lässt sich leicht erweitern.

## Lizenz

MIT – frei nutzbar, gern weitergeben und anpassen.
