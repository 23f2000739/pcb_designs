# LM2596 5V Buck Converter

A 5V fixed-output step-down (buck) DC-DC converter, designed in KiCad
(schematic capture and 2-layer PCB layout).



<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/dc0a1a0b-3248-4252-8c70-6e7e012b72e6" />




## Overview
The board steps a higher DC input voltage down to a regulated 5V using the
LM2596S-5 switching regulator (150 kHz, up to 3A). 

## Specifications
- Input voltage: 7V to 24V DC (limited by the 35V input capacitor rating)
- Output voltage: 5V fixed
- Maximum output current: up to 3A (with adequate heat dissipation)
- Switching frequency: 150 kHz (typical)
- Board: 2-layer PCB, through-hole connectors, SMD regulator/diode/inductor

- ## Circuit description
- **U1 – LM2596S-5:** integrated switch and control circuit; feedback pin
  connected directly to the 5V output (fixed-voltage version)
- **C1 – 100µF/35V:** input capacitor
- **L1:** energy-storage inductor
- **D2 – 1N5822:** Schottky catch diode
- **C2 – 330µF/10V:** output filter capacitor
- **D1 + R1 (330Ω):** power indicator LED
- **J1 / J2:** input and output connectors
- ON/OFF pin tied to GND, so the regulator is always enabled

- ## PCB design notes
- 1.2mm traces for input and output paths
- Catch diode and capacitors placed close to the regulator to keep the
  switching loop short.

- <img width="700" height="400" alt="image" src="https://github.com/user-attachments/assets/9debdd85-830e-4672-b0ad-3ac94b91a530" />


## 3d view
<img width="1337" height="754" alt="buck converter" src="https://github.com/user-attachments/assets/fb3d3859-e56f-4828-9520-fa95a03df442" />


