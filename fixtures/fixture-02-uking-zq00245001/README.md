# Fixture 02 — U'King ZQ00245001

| Field | Value |
| --- | --- |
| ID | `fixture-02-uking-zq00245001` |
| Type | Moving head / pocket moving light (kaleidoscope + laser) |
| Profile manufacturer | dmx-fixture-research |
| Hardware manufacturer / model | Label: ZQ00245001, Dongguan Tongquanqiu Shiye Limited Company. Market name U'King. The QXF also appends `(ZQ02090)` |
| Research status | In progress |
| DMX modes | 15 channels, from the reference manual. Not measured on the unit |
| Firmware | |
| Supply | 230 V figure-8 / flat radio-style inlet labeled POWER. Not a low-voltage connector |
| Units on hand | — |
| Documentation | [Manual rev. 1.0](manual.md) — October 2026 |

## Summary

Compact moving head with an RGBW main LED, kaleidoscope optics, a green laser, an RGB LED ring, and pan and tilt. One 15-channel mode. The channel order is in the public pocket-moving-light manual and matches the QLC+ profile. Nothing has been measured on this unit yet.

The base is printed **Model: ZQ00245001**. The manufacturer line reads Dongguan Tongquanqiu Shiye Limited Company and is cut off at the edge of the label. U'King is the market name from fixture lists and is not on this label. The profile model string is `U'King ZQ00245001 (ZQ02090)`. ZQ02090 is not on the label.

Profile: [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf) (QLC+ 5.2.1). The `Manufacturer` field is `dmx-fixture-research` and names this project, not the hardware maker.

The green laser has no known laser class. Keep CH12 at 0 during tests until the class and the projection area are known.

## Identification

### Markings and rating label

- Model number: ZQ00245001, printed on the base
- Manufacturer print: Dongguan Tongquanqiu Shiye Limited Company. The line ends at the label edge with “Limitedcompan”
- Manufacturer address: 6th Floor, Office Building, Yidalong Science and Technology Park, Bihu Industrial Zone, 39 Bihu Avenue, Wullan Village, Fenggang Town, Dongguan. Printed without spaces, and “Office” as “Of ice”
- Importer: eVatmaster Consulting GmbH, Bettinastr. 30, Frankfurt am Main. The importer line says postal code 60325; the EC REP box says 60326. `contact@evatmaster.com`. Part of the importer line is smudged
- Extra name in the QXF: ZQ02090, not on the label
- Serial number: not on the label
- Marks: CE, “ROSH” on the base label, “RoHS” on the front, WEEE, Made in China
- Firmware:

### Technical data

Profile values are not laboratory measurements. Lumens and color temperature in the QLC+ profile are 0.

| Property | Value | Source |
| --- | --- | --- |
| Main optic | Hexagonal faceted lens on the head | Photo |
| LED field | Round field of small LEDs on the top of the head, small opening in the center. 36 × RGB 5050 only in the reference manual, not counted | Photo / reference manual |
| Laser | Green, listed as 150 mA. That is not an optical power figure and not a laser class | Reference manual |
| Pan / tilt | 540° / 220°, focus fixed | QLC+ profile, not checked on the unit |
| Dimensions (W×H×D) | 200 × 250 × 200 mm | QLC+ profile, not measured |
| Weight | 2.5 kg | QLC+ profile, not measured |
| Supply | 230 V figure-8 / flat radio-style inlet labeled POWER. The label does not print a voltage. Reference manual, mains variant: 100–240 V AC, 50/60 Hz. The 12 V DC variant does not apply to this unit | Photo / user report / reference manual |
| Power consumption | 30 W | Reference manual and QLC+ profile. Not read from the rating label |
| Ambient temperature | Maximum 40 °C | Reference manual |
| DMX | Sockets labeled DMX IN and DMX OUT, 3-pin. Channel count 15 only from the manual | Photo / reference manual |
| Display / menu | 4-digit display, printed LED DISPLAY. Buttons from the left: MENU, UP, DOWN, ENTER | Photo. Menu codes only from the reference manual |

### Menu (short)

Full map in [manual.md](manual.md). `d001` address, `CH15` DMX mode, `Au01` / `Au02` automatic, `SnOn` / `SnOFF` sound, `rPoF` / `rPon` pan direction, `rToF` / `rTon` tilt direction, `rdoF` / `rdon` display, `dFoF` / `dFon` initialization (unclear), `RST` / `REST` reset.

### Photos

| File | Contents |
| --- | --- |
| [photos/label-base.jpg](photos/label-base.jpg) | Base label, model ZQ00245001 |
| [photos/head-kaleidoscope.jpg](photos/head-kaleidoscope.jpg) | Faceted lens, sockets POWER, DMX IN, DMX OUT |
| [photos/head-led-field.jpg](photos/head-led-field.jpg) | LED field on top of the head, yoke |
| [photos/base-display.jpg](photos/base-display.jpg) | Display and buttons MENU UP DOWN ENTER |

Still open: current and power printed on the label, laser class, serial number.

## Files in this folder

| File | Contents |
| --- | --- |
| [manual.md](manual.md) | Operating manual rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 15-channel map with source status |
| [test-notes.md](test-notes.md) | What is documented and what is still missing on the unit |
| [profiles/ZQ00245001-15CH.qxf](profiles/ZQ00245001-15CH.qxf) | QLC+ fixture, matching the installed definition |

## Open questions

- [x] Model ZQ00245001 on the base label
- [x] Manufacturer print and importer read
- [x] POWER is a 230 V figure-8 / flat radio-style inlet, not a low-voltage connector
- [ ] Current and power printed on the label. 30 W is only in the manual and the profile
- [ ] Laser class
- [x] DMX mode and channel count from the reference manual (15)
- [ ] At least one mode verified on the unit
- [ ] Pan 540° and tilt 220° measured
- [ ] Direction of CH5 and behavior of CH7
- [ ] Reset hold time on CH15 (profile: 5 s)
- [ ] `dFoF` / `dFon`
- [x] QLC+ profile matches the installed definition
- [ ] Profile driven live against the fixture
