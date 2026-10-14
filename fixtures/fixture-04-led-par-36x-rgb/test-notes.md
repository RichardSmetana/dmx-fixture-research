# Testnotizen — Fixture 04 (LED PAR 36× RGB, DIP)

## Testumgebung

| Feld | Wert |
| --- | --- |
| Datum | 2026-10-14 |
| Controller / Software | QLC+ 5.2.1 (Profil). Interface nicht protokolliert |
| DMX-Interface | |
| Adresse | 1, nur DIP 1 ein, DIP 2–10 aus |
| Firmware | |
| Exemplar | kein Typenschild |

## Getestete Werte

| Datum | Modus | Kanal | Wert(e) | Beobachtung | Status |
| --- | --- | --- | --- | --- | --- |
| 2026-10-14 | 8CH | CH1–CH3 | 0–255 | Rot, Grün, Blau | Verifiziert |
| 2026-10-14 | 8CH | CH4 | 0–255 | Farbwahl. Grenzen der einzelnen Farben offen | Verifiziert |
| 2026-10-14 | 8CH | CH4 | 0–255 bei CH6 128–255 | Tempo der Überblendung. Richtung offen | Verifiziert |
| 2026-10-14 | 8CH | CH6 | 0, 16, 32, 64, 96, 97, 104, 111, 112, 119, 120, 124, 127 | Farbwechsel | Verifiziert |
| 2026-10-14 | 8CH | CH6 | 128, 160, 192, 224, 255 | Farbüberblendung. Frühere Notiz „nur Rot wird heller“ gehört in diesen Bereich | Verifiziert |
| 2026-10-14 | 8CH | CH7 | 0–255 bei CH6 0–127 | Tempo des Farbwechsels. Richtung offen | Verifiziert |
| 2026-10-14 | 8CH | CH8 | 0 und 255 | 0 aus, 255 voll | Verifiziert |

## Gesichert

- 8 Kanäle. Reihenfolge Rot, Grün, Blau, Farbe/Fade-Tempo, Strobe, Effekt, Wechseltempo, Master.
- CH6-Grenze bei 128. Darunter Wechsel mit Tempo auf CH7, darüber Fade mit Tempo auf CH4.
- CH8 nicht invertiert.
- Rückseite: CE, AUTO, MUSIC, SPEED, grüne Signallampe, 10 DIP-Schalter, DMX IN mit `1:G` `2:-` `3:+`, DMX OUT, AC90–250V, festes Netzkabel.
- Adresse 1 über DIP 1.

## Vermutet

- DIP 2–9 als Binäradresse 2, 4, 8, 16, 32, 64, 128, 256.
- CH5: 0–15 kein Strobe, 16–255 Strobe. Steht so in der QXF und ist nicht gemessen.

## Unbekannt / offen

- Hersteller, Modell, Seriennummer.
- Richtung von CH4-Fade-Tempo und CH7-Wechseltempo.
- Farbgrenzen auf CH4 und das Zusammenspiel mit CH1–CH3.
- Ob irgendwo innerhalb 0–127 oder 128–255 noch ein zweites Merkmal steckt.
- Ein Wert, der die Automatik abschaltet. CH6 = 0 tut das nicht.
- DIP 10.
- Ablauf von AUTO, MUSIC und dem SPEED-Regler, und ob SPEED dieselben Tempi wie CH4/CH7 ist.
- 20 W, 1,5 kg, 200 mm Würfel, 15°. Nur Profil.

## Unterschiede zwischen Exemplaren

-

## Linked Issues

-
