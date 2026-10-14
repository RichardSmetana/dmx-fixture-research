# INVOLIGHT LEDMH100

## LED Moving Head

| Feld | Wert |
| --- | --- |
| Dokumentation | dmx-fixture-research |
| Hardware-Hersteller | INVOLIGHT |
| Modell | LEDMH100 |
| Typ | RGB-LED-Moving-Head |
| DMX-Modi | 9 / 11 |
| QLC+ | 5.2.1 |
| Dokumentationsstand | 1.0 – Oktober 2026 |

Profil: [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf). Kanäle: [dmx-channels.md](dmx-channels.md). Fotos: [photos/](photos/).

Grundlage ist das 12-seitige Herstellermanual und die QLC+-Datei dieses Projekts. Kanalwerte sind nicht am Gerät gemessen. Der Netzaufdruck ist fotografiert.

**CH6 ist invertiert.** DMX 0 ist volle Helligkeit, 255 ist aus.

Herstellermanual, nur verlinkt:

- https://www.manualslib.com/manual/1108857/Involight-Ledmh100.html
- https://manualzz.com/doc/7012116/involight-ledmh100-led-moving-head-user-manual

---

## 1. Gerät

36 × 1 W LEDs, RGB, motorischer Pan und Tilt, acht Programme, Sound, DMX512. Auf dem Foto ein Feld einzelner LED-Optiken. Die Zahl 36 ist nicht nachgezählt.

`16BT` OFF: 9 Kanäle, 8-bit Pan/Tilt. `16BT` ON: 11 Kanäle, dazu Pan-fein und Tilt-fein. Die ersten neun Kanäle bleiben gleich.

---

## 2. Sicherheit

Nur innen. Nicht Regen oder Feuchtigkeit. Nur an einen passenden, geerdeten Stromkreis. Vor Service trennen. Nicht in die LEDs sehen. Lüftung freihalten. Nicht an einen Netzdimmer. Nicht mit beschädigtem Gehäuse betreiben.

Maximum nach Manual: **40 °C**.

Der Kopf fährt beim Start von selbst. Nicht in den Fahrweg greifen und den Kopf nicht unter Spannung von Hand drücken.

Über Kopf: tragfähige Konstruktion, Schelle, separates Sicherungsseil, Freiraum für Pan und Tilt, Abstand zu Vorhängen und Brennbaren.

---

## 3. Technische Daten

| Größe | Wert | Quelle |
| --- | --- | --- |
| LEDs | 36 × 1 W, RGB | Herstellerdoku |
| Pan / Tilt | 540° / 230° | Herstellerdoku und QXF |
| Winkel | 23° | QXF |
| Lichtstrom | etwa 528 lm | Herstellerdoku und QXF |
| Leistung | 160 W | Herstellerdoku und QXF |
| Netz | AC IN 220V 50Hz, Schalter | Foto |
| Gewicht | 7 kg | Herstellerdoku und QXF |
| Maße | 220 × 376 × 250 mm | Herstellerdoku und QXF |
| Umgebung | max. 40 °C | Herstellerdoku |
| DMX | 3-pin, IN und OUT | Foto |

160 W ist die Herstellerangabe zum ganzen Gerät, nicht die Summe der LED-Nennleistung. Maße, Gewicht, Winkel und Lumen sind nicht nachgemessen. Die Spannung 220 V 50 Hz steht auf dem Sockel.

---

## 4. Anschluss

1. Gerät sichern.
2. Netz an AC IN. Aufdruck: 220V 50Hz. Ein Schalter sitzt daneben.
3. Einschalten und die Initialfahrt abwarten.

DMX, Standardbelegung aus dem Manual, nicht auf dem Gehäuse aufgedruckt:

| Pin | Signal |
| --- | --- |
| 1 | Masse / Schirm |
| 2 | Data − |
| 3 | Data + |

Kette: Konsole, dann DMX IN, weiter über DMX OUT. Am Ende bei Bedarf 120 Ohm.

### Adressen

11 Kanäle, Beispiele:

| Gerät | Start | Kanäle |
| --- | --- | --- |
| 1 | 001 | 1–11 |
| 2 | 012 | 12–22 |
| 3 | 023 | 23–33 |
| 4 | 034 | 34–44 |

9 Kanäle: 001, 010, 019, 028.

Das Herstellermanual nennt 501 als höchste Startadresse im 11-Kanal-Modus. 11 Kanäle passen rechnerisch noch ab 502.

---

## 5. Bedienfeld

Die Anzeige ist 4-stellig, siehe [photos/base-display.jpg](photos/base-display.jpg). Die Tastennamen stammen aus dem Manual, nicht aus einer Nahaufnahme.

| Taste | Funktion |
| --- | --- |
| FUN | Menü / zurück |
| UP | höher / weiter |
| DOWN | tiefer / zurück |
| ENTER | wählen / speichern |

| Menü | Wert | Funktion |
| --- | --- | --- |
| Adresse | 001–501 im 11-Kanal-Hinweis | Startadresse |
| MODE | `M-DM` | DMX |
| MODE | `M-AU` | Automatik |
| MODE | `M-SO` | Sound |
| PRCO | `PR1`–`PR8` | Programm |
| SPCO | `SP01`–`SP15` | Programmtempo, etwa 0,1 s bis 10 s je Schritt |
| r PAN | STND / REV | Pan-Richtung |
| R TILT | STND / REV | Tilt-Richtung |
| r-PT | STND / REV | Pan und Tilt zusammen |
| TEST | ALL, PAN, TITL, RED, GREEN, BLUE | Selbsttest. Der Kopf kann fahren |
| DISP | STND / REV | Display |
| REST | ON | Reset. Motoren können fahren |
| 16BT | ON / OFF | 11 oder 9 Kanäle |

PR1–PR4 sind im Manual Schrittprogramme, PR5–PR8 Überblendungen. Die genauen Folgen sind nicht aufgeschrieben.

---

## 6. DMX

### CH1

| Wert | Funktion |
| --- | --- |
| 0–24 | RGB manuell |
| 25–49 | Programm 1 |
| 50–74 | Programm 2 |
| 75–99 | Programm 3 |
| 100–124 | Programm 4 |
| 125–149 | Programm 5 |
| 150–174 | Programm 6 |
| 175–199 | Programm 7 |
| 200–224 | Programm 8 |
| 225–255 | Sound |

### CH2–CH4

Rot, Grün, Blau. 0 aus, 255 voll. Nur wirksam, wenn CH1 zwischen 0 und 24 liegt.

### CH5

Hängt von CH1 ab.

Bei manueller RGB (CH1 0–24): 0–15 kein Strobe, 16 schnell, 255 langsam.

Bei Programm (CH1 25–224): 0 am schnellsten, 255 am langsamsten.

### CH6

| Wert | Helligkeit |
| --- | --- |
| 0 | 100 % |
| 64 | etwa 75 % |
| 128 | etwa 50 % |
| 192 | etwa 25 % |
| 255 | aus |

Das ist das Hardware-Verhalten. Die QXF beschreibt es so und dreht den Kanal nicht um.

### CH7–CH9

Pan 0–540°, Tilt 0–230°, Geschwindigkeit 0 schnell bis 255 langsam. Richtung über das Menü.

### CH10 und CH11

Nur im 11-Kanal-Modus. Pan fein und Tilt fein.

### Beispiele

Rot ohne Modifier: CH1 = 0, CH2 = 255, CH3 = 0, CH4 = 0, CH5 = 0, CH6 = 0, CH7 = 127, CH8 = 127, CH9 = 128. Im 11-Kanal-Modus CH10 und CH11 etwa 128.

Mit Modifier `Inverted`: denselben Regler für CH6 auf 255 stellen. QLC+ sendet 0, solange kein weiterer Ausgang den Wert nochmal skaliert.

Programm 1: CH1 = 37, CH5 = 128.

Sound: CH1 = 240.

---

## 7. Invertierter Dimmer in QLC+

Ohne Korrektur wird der Schieber nach oben dunkler.

`Ausgang = 255 − Reglerwert`

| Regler | DMX | Helligkeit |
| --- | --- | --- |
| 0 | 255 | 0 % |
| 64 | 191 | etwa 25 % |
| 128 | 127 | etwa 50 % |
| 192 | 63 | etwa 75 % |
| 255 | 0 | 100 % |

In QLC+ 5: Fixture Manager, LEDMH100, Kanaleigenschaften, CH6, Modifier `Inverted`, Workspace speichern. Bei mehreren gleichen Geräten die Änderung auf denselben Typ anwenden.

Der Modifier liegt im Workspace, nicht in der `.qxf`. Import allein dreht den Regler nicht um. Danach Szenen, Überblendungen, Blackout und Grand Master am Gerät prüfen.

QLC+-Doku: https://docs.qlcplus.org/v5/fixture-manager/channel-properties

---

## 8. Master/Slave

Ohne Konsole: DMX-Kette, ein Gerät auf `M-AU` oder `M-SO`, die übrigen auf `M-DM` mit Adresse 001. Keine Konsole an dieser Kette. Nur ein Master. Am Exemplar nicht geprüft.

---

## 9. Fehlersuche

| Problem | Prüfung |
| --- | --- |
| Startet nicht | Netz, Schalter, Sicherung |
| Kein DMX | Adresse, Kabel, Modus `M-DM`, passendes `16BT` |
| Bleibt dunkel | CH6 auf 0, CH1 auf 0–24 |
| Heller Regler macht dunkler | Modifier `Inverted` fehlt |
| Kein RGB | CH1 nicht im Bereich 0–24 |
| Unerwartete Programme | CH1 über 24 |
| Schnelles Blitzen | CH5 über 15 |
| Falsche Richtung | `r PAN`, `R TILT`, `r-PT` |
| Slave folgt nicht | `M-DM` und Adresse 001 |

Bei blockierter Mechanik anhalten und spannungsfrei prüfen.

---

## 10. Wartung

Netz trennen, abkühlen lassen. Kabel, Aufhängung, Sicherungsseil, Lüftung, Lüfter, Optik und Fahrweg prüfen. Staub außen entfernen, keine scharfen Mittel. Motor, Riemen und Elektrik nur durch geeignetes Personal.

---

## 11. Was geprüft ist

| Punkt | Stand |
| --- | --- |
| AC IN 220V 50Hz, Schalter, DMX IN/OUT | Foto |
| 9/11 Kanäle, CH1–CH6, invertierter Dimmer | Herstellerdoku, deckungsgleich mit der QXF |
| Pan 540°, Tilt 230°, 160 W, 528 lm, 23° | Herstellerdoku und QXF, nicht gemessen |
| Modifier `Inverted` | Nur Anleitung, nicht im Workspace geprüft |
| Kanalwerte am Exemplar | Offen |

---

*Ende der Anleitung – Revision 1.0*
