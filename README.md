# Interview PCB Project (KiCad)

A fabrication ready PCB designed as an interview portfolio project.  
Includes full schematic and PCB layout, verified with ERC (Electrical Rules Check) and DRC (Design Rules Check), and validated Gerbers and drills in Gerber Viewer.

![PCB 3D View](screenshots/CP5_04_3D_Front.png)

---

## Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Project Status](#project-status)
- [Repo Structure](#repo-structure)
- [Verification](#verification)
- [Manufacturing Outputs](#manufacturing-outputs)
- [How to Open](#how-to-open)
- [Images](#images)
- [Next Improvements](#next-improvements)

---

## Overview
This project demonstrates an end to end PCB workflow:
schematic capture → layout and routing → design rule checks → manufacturing outputs.

The goal is to show practical board design skills (power, interfaces, layout, manufacturability) in a way that is easy to review quickly in an interview.

---

## Key Features
- USB power input with on board 3.3 V regulation
- Microcontroller based system design
- I2C (Inter Integrated Circuit) sensor bus (IMU)
- Labeled connectors and test points for bring up
- Ground plane implemented
- Manufacturing package generated (Gerbers + PTH and NPTH drills)
- BOM and pick and place exported for assembly readiness

---

## Project Status
- [x] Placement and routing complete
- [x] Ground plane set
- [x] ERC clean
- [x] DRC clean
- [x] 3D view checked for footprint consistency
- [x] Gerbers generated
- [x] Drill files generated (PTH + NPTH)
- [x] Gerbers and drills verified in Gerber Viewer
- [X] BOM committed
- [X] Pick and place committed

---

## Repo Structure
```text
.
├── hardware/                  # KiCad schematic + PCB
├── manufacturing/
│   ├── gerbers/               # plotted Gerbers
│   ├── drill/                 # Excellon drills (PTH + NPTH)
│   ├── bom/                   # BOM exports
│   ├── assembly/              # pick and place / position outputs
│   └── release/               # upload ready ZIP(s)
└── screenshots/               # verification screenshots for quick review
