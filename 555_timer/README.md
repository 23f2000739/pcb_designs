# LM555 Astable Multivibrator 

A free-running oscillator built around the LM555N timer, designed in KiCad.
It blinks an LED at about 1 Hz from a 9V supply.

<img width="526" height="362" alt="image" src="https://github.com/user-attachments/assets/f049e78f-3479-4831-a31f-1d3a4255b8d4" />


## Overview
The LM555 is wired in astable mode. The timing capacitor charges through
R1 and R3 and discharges through R3 into the discharge pin, so the output
switches between HIGH and LOW on its own with no external trigger. The
output drives an LED through a current-limiting resistor.



## Circuit description
- **U1 (LM555N):** timer IC in astable mode
- **R1, R3, C2:** timing network
- **C1:** 0.01 µF decoupling capacitor on the control-voltage pin (pin 5)
- **R2 + D1:** LED output indicator with current-limiting resistor
- Pins 2 (TRIG) and 6 (THRES) are tied together and connected to C2
- Reset pin (4) is tied to Vcc, so the timer is always enabled

## Component values
| Ref | Value | Function |
|---|---|---|
| U1 | LM555N | Timer IC |
| R1 | 3.9 kΩ | Timing resistor |
| R3 | 68 kΩ | Timing resistor |
| C2 | 10 µF / 16 V (electrolytic) | Timing capacitor |
| C1 | 0.01 µF | Control-pin decoupling |
| R2 | 1 kΩ | LED current limiter |
| D1 | LED | Output indicator |

## Working principle
1. C2 charges through R1 and R3 toward Vcc.
2. At 2/3 Vcc the output goes LOW and C2 discharges through R3.
3. At 1/3 Vcc the output goes HIGH and C2 charges again.
4. This repeats continuously, so the LED blinks.

<img width="382" height="352" alt="image" src="https://github.com/user-attachments/assets/e9406509-0818-47ae-a242-a1a8c604bcfe" />

<img width="822" height="710" alt="image" src="https://github.com/user-attachments/assets/64411514-57d6-4a65-baa4-e6a175373de3" />




