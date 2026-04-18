# Testing And Validation

This page records what the repository currently claims, what evidence is present, and what would make the project easier for other builders to trust and reproduce.

## Current Repository-Level Claim

The existing project notes state that the `MBC3 RTC` implementation reproduces the RTC registers and passed RTC-related testing.

## Evidence Currently Stored In-Repo

- Release artifacts for PCB, CPLD firmware, and MCU firmware
- One board image: [`../picture/ChisFlash_MBCX.png`](../picture/ChisFlash_MBCX.png)

## Evidence Not Yet Archived In-Repo

- RTC test screenshots
- Rumble-mode validation notes
- Flashing setup screenshots
- Real hardware photos of finished boards
- Known-good game / cartridge compatibility notes

## Suggested Validation Checklist

### Common

1. Confirm the cartridge powers up and boots reliably
2. Confirm save retention across power cycles
3. Confirm battery-backed behavior is stable
4. Confirm the selected firmware matches the populated hardware

### RTC Mode

1. Confirm time increments correctly across minutes and hours
2. Confirm time persists across power loss
3. Confirm RTC register reads behave as expected in software
4. Confirm date rollover behavior if applicable

### Rumble Mode

1. Confirm rumble trigger behavior in known compatible software
2. Confirm current draw is acceptable
3. Confirm omitted MCU / RTC section does not affect normal operation

## Suggested Files To Add Later

- `docs/testing/rtc-screenshots/`
- `docs/testing/rumble-notes.md`
- `docs/testing/programmer-settings.md`
- `docs/testing/known-good-titles.md`

Even a small amount of archived validation material would make the repository feel much more complete.
