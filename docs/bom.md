# BOM And Parts Status

This repository does not yet contain a checked-in BOM spreadsheet or placement table.

## Current Source Of Truth

For the moment, the practical source of BOM and assembly guidance is still the project page on OSHWHub:

- <https://oshwhub.com/morinaka/chisflash-cqz>

## What We Can Confirm From The Current Repository

- The board supports two modes: `MBC3 RTC` and `MBC5 rumble`
- The RTC version requires both the MCU firmware and the RTC-related populated components
- The rumble version does not require the MCU / RTC section to be populated
- A `0-ohm` resistor option was added for SRAM / FRAM configuration
- A resistor near the battery area must be installed for battery power delivery

## Suggested BOM Files To Add Later

If you want this repository to become self-contained, these are the most useful files to add next:

- `docs/bom/ChisFlash-MBCX_BOM.csv`
- `docs/bom/ChisFlash-MBCX_CPL.csv`
- `docs/bom/ChisFlash-MBCX_AssemblyNotes.md`
- `docs/bom/ChisFlash-MBCX_ValueSubstitutions.md`

## Suggested BOM Sections

- Core logic parts
- RTC-only population differences
- Rumble-only population differences
- SRAM / FRAM option differences
- Crystal and battery-related notes
- Footprint substitutions and package notes

Until those files are stored in-repo, it is best to treat the OSHWHub page as the main assembly reference.
