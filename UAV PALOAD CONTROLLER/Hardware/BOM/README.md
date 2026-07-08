# Bill of Materials (BOM)

This directory contains the **Engineering Bill of Materials (EBOM)** for the **UAV Payload Controller** PCB.

The BOM provides a complete list of electronic components required to assemble the hardware, including passive components, active devices, connectors, protection circuitry, sensors, communication modules, and mechanical interfaces.

---

## Overview

The BOM was generated directly from the KiCad project and represents the design used in the PCB layout. It serves as the primary reference for component selection, PCB assembly, verification, and future hardware revisions.

The current BOM is intended as an **Engineering BOM (EBOM)** rather than a procurement-ready Manufacturing BOM (MBOM).

---

## Contents

| File | Description |
|------|-------------|
| `UAV PAYLOAD CONTROLLER.csv` | Engineering Bill of Materials exported from KiCad |

---

## Information Included

The BOM contains the following information for every component used in the design:

- Reference Designators
- Component Quantity
- Component Value
- DNP (Do Not Populate) Status
- PCB Footprint
- Available Datasheet Links
- Board Exclusion Flags
- BOM Exclusion Flags

---

## Hardware Summary

The design integrates the following functional hardware blocks:

### Processing Unit
- STM32F411RE ARM Cortex-M4 Microcontroller

### Communication Interfaces
- Ai-Thinker RA-02 LoRa Module
- u-blox NEO-M8N GPS Receiver
- CP2102N USB-to-UART Interface

### Sensor Interfaces
- ICM-42688-P 6-Axis IMU
- HX711 Load Cell Amplifier
- Flow Sensor Interface
- Tank Level Sensor Interface

### Storage
- MicroSD Card Socket

### Power Management
- MP1584EN Buck Converter
- AMS1117-3.3 Linear Voltage Regulator
- Input Protection Circuitry
- TVS Protection Diodes
- Ferrite Bead EMI Filter

### Protection Components
- TVS Diodes
- Schottky Diodes
- ESD Protection Devices
- Resettable Fuse

### Supporting Components
- Capacitors
- Resistors
- Inductors
- Crystal Oscillator
- MOSFETs
- LEDs
- Connectors
- Test Points

---

## Component Selection Policy

The BOM specifies the **electrical characteristics** and **PCB footprints** required by the design.

Generic passive components such as:

- Resistors
- Ceramic Capacitors
- Inductors
- Ferrite Beads
- LEDs

are intentionally left without manufacturer-specific part numbers. Equivalent components from any reputable manufacturer may be selected, provided they satisfy the required:

- Electrical Value
- Package Size
- Voltage Rating
- Current Rating
- Tolerance
- Temperature Rating

This allows flexibility in sourcing based on supplier availability and manufacturing preferences.

---

## Active Components

Critical devices such as:

- STM32F411RE Microcontroller
- RA-02 LoRa Module
- NEO-M8N GPS Module
- ICM-42688-P IMU
- HX711 ADC
- CP2102N USB Interface
- MP1584EN Buck Converter
- AMS1117-3.3 Regulator

should preferably match the specified devices or verified compatible equivalents to ensure proper functionality.

---

## DNP Components

Certain components are marked as **DNP (Do Not Populate)**.

These footprints remain on the PCB but are intentionally left unassembled. They may be used for:

- Future hardware revisions
- Design flexibility
- Optional features
- Testing and debugging

---

## Notes

- This BOM is provided for reference and hardware development purposes.
- Manufacturer Part Numbers (MPNs), supplier information, and pricing are intentionally omitted to allow users to source components based on availability and regional preferences.
- Designers and manufacturers should verify component compatibility before production.
- Datasheet references included in the BOM should be consulted prior to component selection.

---

## Recommended Manufacturing Workflow

1. Review the Engineering BOM.
2. Select equivalent or preferred manufacturer components.
3. Verify package compatibility with the PCB footprints.
4. Confirm electrical ratings and operating specifications.
5. Generate a Manufacturing BOM (MBOM) for procurement and assembly.

---

## Software

- **EDA Tool:** KiCad
- **PCB Type:** 4-Layer
- **BOM Type:** Engineering Bill of Materials (EBOM)

---

**Project:** UAV Payload Controller  
**Repository:** PCB-DESIGNS/UAV PAYLOAD CONTROLLER  

