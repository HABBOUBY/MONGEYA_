<div align="center">

# MONGEYA

### Smart Home Cleaning Station with an Autonomous Cleaning Robot

*A modular robotic ecosystem designed to automate repetitive household cleaning tasks.*

<!-- Replace with your best render -->
<img src="media/hero.png" width="900">

![ESP32](https://img.shields.io/badge/ESP32-WROOM--32-red)
![KiCad](https://img.shields.io/badge/PCB-KiCad-blue)
![SolidWorks](https://img.shields.io/badge/CAD-SolidWorks-orange)
![3D Printing](https://img.shields.io/badge/Fabrication-FDM%203D%20Printing-success)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

# About

MONGEYA is a smart cleaning station that automates several repetitive household tasks. It combines multiple cleaning systems inside a single machine and works together with **MONGY**, a compact autonomous robot that leaves the station to clean the floor before returning automatically to recharge.

The entire project was designed from scratch, including the mechanical structure, electronics, embedded system, and custom PCB.

---

# Why I Built This

The inspiration behind MONGEYA comes from my mother.

Every day she spends a significant amount of time cleaning shoes, sorting waste, and handling repetitive household chores. I wanted to design a machine capable of taking over these repetitive tasks, giving her more free time while making home cleaning easier and smarter.

---

# Meet MONGY

MONGY is the autonomous cleaning robot inside MONGEYA.

When the station detects that floor cleaning is needed, MONGY leaves its docking station, cleans the surrounding area using multiple cleaning mechanisms, and automatically returns to recharge.

---

# Features

- Automatic waste sorting
- Automatic chemical dispensing
- Shoe cleaning station
- Autonomous floor cleaning
- Automatic docking
- Automatic battery charging
- LiDAR navigation
- PID motor control
- Custom ESP32 PCB
- Fully 3D printable mechanical design

---

# Hardware

## Main Controller

- ESP32-WROOM-32

## Navigation

- RPLIDAR
- Hall-effect magnetic encoders
- IR sensors

## Motors

- JGB37 DC gear motors
- MG995 servo motors
- MG90 metal gear servo

## Cleaning

- Roller brush
- 12V vacuum pump
- Two 12V dosing pumps

## Batteries

### MONGY

- Compact 3S LiPo battery

### MONGEYA

- Three independent 3S LiPo batteries powering different subsystems.

---

# Dimensions

## MONGY

| Property | Value |
|----------|------:|
| Diameter | 210 mm |
| Height | 50 mm |
| Weight | ~2 kg |

## MONGEYA

| Property | Value |
|----------|------:|
| Length | 400 mm |
| Width | 400 mm |
| Height | 600 mm |
| Weight | ~15 kg |

---

# 3D Printing

## Materials

- ABS for structural and high-stress components
- PLA for lightweight and cosmetic parts

## Recommended Print Settings

| Setting | Value |
|---------|------|
| Layer Height | 0.20 mm |
| Nozzle | 0.4 mm |
| Infill | 20% |
| Walls | 3 |
| Supports | Only where needed |

---

# Fasteners

| Screw | Quantity |
|-------|---------:|
| M3 × 10 mm | 25 |
| M3 × 13 mm | 15 |
| M3 × 15 mm | 15 |
| M3 × 19 mm | 5 |

Total: **60 M3 screws**

---

# Electronics

MONGY uses a custom PCB designed in **KiCad** around the **ESP32-WROOM-32**.

The repository contains:

- PCB Layout
- Schematic
- KiCad Project Files
- Component List (BOM)

The MONGEYA station intentionally uses modular perfboards for auxiliary circuits such as chemical dispensing and opto-isolated interfaces, making maintenance and future upgrades easier.

---

# Repository Structure

```text
mongeya-main/
│
├── 3D/
│   ├── STEP/
│   ├── STL/
│   └── SolidWorks/
│
├── pcb/
│   └── mongy/
│
├── docs/
│
├── media/
│
└── README.md
```

---

# Assembly

1. Print all STL files.
2. Assemble the mechanical structure using the specified M3 screws.
3. Install the motors, pumps and sensors.
4. Mount the custom PCB inside MONGY.
5. Connect batteries and wiring.
6. Upload the firmware.
7. Dock MONGY inside MONGEYA.

---

# CAD Files

This repository includes:

- Native SolidWorks files
- STEP files
- STL files

allowing anyone to modify or reproduce the project.

---

# Documentation

Additional documentation is available inside the **docs/** folder, including:

- Project presentation
- Design renders
- Technical documentation

---

# Gallery

## MONGEYA

*(Insert render here)*

## MONGY

*(Insert render here)*

## PCB

*(Insert PCB images here)*

---

# Future Improvements

- AI-based object recognition
- Automatic water refill
- Mobile application
- Voice assistant integration
- Multi-room navigation

---

# License

This project is released under the **MIT License**.
