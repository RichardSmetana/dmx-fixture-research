# LED PAR 36× RGB (DIP)

## Operation and DMX

| Field | Value |
| --- | --- |
| Documentation | dmx-fixture-research |
| Hardware manufacturer | Unknown |
| Model | Working name LED PAR 36× RGB (DIP) |
| Type | RGB LED PAR / color changer |
| DMX | 8 channels |
| QLC+ | 5.2.1 |
| Documentation | 1.0 — 14 October 2026 |

Profile: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf), mode `8 Channel - research`. Channels: [dmx-channels.md](dmx-channels.md). Photos: [photos/](photos/).

The documented functions come from the measurement on this unit. Manuals of similar PARs are comparison only and do not apply here.

---

## 1. The fixture

Compact RGB PAR with a field of individual LED optics, a yoke, DIP addressing, DMX IN/OUT, automatic, and music mode. Manufacturer and model number are missing.

The working name says 36 optics. The field is visible in the photos. The lenses were not counted one by one.

---

## 2. Safety

Indoor only until an ingress rating is known. No rain or moisture. Use only the supply printed on the housing, here AC90–250V. Disconnect before cleaning. Do not operate it with a damaged housing or cable. Keep ventilation clear. Do not look into the LEDs. Do not connect it to a mains dimmer. Keep combustibles away.

A maximum ambient temperature is not known.

Overhead: a suitable clamp, a load-rated structure, a separate safety cable, air around the housing, and tight screws.

---

## 3. Technical data

| Item | Value | Source |
| --- | --- | --- |
| Color | RGB | Measurement |
| Channels | 8 | Measurement |
| DMX | 3-pin IN/OUT, pin 1 ground, 2 data−, 3 data+ | Printed on the fixture |
| Address | 10 DIP switches | Photo. DIP 10 open |
| Standalone | AUTO, MUSIC, SPEED | Photo. Sequence open |
| Mains | AC90–250V, fixed cable | Photo |
| Power | 20 W | QXF only |
| Weight | 1.5 kg | QXF only |
| Dimensions | 200 × 200 × 200 mm | QXF only |
| Beam angle | 15°, focus fixed | QXF only |

---

## 4. Rear panel

See [photos/rear-panel.jpg](photos/rear-panel.jpg).

| Part | Function |
| --- | --- |
| DIP 1–10 | Address, plus an unexplained tenth switch |
| AUTO | Automatic without a console |
| MUSIC | Music mode |
| SPEED | Speed of the standalone effects |
| Green LED | DMX signal |
| DMX IN | Input, printed `1:G` `2:-` `3:+` |
| DMX OUT | Output |
| Cable | Mains, printed AC90–250V |

AUTO, MUSIC, SPEED, and DIP 10 have not been checked item by item.

---

## 5. Address

DIP 1–9 follow the conventional binary address. DIP 10 is not counted until its function is known.

| Switch | Value |
| --- | --- |
| 1 | 1 |
| 2 | 2 |
| 3 | 4 |
| 4 | 8 |
| 5 | 16 |
| 6 | 32 |
| 7 | 64 |
| 8 | 128 |
| 9 | 256 |
| 10 | Open |

Address 1: only DIP 1 ON. That is how the test ran.

Eight channels. Highest start address: 505.

| Fixture | Start | Range |
| --- | --- | --- |
| 1 | 001 | 1–8 |
| 2 | 009 | 9–16 |
| 3 | 017 | 17–24 |
| 4 | 025 | 25–32 |

---

## 6. DMX

| Channel | Function | Status |
| --- | --- | --- |
| CH1 | Red | Measured |
| CH2 | Green | Measured |
| CH3 | Blue | Measured |
| CH4 | Color macros, and the speed in fade mode | Function measured, boundaries and direction open |
| CH5 | Strobe | Profile proposal only |
| CH6 | 0–127 color change, 128–255 fading | Measured |
| CH7 | Color-change speed | Function measured, direction open |
| CH8 | Master, 0 off, 255 full | Measured |

### CH4

Outside fade mode, CH4 selects colors. The boundaries of the individual colors are missing.

When CH6 is between 128 and 255, CH4 is the fade speed. Whether 0 is slow or fast is open.

### CH5

The QXF proposes: 0–15 no strobe, 16–255 strobe. That was not measured. The direction was not measured either.

### CH6

The boundary is at 128, supported by the individual values listed below.

| Value | Effect | Speed |
| --- | --- | --- |
| 0–127 | Color change | CH7 |
| 128–255 | Color fading | CH4 |

CH6 = 0 is color change. Do not use it as “automatic off”.

Whether values inside one range change a second behavior is open.

### CH7

Speed only during color change. In fade mode, CH7 is not the documented speed channel.

### CH8

0 dark, 255 bright. Not inverted. The percentage steps in between are calculated, not photometric.

### Examples

Color change: CH1–CH5 = 0, CH6 = 64, CH7 = 128, CH8 = 255. Check the speed on CH7 at 0, 64, 128, 192, 255.

Fading: CH1–CH3 = 0, CH4 = 128, CH5 = 0, CH6 = 192, CH7 = 0, CH8 = 255. Check the speed on CH4 at the same steps.

A recipe for pure RGB without automatic effects is still missing.

---

## 7. Standalone

AUTO, MUSIC, and SPEED are on the rear. The exact sequence, and whether SPEED is the same as CH4 or CH7, has not been tested. For a microphone test, do not leave conflicting DMX connected.

---

## 8. Troubleshooting

| Problem | What to check |
| --- | --- |
| No light | CH8 at 255 |
| No DMX | DIP, signal lamp, cable |
| Changes color by itself | CH6 below 128, speed on CH7 |
| Fades by itself | CH6 from 128, speed on CH4 |
| Speed does not respond | In color change use CH7, in fade use CH4 |
| Flashing | CH5 |
| Unexpected RGB | CH4 and CH6 |
| Standalone is running | AUTO or MUSIC |
| Wrong channels | Start address |

---

## 9. Still missing

- Color boundaries on CH4 and how they interact with CH1–CH3
- Strobe threshold and direction
- Whether the two CH6 ranges contain further steps
- Direction of both speeds
- Manufacturer, model, real power, beam angle, dimensions, weight
- DIP 10, AUTO, MUSIC, SPEED

Comparison manuals, not this fixture:

- https://www.manualslib.com/manual/222341/Chauvet-Led-Par200b.html
- https://www.manualslib.com/manual/632713/Chauvet-Led-Par-64-36b.html
- https://images.thomann.de/pics/atg/atgdata/document/manual/c_193245_en_online.pdf

---

## 10. Status of revision 1.0

| Item | Status |
| --- | --- |
| RGB, CH6 boundary at 128, speed channels, CH8 direction | On the unit |
| CH4 color boundaries, speed direction, CH5 | Open |
| AC90–250V, pinout, DIP, AUTO, MUSIC, SPEED | Photo |
| 20 W, dimensions, weight, 15° | Profile only |

---

*End of manual — revision 1.0*
