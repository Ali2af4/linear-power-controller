# linear-power-controller
This project is an adjustable linear power controller, designed to provide smooth, manual control over a DC load.
# Simple DC Linear Dimmer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **⚠️ SAFETY WARNING: DANGEROUS DESIGN AS LABELED**
> The schematic input is labeled "220V". Connecting 220V AC directly to this transformerless circuit is **extremely dangerous and potentially lethal**. This documentation assumes the circuit is powered by a **low-voltage, isolated DC source** for safe operation and testing.

## Project Description

This project is an adjustable linear power controller, designed to provide smooth, manual control over a DC load. It features a Darlington pair power stage, driven by a potentiometer-based control circuit. This simple and robust design is ideal for applications like dimming 12V DC lamps, controlling the speed of small DC motors, or for use as a basic adjustable power source in a lab setting.

## Hardware Design

## Hardware Design

### Circuit Schematic
*The schematic for the power controller circuit.*
<img src="./Screenshot 2025-06-09 010203" alt="Circuit Schematic for DC Dimmer" width="600">

### PCB Layout
*A 3D render of the compact PCB layout.*
<img src="./Screenshot%202025-06-09%20010222.png" alt="PCB Layout 3D Render for DC Dimmer" width="600">

## How It Works

1.  **Input Stage:** A low-voltage DC input is provided at the `P1` connector and filtered by capacitor `C1`.
2.  **Voltage Regulation:** The `BZX55C12` Zener diode (`D3`), along with series resistor `R3`, creates a stable 12V reference voltage for the control circuit.
3.  **Control Stage:** The `1kΩ` potentiometer (`R4`) acts as a variable resistor that allows for manual adjustment of the base current flowing into the driver transistor, `Q2`.
4.  **Amplification Stage:** The driver transistor (`MMBT3904`) and the power transistor (`TIP31C`) form a Darlington pair. This configuration provides a very high current gain, allowing the small base current from the control stage to regulate a much larger current through the load.
5.  **Output Stage:** The `TIP31C` power transistor (`Q1`) operates in its linear region, acting as a variable resistor in series with the load (`RL`). By turning the potentiometer, the effective resistance of `Q1` changes, thus providing smooth and continuous control over the power delivered to the load.

## Key Components

* **Power Transistor:** `TIP31C`
* **Driver Transistor:** `MMBT3904`
* **Zener Diode:** `BZX55C12` (12V)
* **Potentiometer:** `1kΩ`

## Potential Applications

* Dimming 12V DC lamps or LED strips.
* Speed control for small DC motors.
* A simple, adjustable power source for lab experiments.

## Tools Used

* **Schematic & PCB Design:** Altium Designer (or Cadence / Proteus)
