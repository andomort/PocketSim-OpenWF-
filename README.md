# PocketSim

PocketSim is a custom enemy spawning tool for OpenWF that provides a more powerful and convenient alternative to Warframe's normal Simulacrum enemy selection.

It runs as an OpenWF `.pluto` script and provides a browser-based interface for quickly searching for enemies, configuring spawn settings, and spawning them directly into the current mission.

## Features

- Large searchable enemy catalog
- Search enemies by name
- Filter enemies by faction
- Favorites list for frequently used enemies
- Recently used enemy list
- Persistent browser settings
- Enemy levels from **1 to 9999**
- Spawn **1 to 20 enemies at once**
- Multiple spawn positions:
  - At the crosshair
  - In front of the player
  - At the player's position
- Adjustable spacing when spawning multiple enemies
- Option to make spawned enemies friendly
- Option to automatically clear previously spawned enemies before spawning new ones
- Clear all enemies currently tracked by PocketSim
- Double-click an enemy to spawn it
- Press **Enter** to spawn the selected enemy
- Press **Ctrl+K** to immediately focus the search box
- Copy an enemy's internal Warframe resource path
- Small in-game PocketSim status overlay
- Press **F8** to show or hide the PocketSim status overlay
- Designed to use Warframe's normal enemy agent spawning rather than manually recreating enemy behavior

## Requirements

- A working OpenWF installation
- OpenWF Bootstrapper with scripting support enabled
- A Warframe version supported by OpenWF scripting
- A local or private OpenWF environment

PocketSim is intended for use with OpenWF and custom/private Warframe servers.

## Installation

1. Download `PocketSim.pluto` from this repository.

2. Place the file in your OpenWF scripts folder:

   ```text
   OpenWF/Scripts/PocketSim.pluto
   ```

3. Start Warframe through OpenWF.

4. Open the OpenWF client WebUI while Warframe is running.

   The default address is normally:

   ```text
   http://localhost:6155/
   ```

5. Open the **Scripts** section and start `PocketSim.pluto`.

### Optional: Start PocketSim through in-game chat

If OpenWF's **Chat Commands** script is installed and running, PocketSim can also be started by entering:

```text
/script pocketsim
```

Entering the command again will stop the script.

The OpenWF Chat Commands sample script is separate from PocketSim. PocketSim itself does not require Chat Commands once it has been started.

## Usage

### 1. Start PocketSim

Start `PocketSim.pluto` from the OpenWF Scripts page or use:

```text
/script pocketsim
```

if Chat Commands is running.

When PocketSim starts, it will display its browser interface address.

By default, this will normally be:

```text
http://localhost:6155/pocketsim
```

Open this page in your normal browser or through an in-game browser/overlay.

### 2. Select an enemy

Use the search box or faction filters to find the enemy you want.

Click an enemy to select it.

You can also:

- Favorite enemies for quick access later
- View recently spawned enemies
- Copy the enemy's internal resource path

### 3. Configure the spawn

Before spawning, configure the settings you want.

#### Level

Set the enemy level anywhere from:

```text
1 - 9999
```

Several common level presets are also available.

#### Count

Spawn between:

```text
1 - 20
```

enemies at once.

#### Spawn Location

Choose where the enemy should appear:

- **Crosshair** - attempts to spawn the enemy at the location you are aiming at
- **In Front** - spawns the enemy a short distance in front of your Warframe
- **Player** - spawns the enemy at your current position

#### Spacing

Controls the distance between enemies when spawning multiple enemies.

#### Friendly

Changes the spawned enemy to the player's faction.

This can be useful for testing friendly NPC behavior or watching enemies fight each other.

#### Clear First

Automatically removes enemies previously spawned and tracked by PocketSim before creating the new group.

### 4. Spawn the Enemy

Press the **Spawn** button.

You can also:

- Double-click an enemy in the list to spawn it
- Press **Enter** to spawn the currently selected enemy

PocketSim will display the current spawn status in the browser and in its small in-game status overlay.

### 5. Clear Spawned Enemies

Use the **Clear** option in PocketSim to remove enemies currently being tracked by the script.

This is useful when testing large numbers of enemies without needing to restart the mission.

## Keyboard Shortcuts

| Key | Function |
| --- | --- |
| `Ctrl+K` | Focus the enemy search box |
| `Enter` | Spawn the selected enemy |
| `F8` | Show or hide the in-game PocketSim status overlay |

## Special Enemies and NPCs

PocketSim includes enemies and NPC resources that are normally unavailable through the standard Simulacrum.

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

Some special enemies rely on mission-specific scripts, game rules, encounters, animations, or other initialization that normally happens in their original mission.

Because PocketSim allows these enemies to be spawned outside of their intended environment, some special enemies may:

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

PocketSim should also work on other Warframe versions that support OpenWF's scripting system, but compatibility with other versions has **not been tested or guaranteed**.

Warframe's internal enemy resources, resource paths, scripts, and engine behavior can change between updates. Some enemies may therefore fail to load or behave differently on versions other than 42.0.11.

## Disclaimer

PocketSim is an unofficial community project intended for use with **OpenWF and private/custom Warframe environments**.

It is not affiliated with, endorsed by, or supported by Digital Extremes.

Use PocketSim at your own risk.

PocketSim has only been tested and verified on **Warframe 42.0.11**. Other Warframe versions may work if they support OpenWF scripting, but they are currently untested.
