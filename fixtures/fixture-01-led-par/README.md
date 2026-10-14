# Fixture 01 — LED PAR (RGBWAUV Wireless)

| Feld | Wert |
| --- | --- |
| Platzhalter-ID | `fixture-01-led-par` |
| Typ | LED PAR / Color Changer |
| Profil-Hersteller | dmx-fixture-research |
| Hardware-Hersteller / Modell | Unbekannt / Rasha-kompatibler OEM — RGBWAUV Wireless PAR 7CH-12CH |
| Forschungsstand | In Untersuchung |
| DMX-Modi | 7CH verifiziert; 12CH Strobe (CH9) auf V2.20 geprüft, übrige Kanäle vermutet |
| Firmware | V2.20 |
| Versorgung | AC 90–240 V (Aufdruck am Gerät); 90 W nur Profilwert |
| Exemplare im Bestand | — |
| Dokumentationsstand | [Anleitung Rev. 1.1](manual.md) – Oktober 2026 |

## Kurzbeschreibung

Kompakter RGBWAUV-LED-PAR mit sieben Optiken, DMX512 (3-poliger XLR, Ein und Aus), 2,4-GHz-Wireless-DMX, Standalone, Sound und Master/Slave. Bedienfeld und Menü ähneln dem Rasha Professional HEX V12 Wireless Flat PAR. Der Hardware-Hersteller ist nicht nachgewiesen.

Der **7-Kanal-Modus** ist am Gerät verifiziert: Rot, Grün, Blau, Weiß, Amber, UV, Strobe. Im **12-Kanal-Modus** liegen Amber und Weiß vertauscht (Amber CH4, Weiß CH5). Die Strobe-Bereiche auf CH9 sind auf Firmware V2.20 geprüft. Die übrigen 12CH-Kanäle folgen der Fixture-Definition und sind noch nicht vollständig nachgemessen.

Profil: [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf) (QLC+ 5.2.2). Das Feld `Manufacturer` darin ist `dmx-fixture-research` und bezeichnet dieses Projekt, nicht den Gerätehersteller. Der 7CH-Modus heißt im Profil `7 Channel  - probable Rasha/OEM`; die Kanalbelegung selbst ist verifiziert.

Der Ordnername bleibt der Platzhalter, bis Typenschild und Modell feststehen.

## Identifikation

### Beschriftungen und Typenschild

- Modellnummer: nicht erfasst (Arbeitsname: RGBWAUV Wireless PAR 7CH-12CH)
- Seriennummer:
- Firmware am Gerät: V2.20 (`Ver` im Menü)
- Weitere Aufkleber / Logos: CE, WEEE und RoHS auf der Rückseite. Kein Hersteller- oder Modellname lesbar. Menü ähnlich Rasha HEX V12.

### Technische Daten

Profilwerte sind keine Labormessung. Lumen und Farbtemperatur im QLC+-Profil stehen auf 0.

| Eigenschaft | Wert | Quelle |
| --- | --- | --- |
| Abmessungen (B×H×T) | 220 × 220 × 90 mm | QLC+-Profil, nicht unabhängig geprüft |
| Gewicht | 1 kg | QLC+-Profil, nicht unabhängig geprüft |
| LED-Bestückung | 7 Optiken, Anordnung 2–3–2, RGBWAUV | Foto Vorderseite / verifizierter 7CH-Modus |
| Strahlwinkel | Fresnel, fest, 25–40° | QLC+-Profil, nicht unabhängig geprüft |
| Versorgungsspannung | AC 90–240 V, Aufdruck „POWER IN“. Frequenz nicht aufgedruckt | Foto Rückseite |
| Leistungsaufnahme | 90 W | QLC+-Profil |
| Umgebungstemperatur | konservativ max. 45 °C, bis das Schild bestätigt ist | Rasha-Doku nennt 45 °C und 50 °C |
| DMX In/Out | 3-poliger XLR, Beschriftung DMX OUT und DMX IN; Stabantenne für Wireless-DMX | Foto Rückseite |
| Netz Ein/Aus | IEC-Eingang „POWER IN“ und IEC-Ausgang „POWER OUT“. Sicherungswert nicht lesbar | Foto Rückseite |
| Display / Menü | 4-stellige 7-Segment-Anzeige. Tasten von links: MENU, DOWN, UP, ENTER. Firmware V2.20 | Foto Rückseite / Anleitung Rev. 1.1 |
| Vermutete baugleiche Modelle | Rasha Professional HEX V12 Wireless Flat PAR | ähnliches Menü; 32 DMX-Farbpresets der Rasha-Doku werden nicht verwendet |

### Menü (Kurz)

Ausführlich in [manual.md](manual.md). `Addr` 001–512, `Chnd` 7/12, `SLnd` Slav/Nast/Sync/CliC, `CoLo` 1–38, `FADE` 1–3, `FLAS` 1–100, `Auto` 1–9, `Soun` 1–6, `Cust` CC1–CC5, `Dinn` 1–3, `Blnd`, `LED`, `Disp`, `Test`, `Fhrs`, `Ver`, `Rest`.

Die 38 Menüfarben sind unabhängig von den acht DMX-Bereichen auf CH7 im 12CH-Modus.

### Fotos

| Datei | Inhalt |
| --- | --- |
| [photos/front-optics.jpg](photos/front-optics.jpg) | Vorderseite, sieben LED-Optiken, Bügel |
| [photos/rear-three-quarter.jpg](photos/rear-three-quarter.jpg) | Rückseite schräg, Display, Bügel, Lüftung |
| [photos/rear-panel.jpg](photos/rear-panel.jpg) | Anschlüsse, Tasten, Aufdruck AC 90–240 V |

Noch offen: Typenschild mit Hersteller und Modell, Sicherungswert, Platine.

## Dokumentation in diesem Ordner

| Datei | Inhalt |
| --- | --- |
| [manual.md](manual.md) | Bedienungsanleitung Rev. 1.1 |
| [dmx-channels.md](dmx-channels.md) | Kanalbelegung mit Forschungsstatus |
| [test-notes.md](test-notes.md) | Messungen und offene Punkte |
| [profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf) | QLC+-Fixture, Stand der installierten Definition |

## Offene Fragen

- [x] Netzspannung am Gehäuse lesbar (AC 90–240 V)
- [ ] Hardware-Hersteller, Modell, Sicherungswert, Umgebungstemperatur
- [x] DMX-Modi und Kanalzahlen bekannt (7 und 12)
- [x] 7CH-Modus verifiziert
- [x] 12CH CH9 Strobe-Bereiche auf Firmware V2.20 geprüft
- [ ] 12CH Farbkanäle, Presets, Dimmer und CH10–CH12 am Gerät gegengeprüft
- [ ] Dimmerkurven `Dinn` 1–3, Sound-Programme 1–6, Sync/CliC
- [ ] Wireless-Pairing des verbauten Empfängers
- [x] QLC+-Profil entspricht der installierten Definition
- [ ] Profil mit dem Gerät gefahren
