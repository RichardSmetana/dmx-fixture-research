# DMX-Kanalbelegung — Fixture 01 (RGBWAUV Wireless PAR)

Status-Legende: **Verifiziert** · **Vermutet** · **Offen**

Quelle: QLC+-Profil [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf), Firmware V2.20, Anleitung [Rev. 1.1](manual.md). Wo eine Rasha-HEX-V12-Tabelle abweicht, gilt dieses Profil.

## Übersicht der Modi

| Modus | Kanäle | Name in QLC+ | Menü `Chnd` | Stand |
| --- | --- | --- | --- | --- |
| 7 Channel | 7 | 7 Channel  - probable Rasha/OEM | 7 | Verifiziert |
| 12 Channel | 12 | 12 Channel - probable Rasha/OEM | 12 | CH9 verifiziert (V2.20), übrige Kanäle vermutet |

Weiß und Amber sitzen in den beiden Modi an unterschiedlichen Kanälen:

| Farbe | 7CH | 12CH |
| --- | --- | --- |
| Rot | CH1 | CH1 |
| Grün | CH2 | CH2 |
| Blau | CH3 | CH3 |
| Weiß | CH4 | CH5 |
| Amber | CH5 | CH4 |
| UV | CH6 | CH6 |

---

## Modus: 7 Channel (verifiziert)

Kein Master-Dimmer. Intensität 0 = aus, 255 = Maximum.

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Rot, 0–100 % | Verifiziert |
| CH2 | 0–255 | Grün, 0–100 % | Verifiziert |
| CH3 | 0–255 | Blau, 0–100 % | Verifiziert |
| CH4 | 0–255 | Weiß, 0–100 % | Verifiziert |
| CH5 | 0–255 | Amber, 0–100 % | Verifiziert |
| CH6 | 0–255 | UV, 0–100 % | Verifiziert |
| CH7 | 0–15 | Offen / statisches Licht | Verifiziert |
| CH7 | 16–131 | Strobe, langsam bis schnell | Verifiziert |
| CH7 | 132–189 | Puls / Fade hell nach dunkel | Verifiziert |
| CH7 | 190–230 | Puls / Fade dunkel nach hell | Verifiziert |
| CH7 | 231–255 | Offen / maximale Helligkeit | Verifiziert |

### Beispiel: statisches Rot

CH1 = 255, CH2–CH6 = 0, CH7 = 0 (Offen-Bereich).

### Besonderheiten

- CH7 0–15 und 231–255 sind beide offen; 231–255 ist maximale Helligkeit.
- Kein Reset-Bereich in diesem Modus dokumentiert.

---

## Modus: 12 Channel

CH9 ist auf Firmware V2.20 geprüft. Farbkanäle, Presets, Master-Dimmer und CH10–CH12 stehen aus der Fixture-Definition.

| Kanal | DMX-Wert | Funktion | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Rot, 0–100 % | Vermutet |
| CH2 | 0–255 | Grün, 0–100 % | Vermutet |
| CH3 | 0–255 | Blau, 0–100 % | Vermutet |
| CH4 | 0–255 | Amber, 0–100 % | Vermutet |
| CH5 | 0–255 | Weiß, 0–100 % | Vermutet |
| CH6 | 0–255 | UV, 0–100 % | Vermutet |
| CH7 | 0–10 | Keine Funktion | Vermutet |
| CH7 | 11–40 | Farbpreset 1 | Vermutet |
| CH7 | 41–70 | Farbpreset 2 | Vermutet |
| CH7 | 71–100 | Farbpreset 3 | Vermutet |
| CH7 | 101–130 | Farbpreset 4 | Vermutet |
| CH7 | 131–160 | Farbpreset 5 | Vermutet |
| CH7 | 161–190 | Farbpreset 6 | Vermutet |
| CH7 | 191–220 | Farbpreset 7 | Vermutet |
| CH7 | 221–255 | Farbpreset / Weißabgleich | Vermutet |
| CH8 | 0–255 | Master-Dimmer, 0–100 % | Vermutet |
| CH9 | 0–7 | Blackout | Verifiziert |
| CH9 | 8–15 | Offen | Verifiziert |
| CH9 | 16–131 | Strobe, langsam bis schnell | Verifiziert |
| CH9 | 132–139 | Offen | Verifiziert |
| CH9 | 140–181 | Puls: langsam zu, schnell auf | Verifiziert |
| CH9 | 182–189 | Offen | Verifiziert |
| CH9 | 190–231 | Puls: langsam auf, schnell zu | Verifiziert |
| CH9 | 232–239 | Offen | Verifiziert |
| CH9 | 240–247 | Zufalls-Strobe | Verifiziert |
| CH9 | 248–255 | Offen | Verifiziert |
| CH10 | 0–10 | Keine Funktion | Vermutet |
| CH10 | 11–255 | Zufälliger Farbwechsel, langsam bis schnell | Vermutet |
| CH11 | 0–10 | Keine Funktion | Vermutet |
| CH11 | 11–255 | Auto-Farbwechsel, langsam bis schnell | Vermutet |
| CH12 | 0–10 | Keine Funktion | Vermutet |
| CH12 | 11–120 | Auto- / Sound-Programm | Vermutet |
| CH12 | 121–255 | Auto- / Sound- / Strobe-Programm | Vermutet |

### Beispiel: statisches Rot

CH1 = 255, CH2–CH7 = 0, CH8 = 255, CH9 = 255 (Offen), CH10–CH12 = 0.

Ohne CH8 über 0 und CH9 in einem Offen-Bereich bleibt der 12CH-Modus dunkel bzw. schaltet ab.

### Besonderheiten

- Amber (CH4) liegt vor Weiß (CH5). Im verifizierten 7CH-Modus ist es umgekehrt.
- CH9 hat zwischen den Effektbereichen kurze Offen-Fenster (132–139, 182–189, 232–239, 248–255). Die Grenzen sind gemessen; die Pulsbeschreibungen folgen der Fixture-Datei.
- CH10–CH12 starten erst ab Wert 11; 0–10 ist jeweils keine Funktion.
- Die acht DMX-Bereiche auf CH7 ersetzen die 32 DMX-Farbpresets aus dem Rasha-Referenzmanual. Die 38 Farben im Menü `CoLo` sind eine eigene Standalone-Liste.
