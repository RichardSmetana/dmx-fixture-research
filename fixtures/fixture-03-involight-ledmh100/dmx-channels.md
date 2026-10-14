# DMX-Kanalbelegung — Fixture 03 (INVOLIGHT LEDMH100)

Status-Legende: **Referenzmanual** · **Profil** · **Offen**

**Verifiziert** heißt in diesem Projekt: am Gerät getestet. Das trifft hier noch auf keinen Kanalwert zu. Der Netzaufdruck ist fotografiert, die Kanalwerte nicht.

Quelle: Herstellermanual LEDMH100 und [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf). Die ersten neun Kanäle sind in beiden Modi dieselben.

## Übersicht

| Modus | Kanäle | Name in QLC+ | Menü | Stand |
| --- | --- | --- | --- | --- |
| 9 Channel | 9 | 9-Ch 16BT OFF | `16BT` OFF | Referenzmanual |
| 11 Channel | 11 | 11-Ch 16BT ON | `16BT` ON | Referenzmanual |

Das Herstellermanual nennt 501 als höchste Startadresse im 11-Kanal-Modus. Rechnerisch belegen 11 Kanäle ab Adresse 502 noch 502–512.

---

## Gemeinsame Kanäle CH1–CH9

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH1 | 0–24 | Manuelle RGB-Steuerung | Referenzmanual |
| CH1 | 25–49 | Programm 1 | Referenzmanual |
| CH1 | 50–74 | Programm 2 | Referenzmanual |
| CH1 | 75–99 | Programm 3 | Referenzmanual |
| CH1 | 100–124 | Programm 4 | Referenzmanual |
| CH1 | 125–149 | Programm 5 | Referenzmanual |
| CH1 | 150–174 | Programm 6 | Referenzmanual |
| CH1 | 175–199 | Programm 7 | Referenzmanual |
| CH1 | 200–224 | Programm 8 | Referenzmanual |
| CH1 | 225–255 | Sound | Referenzmanual |
| CH2 | 0–255 | Rot, 0 aus, steigend | Referenzmanual |
| CH3 | 0–255 | Grün, 0 aus, steigend | Referenzmanual |
| CH4 | 0–255 | Blau, 0 aus, steigend | Referenzmanual |
| CH5 | 0–15 | Bei CH1 0–24: kein Strobe. Bei CH1 25–224: schnellste Programmgeschwindigkeit | Referenzmanual |
| CH5 | 16–255 | Bei CH1 0–24: Strobe schnell nach langsam. Bei CH1 25–224: Programmgeschwindigkeit schnell nach langsam | Referenzmanual |
| CH6 | 0 | Volle RGB-Helligkeit | Referenzmanual |
| CH6 | 255 | Schwarz | Referenzmanual |
| CH7 | 0–255 | Pan, Profil 0–540° | Referenzmanual / Winkel aus Profil |
| CH8 | 0–255 | Tilt, Profil 0–230° | Referenzmanual / Winkel aus Profil |
| CH9 | 0–255 | Pan/Tilt-Geschwindigkeit, 0 am schnellsten, 255 am langsamsten | Referenzmanual |

CH2–CH4 wirken nur, wenn CH1 im Bereich 0–24 liegt. Laufende Programme können andere Kanäle ignorieren.

CH6 ist invertiert. Ein normaler Regler von 0 nach 255 macht das Gerät dunkler. Im QLC+-Workspace kann der Modifier `Inverted` den Regler umdrehen. Die Formel ist `Ausgang = 255 − Wert`. Der Modifier steht nicht in der QXF.

### Beispiel: statisches Rot, ohne Modifier

CH1 = 0, CH2 = 255, CH3 = 0, CH4 = 0, CH5 = 0, CH6 = 0, CH7 = 127, CH8 = 127, CH9 = 128.

CH6 muss 0 sein, sonst ist das Licht nicht voll.

Mit aktivem Modifier `Inverted` den CH6-Regler auf 255 stellen. QLC+ sendet dann 0, sofern Grand Master und andere Ausgänge nicht weiter skalieren.

### Beispiel Programm 1

CH1 = 37, CH5 = 128.

### Beispiel Sound

CH1 = 240.

---

## Zusätzliche Kanäle im 11-Kanal-Modus

Nur bei `16BT` ON. Im 9-Kanal-Modus gibt es diese Kanäle nicht.

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH10 | 0–255 | Pan fein | Referenzmanual |
| CH11 | 0–255 | Tilt fein | Referenzmanual |

Für eine grobe Mitte zusätzlich CH10 und CH11 auf etwa 128.

### Besonderheiten

- CH5 läuft beim Strobe von schnell nach langsam, nicht umgekehrt.
- CH9 ebenso: 0 schnell, 255 langsam.
- Die Bereiche von CH1 und CH5 decken 0–255 lückenlos ab.
- Pan- und Tilt-Richtung hängen an `r PAN`, `R TILT` und `r-PT`.
