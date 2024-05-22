<p align="center">
  <img src="https://raw.githubusercontent.com/0vergrown/Origins-Wither-Unleashed/main/pack.png" alt="Wither Unleashed cover"/>
</p>

# Origins: Wither Unleashed

Origins: Wither Unleashed is a Minecraft datapack designed to enhance the difficulty of the Wither boss fight, inspired by the Bedrock Edition Wither. This datapack makes the battle more challenging for both Origin users and Java players.

## Dependencies
This datapack requires the following to function properly:
- [Fabric Loader](https://fabricmc.net/) - Recommend loader the mods run on.
- [Fabric API](https://fabricmc.net/use/) - Necessary for running mods in the Fabric mod loader environment.
- [Origins Mod](https://github.com/apace100/origins-fabric) - A Minecraft mod that allows you to choose an Origin at the beginning, granting various abilities and drawbacks.

## Features

### Cataclysmic Demise
- **Functionality**: On death, the Wither now triggers a substantial explosion.
- **Implementation**:
  - **Action**: `origins:action_on_death`
  - **Parameters**: Explosion of power level 2, destruction type set to "break", without self-damage or fire.

### Heart of the Nether
- **Functionality**: The Wither's max health is boosted to a remarkable total of 600 hearts.
- **Implementation**:
  - **Attribute Modification**: Increase of 300 to max health.
  - **Modifier Details**: Applied as an addition operation on `minecraft:generic.max_health`.

### Nether Blitz
- **Functionality**: Periodically, the Wither executes a high-speed dash that generates a shockwave, inflicting Wither effect, blindness, and slowness.
- **Implementation**:
  - **Interval**: Every 600 ticks.
  - **Composite Actions**: Combination of velocity addition, sound effects, particle effects, and an area effect that applies multiple impacts.

### Skeleton Summoning
- **Functionality**: When health drops below 500, the Wither summons Wither Skeletons, each carrying a stone sword and belonging to a predefined team.
- **Implementation**:
  - **Condition**: Health ≤ 500.
  - **Actions**: Sequential entity spawning with integrated delay and special effects, reinforcing thematic consistency with soul fire flame particles and characteristic sounds.

### Nether Blast
- **Functionality**: Wither Skulls fired by the Wither now deliver 25% more knockback.
- **Implementation**:
  - **Attribute Modification**: Knockback attribute of the skulls enhanced by multiplying the total by 1.25.
  - **Effect Details**: Specifically modifies `minecraft:generic.attack_knockback`.

## Installation
To install the Origins: Wither Unleashed datapack, follow these steps:
1. Make sure you have all dependencies installed.
2. Download the latest release of the datapack from the [release page](https://modrinth.com/datapack/origins-wither-unleashed).
3. Place the downloaded file in the `datapacks` folder of your Minecraft world directory.
4. Restart your Minecraft world or use `/reload` if the world is already running.

## Usage
Once installed, summon the Wither boss in your Minecraft world. The enhanced abilities and increased skull knockback will be automatically applied.

## Contributing
Contributions to this project are welcome. You can contribute by:
- Submitting bugs and feature requests.
- Improving the efficiency of the powers used.
- Enhancing the functionality with additional features.
