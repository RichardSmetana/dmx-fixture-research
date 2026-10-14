# Test notes — Fixture 03 (INVOLIGHT LEDMH100)

## Test setup

| Field | Value |
| --- | --- |
| Date | |
| Controller / software | QLC+ 5.2.1 (profile); no measurement setup |
| DMX interface | |
| Address | |
| Firmware | |
| Unit | |

## Values tested

Channel values have not been measured yet.

| Date | Mode | Channel | Value(s) | Observation | Status |
| --- | --- | --- | --- | --- | --- |
| | 9CH / 11CH | CH1–CH11 | see [dmx-channels.md](dmx-channels.md) | Order matches the manufacturer documentation and the QXF | Reference manual |

## Confirmed

- Rear of the base, from the left: DMX IN, print AC IN 220V 50Hz, POWER SWITCH, DMX OUT. A cable is plugged into the mains inlet. See [photos/rear-connectors.jpg](photos/rear-connectors.jpg).
- Front: field of individual LED optics, yoke, base.
- Front of the base: 4-digit display.

## From the manufacturer documentation and the profile

- 36 × 1 W RGB, pan 540°, tilt 230°, 23°, about 528 lm, 160 W, 7 kg, 220 × 376 × 250 mm, maximum 40 °C, indoor only.
- Menu `16BT` OFF = 9 channels, ON = 11 channels. Mode names in QLC+: `9-Ch 16BT OFF`, `11-Ch 16BT ON`.
- CH6 inverted: 0 full, 255 off. QXF text: “0 = full brightness, 255 = blackout”.
- CH5: 0–15 no strobe or fastest program speed, 16–255 fast to slow.
- CH1: eight programs in blocks of 25 starting at 25, sound from 225.
- The QLC+ modifier `Inverted` belongs in the workspace, not in the QXF.
- Power in the profile: 160 W. Lumens: 528.

## Unknown / open

- Rating label with the model text and 160 W. The rear prints the voltage, not the power.
- Whether CH6 is really inverted on this unit.
- Whether CH5 runs from fast to slow.
- Whether `16BT` switches the fine channels exactly this way.
- Pan and tilt angles.
- Button labels in a close photo. The documentation names FUN, UP, DOWN, ENTER.
- Whether the modifier is set in the workspace and whether Grand Master still scales the inversion.

## Differences between units

-

## Linked issues

-
