# Macropad V1 — Hardware

Custom 9-key USB macropad designed using KiCad, based on an STM32G4 microcontroller.

> **Project Status: Early Development / Prototype**
>
> Macropad V1 is currently in its first hardware revision. The design is subject to changes as development and testing progress.

## Overview

Macropad V1 is a custom-designed USB macropad intended to provide programmable buttons and LED indicators through a dedicated host application.

The project focuses on developing a compact, extensible hardware platform with custom firmware and software.

The device communicates with the host using USB 2.0 Full Speed, with a vendor-defined HID interface.

## Hardware Specifications

| Component               | Description                  |
| ----------------------- | ---------------------------- |
| Microcontroller         | STM32G4 Series               |
| USB Interface           | USB 2.0 Full Speed           |
| Connector               | USB Type-C                   |
| Buttons                 | 9 mechanical switches        |
| LEDs                    | 9 reverse-mounted green LEDs |
| Power Supply            | USB 5V / 3.3V LDO regulator  |
| Programming & Debugging | SWD (Tag-Connect)            |
| PCB                     | 2-layer custom PCB           |
| Design Software         | KiCad 9                      |

### Main Features

- Custom-designed PCB and schematic
- 9 individually readable mechanical switches
- 9 independently controllable LEDs
- USB-C connectivity
- On-board 3.3V voltage regulation
- USB ESD protection
- SWD interface for programming and debugging
- Designed for automated PCB assembly where applicable

## PCB Design

The PCB was designed in **KiCad 9**.

The design uses two copper layers and includes dedicated power distribution, ground planes and decoupling capacitors for the STM32 microcontroller.

Some components, including the mechanical switches, are intended for manual assembly.

Manufacturing and assembly are planned around JLCPCB services.

## Repository Contents

This repository contains the hardware design files required to inspect, modify and manufacture the PCB.

These include:

- KiCad project files
- Circuit schematic
- PCB layout
- Component footprints and related design files

### Opening the Project

1. Install KiCad 9 or a compatible version.
2. Clone this repository.
3. Open the `.kicad_pro` project file.
4. Open the schematic or PCB editor as required.

## Firmware & Software

Macropad V1 uses custom firmware developed for the STM32G4 platform.

The firmware is responsible for:

- Reading button states
- Controlling individual LEDs
- Managing USB HID communication
- Exchanging data with the host computer

[Firmware Repository Link](https://github.com/Cogman-1/Macropad_V1_src)

A separate host application is planned to provide configurable button actions, macros and LED behavior.

The host software will consist of a background daemon and a configuration GUI.
