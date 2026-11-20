---
title: "Architecture Overview"
description: "High-level architecture: electrical, firmware, and mechanical design notes."
---

Overview of the electrical, firmware, and mechanical design of this Slice.

## 🧠 Purpose

<!-- Briefly describe the function of the Slice -->

This Slice is a stepper motor controller card for BREADS-compatible systems.

## 🔌 Interfaces

| Signal | Connector | Direction | Voltage | Notes |
| ------ | --------- | --------- | ------- | ----- |
| ...    | ...       | ...       | ...     | ...   |

## 🪛 MCU Pin Mapping

| MCU Pin | Function | Net | Notes |
| ------- | -------- | --- | ----- |
| ...     | ...      | ... | ...   |

### DUMP

- Supported MCU Dev Boards:
  - Raspberry Pi Pico (RP2040)
  - Raspberry Pi Pico W (RP2040)
  - Raspberry Pi Pico 2 (RP2350)
  - Raspberry Pi Pico 2 W (RP2350)
## 🔋 Power Domains

- Logic power: the bus 12 V feeds the AP63205 buck (5 V); the slice 5 V enters the
  Pico's VSYS through D1, and the Pico's 3.3 V feeds the four cards' logic. The
  Pico's VBUS is left unconnected.
- Motor power (VM): 12-24 V nominal on J1, up to 6 A for all four cards. Q1 blocks
  reverse polarity; U2, a TPS26630 eFuse, switches VM, limits it to 6 A (latch-off
  on a fault), soft-starts it, and cuts it while the bus e-stop is low or
  unwired. U2 reports a fault on GPIO5 and its current on GPIO28/ADC2
  (0.50 V/A).
- The WS2812B runs from 5 V with 3.3 V data from GPIO1; its datasheet asks for
  3.5 V on DIN, so the LED works with less margin than specified. This is a
  known, accepted limit.

## 🧩 Mechanical

- Mounting pattern: ...
- Dimensions: ...
- Notes: ...

---

<!-- Optional: Add block diagrams or images under docs/assets/ -->
