# Testnotizen — Fixture 03 (INVOLIGHT LEDMH100)

## Testumgebung

| Feld | Wert |
| --- | --- |
| Datum | |
| Controller / Software | QLC+ 5.2.1 (Profil); kein Mess-Setup |
| DMX-Interface | |
| Adresse | |
| Firmware | |
| Exemplar | |

## Getestete Werte

Kanalwerte sind noch nicht gemessen.

| Datum | Modus | Kanal | Wert(e) | Beobachtung | Status |
| --- | --- | --- | --- | --- | --- |
| | 9CH / 11CH | CH1–CH11 | siehe [dmx-channels.md](dmx-channels.md) | Reihenfolge wie Herstellerdoku und QXF | Referenzmanual |

## Gesichert

- Sockel hinten, von links: DMX IN, Aufdruck AC IN 220V 50Hz, POWER SWITCH, DMX OUT. Kabel steckt im Netzeingang. Siehe [photos/rear-connectors.jpg](photos/rear-connectors.jpg).
- Vorderseite: Feld einzelner LED-Optiken, Bügel, Sockel.
- Sockelvorderseite: 4-stellige Anzeige.

## Aus der Herstellerdoku und dem Profil

- 36 × 1 W RGB, Pan 540°, Tilt 230°, 23°, etwa 528 lm, 160 W, 7 kg, 220 × 376 × 250 mm, max. 40 °C, nur innen.
- Menü `16BT` OFF = 9 Kanäle, ON = 11 Kanäle. Modusnamen in QLC+: `9-Ch 16BT OFF`, `11-Ch 16BT ON`.
- CH6 invertiert: 0 voll, 255 aus. QXF-Text: „0 = full brightness, 255 = blackout“.
- CH5: 0–15 kein Strobe bzw. schnellste Programmgeschwindigkeit, 16–255 schnell nach langsam.
- CH1: acht Programme in 25er-Blöcken ab 25, Sound ab 225.
- QLC+-Modifier `Inverted` gehört ins Workspace, nicht in die QXF.
- Leistung im Profil 160 W. Lumens 528.

## Unbekannt / offen

- Typenschild mit Modellschrift und 160 W. Auf der Rückseite steht die Spannung, nicht die Leistung.
- Ob CH6 am Exemplar wirklich invertiert ist.
- Ob CH5 von schnell nach langsam läuft.
- Ob `16BT` die Fein-Kanäle genau so schaltet.
- Pan- und Tilt-Winkel.
- Tastenbeschriftung aus der Nähe. Die Doku nennt FUN, UP, DOWN, ENTER.
- Ob der Modifier im Workspace gesetzt ist und Grand Master die Invertierung noch skaliert.

## Unterschiede zwischen Exemplaren

-

## Linked Issues

-
