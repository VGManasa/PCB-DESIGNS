# Custom PCB Footprint Library

This directory contains the custom KiCad footprint library used in the **UAV Payload Controller** PCB design.

## Overview

The footprints included in this library are either custom-created or modified to match the mechanical specifications of the components used in this project. These footprints ensure accurate PCB layout, component placement, and manufacturing compatibility.

## Footprints Included

| Footprint | Description |
|-----------|-------------|
| `DIOM4336X265N.kicad_mod` | Diode package footprint |
| `MODULE_RA-02_LORA.kicad_mod` | Ai-Thinker RA-02 LoRa module footprint |
| `PQFN50P300X250X97-14N.kicad_mod` | 14-pin PQFN package footprint |
| `SOIC127P600X170-9N.kicad_mod` | 8-pin SOIC package footprint |

## Usage

To use this footprint library in KiCad:

1. Open **KiCad**.
2. Navigate to **Preferences → Manage Footprint Libraries**.
3. Add the `uav_payload_footlib.pretty` directory as a project or global footprint library.
4. Ensure the library path is correctly linked before opening the PCB layout.

## Notes

- These footprints are intended for use with the **UAV Payload Controller** project.
- Always verify component dimensions with the manufacturer's datasheet before fabrication.
- Any future footprint revisions or additions will be maintained in this directory.

---

**Project:** UAV Payload Controller  
**EDA Software:** KiCad
