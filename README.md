# Hidden Stashes

[![🧪 Tested On](https://img.shields.io/badge/🧪%20Tested%20On-A21.2%20b30-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/hidden-stashes/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/hidden-stashes/actions/workflows/release.yml)

- [Hidden Stashes](#hidden-stashes)
  - [Summary](#summary)
    - [Support](#support)
  - [Features](#features)
    - [Can other players still interact with my stash?](#can-other-players-still-interact-with-my-stash)
  - [Usage](#usage)
  - [Setup](#setup)
    - [Environment / EAC / Hosting Requirements](#environment--eac--hosting-requirements)
    - [Map Considerations for Installation or Uninstallation](#map-considerations-for-installation-or-uninstallation)

## Summary

Add hidden stashes immune to detection by camera clipping/xray.

📺 [Introductory video and demonstration of how it works](https://youtu.be/SvvSQayCzdM)

### Support

🗪 If you would like support for this mod, please feel free to reach out to me via [Discord](https://discord.gg/hYa2sNHXya) (my username is `kanaverum`).

## Features

- Adds a variety of new crafting recipes and chests that can be placed to blend in with the environment.
  - Terrain blocks (when surrounded by other terrain) will stop rendering colliding surfaces. __**This fully defeats camera clipping (xray) and [will prevent players from exploiting it to find your hidden stashes](https://youtu.be/SvvSQayCzdM).**__
- Adds a tutorial phase to the getting started guide to walk players through crafting and placing their first hidden stashes.

### Can other players still interact with my stash?

Yes, they can - these hidden stashes work exactly like an unlocked chest would (other than looking like terrain).

If someone follows you to your stash location and they see you digging in the ground... then filling that ground back in, they'll know you're interacting with something that's buried and will probably go to check it out after you leave. So keep your eyes peeled and avoid frequent visits to your hidden stash locations until a visit is truly necessary or you are the only person on the server.

__**But if players attempt to leverage the camera clipping (xray) exploit, they will not be able to spot your hidden stash since [it does not render within terrain](https://youtu.be/SvvSQayCzdM).**__

## Usage

- Crafting: Simply search "hidden" in the crafting menu to see all new hidden stash recipes.
  - All players start with these crafting recipes.

## Setup

Simply [download](https://github.com/jonathan-robertson/hidden-stashes/releases/latest/download/hidden-stashes.zip) and extract the [latest version](https://github.com/jonathan-robertson/hidden-stashes/releases/latest/) of this mod to your Mods folder.

The location of this folder will depend on your environment.

> :warning: your mods folder may have to be created if it isn't already present in the location listed below

Environment | Mods Folder
--- | ---
Windows PC | Mods folder should be within your `%AppData%\7DaysToDie` directory (paste this into Windows Explorer and press enter to get there)
Windows Server | Mods folder should be located within your 7DTD install directory
Linux Server | Mods folder should be located within your 7DTD install directory

### Environment / EAC / Hosting Requirements

Environment | Compatible | Does EAC Need to be Disabled? | Who needs to install?
--- | --- | --- | ---
Dedicated Server | Yes | no | only server
Peer-to-Peer Hosting | Yes | no | only the host
Single Player Game | Yes | no | self (of course)

### Map Considerations for Installation or Uninstallation

- Does __adding__ this mod require a fresh map?
  - No! You can drop this mod into an ongoing map without any trouble.
- Does __removing__ this mod require a fresh map?
  - Since this mod adds new blocks, removing it from a map could cause some issues (previously placed robotic inbox blocks would now throw exceptions in your logs, at the very least).
  - Journal Entries added to the player Journal will unfortunately remain with their Localization stubs (but will otherwise have no text within them and will not impact gameplay at all).
