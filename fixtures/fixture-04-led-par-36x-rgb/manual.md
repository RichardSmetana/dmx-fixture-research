# LED PAR 36× RGB (DIP)

## Bedienung und DMX

| Feld | Wert |
| --- | --- |
| Dokumentation | dmx-fixture-research |
| Hardware-Hersteller | unbekannt |
| Modell | Arbeitsname LED PAR 36× RGB (DIP) |
| Typ | RGB-LED-PAR / Color Changer |
| DMX | 8 Kanäle |
| QLC+ | 5.2.1 |
| Dokumentationsstand | 1.0 – 14. Oktober 2026 |

Profil: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf), Modus `8 Channel - research`. Kanäle: [dmx-channels.md](dmx-channels.md). Fotos: [photos/](photos/).

Die belegten Funktionen kommen von der Messung an diesem Gerät. Handbücher ähnlicher PARs sind nur Vergleich und gelten hier nicht.

---

## 1. Gerät

Kompakter RGB-PAR mit einem Feld einzelner LED-Optiken, Bügel, DIP-Adressierung, DMX IN/OUT, Automatik und Musikbetrieb. Hersteller und Modellnummer fehlen.

36 Optiken stehen im Arbeitsnamen. Auf den Fotos ist das Feld sichtbar, die Linsen sind nicht einzeln gezählt.

---

## 2. Sicherheit

Nur innen, solange keine Schutzart feststeht. Nicht Regen oder Feuchtigkeit. Nur die Versorgung vom Aufdruck, hier AC90–250V. Vor Reinigung trennen. Nicht mit beschädigtem Gehäuse oder Kabel betreiben. Lüftung frei. Nicht in die LEDs sehen. Nicht an einen Netzdimmer. Brennbares fernhalten.

Eine maximale Umgebungstemperatur ist nicht bekannt.

Über Kopf: passende Schelle, tragfähige Konstruktion, separates Sicherungsseil, Luft um das Gehäuse, Schrauben fest.

---

## 3. Technische Daten

| Größe | Wert | Quelle |
| --- | --- | --- |
| Farbe | RGB | Messung |
| Kanäle | 8 | Messung |
| DMX | 3-pin IN/OUT, Pin 1 Masse, 2 Data−, 3 Data+ | Aufdruck am Gerät |
| Adresse | 10 DIP-Schalter | Foto. DIP 10 offen |
| Standalone | AUTO, MUSIC, SPEED | Foto. Ablauf offen |
| Netz | AC90–250V, festes Kabel | Foto |
| Leistung | 20 W | nur QXF |
| Gewicht | 1,5 kg | nur QXF |
| Maße | 200 × 200 × 200 mm | nur QXF |
| Winkel | 15°, Fokus fest | nur QXF |

---

## 4. Rückseite

Siehe [photos/rear-panel.jpg](photos/rear-panel.jpg).

| Teil | Funktion |
| --- | --- |
| DIP 1–10 | Adresse und eine ungeklärte zehnte Stelle |
| AUTO | Automatik ohne Pult |
| MUSIC | Musikbetrieb |
| SPEED | Tempo der Standalone-Effekte |
| grüne LED | DMX-Signal |
| DMX IN | Eingang, daneben `1:G` `2:-` `3:+` |
| DMX OUT | Ausgang |
| Kabel | Netz, Aufdruck AC90–250V |

AUTO, MUSIC, SPEED und DIP 10 sind noch nicht Punkt für Punkt geprüft.

---

## 5. Adresse

DIP 1–9 entsprechen der üblichen Binäradresse. DIP 10 zählt nicht mit, bis die Funktion feststeht.

| Schalter | Wert |
| --- | --- |
| 1 | 1 |
| 2 | 2 |
| 3 | 4 |
| 4 | 8 |
| 5 | 16 |
| 6 | 32 |
| 7 | 64 |
| 8 | 128 |
| 9 | 256 |
| 10 | offen |

Adresse 1: nur DIP 1 ein. So lief der Test.

Acht Kanäle. Höchste Startadresse: 505.

| Gerät | Start | Bereich |
| --- | --- | --- |
| 1 | 001 | 1–8 |
| 2 | 009 | 9–16 |
| 3 | 017 | 17–24 |
| 4 | 025 | 25–32 |

---

## 6. DMX

| Kanal | Funktion | Stand |
| --- | --- | --- |
| CH1 | Rot | gemessen |
| CH2 | Grün | gemessen |
| CH3 | Blau | gemessen |
| CH4 | Farbmakros, und im Fade-Modus das Tempo | Funktion gemessen, Grenzen und Richtung offen |
| CH5 | Strobe | nur Profilvorschlag |
| CH6 | 0–127 Farbwechsel, 128–255 Überblendung | gemessen |
| CH7 | Tempo des Farbwechsels | Funktion gemessen, Richtung offen |
| CH8 | Master, 0 aus, 255 voll | gemessen |

### CH4

Ohne Fade-Modus wählt CH4 Farben. Die Grenzen der einzelnen Farben fehlen.

Liegt CH6 zwischen 128 und 255, ist CH4 das Tempo der Überblendung. Ob 0 langsam oder schnell ist, ist offen.

### CH5

Die QXF schlägt vor: 0–15 kein Strobe, 16–255 Strobe. Das ist nicht gemessen. Die Richtung auch nicht.

### CH6

Grenze bei 128, durch die genannten Einzelwerte belegt.

| Wert | Effekt | Tempo |
| --- | --- | --- |
| 0–127 | Farbwechsel | CH7 |
| 128–255 | Farbüberblendung | CH4 |

CH6 = 0 ist Farbwechsel. Nicht als „Automatik aus“ verwenden.

Ob Werte innerhalb eines Bereichs noch etwas Zweites ändern, ist offen.

### CH7

Tempo nur im Farbwechsel. Im Fade-Modus ist CH7 nicht der belegte Tempokanal.

### CH8

0 dunkel, 255 hell. Nicht invertiert. Die Prozentstufen dazwischen sind rechnerisch, nicht photometrisch.

### Beispiele

Farbwechsel: CH1–CH5 = 0, CH6 = 64, CH7 = 128, CH8 = 255. Tempo an CH7 mit 0, 64, 128, 192, 255 prüfen.

Überblendung: CH1–CH3 = 0, CH4 = 128, CH5 = 0, CH6 = 192, CH7 = 0, CH8 = 255. Tempo an CH4 mit denselben Stufen prüfen.

Ein Rezept für reines RGB ohne Automatik fehlt noch.

---

## 7. Standalone

AUTO, MUSIC und SPEED sitzen auf der Rückseite. Der genaue Ablauf und ob SPEED dasselbe ist wie CH4 oder CH7, ist nicht geprüft. Für den Mikrofontest kein widersprechendes DMX anliegen lassen.

---

## 8. Fehlersuche

| Problem | Prüfung |
| --- | --- |
| Kein Licht | CH8 auf 255 |
| Kein DMX | DIP, Signallampe, Kabel |
| Wechsel von allein | CH6 unter 128, Tempo an CH7 |
| Überblendung von allein | CH6 ab 128, Tempo an CH4 |
| Tempo reagiert nicht | Im Wechsel CH7, im Fade CH4 |
| Blitzen | CH5 |
| RGB unerwartet | CH4 und CH6 |
| Standalone läuft | AUTO oder MUSIC |
| Falsche Kanäle | Startadresse |

---

## 9. Was noch fehlt

- Farbgrenzen auf CH4 und das Zusammenspiel mit CH1–CH3
- Strobe-Schwelle und Richtung
- Ob die beiden CH6-Bereiche intern noch etwas staffeln
- Richtung der beiden Tempi
- Hersteller, Modell, echte Leistung, Winkel, Maße, Gewicht
- DIP 10, AUTO, MUSIC, SPEED

Vergleichsmanuals, nicht dieses Gerät:

- https://www.manualslib.com/manual/222341/Chauvet-Led-Par200b.html
- https://www.manualslib.com/manual/632713/Chauvet-Led-Par-64-36b.html
- https://images.thomann.de/pics/atg/atgdata/document/manual/c_193245_en_online.pdf

---

## 10. Stand 1.0

| Punkt | Stand |
| --- | --- |
| RGB, CH6-Grenze 128, Tempokanäle, CH8-Richtung | am Gerät |
| CH4-Farbgrenzen, Temporichtung, CH5 | offen |
| AC90–250V, Pinbelegung, DIP, AUTO, MUSIC, SPEED | Foto |
| 20 W, Maße, Gewicht, 15° | nur Profil |

---

*Ende der Anleitung – Revision 1.0*
