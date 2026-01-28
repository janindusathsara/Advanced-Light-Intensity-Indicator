# Advanced-Light-Intensity-Indicator

A fully hardware-based ambient light monitoring and analysis system implemented using analog circuits and discrete digital logic, without microcontrollers or programmable ICs.

## Project Overview

The **Advanced Light Intensity Indicator (ALII)** is a digital hardware design project developed for the **EE3204 - Digital Signal Processing module (Semester 3)** at the **University of Moratuwa**.

The system measures ambient light intensity using an LDR, removes power-line noise through analog filtering, stabilizes readings against transient fluctuations, and computes both real-time and time-averaged light intensity values.  

A strict design constraint was imposed: **no microcontrollers, programmable ICs, or task-specific ICs** were allowed. The complete system was implemented using **analog components, logic gates, flip-flops, counters, and timers**.
## System Architecture

The ALII system is divided into four main functional blocks:

1. **Analog Filter**
   - Second-order Butterworth low-pass filter
   - Suppresses 50–100 Hz power-line interference
   - Preserves slow ambient light variations

2. **LDR-Based Real-Time Monitoring**
   - LDR voltage divider with comparator-based quantization
   - 3-bit digital output representing light levels (0–7)
   - Real-time display using a seven-segment decoder and display

3. **Stability Detection**
   - Prevents false updates caused by short-term light changes
   - Output updates only if the light level remains stable
   - Adjustable stability duration: **30 s – 300 s**

4. **Time-Based Averaging**
   - Computes average light intensity over extended periods
   - Adjustable averaging window: **300 s – 900 s**
   - Implemented using integrators, counters, adders, and flip-flop accumulators

## Simulation

The complete system was simulated using **Falstad Circuit Simulator**.

🔗 **Live Simulation Link:**  
https://www.falstad.com/circuit/circuitjs.html?ctz=...

> The simulation demonstrates:
> - Noise suppression in the analog filter stage  
> - Real-time light intensity quantization (0–7)  
> - Stability-based update logic  
> - Time-domain averaging and separate averaged output display  

Simulation files included in this repository correspond to individual functional blocks and the integrated system.

## Repository Contents

- `/simulation/` – Falstad simulation files for individual subsystems and full integration  
- `/report/` – Project report detailing design methodology, calculations, and results  
- `/figures/` – Circuit diagrams and block diagrams used in the report  
- `README.md` – Project overview and documentation

## Design Constraints

- ❌ No microcontrollers  
- ❌ No programmable ICs  
- ❌ No task-specific ICs  

✔ Allowed components:
- Logic gates  
- Flip-flops  
- Counters  
- Timers (555)  
- Operational amplifiers  
- Discrete analog components

## Applications

- Energy-efficient lighting systems  
- Smart infrastructure and public lighting  
- Hardware-based sensor monitoring  
- Educational reference for discrete DSP-oriented hardware design

## Academic Context

Course: Digital Signal Processing  
Department: Electrical Engineering  
University: University of Moratuwa  

This repository is intended for **educational and demonstration purposes**.







