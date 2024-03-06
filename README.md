# Fallout 4 VR modlist<a name="top"></a>
Fallout 4 VR sucks quite badly for modern VR standards.
Gameplay is lackluster, graphics and lighting are bad, performance is bad, and there's plenty of VR-only bugs.
As is typical with Bethesda games, you can fix most of that with a whole lot of mods.
The modding scene for FO4VR has evolved a lot over time, and as a result not all tips and tricks you read online are
still accurate.

In this document I describe what I did to get a stable, enjoyable, reasonable-looking game out of Fallout 4 VR.
There are other resources out there, like
[GingasVR's excellent overhaul](https://docs.google.com/document/d/1KjAhJ3RAqUxp5TYivW7fjSC_XVEuAafiJmHfCVnb2VI/), but
that overhaul is too non-vanilla for my tastes.
So I wrote down what I did to create a mostly vanilla experience.

I did not focus as much on performance as other guides do because I have a powerful computer.
However, I still avoided mods that negatively affect performance.

(**TODO: Add note linking reader to TOC button.**)


# 1 How to read this guide<a name="how-to-read"></a> <small><sup>[top ▲](#top)</sup></small>
Read it carefully. Don't skip parts.

## 1.1 About modding Fallout 4 VR<a name="about-modding-fo4vr"></a>
(**TODO: Lower your expectations, instabilities, difficulties, etc.**)

## 1.2 About version numbers<a name="about-version-numbers"></a>
Whenever I mention a tool or a mod, I will write down which version and variant I used.
For example, I might write "F4SEVR (v0.6.20)" to mean that I downloaded version 0.6.20 of
[F4SEVR](https://f4se.silverlock.org/).

If the version I wrote down is still the latest version when you're reading this, then just use that version.
If a newer version exists, and I don't explicitly mention you should download the version I mention, then you'll have to
judge for yourself whether it's more likely the update will _fix_ bugs or will _add_ bugs.

## 1.3 About tags<a name="about-tags"></a>
Some choices I make are more vanilla than others, and some choices make sense for people who already played Fallout 4,
but make no sense for first-time Fallout 4 players.
Therefore, I will tag tools and mods to let you know what to expect.
Here is a list of tags.

* required means that, without it, the game is barely playable at all, or is not worth it in VR.
  Tools and mods with this tag are relevant for everyone regardless of personal taste.
* recommended means that it _significantly_ improves the game for _all_ players, but if you _insist_, you can choose to
  ignore my recommendation.
* optional means that I really like the additions, and think they are good, but will leave it up to you whether you use
  them.

## 1.4 Abbreviations<a name="abbreviations"></a>
|                   |                                                                                      |
|-------------------|--------------------------------------------------------------------------------------|
| **FO4VR**         | Fallout 4 VR                                                                         |
| **FO4AU**         | Fallout 4: Automatron  (the 1st DLC)                                                 |
| **FO4FH**         | Fallout 4: Far Harbor (the 3rd DLC)                                                  |
| **FO4NW**         | Fallout 4: Nuka-World  (the 6th DLC)                                                 |
| **MO2**           | Mod Organizer 2                                                                      |
| **`[fo4_dir]`**   | Where you installed non-VR FO4. For example, `C:\Steam\steamapps\common\Fallout 4\ ` |
| **`[fo4vr_dir]`** | Where you installed FO4VR. For example, `C:\Steam\steamapps\common\Fallout 4 VR\ `   |
| **`[username]`**  | Your Windows username                                                                |


# 2 Setup<a name="setup"></a> <small><sup>[top ▲](#top)</sup></small>
(**TODO: Foreword**)

## 2.1 Removing old files<a name="removing-old-files"></a>
> [!NOTE]
> If you have never installed FO4VR on your computer before, you can skip this section.

If you previously used other mods for FO4VR, make sure those are removed.
If you used MO2, make you use a clean MO2 profile, preferably by creating a new profile.
If you previously installed mods without a mod manager, make _extra_ sure you completely remove all mods.

You can remove old files as follows.
* Delete the `C:\Users\**[username]**\AppData\Local\Fallout4VR\ ` directory in its entirety.
  This contains old configuration files.
* The following apply only if you have already installed FO4VR:
  * Delete the entire `[fo4vr_dir]` directory (check the [abbreviations](#abbreviations) to know which directory I
    mean), _except_ (1) `[fo4vr_dir]\Data\Video\ ` and (2) all files in `[fo4vr_dir]\Data\ ` that start with Fallout 4.
  * In Steam, verify the integrity of FO4VR's game files.
    (How? [Check this Steam's help pages.](https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB))

## 2.2 Software requirements<a name="software-requirements"></a>
> [!WARNING]
> Read this section carefully!

* **Windows 11** (v23H2) (required)
  * I use Linux for everything, including gaming, but for VR gaming it's just not a good choice as of 2024.
* **Fallout 4 VR** (v1.2.72) (required) (**TODO: verify FO4 and FO4VR version numbers**)
  * Do **not** install FO4VR in or below `C:\Program Files (x86)\ `.
    Doing so may result in specific mods/tools unexpectedly failing because Windows doesn't like it when software
    changes things in `Program Files (x86)`.
  * If you're fine with not putting FO4VR on your `C:\ ` drive,
    [install FO4VR on another drive as explained in Steam's help pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    That said, for performance reasons, it's best to install FO4VR on an SSD.
  * If you don't want to or cannot put FO4VR on another drive,
    [move your entire Steam installation to another directory as explain in Steam's help pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    Personally, I went for `C:\Users\[username]\Steam\ `.
  * No, there is no simpler way. Yes, this is required.
* **Fallout 4 with all DLC** (v1.10.163) (recommended)
  * Why?
    [More information below.](#using-dlc-in-fo4vr)
* **[Mod Organizer 2](https://www.modorganizer.org/)** (v2.5.0) (required)
  * Use the `.exe` installer.
  * (Preferably) install on the same drive as where you installed FO4VR.
  * Install MO2 in a place where you don't need admin rights to access it.
    For example, install it somewhere in your home directory.
    Personally, I went for `C:\Users\[username]\MO2\ `.
  * (**TODO: Explain instances.**)
* **[Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)** ([direct link](https://aka.ms/vs/17/release/vc_redist.x64.exe)) (required)
* **[7-Zip](https://7-zip.org/)** (required)

## 2.3 Using DLC in FO4VR<a name="using-dlc-in-fo4vr"></a>
FO4VR does not include the DLC, which sucks.
Luckily, if you have non-VR FO4, you can just copy the DLC files into your FO4VR installation and then install a few
patches (the required patches are listed in the next section (**TODO: Link to that section**)).
If you don't have non-VR FO4 with DLC, and don't want to buy it, you can safely skip the steps that require DLC.

To copy non-VR FO4's DLC into FO4VR, go to the `[fo4_dir]\Data\ ` directory and copy all files that start with DLC
(except those that start with `DLCUltraHighResolution`) to `[fo4vr_dir]\Data\ `.


# 3 Configuration<a name="configuration"></a> <small><sup>[top ▲](#top)</sup></small>
## 3.1 Basic settings<a name="basic-settings"></a>
(**TODO: steam and windows and in-game (e.g. character lighting) and with MO2**)

## 3.2 INI configuration<a name="ini-configuration"></a>
INI files allow you to change many settings that are not found in the game's menus.
To edit these settings, shut down FO4VR if it is running and open MO2.
Then, in the main toolbar, click "Tools" (the icon has puzzle pieces), and click "INI Editor".
In this window, select the tab `fallout4custom.ini`.

### 3.2.1 How does an INI file work?
Take a look at the tab `fallout4.ini` to get a feel of what an INI looks like.

* An INI file is divided into sections, indicated by square brackets.
  For example, the line `[Display]` starts a section with display settings.
  A section ends when a new section starts.
* After starting a section you can set variables, one on each line.
  A variable has a name and a value, separated by an equals sign.
  For example, `fItemRotationSpeed=0.4` changes the variable `fItemRotationSpeed` to have value `0.4`.
* The names of sections and variables are important.
  You cannot choose your own names.
* Variables should be in the correct section.
  Putting a variable in the wrong section has no effect.
* If you have multiple lines setting the same variable, only the first assignment is used.
* You cannot split up a section.
  If you start section `[Display]`, then start section `[VR]`, and then again start section `[Display]`, the settings in
  the second `[Display]` section are ignored.

### 3.2.2 Recommended INI settings
> [!IMPORTANT]
> The following changes should go into `fallout4custom.ini`.

> [!IMPORTANT]
> Make sure each section/variable occurs at most once.

* (required) Default MO2 settings.
  * ```ini
    [General]
    sLocalSavePath=__MO_Saves\
    bUseMyGamesDirectory=1
    ```
* (required) Ensures mods load correctly.
  * ```ini
    [Archive]
    sResourceDataDirsFinal=
    bInvalidateOlderFiles=1
    sResourceStartUpArchiveList=Fallout4 - Startup.ba2, Fallout4 - Shaders.ba2, Fallout4 - Interface.ba2, Fallout4_VR - Shaders.ba2
    sResourceIndexFileList=Fallout4 - Textures1.ba2, Fallout4 - Textures2.ba2, Fallout4 - Textures3.ba2, Fallout4 - Textures4.ba2, Fallout4 - Textures5.ba2, Fallout4 - Textures6.ba2, Fallout4 - Textures7.ba2, Fallout4 - Textures8.ba2, Fallout4 - Textures9.ba2, Fallout4_VR - Main.ba2, Fallout4_VR - Textures.ba2
    ```
* (required) Disable in-game supersampling. (If you want supersampling, use the SteamVR settings.)
  * ```ini
    [VRDisplay]
    fRenderTargetSizeMultiplier=1.0
    ```
* (recommended) Improved TAA performance/quality trade-off. Most other FO4VR guides recommend these same values.
  * ```ini
    [Display]
    fTAAPostSharpen=0.675
    fTAASharpen=1.0000
    fTAAHighFreq=0.8000
    fTAALowFreq=0.5000
    fTAAPostOverlay=0.675
    ```
* (recommended) Increases Pip-Boy rendering quality.
  * ```ini
    [Display]
    uPipboyTargetHeight=1400
    uPipboyTargetWidth=1752
    ```
* (recommended) Allows sprinting even if you are looking to your side.
  * ```ini
    [Controls]
    fSprintStopDirectionThresholdDegrees=360.0000
    ```
* (recommended) Increases rotation speed of items in workshop mode.
  * ```ini
    [Workshop]
    fItemRotationSpeed=0.4
    ```
* (recommended) Makes swimming slightly easier.
  * ```ini
    [VR]
    fSwimSpeedScalar=1.2500
    fVrSwimDragCoefficient=0.0500
    fVrSwimHMDFloatThreshold=0.7200
    bVrSwimDeliberateResurface=1
    ```
* (optional) Changes direction movement to be relative to headset instead of controller. Enable this only if you like this.
  * ```ini
    [VRInput]
    bUseWandDirectionalMovement=0
    ```


# 4 List of Mods<a name="list-of-mods"></a> <small><sup>[top ▲](#top)</sup></small>
> [!INFO]
> Make sure you know [what the abbreviations mean](#abbreviations) and understand
> [the relevance of version numbers](#about-version-numbers).

* **TODO: About load order** 
* **TODO: Control scheme from Workshop**
* **TODO: Distinguish between VR-specific mods and general recommendations**

## 4.1 External libraries<a name="external-libraries"></a>
First of all, here's a few required mods/tools.
These are essentially toolkits that directly alter the game engine, and are required by many other mods.

> [!IMPORTANT]
> These mods should be installed manually.
> They should not be installed with MO2.

> [!IMPORTANT]
> These mods should be installed into `[fo4vr_dir]`, _not_ into `[fo4vr_dir]\Data\ `.

1. [F4SEVR](https://f4se.silverlock.org/) (required) (v0.6.20) (VR runtime 1.2.72)  
   This is a framework that allows modders to write custom scripts. Many other mods require this.
   * To download, go to [the F4SE website](https://f4se.silverlock.org/), find the `Fallout 4 VR runtime`, and click
     "7z archive".
   * Use [7-Zip](https://7-zip.org/) to extract the downloaded file into `[fo4vr_dir]`.
     If you did it correctly, you should have the file `f4sevr_1_2_72.dll` in the same directory as `Fallout4VR.exe`.
     If this is not the case, you probably created the directory `[fo4vr_dir]\f4sevr_0_6_20\ `, and you should copy the
     contents of that directory into `[fo4vr_dir]`.
2. [fo4vr_improvements](https://github.com/fholger/f4ovr_improvements) (required) (vcas_v2)  
   Improves some filters and shaders specifically for VR, and fixes issues the game has with Valve Index controllers.
   (If you don't use Index, this won't hurt either.)
   * To download, go to [the mod's releases page](https://github.com/fholger/f4ovr_improvements/releases), and download
     the file `fo4vr_contrast_adaptive_sharpening_v2.7z`.
   * Use 7-Zip to extract the downloaded file into `[fo4vr_dir]`.
     When prompted, choose to overwrite existing files.
     If you did it correctly, you should have the file `fo4_openvr.cfg` in the same directory as `Fallout4VR.exe`.
   * After installing, if you verify the integrity of your game files in Steam, Steam will (partially) overwrite this
     mod, and you will have to re-install this mod.
3. [vrperfkit](https://github.com/fholger/vrperfkit) (required) (v0.3)  
   Enables upscaling and foveated rendering, which improves performance by a lot.
   * To download, go to [the mod's releases page](https://github.com/fholger/vrperfkit/releases), and download the file
     `vrperfkit_v0.3.zip`.
   * Extract the downloaded file into `[fo4vr_dir]`.
     When prompted, choose to overwrite existing files.
     If you did it correctly, you should have the file `vrperfkit.yml` in the same directory as `Fallout4VR.exe`.
   * After installing, find the file `vrperfkit.yml`, open it with Notepad, and change `method: cat` to `method: fsr`.
     Otherwise (at least on my machine), the game looks fine on my monitor, but inside my VR headset the screen is
     black.
   * After installing, if you verify the integrity of your game files in Steam, Steam will (partially) overwrite this
     mod, and you will have to re-install this mod.
   * I previously tried [Fallout4 Upscaler VR](https://www.nexusmods.com/fallout4/mods/73715) (v1.0.3), but couldn't get
     it working.
4. [xSE PluginPreloader F4](https://www.nexusmods.com/fallout4/mods/33946) (required) (v0.2.5.1)  
   Will pre-load F4SEVR scripts before loading a save.
   * Extract the downloaded file into `[fo4vr_dir]`.
     If you did it correctly, you should have the file `IpHlpAPI.dll` in the same directory as `Fallout4VR.exe`.

## 4.2 Libraries<a name="libraries"></a>
> [!INFO]
> From now on, all listed mods should be downloaded and installed through MO2.

The mods in this section provide utilities used in other mods. These do not affect your game directly, but are required by many other mods.

1. [Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327) (required) (v1.10.163.0)
2. [VR Address Library for F4SEVR](https://www.nexusmods.com/fallout4/mods/64879) (required) (v1.6.1)
3. [Fallout4 VR Tools](https://www.nexusmods.com/fallout4/mods/45167) (required) (v0.1)

## 4.3 Stability and Patches<a name="stability-and-patches"></a>
These mods fix bugs, either in the base game or in other mods.

1. [Fallout 4 Version Check Patcher](https://www.nexusmods.com/fallout4/mods/42497) (required) (v1.00)  
   (**TODO: Move this to Section 1.1?**)
   FO4VR and FO4 don't have the exact same engine because FO4VR is derived from an older version of FO4.
   If someone makes a mod for FO4, it will contain the version number of the engine it's made for.
   If you then use this mod in FO4VR, you'll get warnings because the mod uses a newer version of the engine you're
   using.
   This mod disables those warnings.
   The only major relevant bug that can accidentally occur because of this version mismatch is that your game will crash 
   immediately when you load an incompatible mod, so if you see the warning (without using this mod) then it means you
   didn't have problems anyway...
2. [Unofficial Fallout 4 Patch - UFO4P](https://www.nexusmods.com/fallout4/mods/4598) (required) (v2.1.5) (requires all DLC)  
   Fixes a bunch of bugs, big and small, in the base game.
   Technically, VR is not supported by the mod authors (like with most other mods on this list), and technically the
   patches are written for a slightly different game version, but overall the pros outweigh the cons.
3. [Unofficial Fallout 4 VR Fix](https://www.nexusmods.com/fallout4/mods/47117) (required) (v1) (requires all DLC)  
   Fixes a VR-specific bug in UFO4P.
   * Load order: Below UFO4P (**TODO: Move this elsewhere?**)
4. [DLCVR - Fallout 4 VR and DLC standalone bug fixes](https://www.nexusmods.com/fallout4/mods/28842) (required) (v1.0.4) (requires FO4FH or FO4NW)  
   Fixes issues specific to FO4FH and FO4NW, relating to invisible floors and so on.
   * Choose the appropriate variant for your DLC.
5. [Edmond's Automatron VR Workbench Rebuild](https://www.nexusmods.com/fallout4/mods/55692) (required) (v1.0) (requires FO4AU)  
   Re-implements parts of FO4AU that did not work in VR. Some parts of FO4AU are still broken even with this mod.
   * Choose variant "No wild edits".
6. [Buffout 4](https://www.nexusmods.com/fallout4/mods/47359) (required) (v1.28.6)  
   Fixes engine bugs and adds a crash logger.
7. [Buffout 4 NG with PDB support](https://www.nexusmods.com/fallout4/mods/64880) (required) (v1.13.1)  
   Same as above, but for VR.
8. [Multiple Floors Sandboxing](https://www.nexusmods.com/fallout4/mods/15608) (required) (v1.0)  
   In locations with multiple storeys, NPCs walk only on the ground storey.
   This mod fixes that behaviour so NPCs walk on all storeys.
9. [No Aggro Impact Landing (Power Armor)](https://www.nexusmods.com/fallout4/mods/9019) (required) (v1.0)  
   If you wear power armour and fall from a height, you will create a shock wave that damages NPCs around you.
   Friendly NPCs damaged this way may become hostile, even if you do so by accident.
   This mod ensures that you do not accidentally turn friendly NPCs hostile this way.
10. [Radio Reverb Fix](https://www.nexusmods.com/fallout4/mods/16563) (recommended) (v1)  
    Applies reverb to your radio when applicable.
    * Choose either variant.
      I chose "Subtle" (listed under "Optional files").
11. [Bird Fix](https://www.nexusmods.com/fallout4/mods/45429) (required) (v1)  
    Fixes a bug where birds are _always_ flying into buildings for some reason.
12. **TODO: My own custom patches!**

## 4.4 Performance<a name="performance"></a>
1. [Insignificant Object Remover](https://www.nexusmods.com/fallout4/mods/9835) (required) (v1.0)
2. [FAR - Faraway Area Reform](https://www.nexusmods.com/fallout4/mods/20713) (required) (v1.2)
   * Choose variant "Default Resolution".

## 4.5 Graphics<a name="graphics"></a>
1. [Burst Impact Blast FX](https://www.nexusmods.com/fallout4/mods/57789) (recommended) (v9.51 + v0.952)
   * Download the main file (v9.51) _and_ the bloatfly patch (v0.952).
   * All options in the FOMOD installer are fine.
     If you're lazy, just spam "Next".
2. [Visible Galaxy 4k and Framework](https://www.nexusmods.com/fallout4/mods/19127) (required) (v1.0)
   * Choose variant "Visible Galaxy".
3. [Fallout 4 HD Overhaul 2k](https://www.nexusmods.com/fallout4/mods/65720) (required) (v1.01)  
   FO4VR's default textures are too ugly for VR, and the high-resolution texture pack is (supposedly) too
   VRAM-consuming.
   This texture pack provides a nice balance.
   * Download all files in section "Main files".
4. [Vivid Fallout - All in One](https://www.nexusmods.com/fallout4/mods/25714) (recommended) (v1.9)  
   Adds even nicer textures, but may have some performance impact.
   * Choose variant "Best choice".
5. [Water Enhanced](https://www.nexusmods.com/fallout4/mods/3281) (required) (v1)  
   Improves water textures.
   * Choose variant "2K Water".
6. [Detailed Feral Ghouls](https://www.nexusmods.com/fallout4/mods/20555) (recommended) (v3.1)
   * Choose variant "Better Performance - Non ESP Version".
7. [Classic Ghouls Redux](https://www.nexusmods.com/fallout4/mods/57362) (optional) (v1)  
   Changes (non-feral) ghoul textures to look more like ghouls from Fallout 3.

## 4.6 Lighting<a name="lighting"></a>
(**TODO: Note source from which I stole this configuration.**)

1. [Darker Nights](https://www.nexusmods.com/fallout4/mods/191) (recommended) (v1.11p6)
   * Choose the main file _and_ "No Glow Fix for Far Harbor DLC".
2. [PhyLight](https://www.nexusmods.com/fallout4/mods/25740) (required) (v1.1)
   * Choose variant "PhyDark (164)" _and_ "No Interior Dust or Fog".
3. [Vanilla Eye Adaptation Fix - All DLC](https://www.nexusmods.com/fallout4/mods/52129) (required) (v1.1)
   * Choose the variant with version 1.1.
4. [Fr4nsson's Light Tweaks](https://www.nexusmods.com/fallout4/mods/2139) (required) (v1.6)
   * Choose variant "plus Bloom Remover".
5. [Interiors Enhanced - Darker Ambient Light and Fog](https://www.nexusmods.com/fallout4/mods/8768) (required) (v2.0)

## 4.7 Sound<a name="sound"></a>
1. [Faded Glory - A Post-Apocalyptic Soundscape](https://www.nexusmods.com/fallout4/mods/26014) (optional) (v5-1)
2. [Fallout Suite - Soundtrack Extension](https://www.nexusmods.com/fallout4/mods/15870) (optional) (v1.1)
3. [Bleak Beauty - A Fallout 4 Fan Made OST](https://www.nexusmods.com/fallout4/mods/9663) (optional) (v1.2)
4. [Musical Lore - Wasteland Edition (Soundtrack Mod By Nir Shor)](https://www.nexusmods.com/fallout4/mods/14531) (optional) (v1.6)  
   Adds new high-quality songs to the game's radio.
5. [Ambient Wasteland - Fallout 4 Edition](https://www.nexusmods.com/fallout4/mods/25343) (recommended) (v0.1)  
   Adds a whole bunch of ambient, distant background sounds to make the world feel more lively.
6. [Realistic Reverb and Ambience Overhaul - VR and FP](https://www.nexusmods.com/fallout4/mods/61140) (recommended) (v6)  
   Tweaks sound levels in "Ambient Wasteland - Fallout 4 Edition" for VR.
   * Choose variant "Realistic Reverb and Ambience Overhaul V6".
   * Requires "Ambient Wasteland - Fallout 4 Edition".
7. [Project Reality Footsteps FO4](https://www.nexusmods.com/fallout4/mods/35904) (recommended) (v1.7)  
   Adds more different kinds of footstep sounds.
   * Choose variant "Project Reality Footsteps FO4 1.7 BA2".
8. [Not Great Not Terrible - Scarier Geiger Counter Sounds](https://www.nexusmods.com/fallout4/mods/45354) (optional) (v1.0)  
   Replaces geiger counter sounds to be more intense.
   * Choose either variant. I chose "Quieter Version".

## 4.8 UI<a name="ui"></a>
The UI in VR is unintuitive to navigate, and the key bindings shown in the UI are usually incorrect.
Unfortunately, there are currently no good UI mods for VR.
[FallUI](https://www.nexusmods.com/fallout4/mods/48758) (v2.2.1) sort of works, but suffers from a variety of bugs in
VR, like bad contrast between text and background, menus being too small, and some VR-only menus not being replaced at
all.
[MCM](https://www.nexusmods.com/fallout4/mods/21497) (v1.39) also doesn't work; mods that use MCM are fine, but you
can't configure them through MCM.

1. [Full Dialog VR](https://www.nexusmods.com/fallout4/mods/28516/) (recommended) (v1.1)
   In conversations, you usually have four response options.
   The game summarises these using keywords.
   This is annoying, because your character may say something completely different from what you expected.
   This mod replaces the keywords with the full line your character will say.
   * After installing, edit the mod's files, and remove the file `interface\MultiActivateMenu.swf`.
     This fixes a bug where no text is shown at all when talking with followers.

## 4.9 Gameplay<a name="gameplay"></a>
1. [FRIK - Full Player Body with IK](https://www.nexusmods.com/fallout4/mods/53464) (required) (v0.58)  
   Allows you to see your hands. Absolutely required for immersion.
   * Requires some configuration. (**TODO: Link**)
   * > [!WARNING]
     > Download this mod, but leave this mod de-activated for now.
   * I tried [Idle Hands](https://www.nexusmods.com/fallout4/mods/42922) (v3.0.5) before as an alternative, but couldn't 
     get it working.
2. [Player Collision Options - nocollide actors](https://www.nexusmods.com/fallout4/mods/41866) (required) (v1.0)  
   Normally, when you get close to an NPC in VR, the game will push you back. This is annoying and disorienting when you
   want to roleplay or pet your dog.
   This disables collisions between you and NPCs.
3. [Realistic Death Physics - No Animations](https://www.nexusmods.com/fallout4/mods/4371) (recommended) (v1.2)  
   Merely "recommended" because there is a slightly increased chance that there's some physical glitching going on.
   The trade-off there is yours to make.
   * Choose variant "ALL DLC version".
4. [PipBoy VR light](https://www.nexusmods.com/fallout4/mods/29245) (required) (v1.1)  
   In VR, the default Pip-Boy light (the "flashlight") is just a weak glow around you.
   I really liked the flashlight in Half-Life: Alyx.
   This mod changes the shape of the Pip-Boy's light to be like a flashlight, and does so with no performance overhead.
   I personally chose the small light because I want it to be scary, but you can choose any variant you want.
   * Choose the single main file _and_ one optional file.
     (I chose "Gun style aimed Small Gobo".)
5. [Everyone's Best Friend](https://www.nexusmods.com/fallout4/mods/13459) (recommended) (v3.0.0)  
   Normally you can only have one follower, but Dogmeat really isn't comparable to the depth of the other companions.
   But Dogmeat is also really cute.
   This mods lets you have both Dogmeat and any other companion at the same time.
   * Also install [EBF UFO4P compatibility fix](https://www.nexusmods.com/fallout4/mods/43409) (v2.1.0)
6. [Splinterz - Breakable Wooden Doors](https://www.nexusmods.com/fallout4/mods/21521) (optional) (v1.3)  
   Allows you to break doors. Pretty cool.

## 4.10 Combat<a name="combat"></a>
(**TODO: Source**)

1. [See-Through-Scopes](https://www.nexusmods.com/fallout4/mods/9476) (required) (v2.5.3)  
   Changes in-game scopes so they are see-through. Required for the next mod.
2. [Better Scopes VR](https://www.nexusmods.com/fallout4/mods/61214) (required) (v0.9)  
   This one is _absolutely_ required.
   Without this mod, when you look down a scope, your screen turns black and you get a full-screen 2D projection of what
   you can see through your scope.
   Absolutely horrible and nauseating.
   This mod removes that screen, and just lets you look through the actual scope.
   * Choose only the main file, not the optional file.
3. [Bullet Time VATS VR](https://www.nexusmods.com/fallout4/mods/72502) (required) (vb1.1)  
   In vanilla, VATS is a gameplay mechanic that pauses combat and lets you select body parts to target, which you will
   then automatically shoot at.
   This sucks in VR, because you don't get to aim the gun and pull the trigger yourself.
   This mod replaces VATS with bullet time.
   * Additional configuration (**TODO: link**).
4. [Critical Hits Outside of VATS](https://www.nexusmods.com/fallout4/mods/12653) (required) (v1.1.3)  
   The above Bullet Time mod actually disables VATS, and thus completely removes critical hits from the game.
   This mod allows you to score critical hits again, even outside of bullet time.
5. [Hip-Fire Perk Replacers](https://www.nexusmods.com/fallout4/mods/40702) (required) (v1.2)  
   In vanilla, hip-fire is when you shoot without aiming down the sights.
   In VR, hip-fire doesn't exist.
   As a result, hip-fire perks are useless.
   This mod makes those perks useful again.
6. [Weapon Accuracy Redone for VR](https://www.nexusmods.com/fallout4/mods/40669) (required) (v1.0)  
   In VR it's super annoying if you're clearly aiming at an enemy and then the game decides the shot didn't hit because
   of some random die.
   This mod reduces weapon spread and recoil to make accuracy in VR more rewarding.
7. [Better Low Health](https://www.nexusmods.com/fallout4/mods/6018) (recommended) (v1.0)  
   Your health bar is visible on the inside of your wrist, but that's also where you're holding your gun, so during
   combat you typically don't really know how much health you have left.
   The game shows some visual effects at 20% health left, but that's usually too late.
   This mod increases that threshold to 50%.
   * Choose variant "50".
8. [More Noticeable Hit Effect](https://www.nexusmods.com/fallout4/mods/6157) (required) (v1.0)  
   I noticed that during fights I usually had no idea if bullets were flying past me or into me.
   This mod makes it much more noticeable when you are being hit.
   * Choose variant "aMedium".

## 4.11 Difficulty / Survival<a name="difficulty-survival"></a>
Fallout 4 is not a difficult game, even at higher difficulties.
In VR, it only gets easier.
Mods in this category affect the difficulty.
Some (but not all) of them assume you play in Survival mode, which I recommend you do anyway.

1. [Survival Options](https://www.nexusmods.com/fallout4/mods/14650) (recommended) (v1.7.1)  
   Allows you to customise your survival mode experience. Lets you re-enable fast travel, manual saves, auto-saves, and
   change damage multipliers.
   * In-game config! (**TODO: Config link**)
   * Recommended even for non-survival playthroughs! (**TODO: Config link**)
2. [JOURNEY](https://www.nexusmods.com/fallout4/mods/12685) (recommended) (v1.6.1)  
   Re-enables a restricted form of fast travel. You can use this together with
   [Survival Options](https://www.nexusmods.com/fallout4/mods/14650).
   * In-game config! (**TODO: link**)
3. [Campsite](https://www.nexusmods.com/fallout4/mods/11734) (recommended) (v1.0.4)  
   Lets you bring a tent with you so you can sleep anywhere.
4. [Loot Logic and Reduction With optional Harvest Restrictions](https://www.nexusmods.com/fallout4/mods/21366) (recommended) (v1.5.3.1)  
   Reduces loot found in containers. Otherwise you'll quickly find you'll have so much ammo and chems the game just
   totally isn't challenging anymore.
5. [NPC Loot Drop rebalance](https://www.nexusmods.com/fallout4/mods/24163) (recommended) (v1.0)  
   Reduces loot found on NPCs, in line with the above mod.
6. [Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/29447) (recommended) (v1.5.4)  
   In survival, you have less carrying capacity and heavier items. These backpacks will come in use.
7. [Dogmeat's Backpack](https://www.nexusmods.com/fallout4/mods/10111) (recommended) (v2.0)  
   As above, but now for your companion.
8. [Dogmeat's Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/62037) (recommended) (v1.3)  
   Re-balances the above mod to be in line with the one above that.
9. (**TODO: Test this**) [Headshot Damage Multiplier](https://www.nexusmods.com/fallout4/mods/33546) (recommended) (v1.0)
   * Choose variant "x5".
10. [Radiation Overhaul - 4x More Radiation Across the Wasteland](https://www.nexusmods.com/fallout4/mods/13790) (optional) (v1.1)  
    Makes radiation actually dangerous.

## 4.12 Settlements<a name="settlements"></a>
I think Fallout 4's settlements are very flawed.
In VR, they are not necessarily more or less flawed than in non-VR, so the mods in this section are not VR-specific.
However, several of these mods require VR-specific tweaks.
That said, this entire section is recommended, because the VR experience is no worse than the non-VR experience with or
without these.
If you don't intend to engage with settlements at all, you can skip this section.

1. [Sim Settlements](https://www.nexusmods.com/fallout4/mods/21872) (recommended) (v4.1.7)
   Completely changes the way settlements are built.
   Instead of you building everything, settlers will build and upgrade their own houses in designated locations.
   I especially like the "leaders" feature, where you can appoint a settlement leader who will oversee the placement of
   all buildings in the settlement.
   It just works.
   * Choose variant "Three In One".
   * > [!CAUTION]
     > You **must** choose version 4.1.7.
     > Do **not** choose a newer version.
   * For configuration, see **TODO: Config link**.
   * **TODO: SS2 guide link.**
2. [Leaders Of The Commonwealth](https://www.nexusmods.com/fallout4/mods/30495) (recommended) (v2)  
   With basic Sim Settlements, only your followers are leaders.
   Especially at the start of the game, it's frustrating if your settlements can't grow because you don't have enough
   leaders for the number of settlements you find.
   This mod designates several unique settlers from the base game as leaders.
   * Choose variant "Vanilla Looks No New npcs".
3. [Salvage Beacons](https://www.nexusmods.com/fallout4/mods/18757) (optional) (v1.0.4)  
   Carrying junk back to your settlement is frankly a waste of time.
   This lets you drop off your junk and whatnot in any container, then mark that container, and your settlers will take
   back your loot to your settlement.
4. [IDEK's Logistics Station 2](https://www.nexusmods.com/fallout4/mods/48389) (recommended) (v2.1.3)  
   I wasn't sure whether to make this recommended or required.
   In Fallout 4, you can connect your settlements using supply routes, which allows the settlements to share resources.
   Unfortunately, this feature is super annoying to use, hard to get right, and hard to manage.
   This mod automates most of that part:
   You just build one object, assign a settler, and the mod will handle all the routing.
   There's also a bunch of other really useful features which improve the stability of your trading routes.
   * [Make sure you configure this mod after you've started the game.](#configuring-your-mods)
   * There is an option to integrate this with Sim Settlements and with Salvage Beacons, but I didn't use those
     integrations because I couldn't figure them out.
5. (TODO: **local leader**)


# 5 Configuring your mods<a name="configuring-your-mods"></a> <small><sup>[top ▲](#top)</sup></small>
(**TODO**)


# A. Launching and running<a name="launching-and-running"></a> <small><sup>[top ▲](#top)</sup></small>
(**TODO: Rephrase and restructure this.**)

* Always launch through MO2.
  Always use F4SEVR!
  (**TODO: Describe how to add F4SEVR in MO2**)
* Remove external gamepads before launching the game.
* Start your VR controllers before launching the game.
  If you start them too late, some buttons will not work, you'll notice this in the main menu when you try to scroll
  down.
  In that case, restart the game.
* In the main menu, if you select `Continue`, or select `Load` and then choose a save, and you notice nothing happens,
  pull the right trigger again (or whatever button you use to select).
  What happened is that there was a message saying you have changed your load order, asking for confirmation, but for
  some reason that message is invisible when in the main menu.
  If you want to see what the difference in load order is, then load the save, and then while in-game load that save;
  now the message will be visible.
* QuickSave is extremely unreliable and very often breaks mods/saves.
  AutoSave is somewhat unreliable and sometimes breaks mods.
  Therefore, manually save often, and avoid loading QuickSaves or AutoSaves.
  (Making an AutoSave or QuickSave by itself is not harmful.
  It's just that you shouldn't load them.)
  You can use the Survival Options mod mentioned earlier to replace Quick-Saves with Saves.
* Don't use your pipboy while the light is on!
  You may get a CTD otherwise.
  Some claim that Buffout4 fixes this, but in my game, it didn't, as I would continue to CTD.
* If you die, load your previous save manually.
  (**TODO: Is there a mod that increases the load time, or otherwise changes this?**)
* Don't swim, lol
