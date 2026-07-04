<div align="center">

# MONGEYA

### Smart Home Cleaning Station with an Autonomous Cleaning Robot

*A modular robotic ecosystem designed to automate repetitive household cleaning tasks.*

<img src="04_media/hero.png.PNG" width="900">

![ESP32](https://img.shields.io/badge/ESP32-WROOM--32-red)
![KiCad](https://img.shields.io/badge/PCB-KiCad-blue)
![3D Printing](https://img.shields.io/badge/Fabrication-FDM%203D%20Printing-success)
![License](https://img.shields.io/badge/License-MIT-green)

Built by **HABBOUBY EDEM** for [Beest](https://beest.hackclub.com/)

</div>

---

# About

MONGEYA is a smart cleaning station that automates several repetitive household tasks. It combines multiple cleaning systems inside a single machine and works together with **MONGY**, a compact autonomous robot that leaves the station to clean the floor before returning automatically to recharge.

The entire mechanical structure, electronics, and custom PCB were designed from scratch.

---

# Scope of This Submission

This submission covers the **mechanical design (CAD)** and the **custom PCB (KiCad)** for MONGEYA and Mongy. Firmware/embedded code is not included at this stage — this project is being submitted as a hardware and electronics design.

---

# ⚠️ Note on Physical Fabrication

This submission is provided as a **complete, print-ready CAD and PCB design** (STEP, STL, and KiCad project).

I do not currently have access to a 3D printer, and professional 3D printing services are costly and limited where I live (Tunisia). For this reason, I was not able to physically fabricate and photograph the assembled parts before submission.

Every file needed to reproduce MONGEYA and Mongy — including slicer-ready STL exports and print settings — is included in this repository, so the design can be fabricated and verified by anyone with access to a 3D printer.

**On 3D printing access in Tunisia:** Access to 3D printing hardware in Tunisia is particularly constrained. Import duties and customs taxes on 3D printers and electronics significantly raise their price compared to international markets, putting personal ownership out of reach for many students. Local makerspaces with printing capability are few, mostly concentrated in the capital, and operate as private, paid facilities with limited slots rather than open-access community labs. Online/local printing services exist but are costly and add delays for a project of this scale (multiple large structural parts). For these reasons, physical fabrication of MONGEYA and Mongy has not yet been possible, and the design is submitted as a complete, print-ready package so it can be reproduced and verified by anyone with printer access.

---

# Why I Built This

The inspiration behind MONGEYA comes from my mother.

Every day she spends a significant amount of time cleaning shoes, sorting waste, and handling repetitive household chores. I wanted to design a machine capable of taking over these repetitive tasks, giving her more free time while making home cleaning easier and smarter.

---

# Meet MONGY

MONGY is the autonomous cleaning robot inside MONGEYA.

MONGY leaves its docking station, cleans the surrounding area using multiple cleaning mechanisms, and automatically returns to recharge.

---

# Features

- Automatic waste sorting (aluminum / plastic / paper)
- Automatic chemical dispensing (bleach + cleaning gel)
- Shoe cleaning station
- Autonomous floor cleaning
- Automatic docking and locking mechanism
- Automatic battery charging
- LiDAR navigation
- PID motor control with encoders
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
**MONGY** — Compact 3S LiPo battery
**MONGEYA** — Three independent 3S LiPo batteries powering different subsystems

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

The `02_PCB/mongy/` folder contains:
- Fabrication files (Gerbers, drill files) — `FABRICATION/`
- KiCad libraries — `libs/`
- Component list ([BOM](02_PCB/mongy/Component%20list%20PCB%20DESIGN.xlsx))

The MONGEYA station intentionally uses modular perfboards for auxiliary circuits such as chemical dispensing and opto-isolated interfaces, making maintenance and future upgrades easier.

---

# Repository Structure

```text
mongeya-main/
│
├── 01_3D/
│   ├──01_cleaning robot mongy.rar
│   └── 02_main station mongeya.rar
|   └── 03_STL.rar/
│      
|
├── 02_PCB/
│   └── mongy/
│       ├── FABRICATION/     # Gerbers + drill files
│       └── Component list PCB DESIGN.xlsx
│
├── 03_docs/
│   ├── wiring/
│   └── PRESENTATION.pdf
|   └── IMAGES
|
│
├── 04_media/
│   └── hero.png
|
│
└── README.md
```

**Note on file compression:** The CAD assemblies (STEP/STL) and the KiCad project for Mongy include large mesh and library data, so they are provided as `.rar` archives to keep the repository within GitHub's size limits and reduce clone/download time. Each archive is self-contained and can be extracted with any standard tool (WinRAR, 7-Zip, The Unarchiver). Once extracted, the STL files are directly slicer-ready and the STEP/native files remain fully editable in any CAD application.

---

# Assembly

1. Print all STL files (`01_3D/STL/`) using the settings above.
2. Assemble the mechanical structure using the specified M3 screws — see renders in `03_docs/renders/`.
3. Install the motors, pumps, and sensors.
4. Mount the custom PCB inside Mongy.
5. Connect batteries and wiring — see `03_docs/wiring/`.
6. Dock Mongy inside MONGEYA.

---

# CAD Files

This repository includes:
- STEP files (.step) — `01_3D/STEP/`, fully editable in any CAD tool
- STL files (.stl) — `01_3D/STL/`, ready to slice and print

allowing anyone to modify, remix, or reproduce the project.

---

# Documentation

Additional documentation is available inside `03_docs/`, including:
- Project presentation (`PRESENTATION.pdf`)
- Design renders (`renders/`)
- Wiring diagrams (`wiring/`)

---

# Future Improvements

- AI-based object recognition
- Automatic water refill
- Mobile application
- Voice assistant integration
- Multi-room navigation
- Firmware development (navigation, sorting logic, PID tuning)

---

# License

This project is released under the **MIT License**.
