# Voltage Level Shifter Project

This project demonstrates the design and verification of a **Voltage Level Shifter** using Cadence tools. It includes both schematic and layout designs, along with testbench simulations and waveform analysis.

---

## Abstract

In modern mixed-signal and low-power VLSI systems, interfacing between modules operating at different voltage levels is critical. A **Voltage Level Shifter (VLS)** is designed to safely translate logic signals between two voltage domains (e.g., from 3.3V to 5V or vice versa), ensuring signal integrity and preventing device damage.

This project covers the complete process of designing a voltage level shifter in Cadence Virtuoso, including schematic creation, layout design, and post-layout simulation. The performance of the design is validated using testbenches and waveform analysis to confirm accurate level shifting under various conditions.

---

## Theory

Voltage level shifters are circuits that convert digital signals from one logic level to another. There are typically two types:

- **Low-to-High Level Shifter (LHL)**: Converts signals from a lower voltage domain to a higher one.
- **High-to-Low Level Shifter (HLL)**: Converts signals from a higher voltage domain to a lower one.

### Working Principle

The voltage level shifter generally uses:
- **NMOS pass transistors** for pull-down paths.
- **Cross-coupled PMOS pairs** for pull-up functionality.
- **Enable transistors** or biasing mechanisms to ensure correct operation during transitions.

This ensures that the output signal switches fully between 0 and 5V, even if the input only reaches 3.3V.

In this project:
- A basic **CMOS inverter** is used as a reference.
- The **Voltage Level Shifter** is designed based on cross-coupled inverters and pass-gate logic.
- The schematic and layout are designed and verified.
- Simulation waveforms validate the correct functionality.

---

## Discussion

### Design Choices
- **Technology**: Standard CMOS 120nm
- **Supply Voltages**: V<sub>DD</sub>₁ = 13.3V (input domain), V<sub>DD</sub>₂ = 5V (output domain)
- **Testbench**: Applied square wave input at 3.3V logic to test correct translation to 5V logic.

### Observations
- The output waveform follows the input logic pattern with clean transitions.
- Delay introduced by the level shifter is within acceptable limits.
- Power consumption is optimized by choosing suitable transistor sizing.

### Limitations
- Level shifter design may not function correctly for ultra-low voltages without special biasing.
- Additional protection (e.g., ESD) and robustness checks are necessary for production-grade designs.

### Conclusion
This project successfully demonstrates the design and functionality of a CMOS voltage level shifter. It highlights the importance of mixed-voltage interfacing in real-world integrated circuits and provides a foundation for advanced low-power design.

---

## Directory Structure

- `Images/` – Contains all relevant screenshots:
  - Inverter Layout
  - Inverter Schematic
  - Inverter Testbench (TB)
  - Inverter Output Waveform
  - Voltage Level Shifter Schematic
  - Voltage Level Shifter Testbench (TB)
  - Level Shifter Output Waveform

## Tools Used

- **Cadence Virtuoso** – for schematic and layout design
- **Spectre Simulator** – for simulation and waveform analysis

---

## Screenshots

| Type                         | Screenshot |
|------------------------------|------------|
| Inverter Layout              | ![Inverter Layout](Images/Inverter%20Layout.png) |
| Inverter Schematic           | ![Inverter Schematic](Images/Inverter%20Schematic.png) |
| Inverter Testbench           | ![Inverter TB](Images/Inverter%20TB.png) |
| Inverter Waveform            | ![Invertor Waveform](Images/Invertor%20Waveform.png) |
| Level Shifter Waveform       | ![Level Shifter Waveform](Images/Level%20Shifter%20Waveform.png) |
| Level Shifter Schematic      | ![Voltage Level Shifter Schematic](Images/Voltage%20Level%20Shifter%20Schematic.png) |
| Level Shifter Testbench      | ![Voltage Level Shifter TB](Images/Voltage%20Level%20Shifter%20TB.png) |

---
