Flamethrower Turret
Version: 1.0.1
fixed issue where 2 or more flame trap dont work 
Version: 1.0.0

Description
Flamethrower Turret adds flamethrower variants of the Junk Turret (MK1/MK2/MK3) that use Gas Can ammo and apply heat damage + burning effects in a short flame volume instead of firing projectiles.

This release also includes an optional powered "Flamethrower Trap" using the same flame logic.

Key Features
- New deployable flamethrower turrets (MK1 / MK2 / MK3)
- Optional powered flamethrower traps (MK1 / MK2 / MK3)
- Uses Gas Can ammo (ammoGasCan) as fuel
- Flame is a forward volume (OverlapBox) that can hit multiple targets at once
- Optional direct tick damage (heat) + buff application (burning/slow/etc.)
- Fuel consumption is per STARTED second of flame time (prevents “free” partial seconds)
- Durability wear is per second of active flame (mirrors vanilla turret degradation-per-use behavior)
- Multiplayer-safe FX handling (server spawns FX once per burst; clients keep only one live FX and stop cleanly)
- Prevents using the turret item as a handheld weapon (you can still place it)

Installation
This mod must be installed on BOTH the client and the server for multiplayer.

1) Copy the mod folder into:
   ...\7 Days To Die\Mods\
2) Make sure 0_TFP_Harmony is installed and loaded.
3) Dedicated server: install the same mod version on the server AND all clients.

EAC
Easy Anti-Cheat (EAC) MUST be disabled.
This mod uses Harmony patches and custom DLL logic.

  - Adds turret :
    - flameTurretGunMK1
    - flameTurretGunMk2
    - flameTurretGunMK3

  - Adds powered traps:
    - flamethrowerTrapMk1
    - flamethrowerTrapMk2
    - flamethrowerTrapMk3

  - Adds workbench recipes for turret items and trap blocks.

  - Adds crafting unlocks:
    - craftingRobotics unlocks turret tiers (MK1 @ 11+, MK2 @ 51+, MK3 @ 76+)
    - craftingTraps unlocks trap tiers (MK1 @ 25+, MK2 @ 50+, MK3 @ 75+)


Notes / Compatibility
- The mod patches MiniTurretFireController.Fire/Update/shouldIgnoreTarget and ParticleEffect.SpawnParticleEffect.
  Other mods that patch the same methods may conflict.
- If clients do not have the mod installed, they may see broken FX behavior (stop commands) or missing visuals.
- Item name typo for MK2 (gunBotT2flameTurreMk2) is intentionally supported; changing it requires updating XML references.
