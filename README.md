# WPO Hydraulic Utilities

This repository currently targets Forge 1.20.1 on the active branch.

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

- [`SKDS-Core`](https://github.com/dev-willbird1936/SKDS-Core)
- [`Water-Physics-Overhaul`](https://github.com/dev-willbird1936/Water-Physics-Overhaul)
- [`WPO-Environmental-Expansion`](https://github.com/dev-willbird1936/WPO-Environmental-Expansion)

## Build

For local source builds, clone these repositories next to this one so the folder layout is:

```text
../SKDS-Core
../Water-Physics-Overhaul
../WPO-Hydraulic-Utilities
```

Typical local build:

```powershell
.\gradlew.bat build
```

Explicit version build:

```powershell
.\gradlew.bat build -PmcVersion=1.20.1
```

Stage the release jar into the workspace release folder:

```powershell
.\gradlew.bat stageRelease -PmcVersion=1.20.1
```

Version-specific Minecraft and release values now live in `versions/<mcVersion>.properties`. Keep release tags in the form `v1.20.1-<mod-version>`, and branch by Minecraft version when later ports stop being source-compatible.

## Version Strategy

- Stable repository name, without the Minecraft version in the repo title
- `main` for the current maintained line
- `mc/<minecraft-version>` branches when code starts to diverge between game versions
- release tags in the form `v<minecraft-version>-<mod-version>`
