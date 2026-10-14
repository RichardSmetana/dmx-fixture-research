# Test notes — Fixture 02 (U'King ZQ00245001)

## Test setup

| Field | Value |
| --- | --- |
| Date | |
| Controller / software | QLC+ 5.2.1 (profile); no measurement setup |
| DMX interface | |
| Address | |
| Firmware (display / board) | |
| Unit (serial / marking) | |

## Values tested

Nothing has been measured on the unit yet. The table below is the source record, not a measurement series.

| Date | Mode | Channel | Value(s) | Observation | Status |
| --- | --- | --- | --- | --- | --- |
| | 15CH | CH1–CH15 | see [dmx-channels.md](dmx-channels.md) | Order matches the reference manual and the QXF | Reference manual |

## Confirmed

- Base label: Model ZQ00245001. Manufacturer line Dongguan Tongquanqiu Shiye Limited Company, cut off at the edge. Importer eVatmaster Consulting GmbH, Bettinastr. 30, Frankfurt am Main. Two postal codes on the label: 60325 and 60326. CE, ROSH, WEEE, Made in China. ZQ02090 and U'King are not on the label.
- Head: hexagonal faceted lens. Opposite face with a round LED field and a small central opening. Yoke.
- Front of the base: 4-digit display, buttons from the left MENU, UP, DOWN, ENTER. Printed RoHS.
- Rear of the base: POWER socket, then DMX IN and DMX OUT. POWER is a 230 V figure-8 / flat radio-style inlet, not a low-voltage barrel. The label does not print the voltage.

## From the reference manual

- 15 channels in the order pan, pan fine, tilt, tilt fine, speed, master dimmer, strobe, red, green, blue, white, laser, auto/sound, LED ring, reset.
- CH13: 0–30 off, 31–127 auto 1, 128–249 auto 2, 250–255 sound.
- CH14: 0–4 off, 5–109 color selection, 110–255 automatic.
- CH15: reset from 250.
- Menu codes `d001`, `CH15`, `Au01`, `Au02`, `SnOn`, `SnOFF`, `rPoF`, `rPon`, `rToF`, `rTon`, `rdoF`, `rdon`, `dFoF`, `dFon`, `RST` / `REST`.
- Main LED 1 × 15 W RGBW, ring 36 × RGB 5050, green laser 150 mA, maximum 40 °C.
- Supply in the manual: 100–240 V AC, 50/60 Hz, or external 12 V DC, 3 A. Power 30 W.

## From the QLC+ profile

- Model string `U'King ZQ00245001 (ZQ02090)`, mode `15 Channel`, QLC+ 5.2.1.
- Pan 540°, tilt 220°, 200 × 250 × 200 mm, 2.5 kg, focus fixed, DMX 3-pin.
- CH5 fast to slow. CH7 slow to fast, one range 0–255.
- CH12 text: “Green Laser Intensity / On”.
- CH15 text: “Reset (Hold 5s)”.
- Power in both `Physical` blocks: 30 W. The device block previously said 80 W and was aligned to 30 W.

## Unknown / open

- Current rating. 12 V DC, 3 A in the reference manual belongs to a different build and does not apply to this figure-8 inlet.
- Laser class. Do not enable CH12 before that is known. The central opening in the LED field is not labeled as the laser exit.
- ZQ02090 is only in the QXF, not on the label.
- Pan and tilt angles, direction of CH5, behavior of CH7 at individual values.
- Whether the laser dims continuously or only switches.
- Individual colors on CH14 between 5 and 109.
- Whether the reset really has to be held for 5 s.
- Meaning of `dFoF` and `dFon`.
- Master/slave on the unit.
- Whether the profile has been imported and driven against the fixture. The file matches the installed QLC+ definition.

## Differences between units

-

## Linked issues

-
