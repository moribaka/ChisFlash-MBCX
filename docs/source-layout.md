# Source Layout

This repository currently publishes usable release artifacts, but it does not yet include a full source-level hardware and firmware tree.

## Current Practical Layout

| Path | Role |
| --- | --- |
| `gerber/` | Manufacturing-ready board output |
| `pcb/` | PCB project file |
| `pof/` | Released CPLD programming files |
| `mcu/` | Released MCU programming file |
| `picture/` | Visual assets |

## New Normalized Structure Added In This Cleanup

| Path | Purpose |
| --- | --- |
| `docs/` | Human-facing documentation |
| `hardware/` | Future location for hardware release notes and source files |
| `firmware/` | Future location for firmware release notes and source files |

## Why The Release Files Were Not Moved

The existing paths may already be referenced by users, links, or old repository history. To avoid breaking downloads, this cleanup keeps the current artifact paths stable and adds the normalized structure alongside them.

## Suggested Future Tree

```text
.
|-- README.md
|-- README_EN.md
|-- NOTICE.md
|-- LICENSE
|-- docs/
|   |-- README.md
|   |-- assembly.md
|   |-- bom.md
|   |-- testing.md
|   `-- licensing.md
|-- hardware/
|   |-- README.md
|   |-- releases/
|   `-- source/
|-- firmware/
|   |-- README.md
|   |-- releases/
|   `-- source/
|-- gerber/
|-- pcb/
|-- pof/
|-- mcu/
`-- picture/
```

## What To Put In Hardware Source Later

- EDA source project files
- Schematic exports
- BOM and CPL exports
- Assembly drawings
- Revision notes

## What To Put In Firmware Source Later

- MCU source project
- CPLD / HDL project
- Build instructions
- Programmer settings
- Version-to-release mapping

This approach gives the repository a clear long-term destination without forcing a breaking file move today.
