# ESP Smart Outlet

A device developed with an ESP32 microcontroller and relay modules. This device forms the backbone of a centralized remote control system for electrical equipment.

## Features

- Centralized Control
- Remote Control

## Prerequisites

This device was built with [ESPHome](https://esphome.io/) and is intended to work with [Home Assistant.](https://www.home-assistant.io/)

### Modules

- [ESP32 DevKit V1 MCU](https://shopee.ph/ESP-32S-ESP-WROOM-32-ESP32-ESP-32-Bluetooth-and-WIFI-Dual-Core-CPU-with-Low-Power-Consumption-MCU-ESP-32-i.580325202.14223060123?sp_atk=0641a5ae-d303-4cc2-b6fd-913253973a58&xptdk=0641a5ae-d303-4cc2-b6fd-913253973a58)
- [8 Channel Relay Module 5V](https://shopee.ph/1-2-4-8-Channel-5V-12V-10A-Relay-Module-with-Optocoupler-i.18252381.670803085?sp_atk=d5f32ab5-d7fe-4137-818b-2daab4359edb&xptdk=d5f32ab5-d7fe-4137-818b-2daab4359edb)
- [HiLink HLK-5M05 AC/DC Buck Converter 100-240 VAC to 5 DC 1A(5W)](https://shopee.ph/HLK-5M05-HLK-5M03-HLK-5M12-5W-AC-DC-220V-to-12V-5V-3.3V-Buck-Step-Down-Power-Supply-Module-Converter-Intelligent-i.580325202.20209582747)

## Getting Started

### Pictorial Diagram

![pictorial-diagram](https://raw.githubusercontent.com/jepnoda/ESP-Smart-Outlet/main/pictorial-diagram.png)

### Pin Connections

❗❗❗ **The `esp32c3-switches.yaml` config file contains pin mapping for the [ESP32-C3](https://docs.m5stack.com/en/core/stamp_c3), which you can modify depending on your ESP32 development board variant.**

| 8 CH Relay Module | HiLink AC-DC Pin | ESP32 Devkit V1 Pin |
| :---: | :---: | :---: |
| IN1 | ❌ | D13 |
| IN2 | ❌ | D12 |
| IN3 | ❌ | D14 |
| IN4 | ❌ | D27 |
| IN5 | ❌ | D26 |
| IN6 | ❌ | D25 |
| IN7 | ❌ | D33 |
| IN8 | ❌ | D32 |
| VCC | VOUT➕ | VIN |
| GND | VOUT➖ | GND |

---

1. Ensure [ESPhome](https://esphome.io/guides/getting_started_hassio) and [File Editor](https://github.com/home-assistant/addons/blob/master/configurator/DOCS.md) add-ons are installed on your [Home Assistant](https://www.home-assistant.io/getting-started/) instance.
2. Ensure that your ESPHome `secrets.yaml` file is up to date.
3. Using the File Editor add-ons, upload the `esp32c3-switches.yaml` config file to the `config/esphome/` directory.
4. Using the ESPHome dashboard, modify the `esp32c3-switches.yaml` and replace the **redacted** part of the config file.
5. **Build** and **upload** the firmware to your device.
6. Now, you can [integrate](https://www.home-assistant.io/getting-started/concepts-terminology/) the device into your Home Assistant.

---
