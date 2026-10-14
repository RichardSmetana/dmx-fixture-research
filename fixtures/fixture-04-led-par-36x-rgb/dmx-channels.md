# DMX-Kanalbelegung — Fixture 04 (LED PAR 36× RGB, DIP)

Status-Legende: **Verifiziert** · **Vermutet** · **Offen**

Modus in QLC+: `8 Channel - research`. Profil: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf).

Höchste Startadresse für acht Kanäle: 505.

## Übersicht

| Modus | Kanäle | Name in QLC+ | Adresse | Stand |
| --- | --- | --- | --- | --- |
| 8 Channel | 8 | 8 Channel - research | DIP, Test mit Adresse 1 | teils verifiziert |

## Modus: 8 Channel

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Rot | Verifiziert |
| CH2 | 0–255 | Grün | Verifiziert |
| CH3 | 0–255 | Blau | Verifiziert |
| CH4 | 0–255 | Farbmakros, solange nicht der Fade-Modus läuft. Einzelne Farbgrenzen nicht kartiert | Funktion verifiziert, Grenzen offen |
| CH4 | 0–255 | Bei CH6 = 128–255: Tempo der Farbüberblendung. Richtung offen | Funktion verifiziert, Richtung offen |
| CH5 | 0–15 | Kein Strobe | Profil, nicht gemessen |
| CH5 | 16–255 | Strobe. Richtung nicht gemessen | Profil, nicht gemessen |
| CH6 | 0–127 | Automatischer Farbwechsel. Tempo auf CH7 | Verifiziert |
| CH6 | 128–255 | Automatische Farbüberblendung. Tempo auf CH4 | Verifiziert |
| CH7 | 0–255 | Tempo des Farbwechsels, nur bei CH6 = 0–127. Richtung offen | Funktion verifiziert, Richtung offen |
| CH8 | 0 | Aus | Verifiziert |
| CH8 | 1–254 | Helligkeit steigend | Verifiziert |
| CH8 | 255 | Voll | Verifiziert |

CH6 und CH7 sind nicht austauschbar. Im Fade-Modus stellt CH4 das Tempo, nicht CH7.

CH6 = 0 ist Farbwechsel, nicht „Automatik aus“. Ein sicherer Weg zu reinem RGB ohne Automatik ist noch nicht belegt.

### Gemessene CH6-Werte

Farbwechsel: 0, 16, 32, 64, 96, 97, 104, 111, 112, 119, 120, 124, 127.

Überblendung: 128, 160, 192, 224, 255.

### Beispiel Farbwechsel

CH1–CH5 = 0, CH6 = 64, CH7 = 128, CH8 = 255. Tempo nur an CH7 ändern.

### Beispiel Überblendung

CH1–CH3 = 0, CH4 = 128, CH5 = 0, CH6 = 192, CH7 = 0, CH8 = 255. Tempo nur an CH4 ändern.

### Besonderheiten

- CH8 ist nicht invertiert.
- CH5 in der QXF ist ausdrücklich als Vorschlag markiert, nicht als Messung.
- DIP 1 an und DIP 2–10 aus ergab beim Test Adresse 1. Die übrigen Binärwerte sind die übliche Rechnung, DIP 10 ist keine Adressstelle, bis das widerlegt ist.
