# PocketSim

PocketSim is a custom enemy spawning tool for OpenWF that provides a more powerful and convenient alternative to Warframe's normal Simulacrum enemy selection.

It runs as an OpenWF `.pluto` script and provides a web browser interface for quickly searching for enemies, configuring spawn settings, and spawning them directly into the current mission.

## Features

- Web browser UI for easy use
- Large searchable and filterable enemy catalog
- Favorites list for frequently used enemies
- Recently used enemy list
- Persistent browser settings
- Enemy levels from **1 to 9999**
- Spawn **1 to 20 enemies at once**
- Multiple spawn positions
- Adjustable spacing when spawning multiple enemies
- Option to make spawned enemies friendly
- Option to make all enemies Steel Path
- Option to automatically clear previously spawned enemies before spawning new ones
- Clear all enemies currently tracked by PocketSim

## Requirements

- A working OpenWF installation
- A Warframe version supported by OpenWF scripting

PocketSim is intended for use with OpenWF and custom/private Warframe servers.

## Installation

1. Download `PocketSim.pluto` from this repository.

2. Place the file in your OpenWF scripts folder:

   ```text
   OpenWF/Scripts/PocketSim.pluto
   ```

3. Start Warframe through OpenWF.

## Starting PocketSim

### Recommended: Start PocketSim through in-game chat

If OpenWF's **Chat Commands** script is installed and running, which it is enabled to auto-start by default, then the recommended way to start PocketSim is by entering:

```text
/script pocketsim
```

Entering the command again will stop the script.

The OpenWF Chat Commands sample script is separate from PocketSim. PocketSim itself does not require Chat Commands after it has been started.

When PocketSim starts, its browser interface will normally be available at:

```text
http://localhost:6155/pocketsim
```

### Alternative: Start PocketSim through the OpenWF WebUI

1. Start Warframe through OpenWF.

2. Open the OpenWF client WebUI while Warframe is running.

   The default address is normally:

   ```text
   http://localhost:6155/
   ```

3. Open the **Scripts** section.

4. Start `PocketSim.pluto`.

5. Open the PocketSim interface:

   ```text
   http://localhost:6155/pocketsim
   ```

## Usage

### 1. Open the PocketSim Interface

After starting PocketSim, open:

```text
http://localhost:6155/pocketsim
```

The PocketSim interface can be left open in your normal web browser while playing Warframe.

### 2. Select an Enemy

Use the search box and filters to find the enemy you want to spawn.

Click an enemy to select it.

PocketSim also keeps track of your recently used enemies and allows you to save frequently used enemies as favorites.

### 3. Configure the Spawn

Configure the spawn settings before spawning the selected enemy.

#### Level

Set the enemy level anywhere from:

```text
1 - 9999
```

Common level presets are also available.

#### Count

Spawn between:

```text
1 - 20
```

enemies at once.

#### Spawn Position

Choose where the enemies should be created.

Available spawn positions include:

- **Crosshair** - attempts to spawn the enemy at the location you are aiming at
- **In Front** - spawns the enemy a short distance in front of your Warframe
- **Player** - spawns the enemy at your current position

#### Spacing

Controls the distance between enemies when spawning multiple enemies at once.

#### Friendly

Makes the spawned enemy use the player's faction instead of its normal enemy faction.

This can be useful for spawning allies or watching different enemies fight each other.

#### Steel Path

Enables Warframe's native Steel Path enemy modifier.

While enabled, the Steel Path modifier applies to enemies in the current mission.

#### Clear First

Automatically removes enemies previously spawned and tracked by PocketSim before spawning the new group.

### 4. Spawn the Enemy

Press the **Spawn** button to create the selected enemy using the configured settings.

You can also double-click an enemy in the list to quickly spawn it.

### 5. Clear Spawned Enemies

Use the **Clear** option to remove enemies currently being tracked by PocketSim.

This makes it easy to repeatedly test different enemies without restarting the mission.

## Keyboard Shortcuts

| Key | Function |
| --- | --- |
| `Ctrl+K` | Focus the enemy search box in the WebUI |
| `Enter` | Spawn the selected enemy in the WebUI |
| `F8` | Show or hide the in-game PocketSim status overlay in-game |

## Special Enemies and NPCs

PocketSim includes many enemies and NPC resources that are normally unavailable through the standard Simulacrum.

This includes various:

- Bosses
- Quest enemies
- Event enemies
- Special enemy variants
- Friendly NPCs
- Specters
- Companions
- Wildlife
- Mission-specific NPCs
- Other unusual spawnable agents

Some special enemies rely on mission-specific scripts, game rules, encounters, animations, or other initialization that normally occurs when they appear in their intended mission.

Because PocketSim allows these enemies to be spawned outside of their normal environment, some special enemies may:

- Spawn without functioning correctly
- Remain idle
- Lack certain boss mechanics
- Miss mission-specific phases
- Behave differently from their normal mission version
- Fail to spawn entirely

Regular enemies generally do not have this limitation.

## Version Compatibility

PocketSim has currently only been tested extensively on:

```text
Warframe 42.0.11
```

This is the version currently considered the known-working PocketSim environment.

PocketSim should also work on other Warframe versions that support OpenWF scripting, but compatibility with other versions has **not been tested or guaranteed**.

Warframe's internal resources, enemy paths, scripting behavior, and game functions can change between updates. Some enemies or PocketSim features may therefore fail to work or behave differently on versions other than 42.0.11.

## Reporting Bugs

PocketSim has not been tested with every enemy, boss, NPC, or special resource in the catalog. Some entries may fail to spawn, behave incorrectly, or depend on mission-specific functionality.

If you encounter a bug or find an enemy that does not work correctly, please report it through either of these methods:

- Send a message in the [PocketSim Discord thread](https://discord.com/channels/1108159019635462206/1533163974353223680)
- Open an issue on this GitHub repository

When reporting a problem, please include the enemy or boss name, a short description of what happened, and how to reproduce it.
