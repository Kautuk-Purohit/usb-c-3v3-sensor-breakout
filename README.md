# Interview PCB Project (KiCad)

A fabrication ready PCB designed as an interview portfolio project.  
Includes full schematic and PCB layout, verified with ERC (Electrical Rules Check) and DRC (Design Rules Check), and validated Gerbers and drills in Gerber Viewer.

![PCB 3D View](Images/pcb_design/final_pcb_layout_3D_model_front.png)

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
```
---

## Verification
- ERC (Electrical Rules Check): clean
- DRC (Design Rules Check): clean
- 3D Viewer: checked for footprint consistency
- Gerber Viewer: verified copper, mask, silkscreen, outline, and drill alignment (PTH + NPTH)

---

## Manufacturing Outputs
### Fabrication package (upload ready)
- `manufacturing/release/PCB_RELEASE_GERBER_DRILL.zip`

### Assembly data
- BOM: `manufacturing/bom/bom.csv`
- Pick and place: `manufacturing/assembly/<pos_file>.pos` (or `.csv` depending on export)

---

## How to Open
1. Install KiCad (project created in KiCad 9.x recommended).
2. Open the project in `hardware/`.
3. Review:
   - Schematic (`.kicad_sch`)
   - PCB layout (`.kicad_pcb`)
   - 3D Viewer
4. Manufacturing outputs are in `manufacturing/`.

---

## Images
- PCB 3D front: `screenshots/CP5_04_3D_Front.png`
- PCB 3D back: `screenshots/CP5_05_3D_Back.png`
- Gerber overlay: `screenshots/CP5_09_GerberViewer_Overlay.png`
- Drill overlay (PTH + NPTH): `screenshots/CP5_10_GerberViewer_Drills.png`
- (Optional) DRC clean: `screenshots/CP5_03_DRC_Clean.png`

---

## Next Improvements
If I spin a rev B, I would consider:
- Add fiducials and mounting holes (if not present)
- Add additional ESD protection on external connectors (if not present)
- Improve silkscreen placement and reference readability
- Add clearer programming / debug access (if not present)

---

## License
All Rights Reserved.
