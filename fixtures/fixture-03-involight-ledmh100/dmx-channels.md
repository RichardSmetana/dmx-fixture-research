# DMX channel map — Fixture 03 (INVOLIGHT LEDMH100)

Status legend: **Reference manual** · **Profile** · **Open**

**Verified** in this project means tested on the unit. That does not apply to any channel value here yet. The mains print is photographed; the channel values are not.

Source: the LEDMH100 manufacturer manual and [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf). The first nine channels are the same in both modes.

## Overview

| Mode | Channels | Name in QLC+ | Menu | Status |
| --- | --- | --- | --- | --- |
| 9 Channel | 9 | 9-Ch 16BT OFF | `16BT` OFF | Reference manual |
| 11 Channel | 11 | 11-Ch 16BT ON | `16BT` ON | Reference manual |

The manufacturer manual names 501 as the highest start address in 11-channel mode. Eleven channels still fit from address 502 (502–512).

---

## Shared channels CH1–CH9

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH1 | 0–24 | Manual RGB control | Reference manual |
| CH1 | 25–49 | Program 1 | Reference manual |
| CH1 | 50–74 | Program 2 | Reference manual |
| CH1 | 75–99 | Program 3 | Reference manual |
| CH1 | 100–124 | Program 4 | Reference manual |
| CH1 | 125–149 | Program 5 | Reference manual |
| CH1 | 150–174 | Program 6 | Reference manual |
| CH1 | 175–199 | Program 7 | Reference manual |
| CH1 | 200–224 | Program 8 | Reference manual |
| CH1 | 225–255 | Sound | Reference manual |
| CH2 | 0–255 | Red, 0 off, rising | Reference manual |
| CH3 | 0–255 | Green, 0 off, rising | Reference manual |
| CH4 | 0–255 | Blue, 0 off, rising | Reference manual |
| CH5 | 0–15 | With CH1 0–24: no strobe. With CH1 25–224: fastest program speed | Reference manual |
| CH5 | 16–255 | With CH1 0–24: strobe fast to slow. With CH1 25–224: program speed fast to slow | Reference manual |
| CH6 | 0 | Full RGB brightness | Reference manual |
| CH6 | 255 | Blackout | Reference manual |
| CH7 | 0–255 | Pan, profile 0–540° | Reference manual / angle from profile |
| CH8 | 0–255 | Tilt, profile 0–230° | Reference manual / angle from profile |
| CH9 | 0–255 | Pan/tilt speed, 0 fastest, 255 slowest | Reference manual |

CH2–CH4 only take effect when CH1 is in the range 0–24. Running programs can ignore other channels.

CH6 is inverted. A normal fader from 0 to 255 makes the fixture darker. In a QLC+ workspace the modifier `Inverted` can reverse the fader. The formula is `output = 255 − value`. The modifier is not in the QXF.

### Example: static red, without the modifier

CH1 = 0, CH2 = 255, CH3 = 0, CH4 = 0, CH5 = 0, CH6 = 0, CH7 = 127, CH8 = 127, CH9 = 128.

CH6 must be 0, otherwise the light is not full.

With the modifier `Inverted` active, set the CH6 fader to 255. QLC+ then sends 0, unless Grand Master or another output scales the value further.

### Example: program 1

CH1 = 37, CH5 = 128.

### Example: sound

CH1 = 240.

---

## Extra channels in 11-channel mode

Only with `16BT` ON. These channels do not exist in 9-channel mode.

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH10 | 0–255 | Pan fine | Reference manual |
| CH11 | 0–255 | Tilt fine | Reference manual |

For a coarse center, also set CH10 and CH11 to about 128.

### Notes

- CH5 strobe runs from fast to slow.
- CH9 is the same: 0 fast, 255 slow.
- The ranges of CH1 and CH5 cover 0–255 with no gap.
- Pan and tilt direction depend on `r PAN`, `R TILT`, and `r-PT`.
