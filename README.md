# WPO Hydraulic Utilities 1.20.1

Original add-on mod for Water Physics Overhaul, maintained for Forge 1.20.1.

## What It Adds

Hydraulic Utilities adds practical control blocks for moving, directing, filtering, sealing, and testing water in WPO setups.

The current block set includes:

- `Drain`
- `Pump`
- `Nozzle`
- `Valve`
- `Water Grate`
- `Water + Item Grate`
- `Water + Item + No Mob Grate`
- `Watertight Door`
- `Watertight Trapdoor`
- `Creative Water Source`
- `Creative Lava Source`

## System Overview

This add-on is focused on control and infrastructure rather than world simulation.

Its systems let players:

- pull WPO water into internal machine tanks
- push stored water back into the world
- spray or output water through nozzles
- block or allow flow with valves
- filter what passes through a grate
- keep structures sealed with watertight door blocks
- spawn test fluids directly with creative sources

The machine-side tuning is controlled through:

- machine tank capacity in buckets
- drain throughput in WPO water levels
- pump throughput in WPO water levels
- nozzle throughput in WPO water levels
- creative source output in WPO water levels

## Configuration

The common config is stored at:

```text
config/wpo_hydraulic_utilities/common.toml
```

The in-game config screen exposes both system toggles and balance values.

System toggles include:

- drains
- pumps
- nozzles
- creative sources
- valves
- grates
- watertight doors
- watertight trapdoors
- redstone control
- void excess water

## How It Fits With WPO

Hydraulic Utilities assumes the base Water Physics Overhaul simulation already exists and adds player-facing tools around it.

This mod is useful for:

- moving water in controlled builds
- automation setups
- compact test rigs
- sealing structures against WPO water
- creative debugging and reproduction setups

For external fluid transport between machines, Pipez is the recommended companion mod.

## Credits

- Original Water Physics Overhaul work: `Sasai_Kudasai_BM`
- 1.18.2 work used in the porting path: `Felicis`
- 1.20.1 port and repository maintenance: [`dev-willbird1936`](https://github.com/dev-willbird1936)

## Related Repositories

- [`SKDS-Core-1.20.1`](https://github.com/dev-willbird1936/SKDS-Core-1.20.1)
- [`Water-Physics-Overhaul-1.20.1`](https://github.com/dev-willbird1936/Water-Physics-Overhaul-1.20.1)
- [`WPO-Environmental-Expansion-1.20.1`](https://github.com/dev-willbird1936/WPO-Environmental-Expansion-1.20.1)

## Build

For local source builds, clone these repositories next to this one so the folder layout is:

```text
../SKDS-Core-1.20.1
../Water-Physics-Overhaul-1.20.1
../WPO-Hydraulic-Utilities-1.20.1
```

Typical local build:

```powershell
.\gradlew.bat build
```
