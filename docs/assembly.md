# Assembly And Programming

This page summarizes the current build flow based on the files already present in the repository and the original project notes.

## Files Used During Build

- PCB project: [`../pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro`](../pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro)
- Gerber package: [`../gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip`](../gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip)
- RTC CPLD firmware: [`../pof/CPLD_ChisFlash_MBCX_RTC.pof`](../pof/CPLD_ChisFlash_MBCX_RTC.pof)
- Rumble CPLD firmware: [`../pof/CPLD_ChisFlash_MBCX_Motor.pof`](../pof/CPLD_ChisFlash_MBCX_Motor.pof)
- RTC MCU firmware: [`../mcu/MCU_ChisFlashRTC.hex`](../mcu/MCU_ChisFlashRTC.hex)

## Recommended Build Flow

1. Review the board files and open hardware page to confirm parts and assembly orientation.
2. Manufacture the PCB from the Gerber archive or inspect the source PCB project before ordering.
3. Solder the board according to the BOM / assembly guidance from the open hardware page.
4. Choose one operating mode: `MBC3 RTC` or `MBC5 rumble`.
5. Flash the corresponding CPLD firmware.
6. If building the RTC version, populate the MCU and RTC chip and flash the MCU firmware through `SWD` or `TTL`.
7. Verify power and battery behavior before final assembly.

## Important Notes From The Existing README

- A through-hole crystal is recommended because it is expected to drift less and provide better timekeeping stability.
- The resistor near the lower-left side of the battery area must be soldered, otherwise the battery will not supply power correctly.
- The rumble version can omit the MCU and RTC hardware to avoid unnecessary power usage.

## FRAM / SRAM Note

According to the current project notes:

- When using `SRAM`, install the `0-ohm` resistor
- When using FRAM, do not install the `0-ohm` resistor
- For FRAM use, short the diode and resistor pads as described in the original release notes

## PCB Ordering Note

The Gerber archive includes a short text note titled `PCB下单必读.txt`, which points to the JLCPCB ordering guide:

- <https://prodocs.lceda.cn/cn/pcb/order-order-pcb/index.html>

## What Is Still Missing In-Repo

- Local BOM spreadsheet
- Local schematic export
- Assembly photos or annotated placement guide
- Programmer setup screenshots or exact flashing parameters
