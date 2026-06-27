# 🌸 Eudora Menu v1.80
### A YimMenu Lua Script by [meluv__v](https://www.instagram.com/meluv__v/)

> A comprehensive utility menu for GTA Online — featuring money drops, rank editing, stat maximization, custom K/D control, and exclusive vehicle unlocking.

---

## ✨ Features

### 💰 Money Methods
- **OP Money Methods** — Trigger high-value stealth transactions directly from the menu
- **Nightclub Safe Loop** — Automatically fills your Nightclub safe to the cap on a loop

### 🏆 Rank Editor
- **Custom Rank Input** — Type any rank from 1–8000 and apply it instantly
- **One Click Ranks** — Preset buttons for popular ranks: 1, 10, 25, 31, 50, 69, 99, 100, 120, 200, 300, 400, 500, 600, 619, 666, 700, 800, 900, 1000, 3131, 6666, and 8000
- **Crew Rank Editor** — Set your rank across all 5 crew slots simultaneously

### 🔓 Unlocks
- **Unlock Everything** — Max out character stats, apparel, and progress flags
- **All Tattoos** — Unlock all tattoo slots across all categories at once
- **Skull Tattoo** — Unlock the rare 500-headshot skull tattoo
- **Oppressor Mk II Trade Price** — Unlock the trade price unlock flag
- **LSCM Unlocker** — Set your LS Car Meet reputation to 1000 and unlock the prize ride

### ☠️ K/D Editor
- **Custom K/D Input** — Enter any K/D ratio and have kills/deaths calculated automatically
- **Kills & Deaths Editor** — Directly set raw kills and deaths values
- **One Click PLUS K/D** — Preset frozen positive K/Ds: 1, 10, 25, 50, 69, 100, 250, 500, 619, 666, 700, 800, 900, 1000, 3131, and 6969
- **One Click MINUS K/D** — Preset frozen negative K/Ds: -1 through -6969

### 🚗 Vehicle Menu
- **Enable Removed Vehicles** — Re-enable 200+ vehicles that were removed from the in-game store

### 📊 Reports Viewer
- Live view of your Griefing, Exploiting, Bug Abuse, and Voice Chat report counts

---

## 📦 Installation

1. Make sure you have **[YimMenu](https://github.com/YimMenu/YimMenu)** installed
2. Download `Eudora.lua` and `metadata.json`
3. Place both files into your YimMenu scripts folder:
   ```
   %AppData%\YimMenu\scripts\
   ```
4. Launch GTA V with YimMenu, then navigate to **Lua Scripts** and load `Eudora`

---

## 📋 Requirements

| Requirement | Version |
|---|---|
| GTA V | Latest (Enhanced) |
| YimMenu | Latest |
| Lua Scripting | Enabled in YimMenu settings |

---

## 📝 Changelog

### v1.80 — Code Refactor & Bug Fixes
- Refactored 500+ lines of repetitive code into clean data-driven loops (Ranks, K/D, Removed Vehicles)
- Fixed `gui.show_message` spam inside ALL TATTOOS and LSCM REP loops
- Fixed redundant K/D logic that was silently overwriting custom K/D inputs
- Fixed broken FROZEN -1000 K/D value (was using wrong ratio)
- Added transaction cooldown to prevent money drop state machine breaking on double-click
- Fixed undefined `NLCl` variable crash in Nightclub loop
- Fixed "UNLCOKED" typo in Skull Tattoo message
- Fixed trailing comma typo in Crew Rank editor message
- Localized global variables (`player_male`, `FMISSIONC`, etc.) to proper scope

---

## ⚠️ Disclaimer

This script is intended for **educational and offline/private session use only**.  
Using this in GTA Online public sessions may violate Rockstar's Terms of Service and could result in account bans. **Use at your own risk.**

---

## 👏 Credits

| Person | Role |
|---|---|
| **meluv__v** | Script creator & developer |
| **Darwinoox** | First tester |

---

## 📸 Follow

- Instagram: [@meluv__v.gta](https://www.instagram.com/meluv__v/)
