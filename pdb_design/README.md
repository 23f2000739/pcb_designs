# 5V UAV Power Distribution Board (PDB)

This project showcases a manufacturing-ready, 2-layer DC-to-DC Buck Converter circuit board designed in KiCad 8.0, tailored to step down high-voltage drone battery inputs (e.g., 12V 3S LiPo) to a stable 5V rail for flight controllers and critical avionics payloads.

## 🛠️ Key Technical Features
- **Regulator Architecture:** Integrated Texas Instruments LM2596S-5.0 switching regulator stepping down noisy DC inputs to an ultra-stable 5.0V output loop at a switching frequency of 150 kHz.
- **High-Current Power Tracing:** Main power delivery paths are widened to **1.2mm traces** based on IPC-2152 safety margin rules to handle 2A continuous current while preventing thermal trace lifting.
- **EMI & Noise Shielding:** Component layout optimized to keep high-frequency AC switching loops (Regulator, Schottky Catch Diode, and 33µH Inductor) tightly clustered together. The entire bottom copper layer functions as a solid, unbroken **Copper Ground Plane (GND)** to maximize electromagnetic isolation for sensitive drone communication modules.
- **Visual Diagnostics:** Features a current-limited green LED status indicator circuit (330-ohm resistor loop) for instant laboratory bench power validation.

## 📸 Design Architecture & Visuals

### 1. 3D Component Render
*This 3D overview demonstrates realistic system layout spacing and component heights for drone chassis clearance limits.*
![3D Render](3d_render.png)

### 2. Physical 2-Layer Copper Tracking Route
*This view shows the wide 1.2mm copper highways on the Top Red layer, ensuring zero vias on the power net and keeping the bottom layer perfectly solid for interference isolation.*
![PCB Route](pcb_layout.png)

### 3. Logic Schematic Blueprint
*The complete logical connection layout including the feedback loop tracking loop running to Pin 4 for automated voltage regulation.*
![Schematic](schematic.png)

---
*Note: The editable project source data (`.kicad_sch` and `.kicad_pcb`) along with fabrication Gerber blueprints are available in this folder directory.*
