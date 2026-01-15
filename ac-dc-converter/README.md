# AC–DC Converter PCB

This project is a simple AC to DC converter PCB designed using KiCad.  
It converts an AC input into an unregulated DC output using a bridge rectifier and capacitor filtering.

---

## Overview

The AC–DC converter consists of:
- AC input through a 2-pin screw terminal
- Full-wave bridge rectifier using diodes
- Capacitor filter for ripple reduction
- DC output through a 2-pin screw terminal
- LED indicator for DC output presence

This design is intended for **learning and academic purposes**.

---

## Features

- Full-wave bridge rectification
- Capacitor-based DC smoothing
- Screw terminal input and output
- Simple and compact PCB layout
- Designed using **KiCad 9.0**

---

## Input / Output

- **Input:** Low-voltage AC (from transformer)
- **Output:** Unregulated DC voltage

> ⚠️ This board is not regulated. Output voltage depends on input AC and load.

---

## Main Components

- Diodes: 1N4007 (×4)
- Filter Capacitor: Electrolytic capacitor
- LED + current limiting resistor
- 2-pin screw terminal blocks (AC input and DC output)

---

## Files Included

- Schematic (`.kicad_sch`)
- PCB layout (`.kicad_pcb`)
- Gerber files (for fabrication)
- Project documentation

---

## Tools Used

- KiCad 9.0

---

## Safety Notice

⚠️ **This project involves AC input.**
- Use only **low-voltage AC from a transformer**
- Do **not connect directly to mains**
- Maintain proper electrical isolation and clearance
- For educational use only

---


## Author

Designed by **V G Manasa**

