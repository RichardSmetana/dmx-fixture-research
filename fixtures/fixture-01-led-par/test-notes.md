# Testnotizen — Fixture 01 (RGBWAUV Wireless PAR)

## Testumgebung

| Feld | Wert |
| --- | --- |
| Datum | |
| Controller / Software | QLC+ 5.2.2 (Profil); Mess-Setup nicht protokolliert |
| DMX-Interface | |
| Adresse | |
| Firmware (Display / Platine) | V2.20 |
| Exemplar (Seriennr. / Markierung) | |

## Getestete Werte

Der 7-Kanal-Modus ist am Gerät verifiziert. Die Strobe-Bereiche von CH9 im 12-Kanal-Modus sind auf Firmware V2.20 geprüft. Einzelwerte und Datum stehen hier noch nicht.

| Datum | Modus | Kanal | Wert(e) | Beobachtung | Status |
| --- | --- | --- | --- | --- | --- |
| | 7CH | CH1–CH6 | 0–255 | Rot, Grün, Blau, Weiß, Amber, UV | Verifiziert |
| | 7CH | CH7 | 0–15 | Offen / statisches Licht | Verifiziert |
| | 7CH | CH7 | 16–131 | Strobe langsam bis schnell | Verifiziert |
| | 7CH | CH7 | 132–189 | Puls / Fade hell nach dunkel | Verifiziert |
| | 7CH | CH7 | 190–230 | Puls / Fade dunkel nach hell | Verifiziert |
| | 7CH | CH7 | 231–255 | Offen / maximale Helligkeit | Verifiziert |
| | 12CH | CH9 | 0–255, Bereiche wie [dmx-channels.md](dmx-channels.md) | Wertebereiche auf V2.20 geprüft. Pulsrichtung aus der Fixture-Datei | Grenzen verifiziert |

## Gesichert

- Firmware am dokumentierten Gerät: V2.20.
- 7-Kanal-Reihenfolge: Rot, Grün, Blau, Weiß, Amber, UV, Strobe.
- Strobe-Bereiche auf CH7 wie in [dmx-channels.md](dmx-channels.md).
- 12CH CH9: gemessene Wertebereiche. Pulsrichtung aus der Fixture-Datei. Offen-Fenster zwischen den Effektbereichen.
- Fotos: sieben Optiken in Anordnung 2–3–2, Bügel, 4-stellige Anzeige, Tasten von links MENU, DOWN, UP, ENTER.
- Rückseite beschriftet mit DMX OUT, DMX IN, POWER OUT, POWER IN AC90-240V. Stabantenne vorhanden. Zeichen CE, WEEE, RoHS. Kein Hersteller- oder Modellname lesbar.

## Vermutet

- Menüplan in der Anleitung (`Addr`, `Chnd`, `SLnd`, `CoLo` 1–38, `Soun` 1–6, `Cust` CC1–CC5, `Ver`). Nicht Punkt für Punkt am Display protokolliert.
- 12CH-Reihenfolge RGBAWUV, dann Farbpresets, Master-Dimmer, Strobe, Zufallsfarbe, Auto-Farbe, Auto/Sound/Strobe.
- Amber CH4 und Weiß CH5 nur in diesem Modus (gegenüber 7CH vertauscht).
- Acht DMX-Farbbereiche auf CH7 statt der 32 Presets aus dem Rasha-HEX-V12-Manual. Die 38 Menüfarben sind davon unabhängig.
- Gehäuse ca. 220 × 220 × 90 mm, 1 kg, Fresnel 25–40°, 90 W (QLC+-Profil, nicht separat nachgemessen). Die 3-poligen XLR sind auf der Rückseite sichtbar.
- Netzfrequenz 50/60 Hz nur aus dem Rasha-Referenzmanual, nicht auf dem Gehäuseaufdruck.
- Umgebungstemperatur konservativ 45 °C, weil die Rasha-Doku 45 °C und 50 °C nennt.

## Unbekannt / offen

- Eindeutiger Hardware-Hersteller, Modellnummer, Sicherungswert und zulässige Umgebungstemperatur.
- 12CH CH1–CH8 und CH10–CH12 noch nicht vollständig nachgemessen.
- Ob CH7 im 7CH-Modus bei 231–255 nur heller ist als bei 0–15.
- Zuordnung der drei `Dinn`-Stufen zu Dimmerkurven.
- Einzelverhalten von `Soun` 1–6, `FADE` 1–3, `Auto` 1–9, Sync und CliC.
- Pairing des Wireless-Empfängers. Die Frequenz 2,4 GHz steht nicht auf dem Gehäuse, eine eigene Empfangs-LED ist nicht sichtbar.
- Die Profil-Datei entspricht der installierten QLC+-Definition. Ein Live-Gegentest am Gerät steht aus.

## Unterschiede zwischen Exemplaren

-

## Linked Issues

-
