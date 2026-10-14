# U'King ZQ00245001

## Pocket moving head — kaleidoscope and laser

| Field | Value |
| --- | --- |
| Documentation | dmx-fixture-research |
| Hardware manufacturer | Label: Dongguan Tongquanqiu Shiye Limited Company. Market name U'King |
| Model | ZQ00245001. The QXF also appends ZQ02090 |
| Product family | Pocket moving light (kaleidoscope + laser) |
| DMX channels | 15 |
| QLC+ | 5.2.1 |
| Documentation | 1.0 — October 2026 |

Profile: [`profiles/ZQ00245001-15CH.qxf`](profiles/ZQ00245001-15CH.qxf). Channel status: [dmx-channels.md](dmx-channels.md).

The basis is the public manual *LED Moving Head Light Operating Manual – Pocket Moving Light (Kaleidoscope + Laser)*, the QLC+ definition in this project, and the photos in [photos/](photos/). The PDF does not name ZQ00245001. This unit’s base is printed with that number. The DMX values have still not been measured on the unit.

Source status:

- **Reference manual** — described in the original manual
- **Profile** — present only in the QXF
- **Open** — still to check on the unit

---

## 1. Introduction

Compact moving head with:

- RGBW main LED and kaleidoscope optics
- green laser
- extra RGB LED ring
- motorized pan and tilt
- two automatic programs, sound, and master/slave
- DMX512, one mode with 15 channels

### Features

- Pan and tilt with fine control, speed adjustable
- RGBW mixing and a master dimmer
- Strobe
- Laser control on its own channel
- LED ring independent of the main LED
- Pan and tilt reverse, rotatable display, reset

---

## 2. Safety

### General

1. Check the housing, cables, connectors, and rigging.
2. Connect only the supply printed on the rating label.
3. Disconnect mains power before cleaning and service.
4. Do not expose it to rain, moisture, or excessive heat.
5. Do not connect it to a mains dimmer.
6. Do not operate it with a damaged housing or exposed electrical parts.

The reference manual cites a maximum ambient temperature of **40 °C**. Keep ventilation openings clear.

### Movement

The head moves by itself during initialization and when it receives movement commands.

- Keep hands and objects out of the travel path.
- Do not stop the head by hand while the motors are powered.
- Carry it by the base, not by the head.

### Laser

This fixture contains a green laser source. The laser class of this unit is not known.

- Do not look into the exit aperture.
- Do not aim it at people, vehicles, aircraft, or reflective surfaces.
- Do not use it for audience scanning.
- Leave CH12 at 0 until the laser class and a suitable projection area are known.
- Do not remove covers or bypass a safety function.

150 mA in the reference manual is not an optical power figure and does not establish a laser class. Public operation can have further requirements.

### Mounting

Use the supplied yoke and suitable hardware. Overhead: a load-rated structure, a separate safety cable, and a position out of reach. Do not hang it over people while the securing method is still unclear.

---

## 3. Technical data

### 3.1 Reference manual

| Item | Value |
| --- | --- |
| Type | Moving head |
| Main LED | 1 × 15 W RGBW |
| Optics | Kaleidoscope lens |
| Ring | 36 × RGB 5050 |
| Laser | Green, 150 mA |
| Control | DMX512 / auto / sound / master-slave |
| Channels | 15 |
| Mains, AC variant | 100–240 V AC, 50/60 Hz |
| Mains, DC variant | External 12 V DC, 3 A |
| Power | 30 W |
| Ambient | Maximum 40 °C |

The AC and DC figures are different variants, not interchangeable. This unit has a 230 V figure-8 / flat radio-style inlet labeled POWER. It is not a low-voltage connector. The 12 V DC variant does not apply here. The photographed label does not print voltage or current.

### 3.2 QLC+ profile

| Item | Value in the file |
| --- | --- |
| Pan | 540° |
| Tilt | 220° |
| Dimensions | 200 × 250 × 200 mm |
| Weight | 2.5 kg |
| DMX connector | 3-pin |
| Focus | Fixed |
| Power | 30 W |

The device physical block previously said 80 W and was set to 30 W, matching the reference manual and the mode physical block. The rating label has not been read for power. Angles, dimensions, and weight have not been checked on the unit.

---

## 4. Connections

### 4.1 Mains

1. Secure the fixture.
2. Connect a 230 V figure-8 / flat radio-style cable to the POWER inlet. Do not use a low-voltage supply.
3. Connect the correct source.
4. Switch on and wait for the initialization move.

### 4.2 DMX

3-pin XLR, standard pinout from the reference manual:

| Pin | Function |
| --- | --- |
| 1 | Ground / shield |
| 2 | DMX data − |
| 3 | DMX data + |

Controller output to the fixture input. Further fixtures from the output to the next input. Terminate a long run with 120 ohm.

On this unit the sockets are labeled DMX IN and DMX OUT, see [photos/head-kaleidoscope.jpg](photos/head-kaleidoscope.jpg). The pinout is not printed.

### 4.3 Address

The 15-channel mode occupies fifteen consecutive addresses. The highest start address is 498.

| Fixture | Start | Channels |
| --- | --- | --- |
| 1 | 001 | 1–15 |
| 2 | 016 | 16–30 |
| 3 | 031 | 31–45 |
| 4 | 046 | 46–60 |

---

## 5. Control panel

Printed from left to right: MENU, UP, DOWN, ENTER. Next to them is a 4-digit display, labeled LED DISPLAY. See [photos/base-display.jpg](photos/base-display.jpg).

| Button | Function |
| --- | --- |
| MENU | Select a function |
| UP | Next / increase a value |
| DOWN | Previous / decrease a value |
| ENTER | Confirm |

| Display | Selection | Function |
| --- | --- | --- |
| `d001` | 001–512 | DMX start address |
| `CH15` | CH15 | 15-channel mode |
| `Au01` | Auto 1 | Automatic program 1 |
| `Au02` | Auto 2 | Automatic program 2, described in the manual as slower |
| `SnOn` | On | Sound on |
| `SnOFF` | Off | Sound off |
| `rPoF` | Off | Pan normal |
| `rPon` | On | Pan reversed |
| `rToF` | Off | Tilt normal |
| `rTon` | On | Tilt reversed |
| `rdoF` | Off | Display normal |
| `rdon` | On | Display inverted |
| `dFoF` | Off | Initialization, meaning open |
| `dFon` | On | Initialization, meaning open |
| `RST` / `REST` | Reset | Reset the fixture |

Do not change `dFoF` and `dFon` while their effect is unknown. A reset can make the head move.

The manual does not describe a second DMX mode.

---

## 6. DMX

Mode in QLC+: `15 Channel`.

| Channel | Function | Values |
| --- | --- | --- |
| CH1 | Pan | 0–255, profile 0–540° |
| CH2 | Pan fine | 0–255 |
| CH3 | Tilt | 0–255, profile 0–220° |
| CH4 | Tilt fine | 0–255 |
| CH5 | Speed | 0–255, profile fast to slow |
| CH6 | Master dimmer | 0 minimum, 255 maximum |
| CH7 | Strobe | 0–255, profile slow to fast |
| CH8 | Red | 0–255 |
| CH9 | Green | 0–255 |
| CH10 | Blue | 0–255 |
| CH11 | White | 0–255 |
| CH12 | Green laser | 0–255 |
| CH13 | Auto / sound | see below |
| CH14 | LED ring | see below |
| CH15 | Reset | 0–249 off, 250–255 reset |

### CH13

| DMX value | Function |
| --- | --- |
| 0–30 | No program |
| 31–127 | Automatic 1 |
| 128–249 | Automatic 2 |
| 250–255 | Sound |

A running program can override other channels.

### CH14

| DMX value | Function |
| --- | --- |
| 0–4 | Ring off |
| 5–109 | Color selection, without an individual color table |
| 110–255 | Automatic ring effects |

### CH15

| DMX value | Function |
| --- | --- |
| 0–249 | No function |
| 250–255 | Reset |

The profile says a 5 s hold. The manual does not. Keep the channel below 250 in normal use.

### CH12

Manual: laser dimmer. Profile: intensity / on. Whether the value acts continuously is open.

Leave CH12 at 0 for the first check. Do not enable it before the laser class and the projection area are known.

### Red example

| Channel | Value |
| --- | --- |
| CH1–CH5 | 128 |
| CH6 | 255 |
| CH7 | 0 |
| CH8 | 255 |
| CH9–CH15 | 0 |

If the fixture stays dark, that does not by itself mean the wiring is wrong. CH7 has no documented open value.

Further mix examples for CH8–CH11, with a suitable CH6: red 255/0/0/0, green 0/255/0/0, blue 0/0/255/0, white 0/0/0/255, yellow 255/255/0/0, cyan 0/255/255/0, magenta 255/0/255/0. Those are calculated values, not measured colors.

Check values for CH13: 0, 64, 180, 252. For CH14: 0, 20, 64, 100, 128, 192, 255. Results are not in the test notes yet.

---

## 7. Master/slave

The reference manual describes master/slave without an external controller: fixtures in a DMX chain, the first on auto or sound, no console on the master, the others as slaves. Whether slaves follow automatically has not been tested on ZQ00245001.

---

## 8. Troubleshooting

| Problem | What to check |
| --- | --- |
| Does not start | Supply and connector, rating label |
| No DMX response | Address, cable, signal, mode `CH15` |
| Main light dark | CH6 and CH7 |
| No movement | CH1–CH5, clearance |
| Unexpected movement | CH13 |
| Wrong colors | CH8–CH11 |
| Ring does not respond | CH14 in one of the three ranges |
| Sound does not respond | `SnOn`, microphone, no conflicting DMX |
| Reset repeats | CH15 below 250 |
| Laser stays off | Do not bypass it. Check the laser class and the documentation |

Take it out of service if it overheats, makes unusual noise, or shows electrical damage.

---

## 9. Maintenance

Disconnect mains power, let it cool, check the head, cables, and rigging, remove dust from the outside and the vents, keep the travel path clear, and check the safety cable. Clean the optics only with a soft cloth, without harsh solvents. Leave electrics, motors, and the laser to qualified personnel.

---

## 10. Sources

Original manual, 5 pages, not stored in this folder:

- https://m.media-amazon.com/images/I/A1z-k2qeD5L.pdf
- https://finale3d.com/wp-content/uploads/2021/03/uking_pocket_moving_light.pdf

Model identification:

- https://forums.pioneerdj.com/hc/en-us/community/posts/17123163989913-U-KING-DMX-ADDITION
- https://forums.pioneerdj.com/hc/en-us/community/posts/9981506922521-U-King-30w-Moving-Head
- https://lightkeyapp.com/en/fixtures

The original manual stays with the rights holders and is only linked.

QLC+: Manufacturer `dmx-fixture-research`, model `U'King ZQ00245001 (ZQ02090)`, mode `15 Channel`, editor 5.2.1.

---

## 11. What has been checked

| Item | Status |
| --- | --- |
| Model ZQ00245001 | Read on the base label |
| ZQ02090 | Only in the QXF model string |
| 15 channels, order, CH13–CH15 ranges | Reference manual, matching the QXF |
| Reset hold time 5 s | Profile only |
| Pan 540°, tilt 220°, dimensions, weight | Profile only |
| CH5 direction, individual CH7 values, CH12 behavior | Open |
| Power | 30 W in the manual and the QXF. Not on the label |
| POWER inlet | 230 V figure-8 / flat radio-style inlet. Not a low-voltage connector |
| Buttons | MENU UP DOWN ENTER, photo |
| Laser class | Unknown |

New measurements go into [test-notes.md](test-notes.md) and the next revision.

---

*End of manual — revision 1.0*
