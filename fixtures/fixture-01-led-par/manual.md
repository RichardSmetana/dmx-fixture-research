# RGBWAUV Wireless PAR 7CH-12CH

## Operating manual and DMX channel reference

| Field | Value |
| --- | --- |
| Fixture profile | RGBWAUV Wireless PAR 7CH-12CH |
| Profile manufacturer | dmx-fixture-research |
| Original manufacturer | Unknown / Rasha-compatible OEM |
| Firmware | V2.20 |
| Fixture type | Color changer |
| DMX modes | 7CH / 12CH |
| QLC+ version | 5.2.2 |
| Documentation | 1.1 — October 2026 |

Profile file: [`profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf`](profiles/Generic-OEM-RGBWAUV-Wireless-7-12CH.qxf).

This manual follows the QLC+ fixture definition in this project. Where the Rasha reference documentation differs, the fixture definition applies. Per-channel research status: [dmx-channels.md](dmx-channels.md).

---

## 1. Introduction

The RGBWAUV Wireless PAR is a compact LED fixture for stage, events, architectural lighting, and mobile use.

It mixes six colors: red, green, blue, white, amber, and ultraviolet.

The fixture supports wired DMX512, wireless DMX, standalone operation, automatic programs, sound control, and master/slave.

The panel and functions resemble the Rasha Professional HEX V12 Wireless Flat PAR. The hardware manufacturer is not identified.

### Features

- Seven LED optics
- RGBWAUV color mixing
- 7-channel and 12-channel DMX
- Wireless DMX receiver with a whip antenna (2.4 GHz according to the description)
- 3-pin XLR DMX input and output
- Master dimmer in 12CH mode
- Strobe, pulse, and random strobe
- 38 standalone color presets
- Automatic color programs
- Sound effects
- Memory for custom colors
- Four-button LED panel
- Firmware version display

---

## 2. Safety

### General

- Do not look directly into the light source.
- Disconnect mains power before maintenance.
- Connect only to a properly grounded circuit.
- Do not connect the fixture to a dimmer pack or a rheostat.
- Do not operate it if the housing, connectors, lenses, or cables are damaged.
- Keep ventilation openings clear.
- Do not expose it to rain or heavy moisture.
- Do not aim the lenses at the sun.
- Disconnect it during long periods of non-use.

### Mounting

Mount the fixture with the adjustable yoke.

Above head height: use a suitable clamp and a separate safety cable.

Leave clearance around the housing for cooling. The Rasha reference manual cites at least 50 cm from adjacent surfaces.

### Temperature

The Rasha documentation cites conflicting maximum ambient temperatures of 45 °C and 50 °C.

Until this fixture’s rating label confirms the limit, use **45 °C** as the conservative maximum.

---

## 3. Connections

### 3.1 Supply

The rear is printed **POWER IN AC90-240V**. Mains frequency is not printed there. The Rasha reference manual also cites 50/60 Hz. That is not confirmed on this unit.

### 3.2 Connector panel

From left to right, see [photos/rear-panel.jpg](photos/rear-panel.jpg):

- 4-digit display and the buttons MENU, DOWN, UP, ENTER
- DMX OUT, 3-pin XLR
- DMX IN, 3-pin XLR
- POWER OUT, IEC
- POWER IN, IEC, printed AC90-240V

The whip antenna sits above the connectors. There is no separate wireless LED on the rear.

### 3.3 Mains

- POWER IN, printed AC90-240V
- POWER OUT for linking more fixtures

Do not exceed the current rating of the connectors or cables. The fuse rating is not readable in the photos.

### 3.4 DMX

3-pin XLR, labeled on the fixture:

- DMX OUT
- DMX IN

Fixtures can be daisy-chained.

### 3.5 Wireless DMX

A whip antenna is fitted. The 2.4 GHz figure comes from the fixture description and is not printed on the housing.

1. Power the fixture on.
2. Select the DMX channel mode.
3. Set the start address.
4. Power on a compatible wireless DMX transmitter.
5. Set the receiver to the same wireless group or ID as the transmitter.
6. Check the display. There is no separate receive LED.

Wireless replaces only the DMX cable. Mains power is still required.

The exact pairing steps depend on the installed receiver module.

---

## 4. Control panel and menu

### 4.1 Buttons

Printed from left to right: MENU, DOWN, UP, ENTER. Next to them is a 4-digit 7-segment display. See [photos/rear-panel.jpg](photos/rear-panel.jpg).

| Button | Function |
| --- | --- |
| MENU | Change menu or go back one level |
| DOWN | Decrease a value / previous item |
| UP | Increase a value / next item |
| ENTER | Select or confirm |

### 4.2 Menu map

| Menu | Values | Description |
| --- | --- | --- |
| Addr | 001–512 | DMX start address |
| Chnd | 7 / 12 | DMX channel mode |
| SLnd | Slav / Nast / Sync / CliC | Fixture and sync modes |
| Shnd / CoLo | 1–38 | Static color presets |
| Shnd / FADE | 1–3 | Color fades |
| Shnd / FLAS | 1–100 | Flash / strobe programs |
| Shnd / Auto | 1–9 | Automatic programs |
| Soun | 1–6 | Sound modes |
| Cust | CC1–CC5 | Custom color presets |
| Dinn | 1–3 | Dimmer modes |
| Blnd | On / Off | Blackout |
| LED | On / Off | Display backlight |
| Disp | Normal / Inverted | Display orientation |
| Test | Start | Self-test |
| Fhrs | Hours | Operating-hour counter |
| Ver | Version | Firmware |
| Rest | Reset | Factory settings |

Sync, CliC, the dimmer curves, and the individual sound programs can differ by firmware or OEM variant and need to be checked one by one.

### 4.3 DMX address

1. Select `Addr`.
2. Press ENTER.
3. Set the address with UP and DOWN.
4. Confirm with ENTER.

Address `001` places the first fixture channel on DMX address 1.

### 4.4 Channel mode

1. Select `Chnd`.
2. Press ENTER.
3. Select `7` or `12`.
4. Confirm with ENTER.

The color order differs:

- **7CH:** CH4 white, CH5 amber
- **12CH:** CH4 amber, CH5 white

These positions follow the QLC+ fixture definition. The 7CH mode is verified on the unit.

### 4.5 Fixture mode (`SLnd`)

| Setting | Function |
| --- | --- |
| Slav | Slave |
| Nast | Master |
| Sync | Synchronization |
| CliC | Additional sync / control mode |

The exact effect of Sync and CliC can differ between firmware and OEM variants.

### 4.6 Static colors

`CoLo` holds 38 predefined colors.

1. Open `Shnd`.
2. Select `CoLo`.
3. Choose a color from 1 to 38.
4. Confirm with ENTER.

The color holds without an automatic change. These 38 menu colors are independent of the DMX preset table on CH7 in 12CH mode.

### 4.7 Fade

`FADE` has three programs: FADE 1, FADE 2, and FADE 3.

The Rasha reference manual describes them from fast to slow.

### 4.8 Flash

`FLAS` runs from 1 to 100.

Higher values mean faster flashes, according to the reference manual.

### 4.9 Automatic

`Auto` contains nine programs, including color changes, fades, and other built-in effects.

### 4.10 Sound

`Soun` contains six modes. The fixture uses its built-in microphone.

Check each sound program individually.

### 4.11 Custom colors

`Cust` stores five presets: CC1, CC2, CC3, CC4, and CC5. Recall them from the menu.

### 4.12 Dimmer

`Dinn` has three settings.

The Rasha documentation describes linear, square-law, inverse-square-law, and S-curve dimming, but it does not assign those curves to the three settings consistently. Test each step on the unit.

### 4.13 Blackout

`Blnd`: On or Off. This affects blackout behavior.

### 4.14 Display

`LED`: leave the display on, or switch it off after it is idle.

`Disp`: normal or inverted display.

### 4.15 Self-test

Select `Test` and press ENTER.

### 4.16 Operating hours

`Fhrs` shows the accumulated operating time.

### 4.17 Firmware

`Ver` shows the firmware.

**On the documented unit: V2.20**

### 4.18 Reset

`Rest` and ENTER restore the factory settings. Stored settings can be lost.

---

## 5. DMX channel map

Mode names in the QLC+ profile:

| Mode | Name in QLC+ | Status |
| --- | --- | --- |
| 7CH | 7 Channel  - probable Rasha/OEM | Channel map verified on the unit. The name has two spaces before the dash. |
| 12CH | 12 Channel - probable Rasha/OEM | CH9 tested on V2.20; other channels from the fixture definition |

### 5.1 Seven channels (7CH)

| Channel | Function | DMX value |
| --- | --- | --- |
| CH1 | Red | 0–255 |
| CH2 | Green | 0–255 |
| CH3 | Blue | 0–255 |
| CH4 | White | 0–255 |
| CH5 | Amber | 0–255 |
| CH6 | UV | 0–255 |
| CH7 | Strobe / pulse | see below |

Intensity rises from 0 (off) to 255 (maximum). There is no separate master dimmer.

#### CH7 — strobe / pulse

| DMX value | Function |
| --- | --- |
| 0–15 | Open / static light |
| 16–131 | Strobe, slow to fast |
| 132–189 | Pulse / fade, bright to dark |
| 190–230 | Pulse / fade, dark to bright |
| 231–255 | Open / maximum brightness |

#### Example: static red (7CH)

| Channel | Value |
| --- | --- |
| CH1 | 255 |
| CH2 | 0 |
| CH3 | 0 |
| CH4 | 0 |
| CH5 | 0 |
| CH6 | 0 |
| CH7 | 0 |

CH7 is in an open range so the light stays on.

### 5.2 Twelve channels (12CH)

| Channel | Function |
| --- | --- |
| CH1 | Red |
| CH2 | Green |
| CH3 | Blue |
| CH4 | Amber |
| CH5 | White |
| CH6 | UV |
| CH7 | Color presets |
| CH8 | Master dimmer |
| CH9 | Strobe / pulse / random strobe |
| CH10 | Random color change |
| CH11 | Auto color change |
| CH12 | Auto / sound / strobe |

#### CH1–CH6

| DMX value | Function |
| --- | --- |
| 0 | Color off |
| 1–255 | Intensity from minimum to maximum |

Order: red, green, blue, amber, white, UV.

#### CH7 — color presets

| DMX value | Function |
| --- | --- |
| 0–10 | No function |
| 11–40 | Color preset 1 |
| 41–70 | Color preset 2 |
| 71–100 | Color preset 3 |
| 101–130 | Color preset 4 |
| 131–160 | Color preset 5 |
| 161–190 | Color preset 6 |
| 191–220 | Color preset 7 |
| 221–255 | Color preset / white balance |

The fixture definition uses these eight ranges.

The Rasha reference manual lists 32 DMX color presets. That table does not match the fixture definition and is not used here. The 38 colors in menu `CoLo` are independent of it.

#### CH8 — master dimmer

| DMX value | Function |
| --- | --- |
| 0–255 | Overall intensity, 0–100% |

#### CH9 — strobe / pulse / random strobe

Tested on firmware V2.20. The value ranges come from the measurement. The pulse descriptions come from the fixture file.

| DMX value | Function |
| --- | --- |
| 0–7 | Blackout |
| 8–15 | Open |
| 16–131 | Strobe, slow to fast |
| 132–139 | Open |
| 140–181 | Pulse: slow close, fast open |
| 182–189 | Open |
| 190–231 | Pulse: slow open, fast close |
| 232–239 | Open |
| 240–247 | Random strobe |
| 248–255 | Open |

#### CH10 — random color change

| DMX value | Function |
| --- | --- |
| 0–10 | No function |
| 11–255 | Random color change, slow to fast |

Speed rises with the DMX value.

#### CH11 — automatic color change

| DMX value | Function |
| --- | --- |
| 0–10 | No function |
| 11–255 | Automatic color change, slow to fast |

Speed rises with the DMX value.

#### CH12 — auto / sound / strobe

| DMX value | Function |
| --- | --- |
| 0–10 | No function |
| 11–120 | Auto / sound program |
| 121–255 | Auto / sound / strobe program |

The exact behavior inside these ranges can depend on the selected program or operating state.

#### Example: static red (12CH)

| Channel | Value |
| --- | --- |
| CH1 | 255 |
| CH2 | 0 |
| CH3 | 0 |
| CH4 | 0 |
| CH5 | 0 |
| CH6 | 0 |
| CH7 | 0 |
| CH8 | 255 |
| CH9 | 255 |
| CH10 | 0 |
| CH11 | 0 |
| CH12 | 0 |

CH8 at full brightness, CH9 in an open range (248–255). The other effect channels are off.

---

## 6. Technical data

The values below are stored in the QLC+ profile. They are profile data, not independently checked laboratory measurements. Lumens and color temperature in the profile are 0 and are placeholders.

### 6.1 Mechanics and optics

| Item | Value |
| --- | --- |
| Fixture type | Color changer |
| Light source | LED |
| LED optics | 7, 2–3–2 layout, front photo |
| Dimensions | 220 × 220 × 90 mm |
| Profile weight | 1 kg |
| Lens | Fresnel |
| Beam angle | 25°–40° |
| Focus | Fixed |
| Pan / tilt | Not applicable |

### 6.2 Electrical

| Item | Value |
| --- | --- |
| Power consumption | 90 W (profile value) |
| Mains | AC 90–240 V, printed on the fixture. Frequency not printed |
| DMX | 3-pin XLR, DMX IN and DMX OUT |
| Wireless | Whip antenna on the fixture; 2.4 GHz from the description |
| Fuse | Rating not readable on the fixture |
| Mains in/out | IEC POWER IN and POWER OUT |

### 6.3 Control

| Item | Value |
| --- | --- |
| Protocol | DMX512 |
| Modes | 7CH / 12CH |
| Standalone | Yes |
| Sound | Yes |
| Master/slave | Yes |
| Wireless DMX | Yes |
| Controls | 4-digit display, buttons MENU DOWN UP ENTER |
| Firmware | V2.20 |

---

## 7. Troubleshooting

| Problem | What to check |
| --- | --- |
| No light | Mains, DMX signal, shutter, and dimmer |
| No DMX response | Address and channel mode |
| Wrong colors in 7CH | CH4 is white, CH5 is amber |
| Wrong colors in 12CH | CH4 is amber, CH5 is white |
| No output in 12CH | CH8 above 0, CH9 in an open range |
| Unexpected flashing | 7CH: check CH7. 12CH: check CH9 |
| Unexpected color programs | 12CH: check CH7 and CH10–CH12 |
| Wireless does not connect | Transmitter compatibility and wireless ID |
| Display does not stay on | Menu `LED` |
| Sound does not respond | Sound mode and microphone |
| Unexpected behavior | Master/slave and the effect channels |

---

## 8. Documentation notes

### 8.1 Sources

1. QLC+ fixture definition RGBWAUV Wireless PAR 7CH-12CH in this project.
2. Observations on firmware V2.20.
3. Reference documentation for the Rasha Professional HEX V12 Wireless Flat PAR.
4. Measurements and operating tests.
5. Front and rear photos in [photos/](photos/).

### 8.2 Identification

The hardware manufacturer is not finally identified. The fixture resembles the Rasha HEX series and has a similar menu.

The `Manufacturer` field in the QLC+ profile is `dmx-fixture-research`. That names the project maintaining the profile. It is not evidence of the hardware manufacturer.

### 8.3 Profile

- QLC+ 5.2.2
- Model: RGBWAUV Wireless PAR 7CH-12CH
- Manufacturer: dmx-fixture-research
- Modes: `7 Channel  - probable Rasha/OEM`, `12 Channel - probable Rasha/OEM`

Channel order, values, and effect descriptions follow this definition. Later profile changes must be copied into this manual.

### 8.4 What has been checked

- **7CH:** channel map verified on the unit.
- **12CH, CH9:** strobe ranges tested on firmware V2.20.
- Color presets, automatic effects, and the other 12CH channels come from the fixture definition. More detailed measurements are still open.
- Dimensions, weight, power consumption, lens type, and beam angle come from the profile and were not independently checked.
- Visible on the housing: seven optics, yoke, DMX OUT/IN, POWER IN AC90-240V, POWER OUT, whip antenna, buttons MENU DOWN UP ENTER, marks CE, WEEE, and RoHS. Manufacturer, model, and mains frequency are not in the photos. There is no separate wireless LED.
- The menu map is described and has not been walked item by item on the display.
- The DMX ranges in both modes cover 0–255 with no gap. That matches the QXF file.

---

*End of manual — revision 1.1*
