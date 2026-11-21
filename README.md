# Slice STPC

## Introduction

Stepper motor controller Slice for BREADS-compatible systems.
This Slice is a carrier board for the [Stepper_card](https://github.com/IanVDS/stepper_card) board. It can carry up to four stepper cards, each with a DRV8825 stepper driver with microstepping and SPI pins for encoder reading.

## Usage

- Motor supply: 12-24 V on J1, up to 6 A total for the four cards.
- The motors only get power while the bus e-stop is high. A fault (over-current,
  over-voltage) latches the supply off until the e-stop or the power is cycled;
  GPIO5 reads low while latched.
- The bus jumpers JP1-JP4 are bridged by default; cut one to isolate that bus line from the Pico.

## Documentation

Please refer to the [docs](/docs) for more info.

---

<div align="center">
  <p>
    <img src="https://img.shields.io/badge/Developed_by-UWO--FAST--et--al-orange" alt="Developed by UWO-FAST et al.">
    <img src="https://img.shields.io/badge/Powered_by-Open_Source-blue" alt="Powered by Open Source">
  </p>
</div>
