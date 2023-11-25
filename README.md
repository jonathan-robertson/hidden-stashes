# Hidden Stashes

[![🧪 Tested On](https://img.shields.io/badge/🧪%20Tested%20On-A21.2%20b30-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/hidden-stashes/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/hidden-stashes/actions/workflows/release.yml)

- [Hidden Stashes](#hidden-stashes)
  - [Summary](#summary)
    - [Support](#support)
  - [Features](#features)
    - [Can other players still interact with my stash?](#can-other-players-still-interact-with-my-stash)
  - [Usage](#usage)
    - [No Treasure Hunter Perk Variant](#no-treasure-hunter-perk-variant)
    - [Container Size Adjustments](#container-size-adjustments)
  - [Setup](#setup)
    - [Environment / EAC / Hosting Requirements](#environment--eac--hosting-requirements)
    - [Map Considerations for Installation or Uninstallation](#map-considerations-for-installation-or-uninstallation)
  - [Special Thanks](#special-thanks)

## Summary

🛡️ Add Hidden Stashes (immune to detection by camera clipping/xray) and a skill to detect them (skill can optionally be removed).

📺 [Introductory video and demonstration of how it works](https://youtu.be/SvvSQayCzdM)

### Support

🗪 If you would like support for this mod, please feel free to reach out to me via [Discord](https://discord.gg/hYa2sNHXya) (my username is `kanaverum`).

## Features

- ⚙️ Adds a variety of new crafting recipes and chests that can be placed to blend in with the environment.
  - 🩻 Terrain blocks (when surrounded by other terrain) will stop rendering colliding surfaces. __**This fully defeats camera clipping (xray) and [will prevent players from exploiting it to find your hidden stashes](https://youtu.be/SvvSQayCzdM).**__
- 📝 Adds a tutorial phase to the getting started guide to walk players through crafting and placing their first hidden stashes.
- ☠️ Updates `Treasure Hunter` to also be capable of detecting Hidden Stashes nearby. This can be helpful for locating your own stash if you forget to mark it on the map, or for finding the stash of your opponent.
  - ⏳ With this skill, the player is required to crouch and stay completely still to focus on nearby stashes for an extender period of time (even firing a weapon, reloading, or using an item would interrupt focus and reset the timer).
  - 💎 Once the nearby area has been fully examined, the player will see in-world and compass icons indicating the position of nearby Hidden Stashes.

### Can other players still interact with my stash?

⚠️ Yes, they can - these hidden stashes work exactly like an unlocked chest would (other than looking like terrain).

🧐 If someone follows you to your stash location and they see you digging in the ground... then filling that ground back in, they'll know you're interacting with something that's buried and will probably go to check it out after you leave. So keep your eyes peeled and avoid frequent visits to your hidden stash locations until a visit is truly necessary or you are the only person on the server.

🛡️ __**But if players attempt to leverage the camera clipping (xray) exploit, they will not be able to spot your hidden stash since [it does not render within terrain](https://youtu.be/SvvSQayCzdM).**__

## Usage

- ⚙️ Crafting: Simply search "hidden" in the crafting menu to see all new hidden stash recipes.
  - All players start with these crafting recipes.
- 👀 Detection: Invest at least one skill point into the `Treasure Hunter` perk, located within the `Perception` skill tree.
  - ⏳ After that, find you can place a hidden stash and bury it, the crouch near your hidden stash. A timer will count down and then you'll see an icon for your hidden stash if you are close enough to it.
  - ❌ When you get up to move, fire a weapon, or perform almost any other action (besides simply looking around), all hidden stash icons will disappear and you'll need to wait while crouching once more if you want to see them again.

### No Treasure Hunter Perk Variant

🤔 If you dislike the idea of players being able to detect Hidden Stashes, you can remove that functionality by copying the contents of `Config/variant-without-perk` into `Config`.

- ℹ️ Once copied/overwritten, this mod will no longer include the changes to `Treasure Hunter` (meaning that players will have no way of detecting Hidden Stashes other than digging and directly interacting with them).
- 🛠️ You can make this change at any time, even in an active map! Restarting the server will cause the change to go into effect and will not cause harm to your map or world save in any way.
  - ✅ If you later decide to add the perk back, you can do so by copying `Config/default-with-perk` into `Config` - again, without causing any harm to your ongoing map.

### Container Size Adjustments

- 🛠️ If you aren't happy with the container size of the hidden stashes (maybe you want them larger or smaller), you can easily adjust this by modifying the `size` field in `Config/loot.xml`.
  - ✅ Changing this value will have *no* negative effect on an existing map; just keep in mind that any stashes already placed will have the *original* size values before your change.

## Setup

📦 Simply [download](https://github.com/jonathan-robertson/hidden-stashes/releases/latest/download/hidden-stashes.zip) and extract the [latest version](https://github.com/jonathan-robertson/hidden-stashes/releases/latest/) of this mod to your Mods folder.

🔍 The location of this folder will depend on your environment.

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
  - ✅ No! You can drop this mod into an ongoing map without any trouble.
- Does __removing__ this mod require a fresh map?
  - ⚠️ Since this mod adds new blocks, removing it from a map could cause some issues (previously placed robotic inbox blocks would now throw exceptions in your logs, at the very least).
  - ⚠️ Journal Entries added to the player Journal will unfortunately remain with their Localization stubs (but will otherwise have no text within them and will not impact gameplay at all).

## Special Thanks

- 🎉 Much thanks to @Zipcore for suggesting a method to temporarily detect Hidden Stashes via quests and nav markers!
