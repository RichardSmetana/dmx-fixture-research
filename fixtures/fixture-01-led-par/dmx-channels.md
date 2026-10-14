# DMX channel map — Fixture 01 (RGBWAUV wireless PAR)

Status legend: **Verified** · **Suspected** · **Open**

Source: QLC+ profile [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf), firmware V2.20, and [manual rev. 1.1](manual.md). Where a Rasha HEX V12 table differs, this profile applies.

## Modes

| Mode | Channels | Name in QLC+ | Menu `Chnd` | Status |
| --- | --- | --- | --- | --- |
| 7 Channel | 7 | 7 Channel  - probable Rasha/OEM | 7 | Verified |
| 12 Channel | 12 | 12 Channel - probable Rasha/OEM | 12 | CH9 verified (V2.20); other channels suspected |

The 7CH mode name has two spaces between “Channel” and the dash, exactly as in the QXF file.

White and amber sit on different channels in the two modes:

| Color | 7CH | 12CH |
| --- | --- | --- |
| Red | CH1 | CH1 |
| Green | CH2 | CH2 |
| Blue | CH3 | CH3 |
| White | CH4 | CH5 |
| Amber | CH5 | CH4 |
| UV | CH6 | CH6 |

---

## Mode: 7 Channel (verified)

No master dimmer. Intensity 0 = off, 255 = maximum.

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Red, 0–100% | Verified |
| CH2 | 0–255 | Green, 0–100% | Verified |
| CH3 | 0–255 | Blue, 0–100% | Verified |
| CH4 | 0–255 | White, 0–100% | Verified |
| CH5 | 0–255 | Amber, 0–100% | Verified |
| CH6 | 0–255 | UV, 0–100% | Verified |
| CH7 | 0–15 | Open / static light | Verified |
| CH7 | 16–131 | Strobe, slow to fast | Verified |
| CH7 | 132–189 | Pulse / fade, bright to dark | Verified |
| CH7 | 190–230 | Pulse / fade, dark to bright | Verified |
| CH7 | 231–255 | Open / maximum brightness | Verified |

### Example: static red

CH1 = 255, CH2–CH6 = 0, CH7 = 0 (open range).

### Notes

- CH7 0–15 and 231–255 are both open. 231–255 is maximum brightness.
- No reset range is documented in this mode.

---

## Mode: 12 Channel

The CH9 value ranges were tested on firmware V2.20. The pulse direction in 140–181 and 190–231 follows the fixture file. Color channels, presets, the master dimmer, and CH10–CH12 come from the fixture definition. Every channel’s ranges cover 0–255 without a gap.

| Channel | DMX value | Function | Status |
| --- | --- | --- | --- |
| CH1 | 0–255 | Red, 0–100% | Suspected |
| CH2 | 0–255 | Green, 0–100% | Suspected |
| CH3 | 0–255 | Blue, 0–100% | Suspected |
| CH4 | 0–255 | Amber, 0–100% | Suspected |
| CH5 | 0–255 | White, 0–100% | Suspected |
| CH6 | 0–255 | UV, 0–100% | Suspected |
| CH7 | 0–10 | No function | Suspected |
| CH7 | 11–40 | Color preset 1 | Suspected |
| CH7 | 41–70 | Color preset 2 | Suspected |
| CH7 | 71–100 | Color preset 3 | Suspected |
| CH7 | 101–130 | Color preset 4 | Suspected |
| CH7 | 131–160 | Color preset 5 | Suspected |
| CH7 | 161–190 | Color preset 6 | Suspected |
| CH7 | 191–220 | Color preset 7 | Suspected |
| CH7 | 221–255 | Color preset / white balance | Suspected |
| CH8 | 0–255 | Master dimmer, 0–100% | Suspected |
| CH9 | 0–7 | Blackout | Verified |
| CH9 | 8–15 | Open | Verified |
| CH9 | 16–131 | Strobe, slow to fast | Verified |
| CH9 | 132–139 | Open | Verified |
| CH9 | 140–181 | Pulse: slow close, fast open | Ranges verified, direction from profile |
| CH9 | 182–189 | Open | Verified |
| CH9 | 190–231 | Pulse: slow open, fast close | Ranges verified, direction from profile |
| CH9 | 232–239 | Open | Verified |
| CH9 | 240–247 | Random strobe | Verified |
| CH9 | 248–255 | Open | Verified |
| CH10 | 0–10 | No function | Suspected |
| CH10 | 11–255 | Random color change, slow to fast | Suspected |
| CH11 | 0–10 | No function | Suspected |
| CH11 | 11–255 | Auto color change, slow to fast | Suspected |
| CH12 | 0–10 | No function | Suspected |
| CH12 | 11–120 | Auto / sound program | Suspected |
| CH12 | 121–255 | Auto / sound / strobe program | Suspected |

### Example: static red

CH1 = 255, CH2–CH7 = 0, CH8 = 255, CH9 = 255 (open), CH10–CH12 = 0.

Without CH8 above 0 and CH9 in an open range, 12CH mode stays dark or blacks out.

### Notes

- Amber (CH4) is before white (CH5). The verified 7CH mode is the other way around.
- CH9 has short open windows between the effect ranges (132–139, 182–189, 232–239, 248–255). The boundaries were measured. The pulse wording follows the fixture file.
- CH10–CH12 start at value 11. 0–10 is no function on each of them.
- The eight DMX ranges on CH7 replace the 32 DMX color presets in the Rasha reference manual. The 38 colors in menu `CoLo` are a separate standalone list.
