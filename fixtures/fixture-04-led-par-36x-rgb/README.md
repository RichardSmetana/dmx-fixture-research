# Fixture 04 — LED PAR 36× RGB (DIP)

| Field | Value |
| --- | --- |
| ID | `fixture-04-led-par-36x-rgb` |
| Type | RGB LED PAR / color changer |
| Profile manufacturer | dmx-fixture-research |
| Hardware manufacturer / model | Unknown. Working name LED PAR 36× RGB (DIP) |
| Research status | In progress |
| DMX modes | 8 channels. RGB, CH6 effects, and the CH8 dimmer checked on the unit. Strobe and macro boundaries open |
| Firmware | |
| Supply | Printed AC90–250V, fixed mains cable |
| Units on hand | — |
| Documentation | [Manual rev. 1.0](manual.md) — October 2026 |

## Summary

Round RGB PAR with a field of individual LED optics, a yoke, and 10 DIP switches. One 8-channel mode. Manufacturer and model number are unknown. Similar PARs use different maps. The measurement on this unit applies.

**CH6 selects the effect, not the speed.** 0–127 is automatic color change, speed on CH7. 128–255 is color fading, speed on CH4. CH6 = 0 is already color change, not “effect off”.

**CH8 is a normal dimmer.** 0 is off, 255 is full.

Profile: [`profiles/LED_PAR_36x_RGB_(DIP).qxf`](profiles/LED_PAR_36x_RGB_(DIP).qxf) (QLC+ 5.2.1), mode `8 Channel - research`. The `Manufacturer` field is `dmx-fixture-research`.

## Identification

### Markings

- Model number: none
- Rear: CE, AUTO, MUSIC, SPEED knob, green DMX signal lamp, 10 red DIP switches
- DMX IN printed `1:G`, `2:-`, `3:+`. DMX OUT next to it
- Bottom: AC90–250V. Mains cable fixed through a grommet, no separate appliance inlet
- Serial number: none

### Technical data

20 W, 1.5 kg, 200 × 200 × 200 mm, and 15° exist only in the QXF and were not measured. Lumens and color temperature in the profile are 0.

| Property | Value | Source |
| --- | --- | --- |
| Optics | Field of individual LED lenses, RGB. 36 pieces in the working name, not counted | Photo / working name |
| Supply | AC90–250V, fixed cable | Rear photo |
| Power consumption | 20 W | QXF only |
| Dimensions / weight | 200 × 200 × 200 mm, 1.5 kg | QXF only |
| Beam angle | 15°, focus fixed, no pan/tilt | QXF only |
| DMX | 8 channels, 3-pin IN and OUT | Measurement / photo |
| Address | DIP 1–9 binary. DIP 10 unexplained. Address 1 with only DIP 1 ON was used in the test | Measurement / conventional binary address |
| Standalone | AUTO, MUSIC, SPEED | Photo. Sequence not logged |

### Photos

| File | Contents |
| --- | --- |
| [photos/front-leds.jpg](photos/front-leds.jpg) | LED field, yoke |
| [photos/front-side.jpg](photos/front-side.jpg) | Side, cooling fins, yoke |
| [photos/rear-panel.jpg](photos/rear-panel.jpg) | DIP, AUTO, MUSIC, SPEED, DMX, AC90–250V |

## Files in this folder

| File | Contents |
| --- | --- |
| [manual.md](manual.md) | Operating manual rev. 1.0 |
| [dmx-channels.md](dmx-channels.md) | 8-channel map with measurement status |
| [test-notes.md](test-notes.md) | Measured values and open points |
| [profiles/LED_PAR_36x_RGB_(DIP).qxf](profiles/LED_PAR_36x_RGB_(DIP).qxf) | QLC+ fixture |

## Open questions

- [ ] Manufacturer and model
- [x] 8-channel DMX, RGB, CH6 ranges, CH8 direction
- [ ] CH4 color boundaries and the direction of both speeds
- [ ] CH5 strobe boundaries and direction
- [ ] DIP 10, AUTO, MUSIC, SPEED
- [ ] Whether any value turns automatic effects fully off. CH6 = 0 does not
- [ ] Power, dimensions, weight, beam angle
- [x] QLC+ profile matches the installed definition
- [ ] Profile checked live against the fixture for the channels that are still open
