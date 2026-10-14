# Testnotizen — Fixture 02 (U'King ZQ00245001)

## Testumgebung

| Feld | Wert |
| --- | --- |
| Datum | |
| Controller / Software | QLC+ 5.2.1 (Profil); kein Mess-Setup |
| DMX-Interface | |
| Adresse | |
| Firmware (Display / Platine) | |
| Exemplar (Seriennr. / Markierung) | |

## Getestete Werte

Am Gerät ist noch nichts gemessen. Die Tabelle unten ist die Quellenlage, keine Messreihe.

| Datum | Modus | Kanal | Wert(e) | Beobachtung | Status |
| --- | --- | --- | --- | --- | --- |
| | 15CH | CH1–CH15 | siehe [dmx-channels.md](dmx-channels.md) | Reihenfolge wie Referenzmanual und QXF | Referenzmanual |

## Gesichert

- Sockelschild: Model ZQ00245001. Herstellerzeile Dongguan Tongquanqiu Shiye Limited Company, am Rand abgeschnitten. Importeur eVatmaster Consulting GmbH, Bettinastr. 30, Frankfurt am Main. PLZ auf dem Schild doppelt: 60325 und 60326. CE, ROSH, WEEE, Made in China. ZQ02090 und U'King stehen nicht auf dem Schild.
- Kopf: Facettenlinse aus Sechsecken. Gegenfläche mit rundem LED-Feld und kleiner zentraler Öffnung. Bügel.
- Sockel vorn: 4-stellige Anzeige, Tasten von links MENU, UP, DOWN, ENTER. Aufdruck RoHS.
- Sockel hinten: Buchse POWER, daneben DMX IN und DMX OUT. POWER ist ein 230-V-Flachstecker wie an Radios, kein Niedervolt-Hohlstecker. Das Schild druckt die Spannung nicht.

## Aus dem Referenzmanual

- 15 Kanäle in der Reihenfolge Pan, Pan fein, Tilt, Tilt fein, Geschwindigkeit, Master-Dimmer, Strobe, Rot, Grün, Blau, Weiß, Laser, Auto/Sound, LED-Ring, Reset.
- CH13: 0–30 aus, 31–127 Auto 1, 128–249 Auto 2, 250–255 Sound.
- CH14: 0–4 aus, 5–109 Farbwahl, 110–255 Automatik.
- CH15: Reset ab 250.
- Menücodes `d001`, `CH15`, `Au01`, `Au02`, `SnOn`, `SnOFF`, `rPoF`, `rPon`, `rToF`, `rTon`, `rdoF`, `rdon`, `dFoF`, `dFon`, `RST` / `REST`.
- Haupt-LED 1 × 15 W RGBW, Ring 36 × RGB 5050, Laser grün 150 mA, max. 40 °C.
- Versorgung im Manual: 100–240 V AC, 50/60 Hz, oder extern 12 V DC, 3 A. Leistung 30 W.

## Aus dem QLC+-Profil

- Modellstring `U'King ZQ00245001 (ZQ02090)`, Modus `15 Channel`, QLC+ 5.2.1.
- Pan 540°, Tilt 220°, 200 × 250 × 200 mm, 2,5 kg, Fokus fest, DMX 3-pin.
- CH5 schnell nach langsam. CH7 langsam nach schnell, ein Bereich 0–255.
- CH12 Text: „Green Laser Intensity / On“.
- CH15 Text: „Reset (Hold 5s)“.
- Leistung in beiden `Physical`-Blöcken: 30 W. Der Geräte-Block stand vorher auf 80 W und ist angeglichen.

## Unbekannt / offen

- Stromangabe. 12 V DC, 3 A im Referenzmanual gehört zu einer anderen Bauform und trifft auf diesen Flachstecker nicht zu.
- Laserschutzklasse. CH12 nicht zünden, bevor das geklärt ist. Die zentrale Öffnung im LED-Feld ist nicht als Laseraustritt beschriftet.
- ZQ02090 steht nur im QXF, nicht auf dem Schild.
- Pan- und Tilt-Winkel, Richtung von CH5, Verhalten von CH7 bei einzelnen Werten.
- Ob der Laser stufenlos dimmt oder nur schaltet.
- Einzelfarben auf CH14 zwischen 5 und 109.
- Ob der Reset wirklich 5 s gehalten werden muss.
- Bedeutung von `dFoF` und `dFon`.
- Master/Slave am Gerät.
- Ob das Profil importiert und gegen das Gerät gefahren wurde. Die Datei entspricht der installierten QLC+-Definition.

## Unterschiede zwischen Exemplaren

-

## Linked Issues

-
