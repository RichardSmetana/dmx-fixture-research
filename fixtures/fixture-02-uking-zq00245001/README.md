# Fixture 02 — U'King ZQ00245001

| Feld | Wert |
| --- | --- |
| ID | `fixture-02-uking-zq00245001` |
| Typ | Moving Head / Pocket Moving Light (Kaleidoskop + Laser) |
| Profil-Hersteller | dmx-fixture-research |
| Hardware-Hersteller / Modell | Schild: ZQ00245001, Dongguan Tongquanqiu Shiye Limited Company. Marktname U'King. Im QXF zusätzlich `(ZQ02090)` |
| Forschungsstand | In Untersuchung |
| DMX-Modi | 15 Kanäle, aus dem Referenzmanual. Nicht am Gerät gemessen |
| Firmware | |
| Versorgung | 230-V-Flachstecker „POWER“, wie an Radios. Kein Niedervoltstecker |
| Exemplare im Bestand | — |
| Dokumentationsstand | [Anleitung Rev. 1.0](manual.md) – Oktober 2026 |

## Kurzbeschreibung

Kompakter Moving Head mit RGBW-Haupt-LED, Kaleidoskop-Optik, grünem Laser, RGB-LED-Ring sowie Pan und Tilt. Ein Modus mit 15 Kanälen. Die Kanalreihenfolge steht im öffentlichen Pocket-Moving-Light-Manual und stimmt mit dem QLC+-Profil überein. Am Gerät ist noch nichts gemessen.

Auf dem Sockel steht **Model: ZQ00245001**. Der Herstelleraufdruck lautet Dongguan Tongquanqiu Shiye Limited Company, am Schildrand abgeschnitten. U'King ist der Marktname aus den Fixture-Listen und steht nicht auf diesem Schild. Im Profil heißt das Modell `U'King ZQ00245001 (ZQ02090)`; ZQ02090 ist auf dem Schild nicht zu sehen.

Profil: [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf) (QLC+ 5.2.1). Das Feld `Manufacturer` ist `dmx-fixture-research` und bezeichnet dieses Projekt, nicht den Gerätehersteller.

Der grüne Laser hat keine bekannte Laserschutzklasse. CH12 bleibt bei Tests auf 0, bis Klasse und Aufstellort geklärt sind.

## Identifikation

### Beschriftungen und Typenschild

- Modellnummer: ZQ00245001, Aufdruck auf dem Sockel
- Herstelleraufdruck: Dongguan Tongquanqiu Shiye Limited Company. Die Zeile endet am Schildrand mit „Limitedcompan“
- Anschrift Hersteller: 6th Floor, Office Building, Yidalong Science and Technology Park, Bihu Industrial Zone, 39 Bihu Avenue, Wullan Village, Fenggang Town, Dongguan. Auf dem Schild ohne Leerzeichen, „Office“ als „Of ice“
- Importeur: eVatmaster Consulting GmbH, Bettinastr. 30, Frankfurt am Main. Die Importeurzeile nennt 60325, der EC-REP-Kasten 60326. `contact@evatmaster.com`. Die Importeurzeile ist teilweise überdeckt
- Weitere Bezeichnung im QXF: ZQ02090, nicht auf dem Schild
- Seriennummer: nicht auf dem Schild
- Zeichen: CE, auf dem Sockelschild „ROSH“, an der Front „RoHS“, WEEE, Made in China
- Firmware:

### Technische Daten

Profilwerte sind keine Labormessung. Lumen und Farbtemperatur im QLC+-Profil stehen auf 0.

| Eigenschaft | Wert | Quelle |
| --- | --- | --- |
| Hauptoptik | Facettenlinse aus Sechsecken am Kopf | Foto |
| LED-Feld | Rundes Feld kleiner LEDs auf der Kopfoberseite, kleine Öffnung in der Mitte. 36 × RGB 5050 nur im Referenzmanual, nicht gezählt | Foto / Referenzmanual |
| Laser | grün, angegeben als 150 mA. Das ist kein optischer Leistungswert und keine Schutzklasse | Referenzmanual |
| Pan / Tilt | 540° / 220°, Fokus fest | QLC+-Profil, nicht am Gerät geprüft |
| Abmessungen (B×H×T) | 200 × 250 × 200 mm | QLC+-Profil, nicht gemessen |
| Gewicht | 2,5 kg | QLC+-Profil, nicht gemessen |
| Versorgung | Flachstecker 230 V, beschriftet POWER, Bauform wie Radios. Schild ohne Spannungsaufdruck. Referenzmanual der Netzvariante: 100–240 V AC, 50/60 Hz. Die 12-V-DC-Variante gilt hier nicht | Foto / Nutzerangabe / Referenzmanual |
| Leistungsaufnahme | 30 W | Referenzmanual und QLC+-Profil. Typenschild noch nicht gelesen |
| Umgebungstemperatur | max. 40 °C | Referenzmanual |
| DMX | Buchsen beschriftet DMX IN und DMX OUT, 3-polig. Kanalzahl 15 nur aus dem Manual | Foto / Referenzmanual |
| Display / Menü | 4-stellige Anzeige, Aufdruck LED DISPLAY. Tasten von links: MENU, UP, DOWN, ENTER | Foto. Menücodes weiter nur aus dem Referenzmanual |

### Menü (Kurz)

Ausführlich in [manual.md](manual.md). `d001` Adresse, `CH15` DMX-Modus, `Au01` / `Au02` Automatik, `SnOn` / `SnOFF` Sound, `rPoF` / `rPon` Pan-Richtung, `rToF` / `rTon` Tilt-Richtung, `rdoF` / `rdon` Display, `dFoF` / `dFon` Initialisierung (unklar), `RST` / `REST` Reset.

### Fotos

| Datei | Inhalt |
| --- | --- |
| [photos/label-base.jpg](photos/label-base.jpg) | Sockelschild, Modell ZQ00245001 |
| [photos/head-kaleidoscope.jpg](photos/head-kaleidoscope.jpg) | Facettenlinse, Buchsen POWER, DMX IN, DMX OUT |
| [photos/head-led-field.jpg](photos/head-led-field.jpg) | LED-Feld auf der Kopfoberseite, Bügel |
| [photos/base-display.jpg](photos/base-display.jpg) | Display und Tasten MENU UP DOWN ENTER |

Noch offen: Stromangabe am Schild, Laserschutzklasse, Seriennummer.

## Dokumentation in diesem Ordner

| Datei | Inhalt |
| --- | --- |
| [manual.md](manual.md) | Bedienungsanleitung Rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 15-Kanal-Belegung mit Quellenstatus |
| [test-notes.md](test-notes.md) | Was belegt ist und was am Gerät fehlt |
| [profiles/ZQ00245001-15CH.qxf](profiles/ZQ00245001-15CH.qxf) | QLC+-Fixture, Stand der installierten Definition |

## Offene Fragen

- [x] Modell ZQ00245001 auf dem Sockelschild
- [x] Herstelleraufdruck und Importeur gelesen
- [x] POWER ist ein 230-V-Flachstecker, kein Niedervoltstecker
- [ ] Strom und Leistungsaufdruck am Schild. 30 W steht nur in Manual und Profil
- [ ] Laserschutzklasse
- [x] DMX-Modus und Kanalzahl aus dem Referenzmanual (15)
- [ ] Mindestens ein Modus am Gerät verifiziert
- [ ] Pan 540° und Tilt 220° gemessen
- [ ] Richtung von CH5 und Verhalten von CH7
- [ ] Haltedauer des Resets auf CH15 (Profil: 5 s)
- [ ] `dFoF` / `dFon`
- [x] QLC+-Profil entspricht der installierten Definition
- [ ] Profil mit dem Gerät gefahren
