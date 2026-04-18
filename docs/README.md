# Documentation

This directory is the documentation hub for `ChisFlash-MBCX`.

The repository currently contains usable release artifacts, but not yet a fully published source-level hardware and firmware tree. These docs help bridge that gap by making the project easier to browse, build, and maintain.

## Read First

- [assembly.md](assembly.md): Assembly and programming flow
- [bom.md](bom.md): Current BOM status and what still needs to be stored in-repo
- [testing.md](testing.md): Validation status, current evidence, and recommended test checklist
- [licensing.md](licensing.md): Repository-level explanation of licensing, attribution, and commercial-use notes
- [source-layout.md](source-layout.md): Current artifact layout and a future-ready source tree

## Current Artifact Paths

- PCB project: [`../pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro`](../pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro)
- Gerber package: [`../gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip`](../gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip)
- RTC MCU firmware: [`../mcu/MCU_ChisFlashRTC.hex`](../mcu/MCU_ChisFlashRTC.hex)
- CPLD firmware: [`../pof/CPLD_ChisFlash_MBCX_RTC.pof`](../pof/CPLD_ChisFlash_MBCX_RTC.pof), [`../pof/CPLD_ChisFlash_MBCX_Motor.pof`](../pof/CPLD_ChisFlash_MBCX_Motor.pof)
- Board image: [`../picture/ChisFlash_MBCX.png`](../picture/ChisFlash_MBCX.png)

## Current Gaps

- No BOM file is stored in the repository yet
- No schematic export is stored in the repository yet
- No MCU source project is stored in the repository yet
- No CPLD source project is stored in the repository yet
- README mentions RTC validation, but the test screenshots are not yet archived here

## Maintenance Goal

The goal of these docs is to let the repository stay useful now while making it easier to evolve into a complete open hardware project later.
