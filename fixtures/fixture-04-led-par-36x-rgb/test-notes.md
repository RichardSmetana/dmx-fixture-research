# Test notes — Fixture 04 (LED PAR 36× RGB, DIP)

## Test setup

| Field | Value |
| --- | --- |
| Date | 2026-10-14 |
| Controller / software | QLC+ 5.2.1 (profile). Interface not logged |
| DMX interface | |
| Address | 1, only DIP 1 ON, DIP 2–10 OFF |
| Firmware | |
| Unit | No rating label |

## Values tested

| Date | Mode | Channel | Value(s) | Observation | Status |
| --- | --- | --- | --- | --- | --- |
| 2026-10-14 | 8CH | CH1–CH3 | 0–255 | Red, green, blue | Verified |
| 2026-10-14 | 8CH | CH4 | 0–255 | Color selection. Boundaries of the individual colors open | Verified |
| 2026-10-14 | 8CH | CH4 | 0–255 with CH6 128–255 | Fade speed. Direction open | Verified |
| 2026-10-14 | 8CH | CH6 | 0, 16, 32, 64, 96, 97, 104, 111, 112, 119, 120, 124, 127 | Color change | Verified |
| 2026-10-14 | 8CH | CH6 | 128, 160, 192, 224, 255 | Color fading. An earlier note “only red gets brighter” belongs in this range | Verified |
| 2026-10-14 | 8CH | CH7 | 0–255 with CH6 0–127 | Color-change speed. Direction open | Verified |
| 2026-10-14 | 8CH | CH8 | 0 and 255 | 0 off, 255 full | Verified |

## Confirmed

- 8 channels. Order: red, green, blue, color/fade speed, strobe, effect, change speed, master.
- CH6 boundary at 128. Below it, color change with speed on CH7. Above it, fade with speed on CH4.
- CH8 is not inverted.
- Rear: CE, AUTO, MUSIC, SPEED, green signal lamp, 10 DIP switches, DMX IN printed `1:G` `2:-` `3:+`, DMX OUT, AC90–250V, fixed mains cable.
- Address 1 through DIP 1.

## Suspected

- DIP 2–9 as a binary address: 2, 4, 8, 16, 32, 64, 128, 256.
- CH5: 0–15 no strobe, 16–255 strobe. That is how the QXF is written, and it was not measured.

## Unknown / open

- Manufacturer, model, serial number.
- Direction of the CH4 fade speed and the CH7 color-change speed.
- Color boundaries on CH4 and how they interact with CH1–CH3.
- Whether any value inside 0–127 or 128–255 changes a second behavior.
- A value that turns automatic effects off. CH6 = 0 does not.
- DIP 10.
- Sequence of AUTO, MUSIC, and the SPEED knob, and whether SPEED is the same timing as CH4/CH7.
- 20 W, 1.5 kg, 200 mm cube, 15°. Profile only.

## Differences between units

-

## Linked issues

-
