# Tiny Solar Power Supply – 3.3V Regulated Output

A compact solar-powered power supply that converts energy from a small solar panel and a single 1.2 V Ni-MH AA rechargeable battery into a stable **3.3 V regulated output**, suitable for low-power embedded and IoT applications.

---

## 📌 Overview

This project demonstrates a **low-power boost converter–based solar supply** using the **AP3015/AP3015A micropower DC/DC step-up converter**.  
During daylight, the solar panel charges the battery and disables the boost converter. When light is no longer available, the circuit automatically enables the boost converter and powers the load from the battery.

The design focuses on **efficiency, simplicity, and compact size**, making it ideal for small standalone electronics.

---

## ⚙️ Features

- Regulated **3.3 V output**
- Operates from a **single 1.2 V Ni-MH AA battery**
- Supports **solar charging**
- Automatic **day/night power switching**
- Low-power, high-efficiency design
- Compact PCB footprint

---

## 🔋 How It Works

1. **Daytime Operation**
   - Solar panel charges the Ni-MH battery through a diode.
   - A MOSFET disables the boost converter to prevent unnecessary power loss.

2. **Nighttime Operation**
   - Solar voltage drops.
   - Boost converter is enabled automatically.
   - Battery voltage is stepped up and regulated to **3.3 V**.

The output voltage is set using a resistor feedback network:


---

## 🧩 Main Components

- **AP3015 / AP3015A** – Micropower boost DC/DC converter  
- **2N7002** – MOSFET for automatic switching  
- **SS14** – Schottky diodes  
- **10 µH Inductor**
- Ceramic capacitors (X7R)

---

## 📋 Bill of Materials (BOM)

| Component | Value / Part Number |
|---------|---------------------|
| IC1 | AP3015 / AP3015A |
| L1 | 10 µH, ≥680 mA |
| D1, D2 | SS14 |
| T1 | 2N7002 |
| R1 | 1 MΩ |
| R2 | 604 kΩ (1%) |
| R3 | 10 kΩ |
| R4 | 1 MΩ |
| C1 | 4.7 µF |
| C2 | 22 µF |
| C3 | 10 pF |

---

## 🔌 Connections

| Connector | Description |
|---------|-------------|
| K1 | 3.3 V Output |
| K2 | Battery Input |
| K3 | Manual ON/OFF (optional) |
| K4 | Solar Panel Input |

---

## 📐 Files Included

- Schematic
- PCB layout
- Gerber files
- BOM
- Documentation

---

## 🛠 Applications

- Solar-powered IoT devices
- Low-power microcontroller projects
- Environmental sensors
- Educational electronics projects

---

## 📄 Reference

Based on **“Tiny Solar Supply – Sunlight In, 3.3 V Out”**  
Original concept by **Clemens Valens**, Elektor Magazine.

---


