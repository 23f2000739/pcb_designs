# 5V Regulated Power Supply (LM7805)

A linear regulated 5V DC power supply designed in KiCad. It converts an AC
transformer output into a stable 5V DC output using a bridge rectifier,
a reservoir capacitor and an LM7805 voltage regulator.

<img width="642" height="315" alt="image" src="https://github.com/user-attachments/assets/daa8c837-7a56-4b27-9077-10a53a7b3da0" />


## Overview
The AC input is full-wave rectified by a bridge of four 1N4007 diodes and
smoothed by a filter capacitor. The LM7805 then regulates the DC voltage
down to a fixed 5V. A power LED shows when the output is live.

## Specifications
- Input: 9V-12V AC (from a step-down transformer)
- Output: 5V DC regulated
- Maximum output current: 1A (heatsink recommended at higher loads)
- Regulator: LM7805, TO-220 package

## Circuit description
- **J1:** AC input connector
- **D1-D4 (1N4007):** full-wave bridge rectifier
- **C1:** polarized filter (reservoir) capacitor
- **C2, C3:** high-frequency decoupling capacitors at the regulator input and output
- **U1 (LM7805):** 5V linear voltage regulator
- **R1 + D5:** power indicator LED with current-limiting resistor

## Working principle
1. The transformer steps the mains voltage down to a low AC voltage.
2. The bridge rectifier converts AC to pulsating DC.
3. C1 smooths the pulsating DC into DC with small ripple.
4. The LM7805 regulates this to a constant 5V.
5. C3 stabilizes the output, and the LED indicates power.


<img width="462" height="356" alt="image" src="https://github.com/user-attachments/assets/4f1e3508-bab7-47ee-8432-cb0d38246e50" />

<img width="827" height="601" alt="image" src="https://github.com/user-attachments/assets/4dd875c3-e235-40dc-a378-302c2b41bc78" />
