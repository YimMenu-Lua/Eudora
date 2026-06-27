# Eudora Menu — Feature Architecture

This document outlines the internal structure of `Eudora.lua` for contributors and developers who want to understand how the menu is built.

---

## Menu Hierarchy

```
EUDORA (gui.get_tab)
├── MONEY METHODS
│   ├── OP MONEY METHODS        (TransactionManager — stealth drops)
│   └── NIGHTCLUB SAFE LOOP     (globals loop via script.register_looped)
│
├── RANKS
│   ├── RANK EDITOR             (custom input → stats.set_int CHAR_SET_RP_GIFT_ADMIN)
│   ├── ONE CLICK RANKS         (data-driven ipairs loop, 23 presets)
│   └── CREW RANK EDITOR        (sets MPPLY_CREW_LOCAL_XP_0 through _4)
│
├── UNLOCKS
│   ├── UNLOCK EVERYTHING       (stats flags, apparel, progress)
│   └── LSCM UNLOCKER           (globals loop + prize ride flag)
│
├── VEHICLE MENU
│   └── ENABLE REMOVED VEHICLES (200+ global offsets via ipairs loop)
│
├── K/D STATS (KDS)
│   ├── CUSTOM K/D SETTER       (math-derived kills/deaths from input ratio)
│   ├── KILLS/DEATHS EDITOR     (raw input)
│   └── ONE CLICK K/Ds
│       ├── PLUS K/D            (16 presets, ipairs loop)
│       └── MINUS K/D           (16 presets, ipairs loop)
│
└── CREDITS / INFO
    └── Social links, tester credits
```

---

## Key Stats

| Stat Name | Purpose |
|---|---|
| `MPPLY_LAST_MP_CHAR` | Determines character slot (MP0 / MP1) |
| `MPX() .. "CHAR_SET_RP_GIFT_ADMIN"` | Sets player rank RP |
| `MPPLY_KILLS_PLAYERS` | Kill count (used for K/D) |
| `MPPLY_DEATHS_PLAYER` | Death count (used for K/D) |
| `MPPLY_CREW_LOCAL_XP_0` – `_4` | Crew rank XP for all 5 slots |
| `MPX() .. "TATTOO_FM_UNLOCKS_N"` | Unlocks tattoo slot N (0–53) |

---

## TransactionManager

The `TransactionManager` class handles stealth money drops using Rockstar's internal `NETSHOPPING` natives.

```
TriggerTransaction(item_hash)
  └── Executes inside "shop_controller" script context
      ├── Checks / clears active basket
      ├── NET_GAMESERVER_BEGIN_SERVICE  →  opens transaction
      └── NET_GAMESERVER_CHECKOUT_START →  commits transaction
```

A **3-second cooldown** is enforced between drops to prevent transaction state corruption.

---

## Nightclub Loop

Runs via `script.register_looped("nightclubremotelooptest")` and fires every ~3.5 seconds while the checkbox is enabled.

Sets globals in the range `262145 + IncomeStart` → `262145 + IncomeEnd` to `SafeAmount` (250,000), simulating max nightclub income and filling the safe.
