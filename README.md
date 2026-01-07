# Tiny Solar Power Supply (3.3V / 5V) – KiCad PCB Design

## Overview
This project presents a **compact, efficient Tiny Solar Power Supply PCB** designed using **KiCad**.  
The board accepts power from a **solar panel and/or battery**, automatically manages source selection, and generates a **regulated DC output** using a high-efficiency **switch-mode DC-DC converter**.

The design is suitable for **breadboard prototyping**, low-power embedded systems, and IoT applications where space and efficiency are critical.

---

## Key Features
- Solar + Battery input with **diode OR-ing**
- High-efficiency **switch-mode DC-DC converter**
- Automatic enable/disable using MOSFET-based control
- Regulated **3.3V output** (configurable via feedback network)
- Compact **2-layer PCB**
- Fully verified with **ERC & DRC checks**
- Complete **schematic, PCB layout, and 3D model**

---

## Circuit Functionality
The circuit is based on the **AP3015/AP3015A boost converter**, which steps up a low input voltage (from a solar panel or battery) to a regulated output.

- **Input Power Stage**
  - Solar and battery inputs are isolated using **Schottky diodes (SS14)** to prevent reverse current.
  - The higher available voltage source automatically supplies the circuit.

- **Enable / Shutdown Control**
  - A **2N7002 NMOS** controls the SHDN pin of the converter.
  - This ensures the converter only operates when sufficient input voltage is present.

- **DC-DC Conversion**
  - The converter switches at high frequency.
  - Energy is stored in the inductor and transferred to the output through a Schottky diode.
  - This provides high efficiency compared to linear regulators.

- **Feedback & Regulation**
  - A resistor divider feeds back the output voltage to the FB pin.
  - The converter dynamically adjusts duty cycle to maintain a stable output.

- **Filtering**
  - Input and output capacitors reduce ripple and switching noise.

---

## Main Components
- **DC-DC Converter:** AP3015 / AP3015A  
- **Inductor:** ASPI-0630LR-100M-T15 (10 µH)  
- **Diodes:** SS14 Schottky diodes  
- **MOSFET:** 2N7002  
- **Capacitors:** X7R ceramic capacitors  
- **Connectors:** 2.54 mm pin headers (breadboard compatible)

---

## Tools Used
- **KiCad 9**
  - Schematic capture
  - PCB layout
  - 3D visualization
  - ERC & DRC validation

---

## Applications
- Solar-powered embedded systems
- IoT sensor nodes
- Low-power microcontroller projects

---





