# STM32 MPU6050 BLE Sensor Board 🚀

> **Status:** 🚧 Work In Progress (WIP) - Schematic Phase Complete

This repository contains the KiCad hardware design files for a custom, professional-grade motion tracking and wireless communication board. The system is designed to read 6-DoF motion data and transmit it over Bluetooth Low Energy (BLE) to a mobile application (Android/iOS).

## 🛠️ Hardware Specifications

The board is designed around a hierarchical schematic structure in KiCad and features the following core components:

*   **Microcontroller:** STM32F407VGT6 (ARM Cortex-M4) running at 8MHz external crystal oscillator.
*   **Motion Sensor:** MPU-6050 (3-axis Gyroscope & 3-axis Accelerometer) communicating via I2C.
*   **Wireless Communication:** HM-10 BLE (Bluetooth Low Energy) Module communicating via UART.
*   **Power Supply:** USB Type-C input (with 5.1kΩ CC pull-down resistors for smart charger compatibility) regulated to a clean 3.3V using an AP2112K-3.3 LDO.
*   **Debugging/Programming:** Standard 4-pin SWD header for ST-Link.

## 📂 Project Structure

This project utilizes KiCad's hierarchical sheet feature for a clean, modular design:
*   `power_supply.kicad_sch` - USB-C input, LDO, and decoupling.
*   `STM32_MCU.kicad_sch` - Core MCU, crystal, SWD, and boot configurations.
*   `sensor_mpu6050.kicad_sch` - Motion sensor and I2C pull-ups.
*   `comm_bluetooth.kicad_sch` - HM-10 BLE module integration.
*   `CompLib/` - Custom footprint and symbol library containing project-specific components.

## 📝 To-Do List / Next Steps

- [x] Component selection and BOM creation
- [x] Hierarchical schematic design
- [x] Footprint assignments and custom library generation
- [ ] PCB Layout and Component Placement (Current Phase)
- [ ] Signal routing and Ground plane pours
- [ ] 3D Model integration and final review
- [ ] Gerber generation for fabrication

---
*Designed with KiCad*
