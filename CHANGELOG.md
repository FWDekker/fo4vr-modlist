# Changelog
## [unreleased]
### Changed
* Changed [Multiple Floors Sandboxing](https://www.nexusmods.com/fallout4/mods/15608) from _required_ to _recommended_.
* Changed [No Aggro Impact Landing (Power Armor)](https://www.nexusmods.com/fallout4/mods/9019) from _required_ to _recommended_.


## [1.1.1] -- 2024-04-24
This version contains a few minor updates to mods and a few clarifications in the installation instructions. 

### How to upgrade
Follow these steps to update your mod list from v1.1.0 to v1.1.1 of my guide.

* Update [Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/29447) from v1.5.4 to v1.5.6.
* Remove [Backpacks of the Commonwealth - Dirty Edit Patch](https://www.nexusmods.com/fallout4/mods/79705).

### Added
* Added small note on [FRIK](https://www.nexusmods.com/fallout4/mods/53464) alpha 64. This version is currently untested in my guide, but is _probably_ fine.

### Changed
* Updated [Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/29447) from v1.5.4 to v1.5.6.
* Updated [UFO4P - VR weapon and armor keyword crash patch](https://www.nexusmods.com/fallout4/mods/79711) from v2.1.5-1.0.4 to v2.1.5-1.0.5.
* Updated [Classic Ghouls Redux - UFO4P and LotC patch](https://www.nexusmods.com/fallout4/mods/79713) from v1-1.0.4 to v1-1.0.5.
* Updated [Radiation Overhaul - UFO4P and item name patch](https://www.nexusmods.com/fallout4/mods/79708) from v1.1-1.0.3 to v1.1-1.0.4.
* Clarified which individual in-game settings are required, recommended, and optional.
* Emphasised the need to change the config for [vrperfkit](https://github.com/fholger/vrperfkit) to ensure the game properly displays in the headset, since several users overlooked this.

### Removed
* Removed [Backpacks of the Commonwealth - Dirty Edit Patch](https://www.nexusmods.com/fallout4/mods/79705).

### Fixed
* Corrected the version number of [Buffout 4 NG](https://www.nexusmods.com/fallout4/mods/64880) from v1.13.1 to v1.31.1. ([#12](https://github.com/FWDekker/fo4vr-modlist/issues/12))
* Fixed a small typo in the [vrperfkit](https://github.com/fholger/vrperfkit) installation instructions.


## [1.1.0] -- 2024-04-09
Thank you, everyone, for the great reactions!

I've incorporated plenty of comments and feedbacks, and fixed a few errors.

### How to upgrade
Follow these steps to update your mod list from v1.0.0 to v1.1.0 of my guide.

* Mods
  * Remove [Hip-Fire Perk Replacers](https://www.nexusmods.com/fallout4/mods/40702). This mod can be removed safely from an existing playthrough.
  * Remove [Unofficial Fallout 4 VR Fix](https://www.nexusmods.com/fallout4/mods/47117). This mod can be removed safely from an existing playthrough.
  * Unless you play survival difficulty, remove [Survival Options](https://www.nexusmods.com/fallout4/mods/14650). This mod can be removed safely from an existing playthrough.
  * Update [VR weapon and armor keyword crash patch](https://www.nexusmods.com/fallout4/mods/79711) from v2.1.5-1.0.3 to v2.1.5-1.0.4.
* Settings
    * Add the "Fix glowing hair" config from Section 3.2.2 to your INI configuration.
    * Add the "Increase UI rendering quality" config from Section 3.2.2 to your INI configuration.
    * Update your settings for [Survival Options](https://www.nexusmods.com/fallout4/mods/14650) according to Section 5.4.3.
* Notes
  * Unlike what this guide said earlier, using quicksaves and autosaves is actually fine.
  * If you did not finish the prologue yet, disable [UFO4P](https://www.nexusmods.com/fallout4/mods/4598), start a new game, and follow Section 5 of the guide again.

### Added
* Added description of guide's limitations to introduction.
* Added an INI config snippet for fixing weirdly glowing hair.
* Added an INI config snippet for improving the quality of the UI.
* Added note about anecdotal reports about issues with UFO4P in other guides.
* Added [Binaural 3D Surround Sound for Headphones](https://www.nexusmods.com/fallout4/mods/39692).
* Added instructions on how to obtain settings holotapes for [Survival Options](https://www.nexusmods.com/fallout4/mods/14650) and [Bullet Time VATS VR](https://www.nexusmods.com/fallout4/mods/72502).
* Added additional tips for troubleshooting with FRIK.

### Changed
* Changed [UFO4P](https://www.nexusmods.com/fallout4/mods/4598) from _required_ to _recommended_.
* Changed [Radio Reverb Fix](https://www.nexusmods.com/fallout4/mods/16563) from _recommended_ to <sub>![optional]</sub>.
* Changed [Water Enhanced](https://www.nexusmods.com/fallout4/mods/3281) from _required_ to _recommended_.
* Changed [PipBoy VR light](https://www.nexusmods.com/fallout4/mods/29245) from _required_ to _recommended_.
* Changed [More Noticeable Hit Effect](https://www.nexusmods.com/fallout4/mods/6157) from _required_ to _recommended_.
* Updated [VR weapon and armor keyword crash patch](https://www.nexusmods.com/fallout4/mods/79711) from v2.1.5-1.0.3 to v2.1.5-1.0.4.
* Changed "I did not test Sim Settlements 2, avoid it" to "I did not test Sim Settlements 2".
* Improved cross-sectional navigation in various ways.

### Removed
* Removed [Hip-Fire Perk Replacers](https://www.nexusmods.com/fallout4/mods/40702). Hip-fire is less broken in VR than I thought, so this mod isn't actually necessary. It's fine to keep using this mod, but it's no longer part of this guide. You can remove the mod safely from an existing playthrough, because it only edits existing perks, without adding or removing any.
* Removed [Unofficial Fallout 4 VR Fix](https://www.nexusmods.com/fallout4/mods/47117). Since this guide now requires that [UFO4P](https://www.nexusmods.com/fallout4/mods/4598) is disabled during the prologue, this patch is no longer required. You can remove the mod safely from an existing playthrough, because it affects only the first time you exit Vault 111.
* Removed [Survival Options](https://www.nexusmods.com/fallout4/mods/14650) for non-survival playthroughs. Using quicksaves and autosaves is actually fine, so there's no need to use this mod in non-survival mode.

### Fixed
* Fixed an incorrect claim that critical hits do not exist outside of VATS.
* Fixed an incorrect claim that using autosaves and quicksaves is unsafe and causes bugs. Apparently, this advice has been incorrect since the release of Oblivion, 18 years ago...
* Require that [UFO4P](https://www.nexusmods.com/fallout4/mods/4598) is disabled during entirety of prologue, since this causes a crash when exiting Vault 111.


## [1.0.0] -- 2024-04-01
Initial release.
