# RGBWAUV Wireless PAR 7CH-12CH

## Bedienungsanleitung und DMX-Kanalreferenz

| Feld | Wert |
| --- | --- |
| Fixture-Profil | RGBWAUV Wireless PAR 7CH-12CH |
| Profil-Hersteller | dmx-fixture-research |
| Originalhersteller | Unbekannt / Rasha-kompatibler OEM |
| Firmware | V2.20 |
| Gerätetyp | Color Changer |
| DMX-Modi | 7CH / 12CH |
| QLC+-Version | 5.2.2 |
| Dokumentationsstand | 1.1 – Oktober 2026 |

Profil-Datei: [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf).

Diese Anleitung beschreibt das Gerät nach der QLC+-Fixture-Definition dieses Projekts. Wo die Rasha-Referenzdokumentation abweicht, gilt die Fixture-Definition. Forschungsstatus der einzelnen Kanäle: [dmx-channels.md](dmx-channels.md).

---

## 1. Einleitung

Der RGBWAUV Wireless PAR ist ein kompakter LED-Scheinwerfer für Bühne, Veranstaltung, Architekturlicht und mobilen Einsatz.

Er mischt sechs Farben: Rot, Grün, Blau, Weiß, Amber und Ultraviolett.

Das Gerät unterstützt DMX512 per Kabel, Wireless-DMX, Standalone-Betrieb, Automatikprogramme, Soundsteuerung und Master/Slave.

Bedienfeld und Funktionen ähneln dem Rasha Professional HEX V12 Wireless Flat PAR. Der Hardware-Hersteller ist nicht eindeutig identifiziert.

### Merkmale

- Sieben LED-Optiken
- RGBWAUV-Farbmischung
- DMX mit 7 und 12 Kanälen
- Wireless-DMX-Empfänger mit Stabantenne (2,4 GHz laut Beschreibung)
- DMX-Ein- und Ausgang, 3-poliger XLR
- Master-Dimmer im 12CH-Modus
- Strobe, Puls und Zufalls-Strobe
- 38 Standalone-Farbpresets
- Automatische Farbprogramme
- Sound-Effekte
- Speicher für eigene Farben
- LED-Bedienfeld mit vier Tasten
- Anzeige der Firmware-Version

---

## 2. Sicherheit

### Allgemein

- Nicht direkt in die Lichtquelle blicken.
- Vor Wartung vom Netz trennen.
- Nur an einen ordnungsgemäß geerdeten Stromkreis anschließen.
- Nicht an einen Dimmerpack oder einen Stellwiderstand anschließen.
- Nicht betreiben, wenn Gehäuse, Steckverbinder, Linsen oder Leitungen beschädigt sind.
- Lüftungsöffnungen freihalten.
- Nicht Regen oder starker Feuchtigkeit aussetzen.
- Linsen nicht in die Sonne richten.
- Bei längerem Nichtgebrauch vom Netz trennen.

### Montage

Die Montage erfolgt über den verstellbaren Bügel.

Über Kopf oder über Personenhöhe: geeignete Schelle und ein separates Sicherungsseil.

Rund um das Gehäuse genug Abstand zur Kühlung lassen. Das Rasha-Referenzmanual nennt mindestens 50 cm zu benachbarten Flächen.

### Temperatur

Die Rasha-Dokumentation nennt widersprüchlich 45 °C und 50 °C als maximale Umgebungstemperatur.

Solange das Typenschild dieses Geräts das nicht bestätigt, gilt **45 °C** als konservative Obergrenze.

---

## 3. Anschlüsse

### 3.1 Versorgung

Auf der Rückseite steht **POWER IN AC90-240V**. Eine Netzfrequenz ist dort nicht aufgedruckt. Das Rasha-Referenzmanual nennt zusätzlich 50/60 Hz; das ist am Gerät nicht bestätigt.

### 3.2 Anschlussfeld

Von links nach rechts, siehe [photos/rear-panel.jpg](photos/rear-panel.jpg):

- 4-stellige Anzeige und die Tasten MENU, DOWN, UP, ENTER
- DMX OUT, 3-poliger XLR
- DMX IN, 3-poliger XLR
- POWER OUT, IEC
- POWER IN, IEC, Aufdruck AC90-240V

Die Stabantenne sitzt oberhalb der Buchsen. Eine eigene Wireless-LED ist auf der Rückseite nicht zu sehen.

### 3.3 Netz

- POWER IN, Aufdruck AC90-240V
- POWER OUT zum Weiterschleifen weiterer Geräte

Den zulässigen Strom von Steckverbindern und Leitungen nicht überschreiten. Der Sicherungswert ist auf den Fotos nicht lesbar.

### 3.4 DMX

3-poliger XLR, auf dem Gerät beschriftet:

- DMX OUT
- DMX IN

Die Geräte lassen sich in einer DMX-Kette verbinden.

### 3.5 Wireless-DMX

Eine Stabantenne ist am Gerät vorhanden. Die Angabe 2,4 GHz stammt aus der Gerätebeschreibung und steht nicht auf dem Gehäuse.

1. Gerät einschalten.
2. DMX-Kanalmodus wählen.
3. Startadresse setzen.
4. Den passenden Wireless-DMX-Sender einschalten.
5. Empfänger auf dieselbe Wireless-Gruppe bzw. dieselbe ID wie der Sender stellen.
6. Das Display prüfen. Eine separate Empfangs-LED ist nicht vorhanden.

Wireless ersetzt nur das DMX-Kabel. Netzversorgung bleibt nötig.

Der genaue Pairing-Ablauf hängt vom verbauten Empfängermodul ab.

---

## 4. Bedienfeld und Menü

### 4.1 Tasten

Aufdruck von links nach rechts: MENU, DOWN, UP, ENTER. Daneben eine 4-stellige 7-Segment-Anzeige. Siehe [photos/rear-panel.jpg](photos/rear-panel.jpg).

| Taste | Funktion |
| --- | --- |
| MENU | Menü wechseln oder eine Ebene zurück |
| DOWN | Wert verringern / vorheriger Eintrag |
| UP | Wert erhöhen / nächster Eintrag |
| ENTER | Auswählen oder bestätigen |

### 4.2 Menüplan

| Menü | Werte | Beschreibung |
| --- | --- | --- |
| Addr | 001–512 | DMX-Startadresse |
| Chnd | 7 / 12 | DMX-Kanalmodus |
| SLnd | Slav / Nast / Sync / CliC | Geräte- und Sync-Modi |
| Shnd / CoLo | 1–38 | Statische Farbpresets |
| Shnd / FADE | 1–3 | Farbüberblendungen |
| Shnd / FLAS | 1–100 | Blitz- / Strobe-Programme |
| Shnd / Auto | 1–9 | Automatikprogramme |
| Soun | 1–6 | Sound-Modi |
| Cust | CC1–CC5 | Eigene Farbpresets |
| Dinn | 1–3 | Dimmer-Modi |
| Blnd | On / Off | Blackout |
| LED | On / Off | Display-Beleuchtung |
| Disp | Normal / Inverted | Display-Ausrichtung |
| Test | Start | Selbsttest |
| Fhrs | Stunden | Betriebsstundenzähler |
| Ver | Version | Firmware |
| Rest | Reset | Werkseinstellungen |

Sync, CliC, die Dimmerkurven und die einzelnen Sound-Programme können je nach Firmware oder OEM-Variante abweichen und sind einzeln zu prüfen.

### 4.3 DMX-Adresse

1. `Addr` wählen.
2. ENTER.
3. Adresse mit UP und DOWN einstellen.
4. Mit ENTER bestätigen.

Adresse `001` legt den ersten Gerätekanal auf DMX-Adresse 1.

### 4.4 Kanalmodus

1. `Chnd` wählen.
2. ENTER.
3. `7` oder `12` wählen.
4. Mit ENTER bestätigen.

Die Farbreihenfolge unterscheidet sich:

- **7CH:** CH4 Weiß, CH5 Amber
- **12CH:** CH4 Amber, CH5 Weiß

Diese Positionen folgen der QLC+-Fixture-Definition. Der 7CH-Modus ist am Gerät verifiziert.

### 4.5 Gerätemodus (`SLnd`)

| Einstellung | Funktion |
| --- | --- |
| Slav | Slave |
| Nast | Master |
| Sync | Synchronisation |
| CliC | Weiterer Sync-/Steuermodus |

Die genaue Wirkung von Sync und CliC kann zwischen Firmware- und OEM-Varianten abweichen.

### 4.6 Statische Farben

`CoLo` enthält 38 vordefinierte Farben.

1. `Shnd` öffnen.
2. `CoLo` wählen.
3. Farbe 1 bis 38 wählen.
4. Mit ENTER bestätigen.

Die Farbe steht ohne automatischen Wechsel. Diese 38 Menüfarben sind unabhängig von der DMX-Presettabelle auf CH7 im 12CH-Modus.

### 4.7 Fade

`FADE` hat drei Programme: FADE 1, FADE 2, FADE 3.

Das Rasha-Referenzmanual beschreibt sie von schnell nach langsam.

### 4.8 Flash

`FLAS` reicht von 1 bis 100.

Höhere Werte bedeuten laut Referenzmanual schnellere Blitze.

### 4.9 Automatik

`Auto` enthält neun Programme, darunter Farbwechsel, Überblendungen und weitere eingebaute Effekte.

### 4.10 Sound

`Soun` enthält sechs Modi. Das Gerät nutzt das eingebaute Mikrofon.

Jedes Sound-Programm einzeln prüfen.

### 4.11 Eigene Farben

`Cust` speichert fünf Presets: CC1, CC2, CC3, CC4, CC5. Abruf über das Menü.

### 4.12 Dimmer

`Dinn` hat drei Einstellungen.

Die Rasha-Dokumentation beschreibt linear, Square-Law, Inverse-Square-Law und S-Kurve, ordnet diese Kurven den drei Einstellungen aber nicht einheitlich zu. Das Verhalten jeder Stufe ist am Gerät zu prüfen.

### 4.13 Blackout

`Blnd`: On oder Off. Beeinflusst das Blackout-Verhalten.

### 4.14 Display

`LED`: Display an lassen oder nach Nichtbenutzung abschalten.

`Disp`: Anzeige normal oder invertiert.

### 4.15 Selbsttest

`Test` wählen und ENTER.

### 4.16 Betriebsstunden

`Fhrs` zeigt die aufgelaufene Betriebszeit.

### 4.17 Firmware

`Ver` zeigt die Firmware.

**Am dokumentierten Gerät: V2.20**

### 4.18 Reset

`Rest` und ENTER stellen die Werkseinstellungen wieder her. Gespeicherte Einstellungen können verloren gehen.

---

## 5. DMX-Kanalbelegung

Modusnamen im QLC+-Profil:

| Modus | Name in QLC+ | Stand |
| --- | --- | --- |
| 7CH | 7 Channel  - probable Rasha/OEM | Kanalbelegung am Gerät verifiziert. Der Name enthält zwei Leerzeichen vor dem Gedankenstrich. |
| 12CH | 12 Channel - probable Rasha/OEM | CH9 auf V2.20 geprüft, übrige Kanäle aus der Fixture-Definition |

### 5.1 Sieben Kanäle (7CH)

| Kanal | Funktion | DMX-Wert |
| --- | --- | --- |
| CH1 | Rot | 0–255 |
| CH2 | Grün | 0–255 |
| CH3 | Blau | 0–255 |
| CH4 | Weiß | 0–255 |
| CH5 | Amber | 0–255 |
| CH6 | UV | 0–255 |
| CH7 | Strobe / Puls | siehe unten |

Die Intensität steigt von 0 (aus) bis 255 (Maximum). Es gibt keinen separaten Master-Dimmer.

#### CH7 – Strobe / Puls

| DMX-Wert | Funktion |
| --- | --- |
| 0–15 | Offen / statisches Licht |
| 16–131 | Strobe, langsam bis schnell |
| 132–189 | Puls / Fade, hell nach dunkel |
| 190–230 | Puls / Fade, dunkel nach hell |
| 231–255 | Offen / maximale Helligkeit |

#### Beispiel: statisches Rot (7CH)

| Kanal | Wert |
| --- | --- |
| CH1 | 255 |
| CH2 | 0 |
| CH3 | 0 |
| CH4 | 0 |
| CH5 | 0 |
| CH6 | 0 |
| CH7 | 0 |

CH7 steht in einem Offen-Bereich, damit das Licht dauerhaft an bleibt.

### 5.2 Zwölf Kanäle (12CH)

| Kanal | Funktion |
| --- | --- |
| CH1 | Rot |
| CH2 | Grün |
| CH3 | Blau |
| CH4 | Amber |
| CH5 | Weiß |
| CH6 | UV |
| CH7 | Farbpresets |
| CH8 | Master-Dimmer |
| CH9 | Strobe / Puls / Zufalls-Strobe |
| CH10 | Zufälliger Farbwechsel |
| CH11 | Auto-Farbwechsel |
| CH12 | Auto / Sound / Strobe |

#### CH1–CH6

| DMX-Wert | Funktion |
| --- | --- |
| 0 | Farbe aus |
| 1–255 | Intensität von Minimum bis Maximum |

Reihenfolge: Rot, Grün, Blau, Amber, Weiß, UV.

#### CH7 – Farbpresets

| DMX-Wert | Funktion |
| --- | --- |
| 0–10 | Keine Funktion |
| 11–40 | Farbpreset 1 |
| 41–70 | Farbpreset 2 |
| 71–100 | Farbpreset 3 |
| 101–130 | Farbpreset 4 |
| 131–160 | Farbpreset 5 |
| 161–190 | Farbpreset 6 |
| 191–220 | Farbpreset 7 |
| 221–255 | Farbpreset / Weißabgleich |

Die Fixture-Definition verwendet diese acht Bereiche.

Das Rasha-Referenzmanual listet 32 DMX-Farbpresets. Diese Tabelle passt nicht zur Fixture-Definition und wird hier nicht verwendet. Die 38 Farben im Menü `CoLo` sind davon unabhängig.

#### CH8 – Master-Dimmer

| DMX-Wert | Funktion |
| --- | --- |
| 0–255 | Gesamtintensität, 0–100 % |

#### CH9 – Strobe / Puls / Zufalls-Strobe

Auf Firmware V2.20 geprüft. Die Wertebereiche stammen aus der Messung, die Pulsbeschreibungen aus der Fixture-Datei.

| DMX-Wert | Funktion |
| --- | --- |
| 0–7 | Blackout |
| 8–15 | Offen |
| 16–131 | Strobe, langsam bis schnell |
| 132–139 | Offen |
| 140–181 | Puls: langsam zu, schnell auf |
| 182–189 | Offen |
| 190–231 | Puls: langsam auf, schnell zu |
| 232–239 | Offen |
| 240–247 | Zufalls-Strobe |
| 248–255 | Offen |

#### CH10 – Zufälliger Farbwechsel

| DMX-Wert | Funktion |
| --- | --- |
| 0–10 | Keine Funktion |
| 11–255 | Zufälliger Farbwechsel, langsam bis schnell |

Die Geschwindigkeit steigt mit dem DMX-Wert.

#### CH11 – Automatischer Farbwechsel

| DMX-Wert | Funktion |
| --- | --- |
| 0–10 | Keine Funktion |
| 11–255 | Automatischer Farbwechsel, langsam bis schnell |

Die Geschwindigkeit steigt mit dem DMX-Wert.

#### CH12 – Auto / Sound / Strobe

| DMX-Wert | Funktion |
| --- | --- |
| 0–10 | Keine Funktion |
| 11–120 | Auto- / Sound-Programm |
| 121–255 | Auto- / Sound- / Strobe-Programm |

Das genaue Verhalten in diesen Bereichen kann vom gewählten Programm oder Betriebszustand abhängen.

#### Beispiel: statisches Rot (12CH)

| Kanal | Wert |
| --- | --- |
| CH1 | 255 |
| CH2 | 0 |
| CH3 | 0 |
| CH4 | 0 |
| CH5 | 0 |
| CH6 | 0 |
| CH7 | 0 |
| CH8 | 255 |
| CH9 | 255 |
| CH10 | 0 |
| CH11 | 0 |
| CH12 | 0 |

CH8 auf voller Helligkeit, CH9 in einem Offen-Bereich (248–255). Die übrigen Effektkanäle sind aus.

---

## 6. Technische Daten

Die Werte unten stehen so im QLC+-Profil. Sie sind Profildaten, keine unabhängig geprüften Labormessungen. Lumen und Farbtemperatur im Profil sind 0 und damit Platzhalter.

### 6.1 Mechanik und Optik

| Größe | Wert |
| --- | --- |
| Gerätetyp | Color Changer |
| Lichtquelle | LED |
| LED-Optiken | 7, Anordnung 2–3–2, Foto Vorderseite |
| Abmessungen | 220 × 220 × 90 mm |
| Gewicht im Profil | 1 kg |
| Linse | Fresnel |
| Abstrahlwinkel | 25°–40° |
| Fokus | fest |
| Pan / Tilt | entfällt |

### 6.2 Elektrik

| Größe | Wert |
| --- | --- |
| Leistungsaufnahme | 90 W (Profilwert) |
| Netz | AC 90–240 V, Aufdruck am Gerät. Frequenz nicht aufgedruckt |
| DMX | 3-poliger XLR, DMX IN und DMX OUT |
| Wireless | Stabantenne am Gerät; 2,4 GHz aus der Gerätebeschreibung |
| Sicherung | Wert am Gerät nicht lesbar |
| Netz Ein/Aus | IEC POWER IN und POWER OUT |

### 6.3 Steuerung

| Größe | Wert |
| --- | --- |
| Protokoll | DMX512 |
| Modi | 7CH / 12CH |
| Standalone | ja |
| Sound | ja |
| Master/Slave | ja |
| Wireless-DMX | ja |
| Bedienung | 4-stellige Anzeige, Tasten MENU DOWN UP ENTER |
| Firmware | V2.20 |

---

## 7. Fehlersuche

| Problem | Mögliche Ursache / Abhilfe |
| --- | --- |
| Kein Licht | Netz, DMX-Signal, Shutter und Dimmer prüfen |
| Keine DMX-Reaktion | Adresse und Kanalmodus prüfen |
| Falsche Farben in 7CH | CH4 ist Weiß, CH5 ist Amber |
| Falsche Farben in 12CH | CH4 ist Amber, CH5 ist Weiß |
| Kein Output in 12CH | CH8 über 0, CH9 in einen Offen-Bereich |
| Unerwartetes Blitzen | 7CH: CH7 prüfen. 12CH: CH9 prüfen |
| Unerwartete Farbprogramme | 12CH: CH7 und CH10–CH12 prüfen |
| Wireless verbindet nicht | Senderkompatibilität und Wireless-ID prüfen |
| Display bleibt nicht an | Menü `LED` prüfen |
| Sound reagiert nicht | Sound-Modus und Mikrofon prüfen |
| Unerwartetes Verhalten | Master/Slave und Effektkanäle prüfen |

---

## 8. Dokumentationshinweise

### 8.1 Quellen

1. QLC+-Fixture-Definition RGBWAUV Wireless PAR 7CH-12CH in diesem Projekt.
2. Beobachtungen an Firmware V2.20.
3. Referenzdokumentation Rasha Professional HEX V12 Wireless Flat PAR.
4. Messungen und Betriebstests.
5. Fotos von Vorderseite und Rückseite in [photos/](photos/).

### 8.2 Identifikation

Der Hardware-Hersteller ist nicht abschließend bestimmt. Das Gerät ähnelt der Rasha-HEX-Serie und hat ein vergleichbares Menü.

Das Feld `Manufacturer` im QLC+-Profil ist `dmx-fixture-research`. Das bezeichnet das Projekt, das das Profil pflegt, und ist kein Nachweis des Hardware-Herstellers.

### 8.3 Profil

- QLC+ 5.2.2
- Modell: RGBWAUV Wireless PAR 7CH-12CH
- Manufacturer: dmx-fixture-research
- Modi: `7 Channel  - probable Rasha/OEM`, `12 Channel - probable Rasha/OEM`

Kanalbelegung, Werte und Effektbeschreibungen folgen dieser Definition. Änderungen am Profil sind in dieser Anleitung nachzuziehen.

### 8.4 Was geprüft ist

- **7CH:** Kanalbelegung am Gerät verifiziert.
- **12CH, CH9:** Strobe-Bereiche auf Firmware V2.20 geprüft.
- Farbpresets, Automatik und die übrigen 12CH-Kanäle stehen aus der Fixture-Definition. Detailliertere Messungen stehen noch aus.
- Abmessungen, Gewicht, Leistungsaufnahme, Linsentyp und Abstrahlwinkel stammen aus dem Profil und sind nicht unabhängig geprüft.
- Am Gehäuse sichtbar: sieben Optiken, Bügel, DMX OUT/IN, POWER IN AC90-240V, POWER OUT, Stabantenne, Tasten MENU DOWN UP ENTER, Zeichen CE, WEEE und RoHS. Herstellername, Modell und Netzfrequenz stehen auf den Fotos nicht. Eine eigene Wireless-LED fehlt.
- Der Menüplan ist beschrieben und noch nicht Punkt für Punkt am Display protokolliert.
- Die DMX-Bereiche in beiden Modi decken jeweils 0–255 ohne Lücke ab. Das entspricht der QXF-Datei.

---

*Ende der Anleitung – Revision 1.1*
