# Hardware - PCB Design

This directory contains the complete KiCad source files for the **UAV Payload Controller PCB**.

## Overview

The PCB is designed as the central controller for an agricultural UAV payload system. It integrates sensing, communication, storage, and control peripherals required for autonomous payload management.

## Design Software

- KiCad

## Project Files

| File | Description |
|------|-------------|
| `UAV PAYLOAD CONTROLLER.kicad_pro` | KiCad project file |
| `UAV PAYLOAD CONTROLLER.kicad_pcb` | PCB layout |
| `UAV PAYLOAD CONTROLLER.kicad_sch` | Top-level schematic |
| `FLOW_SENSOR.kicad_sch` | Flow sensor circuit |
| `GPS.kicad_sch` | GPS module |
| `IMU.kicad_sch` | IMU interface |
| `LoRA_MODULE.kicad_sch` | LoRa communication module |
| `POWER_SUPPLY.kicad_sch` | Power supply circuitry |
| `PUMP_UNIT.kicad_sch` | Pump driver section |
| `SD.kicad_sch` | SD card interface |
| `STM32_UNIT.kicad_sch` | STM32 microcontroller section |
| `TANK_SENSOR.kicad_sch` | Tank level sensing |
| `UART_Interface.kicad_sch` | UART interface |
| `USB_INTERFACE.kicad_sch` | USB interface |
| `uav_payload_lib.kicad_sym` | Custom symbol library |
| `uav_payload_footlib.pretty/` | Custom footprint library |

## Hardware Features
- Power Supply, Regulation & Protection
- STM32-based controller
- LoRa wireless communication
- GPS interface
- IMU integration
- SD card storage
- USB interface
- UART debugging
- Flow sensor interface
- Tank level sensing
- Pump control circuitry

## Notes

- This folder contains only the KiCad design source files.
- Manufacturing files (Gerbers, drill files) are provided separately.
- The project is under active development, and future revisions may include design improvements and additional features.

