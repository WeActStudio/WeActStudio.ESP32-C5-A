# WeAct ESP32\-C5\-A Development Board

[中文版本](./README-ZH.md)

**Module Model**: ESP32C5-WROOM1-N16R8 / ~~ESP32C5-WROOM1-N8R8~~ / ~~ESP32C5-WROOM1-N8R4~~

**Chip Version**: v1.0

**Supported Protocols**: Wi-Fi 6 (2.4G/5GHz Dual-Band), BLE 5.0, Zigbee 3.0, Thread 1.4, Matter

---

## 📌 Project Introduction

This repository provides complete open-source hardware and software development resources for the **WeAct ESP32-C5-A Development Board**.

The ESP32-C5 is Espressif’s new-generation **RISC-V architecture** IoT main controller. It natively supports **2.4G + 5GHz dual-band Wi-Fi 6**, delivering high-speed wireless transmission, low-power operation, and multi-protocol networking capabilities. It is widely applied in smart home devices, Matter gateways, IoT data acquisition terminals, battery-powered low-power devices, wireless control products, and PCB scheme verification.

---

## ⚙️ Core Hardware Specifications

- **Main Controller**: ESP32-C5 (Chip Revision v1.0)

- **Processor Architecture**: Single-core RISC-V @ 240MHz, equipped with a 40MHz low-power LP core

- **Wireless Capability**: Dual-band Wi-Fi 6, BLE 5.0, 802.15.4 protocol stack (Zigbee / Thread / Matter)

- **Storage Configuration (Full Version Compatibility)**
  
  - ~~N8R4: 8MB Flash + 4MB PSRAM~~
  
  - ~~N8R8: 8MB Flash + 8MB PSRAM~~
  
  - N16R8: 16MB Flash + 8MB PSRAM

- **Onboard Peripherals**: CH343P high-speed serial chip, Type-C power supply and download interface, automatic download circuit (no BOOT key required), full GPIO pinout

- **Power Supply**: 5V Type-C input, core operating voltage 3.3V

---

## 🛠️ Development Environment Support

Fully compatible with mainstream ESP32 development platforms. It is recommended to use the latest versions to obtain complete ESP32-C5 kernel support:

- **ESP-IDF**: v5.4 and above (Recommended **v5.5**, fully compatible with ESP32-C5 v1.0)

- **Arduino ESP32**: Latest stable core library

- **PlatformIO**: Native support, directly importable for compilation and flashing

---

## 🚀 Quick Start

### 1. Environment Preparation

Build the corresponding development environment, install the ESP32-C5 chip support package, and install the CH343P serial port driver.

### 2. Compilation & Flashing

Select `ESP32C5` as the project target. Compile and download firmware via the onboard Type-C interface without manually entering BOOT mode.

### 3. Serial Port Debugging

Baud rate: **115200** for log output, variable debugging and device status monitoring.

---

## 💡 Core Functional Adaptation

- **Dual-band Wi-Fi 6**: Supports 2.4G/5G band switching, high-speed data transmission and anti-interference networking

- **Low-Power Development**: Supports independent LP core operation and deep sleep mode, suitable for battery-powered low-power products

- **Multi-protocol Intelligent Networking**: Compatible with Zigbee / Thread / Matter for building smart home multi-device gateways

- **Rich Peripheral Expansion**: Full pin exposure, compatible with sensors, displays, actuators and other peripheral devices

---

## ⚠️ Hardware Development & Mass Production Notes

- This board adopts the **ESP32-C5 v1.0 initial silicon revision**. Refer to Espressif’s official errata manual for mass-production PCB design to avoid known hardware issues.

- 5GHz Wi-Fi requires strict PCB impedance control, trace routing and complete ground plane design. RF circuits must comply with official Espressif RF design specifications.

- This hardware has three Flash/PSRAM configuration versions. **The BOM and firmware partition table must strictly match the actual module model for mass production**.

- Enable protocol time-sharing mechanism for multi-protocol concurrent scenarios to avoid signal conflicts among Wi-Fi, BLE and 802.15.4 protocols.

---

## ❓ FAQ

- **Flashing Failure**: Confirm CH343P driver is installed correctly, use a data-transfer Type-C cable, and select the correct device port.

- **Abnormal Program Operation**: ESP32-C5 does not support old IDF versions. Please use ESP-IDF v5.4 or newer.
