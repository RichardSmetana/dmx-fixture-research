# INVOLIGHT LEDMH100

## LED moving head

| Field | Value |
| --- | --- |
| Documentation | dmx-fixture-research |
| Hardware manufacturer | INVOLIGHT |
| Model | LEDMH100 |
| Type | RGB LED moving head |
| DMX modes | 9 / 11 |
| QLC+ | 5.2.1 |
| Documentation | 1.0 — October 2026 |

Profile: [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf). Channels: [dmx-channels.md](dmx-channels.md). Photos: [photos/](photos/).

The basis is the 12-page manufacturer manual and the QLC+ file in this project. Channel values have not been measured on the unit. The mains print is photographed.

**CH6 is inverted.** DMX 0 is full brightness, 255 is off.

Manufacturer manual, linked only:

- https://www.manualslib.com/manual/1108857/Involight-Ledmh100.html
- https://manualzz.com/doc/7012116/involight-ledmh100-led-moving-head-user-manual

---

## 1. The fixture

36 × 1 W LEDs, RGB, motorized pan and tilt, eight programs, sound, DMX512. The photo shows a field of individual LED optics. The count of 36 was not made from the photo.

`16BT` OFF: 9 channels, 8-bit pan/tilt. `16BT` ON: 11 channels, plus pan fine and tilt fine. The first nine channels stay the same.

---

## 2. Safety

Indoor only. No rain or moisture. Connect only to a suitable grounded circuit. Disconnect before service. Do not look into the LEDs. Keep ventilation clear. Do not connect it to a mains dimmer. Do not operate it with a damaged housing.

Maximum from the manual: **40 °C**.

The head moves by itself at startup. Do not reach into the travel path, and do not push the head by hand while it is powered.

Overhead: a load-rated structure, a clamp, a separate safety cable, clearance for pan and tilt, and distance from curtains and combustibles.

---

## 3. Technical data

| Item | Value | Source |
| --- | --- | --- |
| LEDs | 36 × 1 W, RGB | Manufacturer documentation |
| Pan / tilt | 540° / 230° | Manufacturer documentation and QXF |
| Beam angle | 23° | QXF |
| Luminous flux | About 528 lm | Manufacturer documentation and QXF |
| Power | 160 W | Manufacturer documentation and QXF |
| Mains | AC IN 220V 50Hz, switch | Photo |
| Weight | 7 kg | Manufacturer documentation and QXF |
| Dimensions | 220 × 376 × 250 mm | Manufacturer documentation and QXF |
| Ambient | Maximum 40 °C | Manufacturer documentation |
| DMX | 3-pin, IN and OUT | Photo |

160 W is the manufacturer’s rating for the whole fixture, not the sum of the LED ratings. Dimensions, weight, beam angle, and lumens have not been remeasured. The voltage 220 V 50 Hz is printed on the base.

---

## 4. Connections

1. Secure the fixture.
2. Connect mains to AC IN. Print: 220V 50Hz. A switch sits next to it.
3. Switch on and wait for the initialization move.

DMX, standard pinout from the manual, not printed on the housing:

| Pin | Signal |
| --- | --- |
| 1 | Ground / shield |
| 2 | Data − |
| 3 | Data + |

Chain: console, then DMX IN, onward through DMX OUT. Terminate with 120 ohm if needed.

### Addresses

11 channels, examples:

| Fixture | Start | Channels |
| --- | --- | --- |
| 1 | 001 | 1–11 |
| 2 | 012 | 12–22 |
| 3 | 023 | 23–33 |
| 4 | 034 | 34–44 |

9 channels: 001, 010, 019, 028.

The manufacturer manual names 501 as the highest start address in 11-channel mode. Eleven channels still fit from 502.

---

## 5. Control panel

The display is 4 digits, see [photos/base-display.jpg](photos/base-display.jpg). The button names come from the manual, not from a close photo.

| Button | Function |
| --- | --- |
| FUN | Menu / back |
| UP | Higher / next |
| DOWN | Lower / previous |
| ENTER | Select / save |

| Menu | Value | Function |
| --- | --- | --- |
| Address | 001–501 in the 11-channel note | Start address |
| MODE | `M-DM` | DMX |
| MODE | `M-AU` | Automatic |
| MODE | `M-SO` | Sound |
| PRCO | `PR1`–`PR8` | Program |
| SPCO | `SP01`–`SP15` | Program speed, about 0.1 s to 10 s per step |
| r PAN | STND / REV | Pan direction |
| R TILT | STND / REV | Tilt direction |
| r-PT | STND / REV | Pan and tilt together |
| TEST | ALL, PAN, TITL, RED, GREEN, BLUE | Self-test. The head can move |
| DISP | STND / REV | Display |
| REST | ON | Reset. Motors can move |
| 16BT | ON / OFF | 11 or 9 channels |

In the manual, PR1–PR4 are step programs and PR5–PR8 are fades. The exact sequences are not written down.

---

## 6. DMX

### CH1

| Value | Function |
| --- | --- |
| 0–24 | Manual RGB |
| 25–49 | Program 1 |
| 50–74 | Program 2 |
| 75–99 | Program 3 |
| 100–124 | Program 4 |
| 125–149 | Program 5 |
| 150–174 | Program 6 |
| 175–199 | Program 7 |
| 200–224 | Program 8 |
| 225–255 | Sound |

### CH2–CH4

Red, green, blue. 0 off, 255 full. Effective only when CH1 is between 0 and 24.

### CH5

Depends on CH1.

With manual RGB (CH1 0–24): 0–15 no strobe, 16 fast, 255 slow.

With a program (CH1 25–224): 0 fastest, 255 slowest.

### CH6

| Value | Brightness |
| --- | --- |
| 0 | 100% |
| 64 | About 75% |
| 128 | About 50% |
| 192 | About 25% |
| 255 | Off |

That is the hardware behavior. The QXF describes it and does not invert the channel itself.

### CH7–CH9

Pan 0–540°, tilt 0–230°, speed 0 fast to 255 slow. Direction through the menu.

### CH10 and CH11

Only in 11-channel mode. Pan fine and tilt fine.

### Examples

Red without the modifier: CH1 = 0, CH2 = 255, CH3 = 0, CH4 = 0, CH5 = 0, CH6 = 0, CH7 = 127, CH8 = 127, CH9 = 128. In 11-channel mode, set CH10 and CH11 to about 128.

With the modifier `Inverted`: set the same CH6 fader to 255. QLC+ sends 0 as long as no further output scales the value again.

Program 1: CH1 = 37, CH5 = 128.

Sound: CH1 = 240.

---

## 7. Inverted dimmer in QLC+

Without the correction, the fader gets darker as it moves up.

`output = 255 − fader value`

| Fader | DMX | Brightness |
| --- | --- | --- |
| 0 | 255 | 0% |
| 64 | 191 | About 25% |
| 128 | 127 | About 50% |
| 192 | 63 | About 75% |
| 255 | 0 | 100% |

In QLC+ 5: Fixture Manager, LEDMH100, channel properties, CH6, modifier `Inverted`, save the workspace. With several identical fixtures, apply the change to the same type.

The modifier lives in the workspace, not in the `.qxf`. Import alone does not reverse the fader. After that, check scenes, fades, blackout, and Grand Master on the fixture.

QLC+ documentation: https://docs.qlcplus.org/v5/fixture-manager/channel-properties

---

## 8. Master/slave

Without a console: a DMX chain, one fixture on `M-AU` or `M-SO`, the others on `M-DM` with address 001. No console on that chain. Only one master. Not tested on this unit.

---

## 9. Troubleshooting

| Problem | What to check |
| --- | --- |
| Does not start | Mains, switch, fuse |
| No DMX | Address, cable, mode `M-DM`, matching `16BT` |
| Stays dark | CH6 at 0, CH1 at 0–24 |
| A brighter fader makes it darker | Modifier `Inverted` is missing |
| No RGB | CH1 is not in the range 0–24 |
| Unexpected programs | CH1 above 24 |
| Fast flashing | CH5 above 15 |
| Wrong direction | `r PAN`, `R TILT`, `r-PT` |
| Slave does not follow | `M-DM` and address 001 |

Stop and disconnect power if the mechanism is blocked.

---

## 10. Maintenance

Disconnect mains power and let it cool. Check cables, rigging, the safety cable, ventilation, fans, optics, and the travel path. Remove dust from the outside. Do not use harsh cleaners. Leave motors, belts, and electrics to qualified personnel.

---

## 11. What has been checked

| Item | Status |
| --- | --- |
| AC IN 220V 50Hz, switch, DMX IN/OUT | Photo |
| 9/11 channels, CH1–CH6, inverted dimmer | Manufacturer documentation, matching the QXF |
| Pan 540°, tilt 230°, 160 W, 528 lm, 23° | Manufacturer documentation and QXF, not measured |
| Modifier `Inverted` | Instructions only, not checked in a workspace |
| Channel values on this unit | Open |

---

*End of manual — revision 1.0*
