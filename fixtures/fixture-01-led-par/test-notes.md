# Test notes — Fixture 01 (RGBWAUV wireless PAR)

## Test setup

| Field | Value |
| --- | --- |
| Date | |
| Controller / software | QLC+ 5.2.2 (profile). The measurement setup was not recorded |
| DMX interface | |
| Address | |
| Firmware (display / board) | V2.20 |
| Unit (serial / marking) | |

## Values tested

The 7-channel mode is verified on the unit. The CH9 strobe ranges in 12-channel mode were tested on firmware V2.20. Individual readings and the test date are not recorded here yet.

| Date | Mode | Channel | Value(s) | Observation | Status |
| --- | --- | --- | --- | --- | --- |
| | 7CH | CH1–CH6 | 0–255 | Red, green, blue, white, amber, UV | Verified |
| | 7CH | CH7 | 0–15 | Open / static light | Verified |
| | 7CH | CH7 | 16–131 | Strobe, slow to fast | Verified |
| | 7CH | CH7 | 132–189 | Pulse / fade, bright to dark | Verified |
| | 7CH | CH7 | 190–230 | Pulse / fade, dark to bright | Verified |
| | 7CH | CH7 | 231–255 | Open / maximum brightness | Verified |
| | 12CH | CH9 | 0–255, ranges as in [dmx-channels.md](dmx-channels.md) | Ranges tested on V2.20. Pulse direction from the fixture file | Ranges verified |

## Confirmed

- Firmware on the documented unit: V2.20.
- 7-channel order: red, green, blue, white, amber, UV, strobe.
- CH7 strobe ranges as in [dmx-channels.md](dmx-channels.md).
- 12CH CH9: measured value ranges. Pulse direction from the fixture file. Open windows between the effect ranges.
- Photos: seven optics in a 2–3–2 layout, yoke, 4-digit display, buttons from the left MENU, DOWN, UP, ENTER.
- Rear labels: DMX OUT, DMX IN, POWER OUT, POWER IN AC90-240V. Whip antenna present. Marks CE, WEEE, RoHS. No manufacturer or model name is readable.

## Suspected

- Menu map in the manual (`Addr`, `Chnd`, `SLnd`, `CoLo` 1–38, `Soun` 1–6, `Cust` CC1–CC5, `Ver`). Not walked item by item on the display.
- 12CH order RGBAWUV, then color presets, master dimmer, strobe, random color, auto color, auto/sound/strobe.
- Amber on CH4 and white on CH5 in this mode only (swapped relative to 7CH).
- Eight DMX color ranges on CH7 instead of the 32 presets in the Rasha HEX V12 manual. The 38 menu colors are independent of that table.
- Housing about 220 × 220 × 90 mm, 1 kg, Fresnel 25–40°, 90 W (QLC+ profile, not measured separately). The 3-pin XLR connectors are visible on the rear.
- Mains frequency 50/60 Hz only from the Rasha reference manual, not printed on the housing.
- Ambient temperature kept at a conservative 45 °C because the Rasha documentation cites both 45 °C and 50 °C.

## Unknown / open

- Hardware manufacturer, model number, fuse rating, and permitted ambient temperature.
- 12CH CH1–CH8 and CH10–CH12 not fully remeasured.
- Whether 7CH CH7 at 231–255 is only brighter than 0–15.
- Which dimmer curve belongs to each `Dinn` step.
- Individual behavior of `Soun` 1–6, `FADE` 1–3, `Auto` 1–9, Sync, and CliC.
- Wireless receiver pairing. 2.4 GHz is not printed on the housing, and there is no separate receive LED.
- The profile file matches the installed QLC+ definition. A live check against the fixture is still open.

## Differences between units

-

## Linked issues

-
