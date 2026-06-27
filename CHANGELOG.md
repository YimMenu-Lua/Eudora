# Changelog

All notable changes to Eudora Menu will be documented in this file.

---

## [1.80] — 2026-06-27

### Added
- Transaction cooldown on OP Money Methods to prevent double-click state corruption
- Helpful cooldown notification message when triggering drops too fast

### Changed
- Refactored 23 One-Click Rank buttons into a single data-driven `ipairs` loop
- Refactored 200+ `globals.set_int` calls in Removed Vehicles into a loop
- Refactored 16 PLUS K/D preset buttons into a single `ipairs` loop
- Refactored 16 MINUS K/D preset buttons into a single `ipairs` loop
- Localized `player_male`, `FMISSIONC`, `FMISSIONC2020`, `HISLANDP` to `local` scope
- Updated menu header and load messages to reflect v1.80

### Fixed
- `gui.show_message` called 54 times inside ALL TATTOOS loop (now called once after loop)
- `gui.show_message` called 30 times inside LSCM REP 1000 loop (now called once after loop)
- Redundant K/D logic block that silently overwrote the correct kills/deaths calculation
- FROZEN -1000 K/D using `-100,000,000` kills instead of the correct `-1,000,000,000`
- Undefined `NLCl` variable in Nightclub loop causing crash on toggle (commented out with TODO)
- Crew Rank editor message having a stray `, .` at the end
- "UNLCOKED" typo in Skull Tattoo unlock message

---

## [1.70] — Prior

- Initial public release of Eudora Menu
- Money methods, rank editor, K/D editor, unlocks, and vehicle menu
