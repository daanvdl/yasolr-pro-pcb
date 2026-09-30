# YaSolR All-in-One PCB

Compact all-in-one PCB for **YaSolR “The Professional”**.

Based on:  
https://yasolr.carbou.me/build/#the-professional

The board combines the main YaSolR logic and control hardware on a single PCB and can be powered directly from **230 V AC**.

Only the voltage regulator and optional bypass relay remain external.

## Features

- YaSolR “The Professional” configuration
- 230 V AC input
- Wi-Fi
- Wired Ethernet / UTP
- JSY-MK-194T power measurement
- DFR1073 DAC control
- SSD1306 OLED
- DS18B20 support
- Status LEDs
- External bypass relay output
- Fused mains input
- No external ZCD required

## Required Parts

- Hi-Link HLK-5M05
- 5×20 mm fuse holder, 22 mm pitch
- T1A fuse
- 3-pin HB9500 screw terminal
- LilyGO T-ETH-Lite S3
- 3× 330 Ω resistor
- 1× 4.7 kΩ resistor
- SSD1306 OLED
- 2N2222 transistor
- JSY-MK-194T
- DFRobot DFR1073 DAC
- Loncont LSA-H3P50YB *(external)*
- 5 V / 30 A relay module *(external, optional)*

## GPIO Configuration

```json
{
  "pin_ds18": 4,
  "pin_i2c_scl": 40,
  "pin_i2c_sda": 41,
  "pin_lights_g": 8,
  "pin_lights_r": 5,
  "pin_lights_y": 6,
  "pin_o1_dim": 19,
  "pin_o1_ds18": -1,
  "pin_o1_relay": 20,
  "pin_o2_dim": -1,
  "pin_o2_ds18": -1,
  "pin_o2_relay": -1,
  "pin_relay1": -1,
  "pin_relay2": -1,
  "pin_serial1_rx": -1,
  "pin_serial1_tx": -1,
  "pin_serial2_rx": 18,
  "pin_serial2_tx": 17,
  "pin_zcd": -1
}
```

## PCB Manufacturing

Gerber files are available in the **`Gerber/`** directory.

The board was manufactured by **JLCPCB** using:

- 2-layer FR-4
- 1.6 mm PCB thickness
- Standard JLCPCB options

## DIN-Rail Installation

In my installation, the PCB is mounted together with the **LSA-H3P50YB** and the external bypass relay on DIN rail.

For the PCB I use a:
**PM107, Length 150 mm DIN-rail PCB holder**

## Performance

I have been running this setup for several months and the results are very good.

The combination of the JSY-MK-194T, DAC-controlled LSA regulator and YaSolR control loop provides very accurate power regulation, resulting in an almost flat grid-power curve around the configured target.

## Software

YaSolR:  
https://github.com/mathieucarbou/YaSolR

Documentation:  
https://yasolr.carbou.me/

## Safety

**Warning: this PCB is connected directly to 230 V AC mains voltage.**

Only build or install this board if you understand mains-voltage electrical safety.

Use a suitable enclosure, proper fusing, correct wiring, sufficient creepage and clearance, and appropriate protection against accidental contact.

## Disclaimer

This hardware is provided as-is and without warranty.

You are responsible for verifying the PCB, wiring, component ratings and electrical safety before use.