# DMX-Kanalbelegung — Fixture 02 (U'King ZQ00245001)

Status-Legende: **Referenzmanual** · **Profil** · **Offen**

**Verifiziert** im Sinn dieses Projekts heißt: am Gerät getestet. Das trifft hier noch auf keinen Kanal zu.

Quelle: öffentliches Pocket-Moving-Light-Manual und QLC+-Profil [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf). Modusname in QLC+: `15 Channel`. Die fünfzehn Positionen stimmen in Manual und Profil überein.

## Übersicht

| Modus | Kanäle | Name in QLC+ | Menü | Stand |
| --- | --- | --- | --- | --- |
| 15 Channel | 15 | 15 Channel | `CH15` | Referenzmanual, nicht am Gerät gemessen |

Höchste Startadresse für den vollen Modus: 498.

---

## Modus: 15 Channel

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Pan, horizontal. Profil: 0–540° | Referenzmanual / Winkel aus Profil |
| CH2 | 0–255 | Pan fein | Referenzmanual |
| CH3 | 0–255 | Tilt, vertikal. Profil: 0–220° | Referenzmanual / Winkel aus Profil |
| CH4 | 0–255 | Tilt fein | Referenzmanual |
| CH5 | 0–255 | Pan/Tilt-Geschwindigkeit. Profil: schnell nach langsam | Kanal: Referenzmanual. Richtung: Profil |
| CH6 | 0 | Master-Dimmer, Minimum | Referenzmanual |
| CH6 | 1–254 | Helligkeit steigend | Referenzmanual |
| CH6 | 255 | Maximum | Referenzmanual |
| CH7 | 0–255 | Strobe. Profil: langsam nach schnell. Keine Offen-/Zu-Bereiche dokumentiert | Kanal: Referenzmanual. Richtung: Profil. Einzelwerte: Offen |
| CH8 | 0–255 | Rot, 0–100 % | Referenzmanual |
| CH9 | 0–255 | Grün, 0–100 % | Referenzmanual |
| CH10 | 0–255 | Blau, 0–100 % | Referenzmanual |
| CH11 | 0–255 | Weiß, 0–100 % | Referenzmanual |
| CH12 | 0–255 | Grüner Laser. Manual: Dimmen. Profil: Intensität / Ein. Ob stufenlos oder mit Schwelle, ist offen | Referenzmanual / Profil. Verhalten: Offen |
| CH13 | 0–30 | Kein Programm | Referenzmanual |
| CH13 | 31–127 | Automatikprogramm 1 | Referenzmanual |
| CH13 | 128–249 | Automatikprogramm 2 | Referenzmanual |
| CH13 | 250–255 | Sound | Referenzmanual |
| CH14 | 0–4 | LED-Ring aus | Referenzmanual |
| CH14 | 5–109 | Farbwahl des Rings. Einzelne Farben nicht zugeordnet | Referenzmanual. Farbwerte: Offen |
| CH14 | 110–255 | Automatische Ringeffekte | Referenzmanual. Einzelbereiche: Offen |
| CH15 | 0–249 | Keine Funktion | Referenzmanual |
| CH15 | 250–255 | Reset. Profil: 5 s halten. Das Manual bestätigt die Zeit nicht | Bereich: Referenzmanual. Haltedauer: Profil, Offen |

### Beispiel: statisches Rot, Laser aus

CH1–CH4 = 128, CH5 = 128, CH6 = 255, CH7 = 0, CH8 = 255, CH9–CH15 = 0.

CH7 = 0 ist nur ein Testwert. Das Manual sagt nicht, ob 0 Dauerlicht oder dunkel ist.

### Besonderheiten

- CH6 dimmt die RGBW-Hauptlichtquelle. Der LED-Ring liegt auf CH14.
- CH12 bei der ersten Prüfung auf 0 lassen. Laserschutzklasse unbekannt. Nicht in Personen, Fahrzeuge, Luftfahrzeuge oder spiegelnde Flächen richten. Nicht zum Audience-Scanning verwenden.
- Ein aktives Programm auf CH13 kann andere Kanäle übersteuern. Das Zusammenspiel ist nicht geprüft.
- CH15 im Normalbetrieb unter 250 lassen. Der Kopf kann beim Reset fahren.
- Die Bereiche jedes Kanals decken 0–255 lückenlos ab.
