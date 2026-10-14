# Fixture 04 — LED PAR 36× RGB (DIP)

| Feld | Wert |
| --- | --- |
| ID | `fixture-04-led-par-36x-rgb` |
| Typ | RGB-LED-PAR / Color Changer |
| Profil-Hersteller | dmx-fixture-research |
| Hardware-Hersteller / Modell | Unbekannt. Arbeitsname LED PAR 36× RGB (DIP) |
| Forschungsstand | In Untersuchung |
| DMX-Modi | 8 Kanäle. RGB, CH6-Effekte, CH8-Dimmer am Gerät geprüft. Strobe und Makrogrenzen offen |
| Firmware | |
| Versorgung | Aufdruck AC90–250V, festes Netzkabel |
| Exemplare im Bestand | — |
| Dokumentationsstand | [Anleitung Rev. 1.0](manual.md) – Oktober 2026 |

## Kurzbeschreibung

Runder RGB-PAR mit einem Feld einzelner LED-Optiken, Bügel und 10 DIP-Schaltern. Ein Modus mit 8 Kanälen. Hersteller und Modellnummer sind nicht bekannt. Ähnliche PARs haben andere Maps. Es gilt die Messung an diesem Exemplar.

**CH6 schaltet den Effekt, nicht die Geschwindigkeit.** 0–127 ist automatischer Farbwechsel, Tempo auf CH7. 128–255 ist Farbüberblendung, Tempo auf CH4. CH6 = 0 ist bereits Farbwechsel, nicht „Effekt aus“.

**CH8 ist ein normaler Dimmer.** 0 ist aus, 255 ist voll.

Profil: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf) (QLC+ 5.2.1), Modus `8 Channel - research`. Das Feld `Manufacturer` ist `dmx-fixture-research`.

## Identifikation

### Beschriftungen

- Modellnummer: nicht vorhanden
- Rückseite: CE, AUTO, MUSIC, SPEED-Regler, grüne DMX-Signallampe, 10 rote DIP-Schalter
- DMX IN mit Aufdruck `1:G`, `2:-`, `3:+`. Daneben DMX OUT
- Unten: AC90–250V. Netzkabel fest durch eine Tülle, kein separater Gerätestecker
- Seriennummer: keine

### Technische Daten

20 W, 1,5 kg, 200 × 200 × 200 mm und 15° stehen nur im QXF und sind nicht gemessen. Lumen und Farbtemperatur im Profil sind 0.

| Eigenschaft | Wert | Quelle |
| --- | --- | --- |
| Optik | Feld einzelner LED-Linsen, RGB. 36 Stück laut Arbeitsname, nicht nachgezählt | Foto / Arbeitsname |
| Versorgung | AC90–250V, festes Kabel | Foto Rückseite |
| Leistungsaufnahme | 20 W | nur QXF |
| Abmessungen / Gewicht | 200 × 200 × 200 mm, 1,5 kg | nur QXF |
| Abstrahlwinkel | 15°, Fokus fest, kein Pan/Tilt | nur QXF |
| DMX | 8 Kanäle, 3-polig IN und OUT | Messung / Foto |
| Adresse | DIP 1–9 binär. DIP 10 ungeklärt. Adresse 1 mit nur DIP 1 ein wurde beim Test benutzt | Messung / übliche Binäradresse |
| Standalone | AUTO, MUSIC, SPEED | Foto. Ablauf nicht protokolliert |

### Fotos

| Datei | Inhalt |
| --- | --- |
| [photos/front-leds.jpg](photos/front-leds.jpg) | LED-Feld, Bügel |
| [photos/front-side.jpg](photos/front-side.jpg) | Seite, Kühlrippen, Bügel |
| [photos/rear-panel.jpg](photos/rear-panel.jpg) | DIP, AUTO, MUSIC, SPEED, DMX, AC90–250V |

## Dokumentation in diesem Ordner

| Datei | Inhalt |
| --- | --- |
| [manual.md](manual.md) | Bedienungsanleitung Rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 8-Kanal-Belegung mit Messstatus |
| [test-notes.md](test-notes.md) | Gemessene Werte und offene Punkte |
| [profiles/LED_PAR_36x_RGB_(DIP).qxf](profiles/LED_PAR_36x_RGB_(DIP).qxf) | QLC+-Fixture |

## Offene Fragen

- [ ] Hersteller und Modell
- [x] 8-Kanal-DMX, RGB, CH6-Bereiche, CH8-Richtung
- [ ] CH4-Farbgrenzen und Richtung der beiden Tempi
- [ ] CH5 Strobe-Grenzen und Richtung
- [ ] DIP 10, AUTO, MUSIC, SPEED
- [ ] Ob es einen Wert gibt, der Automatik ganz abschaltet. CH6 = 0 tut das nicht
- [ ] Leistung, Maße, Gewicht, Winkel
- [x] QLC+-Profil entspricht der installierten Definition
- [ ] Profil mit dem Gerät gegengeprüft, soweit die offenen Kanäle reichen
