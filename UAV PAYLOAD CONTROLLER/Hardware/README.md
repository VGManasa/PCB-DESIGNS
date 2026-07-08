# Hardware

This directory contains the complete hardware design for the **UAV Payload Controller**, including the PCB design, manufacturing files, component information, and hardware documentation.

The hardware is designed as a **4-layer embedded controller board** intended for UAV-based payload management and sensor integration. It provides processing, communication, power management, data logging, and peripheral interfaces required for autonomous payload operation.

The design has been developed using **KiCad** and includes all resources necessary for hardware review, PCB fabrication, assembly, and future modifications.

---

## Hardware Overview

The UAV Payload Controller integrates multiple functional subsystems into a compact multilayer PCB, enabling reliable operation in embedded UAV applications.

### Major Functional Blocks

- **Processing Unit**
  - STM32F411RE ARM Cortex-M4 Microcontroller

- **Communication Interfaces**
  - LoRa (RA-02) Wireless Module
  - GPS Receiver
  - USB Type-C Interface
  - UART Interface
  - CAN Interface

- **Sensor Interfaces**
  - 6-Axis IMU
  - Tank Level Sensor Interface
  - Flow Sensor Interface
  - HX711 Load Cell Interface

- **Data Storage**
  - MicroSD Card Interface

- **Power Management**
  - Buck Converter
  - 3.3V Voltage Regulation
  - Input Protection Circuitry
  - EMI Filtering
  - TVS and ESD Protection

- **Debug & Development**
  - USB-to-UART Programming Interface
  - Dedicated Test Points
  - Boot Configuration
  - Status LEDs

---

## PCB Specifications

| Parameter | Specification |
|-----------|---------------|
| PCB Type | Multilayer PCB |
| Number of Layers | 4 |
| Top Layer | Signal Routing |
| Inner Layer 1 | Ground Plane |
| Inner Layer 2 | 3.3V Power Plane |
| Bottom Layer | Signal Routing |
| Design Software | KiCad |

The dedicated ground and power planes improve signal integrity, power distribution, electromagnetic compatibility (EMC), and overall board reliability.

---

## Directory Structure

```
Hardware/
├── BOM/
├── Gerbers/
├── Images/
└── PCB/
```

### BOM

Contains the Engineering Bill of Materials (EBOM) generated from the KiCad project. It lists the components, footprints, quantities, and other information required for PCB assembly.

### Gerbers

Contains the manufacturing outputs required for PCB fabrication, including Gerber files, drill files, and fabrication job files.

### Images

Contains PCB layout images, 3D renders, silkscreen views, internal layer visualizations, and schematic overview images for documentation and design review.

### PCB

Contains the complete KiCad project, including schematics, PCB layout, custom symbol libraries, footprint libraries, and all source files required for editing or extending the hardware design.

---

## Design Objectives

The hardware has been designed to provide:

- Reliable embedded processing for UAV payload applications
- Modular sensor integration
- Long-range wireless communication
- Accurate positioning through GPS
- Efficient power management
- Expandability for future hardware revisions
- Ease of debugging, testing, and maintenance

---

## Development Workflow

The hardware design follows the standard PCB development workflow:

1. System Architecture and Schematic Design
2. Component Selection
3. PCB Layout Design
4. Electrical Rule Check (ERC)
5. Design Rule Check (DRC)
6. Gerber Generation
7. Bill of Materials (BOM) Generation
8. Hardware Documentation

---

## Notes

- The hardware is designed using **KiCad**.
- The PCB is implemented as a **4-layer board** with dedicated power and ground planes.
- All manufacturing files required for PCB fabrication are included.
- Component sourcing may be customized based on manufacturer preference and availability while maintaining electrical compatibility.

---

**Project:** UAV Payload Controller  
**Category:** Embedded Systems / UAV Electronics  
**EDA Software:** KiCad

