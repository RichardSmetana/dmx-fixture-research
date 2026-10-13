# dmx-fixture-research

Reverse engineering, DMX channel mappings, documentation and fixture profiles for vintage and unidentified stage lighting equipment.

Technische Dokumentation und DMX-Fixture-Datenbank für ältere, unbekannte oder schlecht dokumentierte Scheinwerfer. Ziel ist, Messungen und Kanalbelegungen so festzuhalten, dass andere Lichttechniker die Geräte ohne erneute Recherche nutzen können.

> **Status:** privat — inhaltlich auf eine spätere öffentliche Freigabe vorbereitet. Der Ordner `raw/` bleibt lokal und wird nicht veröffentlicht.

## Geräteverzeichnis

| Gerät | Typ | DMX-Modi | Forschungsstand | Ordner |
| --- | --- | --- | --- | --- |
| Fixture 01 | LED PAR | Unbekannt | Offen | [fixture-01-led-par](fixtures/fixture-01-led-par/) |
| Fixture 02 | Moving Head | Unbekannt | In Untersuchung | [fixture-02-moving-head](fixtures/fixture-02-moving-head/) |
| Fixture 03 | LED Bar | Unbekannt | Offen | [fixture-03-led-bar](fixtures/fixture-03-led-bar/) |
| Fixture 04 | Effektgerät | Unbekannt | Offen | [fixture-04-effect-light](fixtures/fixture-04-effect-light/) |
| Fixture 05 | Unbekannt | Unbekannt | Offen | [fixture-05-unknown](fixtures/fixture-05-unknown/) |

Die Ordnernamen sind Platzhalter. Nach der Identifikation eines Geräts den Ordner umbenennen, z. B. `fixture-02-moving-head` → `zq00245001-moving-head`, und diese Tabelle aktualisieren.

## Aufbau pro Gerät

Jeder Gerätetyp verwendet dieselbe Struktur:

```text
fixtures/<geräte-id>/
  README.md          — Beschreibung & technische Daten
  dmx-channels.md    — Kanalbelegung je DMX-Modus
  test-notes.md      — Messungen, Besonderheiten, offene Fragen
  photos/            — Gerätebilder
  profiles/          — Steuerungsprofile (.qxf, optional .json)
```

### Was dokumentiert wird

1. **Geräteidentifikation** — Fotos (Vorderseite, Rückseite, Anschlüsse, Typenschild, Display, ggf. Platine), Abmessungen, LED-Bestückung, Versorgungsspannung, Beschriftungen, vermutete baugleiche Modelle.
2. **DMX-Kanalbelegung** — alle Modi getrennt; Kanalnummer, Funktion, Wertebereiche 0–255, Richtung der Effekte, Besonderheiten.
3. **Experimentelle Ergebnisse** — getestete Werte, verifizierte vs. vermutete Funktionen, Firmware-Versionen, Unterschiede zwischen Exemplaren.
4. **Fixture-Profile** — importierbare Dateien für Lichtsteuerungssoftware (zuerst QLC+ `.qxf`).

### Status der Kanalzuordnung

Bei unbekannten Geräten immer einen der drei Zustände angeben:

| Status | Bedeutung |
| --- | --- |
| **Verifiziert** | Am Gerät getestet und bestätigt |
| **Vermutet** | Plausibel, aber noch nicht sicher belegt |
| **Offen** / **Unbekannt** | Noch nicht oder nicht ausreichend geprüft |

## Forschungsablauf

1. Gerät fotografieren (Gehäuse, Anschlüsse, Etiketten, Bedienelemente)
2. Identifikation recherchieren (Modellnummern, baugleiche Geräte, Manuals)
3. DMX-Modi bestimmen (Menüoptionen, verfügbare Kanalzahlen)
4. Kanäle systematisch testen (Funktionen und Wertebereiche protokollieren)
5. Steuerungsprofil erstellen (QLC+-Datei anlegen und mit dem Gerät prüfen)
6. Ergebnisse veröffentlichen (README aktualisieren, offene Fragen dokumentieren)

Offene Einzelfragen können als GitHub Issues geführt werden (z. B. „CH7: Effekt ab DMX-Wert 132 noch ungeklärt“), damit die Gerätedokumentation übersichtlich bleibt.

## Dateiformate

| Format | Verwendungszweck | Priorität |
| --- | --- | --- |
| `.md` | Gerätebeschreibung, Tabellen, Forschung | Sehr hoch |
| `.jpg` / `.png` | Fotos, Platinen, Bedienelemente | Sehr hoch |
| `.qxf` | Importierbare QLC+-Gerätedefinition | Hoch |
| `.json` | Open Fixture Library | Optional |
| `.pdf` | Eigene Anleitungen und Datenblätter | Optional |

## Veröffentlichung (Checkliste)

Vor dem Umschalten auf **public**:

- [ ] Mindestens ein Gerät mit verifizierter Kanalbelegung dokumentiert
- [ ] Eigene Fotos in `fixtures/*/photos/` (keine fremden Manuals ohne Erlaubnis)
- [ ] Keine privaten Pfade, Namen oder Internas in Markdown/Issues
- [ ] `raw/` enthält nichts Commitbares (weiterhin in `.gitignore`)
- [ ] README-Geräteverzeichnis aktualisiert (echte Namen, Modi, Stand)
- [ ] Lizenzhinweis GPL-3.0 und Urheberangaben geprüft
- [ ] Optional: QLC+-Profile (`.qxf`) getestet und abgelegt

Danach auf GitHub: Repository → **Settings** → Visibility → **Public** (oder `gh repo edit --visibility public`).

## Lizenz und Beiträge

- Inhalt dieses Repositorys: [GNU General Public License v3.0](LICENSE) (GPL-3.0).
- Fremde Handbücher nur mit Erlaubnis hochladen; sonst auf die Fundstelle verlinken.
- Nach der öffentlichen Freigabe: Pull Requests und Issues für Korrekturen, neue Geräte und ungeklärte Kanäle willkommen.
