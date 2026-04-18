# Firmware

This directory reserves a normalized home for firmware-related materials.

## Current Situation

The repository's current released firmware files are still kept in the legacy compatibility paths:

- CPLD firmware: [`../pof/CPLD_ChisFlash_MBCX_RTC.pof`](../pof/CPLD_ChisFlash_MBCX_RTC.pof), [`../pof/CPLD_ChisFlash_MBCX_Motor.pof`](../pof/CPLD_ChisFlash_MBCX_Motor.pof)
- MCU firmware: [`../mcu/MCU_ChisFlashRTC.hex`](../mcu/MCU_ChisFlashRTC.hex)

## Directory Intent

- [`releases/`](releases/README.md): future firmware release notes and version mapping
- [`source/`](source/README.md): future MCU source, CPLD / HDL source, and build instructions

For the full repository-level plan, see [../docs/source-layout.md](../docs/source-layout.md).
