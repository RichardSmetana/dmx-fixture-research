# DMX channel map — Fixture 04 (LED PAR 36× RGB, DIP)

Status legend: **Verified** · **Suspected** · **Open**

Mode in QLC+: `8 Channel - research`. Profile: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf).

Highest start address for eight channels: 505.

## Overview

| Mode | Channels | Name in QLC+ | Address | Status |
| --- | --- | --- | --- | --- |
| 8 Channel | 8 | 8 Channel - research | DIP, test at address 1 | Partly verified |

## Mode: 8 Channel

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Red | Verified |
| CH2 | 0–255 | Green | Verified |
| CH3 | 0–255 | Blue | Verified |
| CH4 | 0–255 | Color macros, while fade mode is not running. Individual color boundaries not mapped | Function verified, boundaries open |
| CH4 | 0–255 | With CH6 = 128–255: color-fade speed. Direction open | Function verified, direction open |
| CH5 | 0–15 | No strobe | Profile, not measured |
| CH5 | 16–255 | Strobe. Direction not measured | Profile, not measured |
| CH6 | 0–127 | Automatic color change. Speed on CH7 | Verified |
| CH6 | 128–255 | Automatic color fading. Speed on CH4 | Verified |
| CH7 | 0–255 | Color-change speed, only with CH6 = 0–127. Direction open | Function verified, direction open |
| CH8 | 0 | Off | Verified |
| CH8 | 1–254 | Brightness between off and full | Endpoints verified; intermediate steps not logged |
| CH8 | 255 | Full | Verified |

CH6 and CH7 are not interchangeable. In fade mode, CH4 sets the speed, not CH7.

CH6 = 0 is color change, not “automatic off”. A reliable way to get pure RGB without automatic effects is not documented yet.

### Measured CH6 values

Color change: 0, 16, 32, 64, 96, 97, 104, 111, 112, 119, 120, 124, 127.

Fading: 128, 160, 192, 224, 255.

### Color-change example

CH1–CH5 = 0, CH6 = 64, CH7 = 128, CH8 = 255. Change the speed only on CH7.

### Fade example

CH1–CH3 = 0, CH4 = 128, CH5 = 0, CH6 = 192, CH7 = 0, CH8 = 255. Change the speed only on CH4.

### Notes

- CH8 is not inverted.
- CH5 in the QXF is explicitly marked as a proposal, not as a measurement.
- DIP 1 ON and DIP 2–10 OFF gave address 1 in the test. The other binary values are the conventional calculation. DIP 10 is not an address bit until that is disproved.
