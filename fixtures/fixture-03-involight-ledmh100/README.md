# Fixture 03 — INVOLIGHT LEDMH100

| Feld | Wert |
| --- | --- |
| ID | `fixture-03-involight-ledmh100` |
| Typ | LED Moving Head, RGB |
| Profil-Hersteller | dmx-fixture-research |
| Hardware-Hersteller / Modell | INVOLIGHT LEDMH100 |
| Forschungsstand | In Untersuchung |
| DMX-Modi | 9 Kanäle bei `16BT` OFF, 11 Kanäle bei `16BT` ON. Aus der Herstellerdoku, nicht am Gerät gemessen |
| Firmware | |
| Versorgung | Aufdruck am Sockel: AC IN 220V 50Hz. Leistung 160 W nur in Manual und Profil |
| Exemplare im Bestand | — |
| Dokumentationsstand | [Anleitung Rev. 1.0](manual.md) – Oktober 2026 |

## Kurzbeschreibung

Kompakter LED-Moving-Head mit einem Feld einzelner LED-Optiken, Pan und Tilt. Die ersten neun Kanäle sind in beiden Modi gleich. `16BT` ON hängt Pan-fein und Tilt-fein als CH10 und CH11 an.

**CH6 ist ein invertierter Dimmer.** DMX 0 ist volle RGB-Helligkeit, 255 ist dunkel. Das QXF bildet das so ab. Ein normaler QLC+-Regler wird erst hell, wenn im Workspace der Modifier `Inverted` auf diesem Kanal liegt. Der Modifier steckt nicht in der `.qxf`.

Profil: [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf) (QLC+ 5.2.1). Das Feld `Manufacturer` ist `dmx-fixture-research` und bezeichnet dieses Projekt. Der Hardware-Hersteller ist INVOLIGHT.

## Identifikation

### Beschriftungen

- Modell: LEDMH100, aus dem Herstellermanual und dem Profil. Auf den Fotos nicht als Typenschild lesbar
- Sockel hinten, von links: DMX IN, AC IN 220V 50Hz, POWER SWITCH, DMX OUT
- Display: 4-stellig an der Sockelvorderseite
- Seriennummer:
- Firmware:

### Technische Daten

Lumen im Profil: 528. Farbtemperatur: 0. Die 160 W sind die Herstellerangabe, nicht die Summe aus 36 × 1 W.

| Eigenschaft | Wert | Quelle |
| --- | --- | --- |
| Lichtquelle | 36 × 1 W LED, RGB. Foto zeigt ein Feld einzelner Optiken, nicht nachgezählt | Herstellerdoku / Foto |
| Pan / Tilt | 540° / 230° | Herstellerdoku und QXF, nicht gemessen |
| Abstrahlwinkel | 23°, fest im Kopf | QXF / Herstellerdoku |
| Abmessungen (B×H×T) | 220 × 376 × 250 mm | QXF / Herstellerdoku, nicht gemessen |
| Gewicht | 7 kg | QXF / Herstellerdoku, nicht gemessen |
| Versorgung | AC IN 220V 50Hz, Netzschalter, Kabel am Sockel | Foto Rückseite |
| Leistungsaufnahme | 160 W | Herstellerdoku und QXF. Nicht auf dem fotografierten Schild |
| Umgebungstemperatur | max. 40 °C, nur innen | Herstellerdoku |
| DMX | 3-polig, IN und OUT beschriftet. Modi 9 und 11 | Foto / Herstellerdoku |
| Display / Menü | 4-stellige Anzeige. Tasten FUN, UP, DOWN, ENTER | Foto Anzeige / Herstellerdoku für die Tastennamen |

### Menü (Kurz)

Ausführlich in [manual.md](manual.md). `M-DM` DMX, `M-AU` Automatik, `M-SO` Sound, `PR1`–`PR8`, `SP01`–`SP15`, `r PAN`, `R TILT`, `r-PT`, `TEST`, `DISP`, `REST`, `16BT` ON/OFF.

`16BT` OFF ist der 9-Kanal-Modus, ON der 11-Kanal-Modus. Der QLC+-Modus muss dazu passen.

### Fotos

| Datei | Inhalt |
| --- | --- |
| [photos/front-leds.jpg](photos/front-leds.jpg) | LED-Feld, Bügel, Sockel |
| [photos/base-display.jpg](photos/base-display.jpg) | Seite, 4-stellige Anzeige |
| [photos/rear-connectors.jpg](photos/rear-connectors.jpg) | DMX IN, AC IN 220V 50Hz, Netzschalter, DMX OUT |

Noch offen: Typenschild mit Modell und 160 W, Tastenbeschriftung aus der Nähe.

## Dokumentation in diesem Ordner

| Datei | Inhalt |
| --- | --- |
| [manual.md](manual.md) | Bedienungsanleitung Rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 9- und 11-Kanal-Belegung |
| [test-notes.md](test-notes.md) | Quellen und offene Messungen |
| [profiles/Involight_LEDMH100.qxf](profiles/Involight_LEDMH100.qxf) | QLC+-Fixture |

## Offene Fragen

- [x] Netzanschluss am Gerät gelesen: AC IN 220V 50Hz, Schalter, DMX IN/OUT
- [ ] Typenschild mit Modell und 160 W
- [ ] Dimmer-Inversion und Strobe-Richtung am Gerät geprüft
- [ ] `16BT` gegen die beiden QLC+-Modi gefahren
- [ ] Pan 540° und Tilt 230° gemessen
- [x] QLC+-Profil entspricht der installierten Definition
- [ ] Profil mit dem Gerät gefahren
