# Fixture 03 — INVOLIGHT LEDMH100

| Field | Value |
| --- | --- |
| ID | `fixture-03-involight-ledmh100` |
| Type | LED moving head, RGB |
| Profile manufacturer | dmx-fixture-research |
| Hardware manufacturer / model | INVOLIGHT LEDMH100 |
| Research status | In progress |
| DMX modes | 9 channels with `16BT` OFF, 11 channels with `16BT` ON. From the manufacturer documentation, not measured on the unit |
| Firmware | |
| Supply | Printed on the base: AC IN 220V 50Hz. 160 W only in the manual and the profile |
| Units on hand | — |
| Documentation | [Manual rev. 1.0](manual.md) — October 2026 |

## Summary

Compact LED moving head with a field of individual LED optics, pan, and tilt. The first nine channels are the same in both modes. In QLC+ the modes are named `9-Ch 16BT OFF` and `11-Ch 16BT ON`. `16BT` ON adds pan fine and tilt fine as CH10 and CH11.

**CH6 is an inverted dimmer.** DMX 0 is full RGB brightness, 255 is dark. The QXF records it that way. A normal QLC+ fader only becomes brighter when the workspace modifier `Inverted` is set on this channel. The modifier is not stored in the `.qxf`.

Profile: [`profiles/Involight_LEDMH100.qxf`](profiles/Involight_LEDMH100.qxf) (QLC+ 5.2.1). The `Manufacturer` field is `dmx-fixture-research` and names this project. The hardware manufacturer is INVOLIGHT.

## Identification

### Markings

- Model: LEDMH100, from the manufacturer manual and the profile. Not readable as a rating label in the photos
- Rear of the base, from the left: DMX IN, AC IN 220V 50Hz, POWER SWITCH, DMX OUT
- Display: 4 digits on the front of the base
- Serial number:
- Firmware:

### Technical data

Lumens in the profile: 528. Color temperature: 0. The 160 W figure is the manufacturer’s rating for the whole fixture, not the sum of 36 × 1 W.

| Property | Value | Source |
| --- | --- | --- |
| Light source | 36 × 1 W LED, RGB. The photo shows a field of individual optics, not counted | Manufacturer documentation / photo |
| Pan / tilt | 540° / 230° | Manufacturer documentation and QXF, not measured |
| Beam angle | 23°, fixed in the head | QXF / manufacturer documentation |
| Dimensions (W×H×D) | 220 × 376 × 250 mm | QXF / manufacturer documentation, not measured |
| Weight | 7 kg | QXF / manufacturer documentation, not measured |
| Supply | AC IN 220V 50Hz, power switch, cable at the base | Rear photo |
| Power consumption | 160 W | Manufacturer documentation and QXF. Not on the photographed label |
| Ambient temperature | Maximum 40 °C, indoor only | Manufacturer documentation |
| DMX | 3-pin, IN and OUT labeled. Modes 9 and 11 | Photo / manufacturer documentation |
| Display / menu | 4-digit display. Buttons FUN, UP, DOWN, ENTER | Display photo / manufacturer documentation for the button names |

### Menu (short)

Full map in [manual.md](manual.md). `M-DM` DMX, `M-AU` automatic, `M-SO` sound, `PR1`–`PR8`, `SP01`–`SP15`, `r PAN`, `R TILT`, `r-PT`, `TEST`, `DISP`, `REST`, `16BT` ON/OFF.

`16BT` OFF is the 9-channel mode, ON is the 11-channel mode. The QLC+ mode has to match.

### Photos

| File | Contents |
| --- | --- |
| [photos/front-leds.jpg](photos/front-leds.jpg) | LED field, yoke, base |
| [photos/base-display.jpg](photos/base-display.jpg) | Side, 4-digit display |
| [photos/rear-connectors.jpg](photos/rear-connectors.jpg) | DMX IN, AC IN 220V 50Hz, power switch, DMX OUT |

Still open: a rating label with the model and 160 W, and a close photo of the button labels.

## Files in this folder

| File | Contents |
| --- | --- |
| [manual.md](manual.md) | Operating manual rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 9- and 11-channel map |
| [test-notes.md](test-notes.md) | Sources and open measurements |
| [profiles/Involight_LEDMH100.qxf](profiles/Involight_LEDMH100.qxf) | QLC+ fixture |

## Open questions

- [x] Mains connection read on the unit: AC IN 220V 50Hz, switch, DMX IN/OUT
- [ ] Rating label with model and 160 W
- [ ] Dimmer inversion and strobe direction checked on the unit
- [ ] `16BT` driven against both QLC+ modes
- [ ] Pan 540° and tilt 230° measured
- [x] QLC+ profile matches the installed definition
- [ ] Profile driven live against the fixture
