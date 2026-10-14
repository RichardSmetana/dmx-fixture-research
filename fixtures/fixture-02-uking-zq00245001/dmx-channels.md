# DMX channel map — Fixture 02 (U'King ZQ00245001)

Status legend: **Reference manual** · **Profile** · **Open**

**Verified** in this project means tested on the unit. That does not apply to any channel here yet.

Source: the public pocket-moving-light manual and the QLC+ profile [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf). Mode name in QLC+: `15 Channel`. The fifteen positions match in the manual and the profile.

## Overview

| Mode | Channels | Name in QLC+ | Menu | Status |
| --- | --- | --- | --- | --- |
| 15 Channel | 15 | 15 Channel | `CH15` | Reference manual, not measured on the unit |

Highest start address for the full mode: 498.

---

## Mode: 15 Channel

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Pan, horizontal. Profile: 0–540° | Reference manual / angle from profile |
| CH2 | 0–255 | Pan fine | Reference manual |
| CH3 | 0–255 | Tilt, vertical. Profile: 0–220° | Reference manual / angle from profile |
| CH4 | 0–255 | Tilt fine | Reference manual |
| CH5 | 0–255 | Pan/tilt speed. Profile: fast to slow | Channel: reference manual. Direction: profile |
| CH6 | 0 | Master dimmer, minimum | Reference manual |
| CH6 | 1–254 | Brightness rising | Reference manual |
| CH6 | 255 | Maximum | Reference manual |
| CH7 | 0–255 | Strobe. Profile: slow to fast. No open or closed ranges documented | Channel: reference manual. Direction: profile. Individual values: open |
| CH8 | 0–255 | Red, 0–100% | Reference manual |
| CH9 | 0–255 | Green, 0–100% | Reference manual |
| CH10 | 0–255 | Blue, 0–100% | Reference manual |
| CH11 | 0–255 | White, 0–100% | Reference manual |
| CH12 | 0–255 | Green laser. Manual: dimming. Profile: intensity / on. Whether it is continuous or has a threshold is open | Reference manual / profile. Behavior: open |
| CH13 | 0–30 | No program | Reference manual |
| CH13 | 31–127 | Automatic program 1 | Reference manual |
| CH13 | 128–249 | Automatic program 2 | Reference manual |
| CH13 | 250–255 | Sound | Reference manual |
| CH14 | 0–4 | LED ring off | Reference manual |
| CH14 | 5–109 | Ring color selection. Individual colors not assigned | Reference manual. Color values: open |
| CH14 | 110–255 | Automatic ring effects | Reference manual. Individual ranges: open |
| CH15 | 0–249 | No function | Reference manual |
| CH15 | 250–255 | Reset. Profile: hold 5 s. The manual does not confirm the time | Range: reference manual. Hold time: profile, open |

### Example: static red, laser off

CH1–CH4 = 128, CH5 = 128, CH6 = 255, CH7 = 0, CH8 = 255, CH9–CH15 = 0.

CH7 = 0 is only a test value. The manual does not say whether 0 is open light or dark.

### Notes

- CH6 dims the RGBW main source. The LED ring is on CH14.
- Leave CH12 at 0 for the first check. Laser class unknown. Do not aim it at people, vehicles, aircraft, or reflective surfaces. Do not use it for audience scanning.
- An active program on CH13 can override other channels. That interaction has not been tested.
- Keep CH15 below 250 in normal use. The head can move during a reset.
- Each channel’s ranges cover 0–255 with no gap.
