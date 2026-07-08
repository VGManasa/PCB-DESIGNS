# Gerber Files

This directory contains the manufacturing files for the **UAV Payload Controller** PCB.

## Overview

The Gerber package was generated using KiCad and is intended for PCB fabrication.

**PCB Specifications**

- PCB Type: 4-Layer
- CAD Software: KiCad
- Manufacturing Format: RS-274X Gerber
- Drill Format: Excellon

## Included Files

### Copper Layers

- `UAV PAYLOAD CONTROLLER-F_Cu.gtl` – Top Copper
- `UAV PAYLOAD CONTROLLER-In1_Cu.g1` – Inner Copper Layer 1
- `UAV PAYLOAD CONTROLLER-In2_Cu.g2` – Inner Copper Layer 2
- `UAV PAYLOAD CONTROLLER-B_Cu.gbl` – Bottom Copper

### Solder Mask

- `UAV PAYLOAD CONTROLLER-F_Mask.gts`
- `UAV PAYLOAD CONTROLLER-B_Mask.gbs`

### Silkscreen

- `UAV PAYLOAD CONTROLLER-F_Silkscreen.gto`
- `UAV PAYLOAD CONTROLLER-B_Silkscreen.gbo`

### Mechanical Layer

- `UAV PAYLOAD CONTROLLER-Edge_Cuts.gm1`

### Drill Files

- `UAV PAYLOAD CONTROLLER-PTH.drl`
- `UAV PAYLOAD CONTROLLER-NPTH.drl`
- `UAV PAYLOAD CONTROLLER-front-in1.drl`
- `UAV PAYLOAD CONTROLLER-front-in2.drl`

### Gerber Job

- `UAV PAYLOAD CONTROLLER-job.gbrjob`

## Notes

- These files are intended for PCB fabrication and manufacturing.
- Verify the Gerber outputs using a Gerber viewer before submitting them to a PCB manufacturer.
- This design corresponds to the latest revision of the UAV Payload Controller hardware.

---
**Project:** UAV Payload Controller  
**EDA Software:** KiCad
