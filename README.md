# SafeGraphCleanup

**Skyrim SE/AE Mod** — Prevents crashes from multi-actor physics/death cleanups in big fights.  
Throttles WIDeadBodyCleanupScript, limits graph updates, safe actor deletion. Compatible with HDT-SMP, CBPC, dense battles.

## Features
- ✅ Crash-proof body cleanup (no infinite loops on 50+ corpses)
- ✅ Physics graph reset without CTDs
- ✅ MCM toggle + actor limit config
- ✅ SKSE64 + USSEP required

## Installation
1. **Requirements:**
   | Mod | Version | Link |
   |-----|---------|------|
   | SKSE64 | 2.2.6+ | skse.silverlock.org |
   | USSEP | Latest | Nexus |
   | PapyrusUtil SE | Latest | Nexus |
   | (Optional) HDT-SMP/CBPC | - | - |

2. **Vortex/MO2:** Drag & drop.
3. **Manual:** Extract to `Data/`, enable `SafeGraphCleanup.esp` in MO2/LE.
4. **Nemesis:** Run "All" + patches if using animation mods.
5. **Test:** Spawn 20+ NPCs, kill 'em, check no CTD.

## Config (MCM)
- `MaxActors`: Default 6 (physics throttle above this)
- `CleanupDelay`: 30s cooldown per cell
- `DebugMode`: Logs to SKSE/Plugins/SafeGraphCleanup.log

## Known Issues
- Rare race condition in heavy modlists — enable DebugMode, share crash log.
- AE 1.6.1170 Version
