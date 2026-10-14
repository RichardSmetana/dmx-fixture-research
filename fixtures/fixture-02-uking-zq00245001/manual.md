# U'King ZQ00245001

## Pocket Moving Head – Kaleidoskop und Laser

| Feld | Wert |
| --- | --- |
| Dokumentation | dmx-fixture-research |
| Hardware-Hersteller | Schild: Dongguan Tongquanqiu Shiye Limited Company. Marktname U'King |
| Modell | ZQ00245001. Im QXF zusätzlich ZQ02090 |
| Gerätefamilie | Pocket Moving Light (Kaleidoskop + Laser) |
| DMX-Kanäle | 15 |
| QLC+ | 5.2.1 |
| Dokumentationsstand | 1.0 – Oktober 2026 |

Profil: [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf). Kanalstatus: [dmx-channels.md](dmx-channels.md).

Grundlage ist das öffentliche Manual *LED Moving Head Light Operating Manual – Pocket Moving Light (Kaleidoscope + Laser)*, die QLC+-Definition dieses Projekts und die Fotos in [photos/](photos/). Das PDF nennt ZQ00245001 nicht. Auf dem Sockel dieses Exemplars steht die Nummer. Die DMX-Werte sind weiterhin nicht am Gerät gemessen.

Quellenstatus:

- **Referenzmanual** — im Originalmanual beschrieben
- **Profil** — nur in der QXF
- **Offen** — am Gerät zu prüfen

---

## 1. Einleitung

Kompakter Moving Head mit:

- RGBW-Haupt-LED und Kaleidoskop-Optik
- grünem Laser
- zusätzlichem RGB-LED-Ring
- motorischem Pan und Tilt
- zwei Automatikprogrammen, Sound und Master/Slave
- DMX512, ein Modus mit 15 Kanälen

### Merkmale

- Pan und Tilt mit Feinabgleich, Geschwindigkeit regelbar
- RGBW-Mischung und Master-Dimmer
- Strobe
- Lasersteuerung auf einem eigenen Kanal
- LED-Ring unabhängig von der Haupt-LED
- Pan- und Tilt-Umkehr, Display drehbar, Reset

---

## 2. Sicherheit

### Allgemein

1. Gehäuse, Leitungen, Stecker und Aufhängung prüfen.
2. Nur die Versorgung anschließen, die auf dem Typenschild steht.
3. Vor Reinigung und Service vom Netz trennen.
4. Nicht Regen, Feuchtigkeit oder übermäßiger Wärme aussetzen.
5. Nicht an einen Netzdimmer anschließen.
6. Nicht mit beschädigtem Gehäuse oder offenen elektrischen Teilen betreiben.

Das Referenzmanual nennt maximal **40 °C** Umgebungstemperatur. Lüftungsöffnungen freihalten.

### Bewegung

Der Kopf fährt bei der Initialisierung und bei Fahrbefehlen von selbst.

- Hände und Gegenstände aus dem Fahrbereich halten.
- Den Kopf nicht von Hand stoppen, solange die Motoren unter Spannung stehen.
- Am Sockel tragen, nicht am Kopf.

### Laser

Dieses Gerät enthält eine grüne Laserquelle. Die Schutzklasse dieses Exemplars ist nicht bekannt.

- Nicht in die Austrittsöffnung blicken.
- Nicht auf Personen, Fahrzeuge, Luftfahrzeuge oder spiegelnde Flächen richten.
- Nicht zum Audience-Scanning verwenden.
- CH12 auf 0 lassen, bis Schutzklasse und ein geeigneter Projektionsbereich feststehen.
- Abdeckungen nicht entfernen und keine Schutzfunktion überbrücken.

150 mA im Referenzmanual sind kein optischer Leistungswert und ergeben keine Laserschutzklasse. Öffentlicher Betrieb kann weitere Auflagen haben.

### Montage

Den vorgesehenen Bügel und geeignetes Material verwenden. Über Kopf: tragfähige Konstruktion, separates Sicherungsseil, außer Reichweite. Nicht über Personen, solange die Absicherung nicht geklärt ist.

---

## 3. Technische Daten

### 3.1 Referenzmanual

| Größe | Wert |
| --- | --- |
| Typ | Moving Head |
| Haupt-LED | 1 × 15 W RGBW |
| Optik | Kaleidoskop-Linse |
| Ring | 36 × RGB 5050 |
| Laser | grün, 150 mA |
| Steuerung | DMX512 / Auto / Sound / Master-Slave |
| Kanäle | 15 |
| Netz, Variante AC | 100–240 V AC, 50/60 Hz |
| Netz, Variante DC | extern 12 V DC, 3 A |
| Leistung | 30 W |
| Umgebung | max. 40 °C |

AC- und DC-Angabe sind verschiedene Varianten, nicht austauschbar. Dieses Exemplar hat einen 230-V-Flachstecker mit der Aufschrift POWER, dieselbe Bauform wie an Radios. Das ist kein Niedervoltstecker. Die 12-V-DC-Variante gilt hier nicht. Das fotografierte Schild druckt Spannung und Strom nicht.

### 3.2 QLC+-Profil

| Größe | Wert in der Datei |
| --- | --- |
| Pan | 540° |
| Tilt | 220° |
| Abmessungen | 200 × 250 × 200 mm |
| Gewicht | 2,5 kg |
| DMX-Stecker | 3-pin |
| Fokus | fest |
| Leistung | 30 W |

Der Geräte-Block stand zuvor auf 80 W und ist auf 30 W gesetzt, wie das Referenzmanual und der Modus-Block. Das Typenschild ist noch nicht gelesen. Winkel, Maße und Gewicht sind nicht am Gerät geprüft.

---

## 4. Anschluss

### 4.1 Netz

1. Gerät sichern.
2. Ein 230-V-Flachsteckerkabel an die Buchse POWER anschließen, wie an Radios. Kein Niedervoltnetzteil verwenden.
3. Richtige Quelle anschließen.
4. Einschalten und die Initialfahrt abwarten.

### 4.2 DMX

3-poliger XLR, Standardbelegung aus dem Referenzmanual:

| Pin | Funktion |
| --- | --- |
| 1 | Masse / Schirm |
| 2 | DMX Data − |
| 3 | DMX Data + |

Ausgang der Steuerung an den Eingang des Geräts. Weitere Geräte vom Ausgang zum nächsten Eingang. Am Ende einer langen Strecke ein 120-Ohm-Abschluss.

Auf diesem Exemplar sind die Buchsen als DMX IN und DMX OUT beschriftet, siehe [photos/head-kaleidoscope.jpg](photos/head-kaleidoscope.jpg). Die Pinbelegung ist nicht aufgedruckt.

### 4.3 Adresse

Der 15-Kanal-Modus belegt fünfzehn aufeinanderfolgende Adressen. Die höchste Startadresse ist 498.

| Gerät | Start | Kanäle |
| --- | --- | --- |
| 1 | 001 | 1–15 |
| 2 | 016 | 16–30 |
| 3 | 031 | 31–45 |
| 4 | 046 | 46–60 |

---

## 5. Bedienfeld

Aufdruck von links nach rechts: MENU, UP, DOWN, ENTER. Daneben eine 4-stellige Anzeige, beschriftet LED DISPLAY. Siehe [photos/base-display.jpg](photos/base-display.jpg).

| Taste | Funktion |
| --- | --- |
| MENU | Funktion wählen |
| UP | weiter / Wert erhöhen |
| DOWN | zurück / Wert verringern |
| ENTER | bestätigen |

| Anzeige | Auswahl | Funktion |
| --- | --- | --- |
| `d001` | 001–512 | DMX-Startadresse |
| `CH15` | CH15 | 15-Kanal-Modus |
| `Au01` | Auto 1 | Automatikprogramm 1 |
| `Au02` | Auto 2 | Automatikprogramm 2, im Manual als langsamer beschrieben |
| `SnOn` | On | Sound ein |
| `SnOFF` | Off | Sound aus |
| `rPoF` | Off | Pan normal |
| `rPon` | On | Pan umgekehrt |
| `rToF` | Off | Tilt normal |
| `rTon` | On | Tilt umgekehrt |
| `rdoF` | Off | Display normal |
| `rdon` | On | Display invertiert |
| `dFoF` | Off | Initialisierung, Bedeutung offen |
| `dFon` | On | Initialisierung, Bedeutung offen |
| `RST` / `REST` | Reset | Gerät zurücksetzen |

`dFoF` und `dFon` nicht verstellen, solange ihre Wirkung unbekannt ist. Ein Reset kann den Kopf fahren lassen.

Einen zweiten DMX-Modus beschreibt das Manual nicht.

---

## 6. DMX

Modus in QLC+: `15 Channel`.

| Kanal | Funktion | Werte |
| --- | --- | --- |
| CH1 | Pan | 0–255, Profil 0–540° |
| CH2 | Pan fein | 0–255 |
| CH3 | Tilt | 0–255, Profil 0–220° |
| CH4 | Tilt fein | 0–255 |
| CH5 | Geschwindigkeit | 0–255, Profil schnell nach langsam |
| CH6 | Master-Dimmer | 0 Minimum, 255 Maximum |
| CH7 | Strobe | 0–255, Profil langsam nach schnell |
| CH8 | Rot | 0–255 |
| CH9 | Grün | 0–255 |
| CH10 | Blau | 0–255 |
| CH11 | Weiß | 0–255 |
| CH12 | Grüner Laser | 0–255 |
| CH13 | Auto / Sound | siehe unten |
| CH14 | LED-Ring | siehe unten |
| CH15 | Reset | 0–249 aus, 250–255 Reset |

### CH13

| DMX-Wert | Funktion |
| --- | --- |
| 0–30 | Kein Programm |
| 31–127 | Automatik 1 |
| 128–249 | Automatik 2 |
| 250–255 | Sound |

Ein laufendes Programm kann andere Kanäle übersteuern.

### CH14

| DMX-Wert | Funktion |
| --- | --- |
| 0–4 | Ring aus |
| 5–109 | Farbwahl, ohne einzelne Farbtabelle |
| 110–255 | Automatische Ringeffekte |

### CH15

| DMX-Wert | Funktion |
| --- | --- |
| 0–249 | Keine Funktion |
| 250–255 | Reset |

Das Profil nennt 5 s Haltezeit. Das Manual tut das nicht. Im Betrieb unter 250 bleiben.

### CH12

Manual: Laser-Dimmer. Profil: Intensität / Ein. Ob der Wert stufenlos wirkt, ist offen.

CH12 bei der ersten Prüfung auf 0 lassen. Nicht zünden, bevor Schutzklasse und Projektionsbereich feststehen.

### Beispiel Rot

| Kanal | Wert |
| --- | --- |
| CH1–CH5 | 128 |
| CH6 | 255 |
| CH7 | 0 |
| CH8 | 255 |
| CH9–CH15 | 0 |

Wenn dabei dunkel bleibt, muss das nicht die Verdrahtung sein. CH7 hat keinen dokumentierten Offen-Wert.

Weitere Mischbeispiele für CH8–CH11, bei passendem CH6: Rot 255/0/0/0, Grün 0/255/0/0, Blau 0/0/255/0, Weiß 0/0/0/255, Gelb 255/255/0/0, Cyan 0/255/255/0, Magenta 255/0/255/0. Das sind Rechenwerte, keine gemessenen Farben.

Prüfwerte für CH13: 0, 64, 180, 252. Für CH14: 0, 20, 64, 100, 128, 192, 255. Ergebnisse stehen noch nicht in den Testnotizen.

---

## 7. Master/Slave

Das Referenzmanual beschreibt Master/Slave ohne externe Steuerung: Geräte in einer DMX-Kette, das erste auf Auto oder Sound, keine Konsole am Master, die übrigen als Slave. Ob Slaves automatisch folgen, ist an ZQ00245001 nicht geprüft.

---

## 8. Fehlersuche

| Problem | Prüfung |
| --- | --- |
| Startet nicht | Versorgung und Stecker, Typenschild |
| Keine DMX-Reaktion | Adresse, Kabel, Signal, Modus `CH15` |
| Hauptlicht dunkel | CH6 und CH7 |
| Keine Fahrt | CH1–CH5, Freiraum |
| Unerwartete Fahrt | CH13 |
| Falsche Farben | CH8–CH11 |
| Ring reagiert nicht | CH14 in einem der drei Bereiche |
| Sound reagiert nicht | `SnOn`, Mikrofon, kein widersprechendes DMX |
| Reset wiederholt sich | CH15 unter 250 |
| Laser bleibt aus | Nicht überbrücken. Schutzklasse und Dokumentation prüfen |

Bei Überhitzung, ungewohnten Geräuschen oder elektrischen Schäden außer Betrieb nehmen.

---

## 9. Wartung

Netz trennen, abkühlen lassen, Kopf, Leitungen und Aufhängung prüfen, Staub außen und an den Lüftungsschlitzen entfernen, Fahrweg freihalten, Sicherungsseil prüfen. Optik nur mit weichem Tuch, ohne scharfe Lösemittel. Elektrik, Motor und Laser nur durch geeignetes Personal.

---

## 10. Quellen

Originalmanual, 5 Seiten, nicht in diesem Ordner abgelegt:

- https://m.media-amazon.com/images/I/A1z-k2qeD5L.pdf
- https://finale3d.com/wp-content/uploads/2021/03/uking_pocket_moving_light.pdf

Modellzuordnung:

- https://forums.pioneerdj.com/hc/en-us/community/posts/17123163989913-U-KING-DMX-ADDITION
- https://forums.pioneerdj.com/hc/en-us/community/posts/9981506922521-U-King-30w-Moving-Head
- https://lightkeyapp.com/en/fixtures

Das Originalmanual bleibt bei den Rechteinhabern und ist nur verlinkt.

QLC+: Manufacturer `dmx-fixture-research`, Modell `U'King ZQ00245001 (ZQ02090)`, Modus `15 Channel`, Editor 5.2.1.

---

## 11. Was geprüft ist

| Punkt | Stand |
| --- | --- |
| Modell ZQ00245001 | Auf dem Sockelschild gelesen |
| ZQ02090 | Nur im Modellstring der QXF |
| 15 Kanäle, Reihenfolge, CH13–CH15-Bereiche | Referenzmanual, deckungsgleich mit der QXF |
| Reset-Haltedauer 5 s | Nur Profil |
| Pan 540°, Tilt 220°, Maße, Gewicht | Nur Profil |
| CH5-Richtung, CH7-Einzelwerte, CH12-Verhalten | Offen |
| Leistung | 30 W in Manual und QXF. Steht nicht auf dem Schild |
| Anschluss POWER | 230-V-Flachstecker wie an Radios. Kein Niedervoltstecker |
| Tasten | MENU UP DOWN ENTER, Foto |
| Laserschutzklasse | Unbekannt |

Neue Messungen kommen in [test-notes.md](test-notes.md) und in die nächste Revision.

---

*Ende der Anleitung – Revision 1.0*
