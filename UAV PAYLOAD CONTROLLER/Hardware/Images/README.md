# Hardware Images

This directory contains visual documentation of the **UAV Payload Controller** hardware design. These images provide a comprehensive overview of the PCB layout, 3D mechanical representation, internal layer organization, silkscreen artwork, and overall system schematic.

The purpose of this directory is to enable reviewers, developers, and manufacturers to quickly understand the board architecture without requiring KiCad or other EDA software.

---

# Directory Structure

```
Images/
├── 3.3V_POWER_PLANE_PLANE_INNER_LAYER_2.png
├── BACK_SILKSCREEN_LAYER_DIM_VIEW.png
├── BACK_SILKSCREEN_LAYER_NORMAL_VIEW.png
├── BOTTOM_LAYER_DIM_VIEW.png
├── BOTTOM_LAYER_NORMAL_VIEW.png
├── BOTTOM_LAYER_PCB_3D_VIEW.png
├── FRONT_SILKSCREEN_LAYER_DIM_VIEW.png
├── FRONT_SILKSCREEN_LAYER_NORMAL_VIEW.png
├── GND_PLANE_INNER_LAYER_1.png
├── OVERALL_SCHEMATIC_ROOT_PAGE_VIEW.png
├── PCB_SIDE_3D_VIEW.png
├── TOP_LAYER_DIM_VIEW.png
├── TOP_LAYER_NORMAL_VIEW.png
├── TOP_LAYER_PCB_3D_VIEW.png
└── README.md
```

---

# Image Descriptions

## PCB Layout Images

### TOP_LAYER_NORMAL_VIEW.png
Displays the complete **Top Copper (F.Cu)** layout of the PCB.

This view includes:

- Component placement
- Copper routing
- Mounting holes
- PCB outline
- Via locations
- Board annotations

This is the primary layout view used for hardware review.

---

### BOTTOM_LAYER_NORMAL_VIEW.png

Displays the **Bottom Copper (B.Cu)** layout of the PCB.

It provides visibility into:

- Bottom-side routing
- Ground connections
- Signal traces
- Copper pours
- Vias and return paths

---

### TOP_LAYER_DIM_VIEW.png

Shows the top layer using a dimmed visualization, making copper features and routing paths easier to distinguish during PCB inspection.

---

### BOTTOM_LAYER_DIM_VIEW.png

Dimmed representation of the bottom copper layer for improved routing visibility and documentation.

---

# 3D PCB Visualization

The following images provide realistic three-dimensional representations of the assembled PCB.

---

### TOP_LAYER_PCB_3D_VIEW.png

Front 3D rendering of the assembled PCB.

Visible hardware includes:

- STM32F411 Microcontroller
- LoRa Communication Module
- GPS Module
- USB Type-C Interface
- IMU Sensor
- Power Supply Circuitry
- Connectors
- Passive Components

---

### BOTTOM_LAYER_PCB_3D_VIEW.png

Rear 3D rendering of the PCB illustrating:

- Bottom mounted components (if any)
- Copper layer visibility
- Mechanical clearances
- Mounting locations

---

### PCB_SIDE_3D_VIEW.png

Side profile of the PCB.

Useful for observing:

- Board thickness
- Component heights
- Mechanical spacing
- Connector placement
- Overall assembly profile

This view assists in enclosure and mechanical integration.

---

# Internal Layer Documentation

Since the UAV Payload Controller is designed as a **4-layer PCB**, the internal layers are included for documentation purposes.

---

### GND_PLANE_INNER_LAYER_1.png

Illustrates the dedicated **Ground Plane (Inner Layer 1)**.

The ground plane provides:

- Low impedance return paths
- Reduced electromagnetic interference (EMI)
- Improved signal integrity
- Enhanced power distribution stability
- Better thermal performance

---

### 3.3V_POWER_PLANE_PLANE_INNER_LAYER_2.png

Illustrates the dedicated **3.3V Power Plane (Inner Layer 2)**.

The power plane:

- Distributes regulated 3.3V power
- Reduces voltage drops
- Improves power integrity
- Minimizes power distribution noise
- Supports high-speed digital circuitry

---

# Silkscreen Documentation

The silkscreen layers contain all PCB markings used for assembly and maintenance.

---

### FRONT_SILKSCREEN_LAYER_NORMAL_VIEW.png

Displays the complete front silkscreen containing:

- Component reference designators
- Board labels
- Connector identifiers
- Pin numbering
- Assembly markings

---

### BACK_SILKSCREEN_LAYER_NORMAL_VIEW.png

Displays the rear silkscreen layer including all markings present on the bottom side of the PCB.

---

### FRONT_SILKSCREEN_LAYER_DIM_VIEW.png

Dimmed visualization of the front silkscreen layer for improved readability during documentation.

---

### BACK_SILKSCREEN_LAYER_DIM_VIEW.png

Dimmed visualization of the rear silkscreen layer.

---

# System Schematic

### OVERALL_SCHEMATIC_ROOT_PAGE_VIEW.png

Provides the top-level hierarchical schematic of the complete UAV Payload Controller.

The schematic presents the overall architecture by illustrating the interconnection of major functional blocks including:

- STM32 Microcontroller
- Power Supply
- GPS Interface
- LoRa Communication
- IMU Sensor
- Flow Sensor Interface
- Tank Sensor Interface
- Pump Control Unit
- USB Interface
- SD Card Interface
- UART Interface

This image serves as the system-level overview of the hardware design.

---

# PCB Specifications

| Parameter | Specification |
|-----------|---------------|
| PCB Type | Multilayer PCB |
| Number of Layers | 4 |
| Top Layer | Signal Routing (F.Cu) |
| Inner Layer 1 | Ground Plane |
| Inner Layer 2 | 3.3V Power Plane |
| Bottom Layer | Signal Routing (B.Cu) |
| Design Tool | KiCad |
| PCB Category | Embedded Systems / UAV Payload Controller |

---

# Purpose of this Directory

The images included in this directory are intended to:

- Provide visual documentation of the PCB design.
- Support hardware design reviews.
- Assist manufacturing and assembly processes.
- Illustrate PCB architecture and layer organization.
- Facilitate understanding of the system without opening the KiCad project.
- Serve as reference material for future hardware revisions.

---

# Notes

- These images are generated directly from the KiCad project and accurately represent the current hardware revision.
- The PCB has been designed as a **4-layer board**, featuring dedicated ground and power planes to improve signal integrity, power distribution, and electromagnetic compatibility.
- The images are intended for documentation and visualization purposes. For manufacturing, fabrication, or modification, refer to the KiCad source files and Gerber outputs available in the `Hardware/PCB` directory.

---

**Project:** UAV Payload Controller  
**Repository:** PCB-DESIGNS/UAV PAYLOAD CONTROLLER  

