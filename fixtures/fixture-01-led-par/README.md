# Fixture 01 — LED PAR (RGBWAUV wireless)

| Field | Value |
| --- | --- |
| Placeholder ID | `fixture-01-led-par` |
| Type | LED PAR / color changer |
| Profile manufacturer | dmx-fixture-research |
| Hardware manufacturer / model | Unknown / Rasha-compatible OEM — RGBWAUV Wireless PAR 7CH-12CH |
| Research status | In progress |
| DMX modes | 7CH verified; 12CH strobe (CH9) tested on V2.20; remaining 12CH channels suspected |
| Firmware | V2.20 |
| Supply | AC 90–240 V printed on the fixture; 90 W is a profile value only |
| Units on hand | — |
| Documentation | [Manual rev. 1.1](manual.md) — October 2026 |

## Summary

Compact RGBWAUV LED PAR with seven optics, wired DMX512 (3-pin XLR in and out), wireless DMX through a whip antenna, standalone, sound, and master/slave. The 2.4 GHz figure comes from the fixture description, not from the housing. The panel and menu resemble the Rasha Professional HEX V12 Wireless Flat PAR. The hardware manufacturer is not identified.

The **7-channel mode** is verified on the unit: red, green, blue, white, amber, UV, strobe. In the **12-channel profile**, amber and white are swapped (amber CH4, white CH5). That order has not been fully remeasured. The CH9 value ranges were tested on firmware V2.20. The pulse direction comes from the fixture file. The other 12CH channels follow the fixture definition.

Profile: [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf) (QLC+ 5.2.2). The `Manufacturer` field is `dmx-fixture-research` and names this project, not the hardware maker. The 7CH mode is named `7 Channel  - probable Rasha/OEM` in the profile (two spaces before the dash). The channel map itself is verified. The 12CH mode is named `12 Channel - probable Rasha/OEM`.

The folder name stays a placeholder until the rating label and model are known.

## Identification

### Markings and rating label

- Model number: not recorded (working name: RGBWAUV Wireless PAR 7CH-12CH)
- Serial number:
- Firmware on the unit: V2.20 (`Ver` in the menu)
- Other marks: CE, WEEE, and RoHS on the rear. No manufacturer or model name is readable. Menu similar to the Rasha HEX V12.

### Technical data

Profile values are not laboratory measurements. Lumens and color temperature in the QLC+ profile are 0.

| Property | Value | Source |
| --- | --- | --- |
| Dimensions (W×H×D) | 220 × 220 × 90 mm | QLC+ profile, not independently checked |
| Weight | 1 kg | QLC+ profile, not independently checked |
| LED fit | 7 optics, 2–3–2 layout, RGBWAUV | Front photo / verified 7CH mode |
| Beam angle | Fresnel, fixed, 25–40° | QLC+ profile, not independently checked |
| Supply voltage | AC 90–240 V, printed “POWER IN”. Frequency not printed | Rear photo |
| Power consumption | 90 W | QLC+ profile |
| Ambient temperature | Conservative maximum 45 °C until the label confirms it | Rasha documentation cites both 45 °C and 50 °C |
| DMX in/out | 3-pin XLR, DMX OUT then DMX IN from the left. Whip antenna present. No separate wireless LED | Rear photo |
| Mains in/out | IEC “POWER IN” and IEC “POWER OUT”. Fuse rating not readable | Rear photo |
| Display / menu | 4-digit 7-segment display. Buttons from the left: MENU, DOWN, UP, ENTER. Firmware V2.20 | Rear photo / manual rev. 1.1 |
| Likely equivalent | Rasha Professional HEX V12 Wireless Flat PAR | Similar menu; the 32 Rasha DMX color presets are not used |

### Menu (short)

Full map in [manual.md](manual.md). `Addr` 001–512, `Chnd` 7/12, `SLnd` Slav/Nast/Sync/CliC, `CoLo` 1–38, `FADE` 1–3, `FLAS` 1–100, `Auto` 1–9, `Soun` 1–6, `Cust` CC1–CC5, `Dinn` 1–3, `Blnd`, `LED`, `Disp`, `Test`, `Fhrs`, `Ver`, `Rest`.

The 38 menu colors are independent of the eight DMX ranges on CH7 in 12CH mode.

### Photos

| File | Contents |
| --- | --- |
| [photos/front-optics.jpg](photos/front-optics.jpg) | Front, seven LED optics, yoke |
| [photos/rear-three-quarter.jpg](photos/rear-three-quarter.jpg) | Rear three-quarter, display, yoke, vents |
| [photos/rear-panel.jpg](photos/rear-panel.jpg) | Connectors, buttons, AC 90–240 V print |

Still open: a rating label with manufacturer and model, the fuse rating, and the circuit board.

## Files in this folder

| File | Contents |
| --- | --- |
| [manual.md](manual.md) | Operating manual rev. 1.1 |
| [dmx-channels.md](dmx-channels.md) | Channel map with research status |
| [test-notes.md](test-notes.md) | Measurements and open points |
| [profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf) | QLC+ fixture, matching the installed definition |

## Open questions

- [x] Mains voltage readable on the housing (AC 90–240 V)
- [ ] Hardware manufacturer, model, fuse rating, ambient temperature
- [x] DMX modes and channel counts known (7 and 12)
- [x] 7CH mode verified
- [x] 12CH CH9 strobe ranges tested on firmware V2.20
- [ ] 12CH color channels, presets, dimmer, and CH10–CH12 checked on the unit
- [ ] `Dinn` 1–3 curves, sound programs 1–6, Sync/CliC
- [ ] Pairing of the installed wireless receiver
- [x] QLC+ profile matches the installed definition
- [ ] Profile driven live against the fixture
