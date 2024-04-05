# Florine's Fallout 4 VR
_Version 1.0.0, see the [CHANGELOG.md](CHANGELOG.md)_

> A thorough, beginner-friendly guide for a stable, vanilla-ish experience.

**Motivation**  
Fallout 4 VR sucks quite badly for modern VR standards.
Gameplay is lackluster; graphics, lighting, and performance are bad; and there's plenty of VR-only bugs in addition to
the bugs in vanilla.
As is typical with Bethesda games, you can fix most of that with a whole lot of mods.
The modding scene for FO4VR has evolved a lot over time, and as a result not all tips and tricks you read online are
still accurate.

This guide aims to be comprehensive and beginner-friendly.
You can choose to follow it in its entirety, or pick and choose parts for your own list.

**Goals**  
I describe what I did to get a **stable, enjoyable, reasonable-looking** game.
Other resources, like
[GingasVR's excellent overhaul](https://docs.google.com/document/d/1KjAhJ3RAqUxp5TYivW7fjSC_XVEuAafiJmHfCVnb2VI/), are
good, but too non-vanilla for my tastes.
Meanwhile, my list only deviates from vanilla when I think there's a very good reason, like replacing VATS with bullet
time because the former just isn't nice in VR.

**Limitations**  
I did my best to make my guide universally applicable to all players.
Still, there's a few limitations which you should keep in mind.

* I didn't really focus on performance, because I have a powerful PC.
  However, I mostly avoided mods that negatively affect performance.
* I personally run a Valve Index and use an AMD GPU.
  This is irrelevant for the vast majority of this guide, except [when including external libraries](#external-libraries).

**Support**  
If you don't understand something, experience in-game issues, have suggestions, or just need some help,
[check out the Discussions page](https://github.com/FWDekker/fo4vr-modlist/discussions) or
[open an issue](https://github.com/FWDekker/fo4vr-modlist/issues).

> [!TIP]
> Use the hamburger menu (≡) in the top-right corner to easily navigate between sections.

---

**Table of contents**  
<a name="toc"></a>[**1 How to read this guide**](#how-to-read)
| [**2 Setup**](#setup)
| [**3 Configuration**](#configuration)
| [**4 List of mods**](#list-of-mods)
| [**5 Playing the game**](#playing-the-game)

---

# 1 How to read this guide<a name="how-to-read"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!TIP]
> Read this guide carefully.

This section deals with the basics:
[Why FO4VR modding is difficult](#about-modding-fo4vr),
[how this guide deals with version numbers](#about-version-numbers),
[how to pick and choose mods from this guide](#about-tags),
and [common abbreviations](#abbreviations).

## 1.1 About modding Fallout 4 VR<a name="about-modding-fo4vr"></a> <small><sup>[top ▲](#toc)</sup></small>
When I tried FO4VR without mods, I intensely disliked the experience, and decided I wanted to add mods.
If you're used to modding Bethesda games, you'll know that it's usually _probably_ fine to just throw a whole bunch of
mods together, as long as you follow the authors' directions on what mods are incompatible.
Unfortunately, that's not true for FO4VR.
The VR version is missing several updates that were released only for the non-VR version, and as a result mods made for
the non-VR version may use features that simply don't exist in the VR version.
Using mods blindly _will_ result in the game crashing regularly.

Overall, you should lower your expectations when modding FO4VR compared to non-VR FO4.
The modding scene just isn't as advanced as that of Skyrim VR.
You may find that your favourite mods just don't work very well in FO4VR, and when browsing mods you should always
carefully consider whether the benefits outweigh the risks.

This modding guide describes the tradeoffs I made, leaning mostly towards the careful side.

## 1.2 About version numbers<a name="about-version-numbers"></a> <small><sup>[top ▲](#toc)</sup></small>
Whenever I mention a tool or a mod, I will write down which version and variant I used.
For example, I might write "F4SEVR (v0.6.20)" to mean that I downloaded version 0.6.20 of
[F4SEVR](https://f4se.silverlock.org/).

If the version I wrote down is still the latest version when you're reading this, then just use that version.
If a newer version exists, and I don't explicitly mention you should download the version I mention, then you'll have to
judge for yourself whether it's more likely the update will _fix_ bugs or will _add_ bugs.

## 1.3 About tags<a name="about-tags"></a> <small><sup>[top ▲](#toc)</sup></small>
Some choices I make are more vanilla than others, and some choices make sense for people who already played Fallout 4,
but make no sense for first-time Fallout 4 players.
Therefore, I will tag tools and mods to let you know what to expect.
Here is a list of tags.

|                |                                                                    |
|----------------|--------------------------------------------------------------------|
| ![required]    | Necessary to make the game worth it in VR. Install this.           |
| ![recommended] | Good for all players. Install this, unless you seriously disagree. |
| ![optional]    | Good, but personal preference. Install if you want.                |

## 1.4 Abbreviations<a name="abbreviations"></a> <small><sup>[top ▲](#toc)</sup></small>
| Abbreviation      | Meaning                                     | Example                                   |
|-------------------|---------------------------------------------|-------------------------------------------|
| **FO4VR**         | Fallout 4 VR                                |                                           |
| **FO4AU**         | Fallout 4: Automatron  (the 1st DLC)        |                                           |
| **FO4FH**         | Fallout 4: Far Harbor (the 3rd DLC)         |                                           |
| **FO4VW**         | Fallout 4: Vault-Tec Workshop (the 5th DLC) |                                           |
| **FO4NW**         | Fallout 4: Nuka-World  (the 6th DLC)        |                                           |
| **MO2**           | Mod Organizer 2                             |                                           |
| **`[fo4_dir]`**   | Where you installed non-VR FO4              | `C:\Steam\steamapps\common\Fallout 4\`    |
| **`[fo4vr_dir]`** | Where you installed FO4VR                   | `C:\Steam\steamapps\common\Fallout 4 VR\` |
| **`[username]`**  | Your Windows username                       | `florine`                                 |


# 2 Setup<a name="setup"></a> <small><sup>[top ▲](#toc)</sup></small>
Before you can start modding FO4VR, you need to make sure you have a clean install and have the right software
installed.

## 2.1 Removing old files<a name="removing-old-files"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!TIP]
> If you haven't installed FO4VR yet, check the [software requirements](#software-requirements) to learn the correct
> installation directory.

> [!NOTE]
> If you have never installed FO4VR on your computer before, you can skip this section.

If you previously used other mods for FO4VR, make sure those are removed.
If you used MO2, make you use a clean MO2 profile, preferably by creating a new profile.
If you previously installed mods without a mod manager, make _extra_ sure you completely remove all mods.

You can remove old files as follows.
1. Delete the `C:\Users\[username]\AppData\Local\Fallout4VR\` directory in its entirety.
   This contains old configuration files.
2. The following apply only if you have already installed FO4VR:
   1. Delete the entire `[fo4vr_dir]` directory, but

      1. **not** `[fo4vr_dir]\Data\Video\`, and
      2. **not** files in `[fo4vr_dir]\Data\` that start with `Fallout4`.

      If you cannot find `[fo4vr_dir]`, check the [abbreviations](#abbreviations).
   2. In Steam, verify the integrity of FO4VR's game files.
      ([Check Steam's help pages to learn how.](https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB))

## 2.2 Software requirements<a name="software-requirements"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!WARNING]
> You should install FO4VR into the right directory.
> Read this section carefully!

* **Windows 11** (v23H2) <sub>![required]</sub>  
  I use Linux for everything, including gaming, but for VR gaming it's just not a good choice as of 2024.
* **SteamVR** (v2.4.3) <sub>![required]</sub>
* **Fallout 4 VR** (v1.2.72.0.1) <sub>![required]</sub>
  * Do **not** install FO4VR in or below `C:\Program Files (x86)\`.
    Doing so may result in specific mods/tools unexpectedly failing, because Windows doesn't like it when software
    changes things in `Program Files (x86)`.
  * If you're fine with not putting FO4VR on your `C:\` drive,
    [install FO4VR on another drive as explained in Steam's help
    pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    For performance reasons, you should prefer installing on an SSD.
  * If you don't want to or cannot put FO4VR on another drive,
    [move your entire Steam installation to another directory as explain in Steam's help
    pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    Personally, I went for `C:\Users\[username]\Steam\`.
  * No, there is no simpler way. Yes, this is required.
* **Fallout 4 with all DLC** (v1.10.163) <sub>![recommended]</sub>  
  [More information below.](#using-dlc-in-fo4vr)
* **[Mod Organizer 2](https://www.modorganizer.org/)** (v2.5.0) <sub>![required]</sub>
  * Use the `.exe` installer.
  * For performance reasons, you should prefer installing on an SSD.
  * Install MO2 in a place where you don't need admin rights to access it.
    For example, install it somewhere in your home directory.
    Personally, I went for `C:\Users\[username]\MO2\`.
  * When launching for the first time, you will be asked to create an instance.
    * You can create a global or a portable instance.
      It doesn't really matter which you choose.
    * Enable profile-specific INIs.
    * Enable profile-specific saves.
* **[Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)** ([direct link](https://aka.ms/vs/17/release/vc_redist.x64.exe)) <sub>![required]</sub>
* **[7-Zip](https://7-zip.org/)** <sub>![required]</sub>

## 2.3 Using DLC in FO4VR<a name="using-dlc-in-fo4vr"></a> <small><sup>[top ▲](#toc)</sup></small>
FO4VR does not include the DLC, which sucks.
Luckily, if you have non-VR FO4, you can just copy the DLC files into your FO4VR installation and then install a few
patches (included in the [mod list](#list-of-mods)).
If you don't have non-VR FO4 with DLC, and don't want to buy it, you can safely skip the steps that require DLC.

To copy non-VR FO4's DLC into FO4VR,
1. go to the `[fo4_dir]\Data\` directory,
2. select all files that start with `DLC`, except those that start with `DLCUltraHighResolution`, and
3. copy those files to `[fo4vr_dir]\Data\`.


# 3 Configuration<a name="configuration"></a> <small><sup>[top ▲](#toc)</sup></small>
You should now have the required software.
Before you install mods, there's some settings to tweak.
These settings relate to stability, visual quality, and performance.

> [!NOTE]
> Even if you skip these steps, at least launch the game once.
> This will set up important files and registry entries.

## 3.1 Basic settings<a name="basic-settings"></a> <small><sup>[top ▲](#toc)</sup></small>
1. **Steam**  
   Go to the settings for Fallout 4 VR.
   Go to "General" and disable "Enable the Steam Overlay while in-game".  
   (If you cannot disable this option, you disabled it globally, which is fine too.)
2. **Windows Explorer**  
   Navigate to `[fo4vr_dir]`, right-click `Fallout4VR.exe`, and click "Properties".
   Go to "Compatibility" and enable "Disable full-screen optimisations".
3. While in-game in VR, in FO4VR's main menu, go to "Settings" and apply the following settings.
   1. _Gameplay_

      | Setting    | Value    |
      |------------|----------|
      | Difficulty | Survival |

      If you don't want to use survival, disable "Save on Rest", "Save on Wait", and "Save on Travel", install
      [Survival Options](https://www.nexusmods.com/fallout4/mods/14650), and follow the
      [in-game configuration](#configure-mods), explained later on.
   2. _Display_

      | Setting          | Value |
      |------------------|-------|
      | Floating markers | Off   |
   3. _VR_

      | Setting                        | Value     |
      |--------------------------------|-----------|
      | Direct movement                | On        |
      | Pip-Boy location               | Projected |
      | Comfort vignette while moving  | Off       |
      | Comfort vignette while turning | Off       |
      | Rotation type                  | Smooth    |
   4. _Performance_

      | Setting               | Value |
      |-----------------------|-------|
      | Anti-aliasing         | TAA   |
      | Anisotropic filtering | 16    |
      | Character lighting    | Off   |

## 3.2 INI configuration<a name="ini-configuration"></a> <small><sup>[top ▲](#toc)</sup></small>
INI files contain extra game settings that are not found in the game's menus.

To edit these settings,
1. shut down FO4VR if it's running,
2. open MO2,
3. in the main menu, click "Tools", then "Tool Plugins", and then "INI Editor", and
4. select the tab `fallout4custom.ini`.

### 3.2.1 How does an INI file work? <small><sup>[top ▲](#toc)</sup></small>
Take a look at the tab `fallout4.ini` to get a feel of what an INI looks like.

INI files obey the following rules.
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

### 3.2.2 Settings you should add <small><sup>[top ▲](#toc)</sup></small>
> [!IMPORTANT]
> The following changes should go into `fallout4custom.ini`.

> [!IMPORTANT]
> Make sure each section/variable occurs at most once.

> [!TIP]
> You can copy-paste all non-optional configs below effortlessly at once
> [from Section 3.2.3](#ini-configuration-combined).

**Default MO2 settings** <sub>![required]</sub>
```ini
[General]
sLocalSavePath=__MO_Saves\
bUseMyGamesDirectory=1
```

**Ensure mods load correctly** <sub>![required]</sub>
```ini
[Archive]
sResourceDataDirsFinal=
bInvalidateOlderFiles=1
sResourceStartUpArchiveList=Fallout4 - Startup.ba2, Fallout4 - Shaders.ba2, Fallout4 - Interface.ba2, Fallout4_VR - Shaders.ba2
sResourceIndexFileList=Fallout4 - Textures1.ba2, Fallout4 - Textures2.ba2, Fallout4 - Textures3.ba2, Fallout4 - Textures4.ba2, Fallout4 - Textures5.ba2, Fallout4 - Textures6.ba2, Fallout4 - Textures7.ba2, Fallout4 - Textures8.ba2, Fallout4 - Textures9.ba2, Fallout4_VR - Main.ba2, Fallout4_VR - Textures.ba2
```

**Disable in-game supersampling** <sub>![required]</sub>  
To enable supersampling, use the SteamVR settings.
```ini
[VRDisplay]
fRenderTargetSizeMultiplier=1.0
```

**Fix glowing hair** <sub>![required]</sub>  
Fixes a bug where hair appears with the wrong colour or glows in the dark.
```ini
[HairLighting]
fHairPrimSpecPow=2.0
fHairPrimSpecScale=0.01
fHairPrimSpecShift=0.26
fHairSecSpecScale=0.01
fHairSecSpecPow=2.0
fHairSecSpecShift=0.26
```

**Improve TAA performance/quality trade-off** <sub>![recommended]</sub>  
Most other FO4VR guides recommend these same values.
```ini
[Display]
fTAAPostSharpen=0.675
fTAASharpen=1.0000
fTAAHighFreq=0.8000
fTAALowFreq=0.5000
fTAAPostOverlay=0.675
```

**Increase Pip-Boy rendering quality** <sub>![recommended]</sub>
```ini
[Display]
uPipboyTargetHeight=1400
uPipboyTargetWidth=1752
```

**Increase UI rendering quality** <sub>![recommended]</sub>
```ini
[VRUI]
iVRUIRenderTargetHeight=4096
iVRUIRenderTargetWidth=4096
```

**Allow sprinting regardless of head orientation** <sub>![recommended]</sub>
```ini
[Controls]
fSprintStopDirectionThresholdDegrees=360.0000
```

**Increase item rotation speed in workshop mode** <sub>![recommended]</sub>
```ini
[Workshop]
fItemRotationSpeed=0.4
```

**Make swimming slightly easier** <sub>![recommended]</sub>
```ini
[VR]
fSwimSpeedScalar=1.2500
fVrSwimDragCoefficient=0.0500
fVrSwimHMDFloatThreshold=0.7200
bVrSwimDeliberateResurface=1
```

**Set move direction relative to headset instead of controller** <sub>![optional]</sub>
```ini
[VRInput]
bUseWandDirectionalMovement=0
```

**Disable in-game tutorial notifications** <sub>![optional]</sub>
```ini
[Interface]
bShowTutorials=0
```

### 3.2.3 All non-optional configs<a name="ini-configuration-combined"></a> <small><sup>[top ▲](#toc)</sup></small>
The block below contains all non-optional configs from Section 3.2.2.
You can copy-paste it into your `fallout4custom.ini` file.
You don't need to keep the old contents, just overwrite it with the block below.

```ini
[General]
sLocalSavePath=__MO_Saves\
bUseMyGamesDirectory=1
[Archive]
sResourceDataDirsFinal=
bInvalidateOlderFiles=1
sResourceStartUpArchiveList=Fallout4 - Startup.ba2, Fallout4 - Shaders.ba2, Fallout4 - Interface.ba2, Fallout4_VR - Shaders.ba2
sResourceIndexFileList=Fallout4 - Textures1.ba2, Fallout4 - Textures2.ba2, Fallout4 - Textures3.ba2, Fallout4 - Textures4.ba2, Fallout4 - Textures5.ba2, Fallout4 - Textures6.ba2, Fallout4 - Textures7.ba2, Fallout4 - Textures8.ba2, Fallout4 - Textures9.ba2, Fallout4_VR - Main.ba2, Fallout4_VR - Textures.ba2
[VRDisplay]
fRenderTargetSizeMultiplier=1.0
[HairLighting]
fHairPrimSpecPow=2.0
fHairPrimSpecScale=0.01
fHairPrimSpecShift=0.26
fHairSecSpecScale=0.01
fHairSecSpecPow=2.0
fHairSecSpecShift=0.26
[Display]
fTAAPostSharpen=0.675
fTAASharpen=1.0000
fTAAHighFreq=0.8000
fTAALowFreq=0.5000
fTAAPostOverlay=0.675
uPipboyTargetHeight=1400
uPipboyTargetWidth=1752
[VRUI]
iVRUIRenderTargetHeight=4096
iVRUIRenderTargetWidth=4096
[Controls]
fSprintStopDirectionThresholdDegrees=360.0000
[Workshop]
fItemRotationSpeed=0.4
[VR]
fSwimSpeedScalar=1.2500
fVrSwimDragCoefficient=0.0500
fVrSwimHMDFloatThreshold=0.7200
bVrSwimDeliberateResurface=1
```

### 3.2.4 Additional settings <small><sup>[top ▲](#toc)</sup></small>
Above are the settings that I used.
There's many more settings you can tweak.
Here's a bunch of other resources that may be useful for you.

* <sub>![reddit]</sub>
  [INI Tweak Megathread](https://www.reddit.com/r/fo4vr/comments/7kenxb/)
* <sub>![reddit]</sub>
  [Comprehensive modding and tweaking guide for Fallout 4 VR](https://www.reddit.com/r/fo4vr/comments/d55jzy/)



# 4 List of mods<a name="list-of-mods"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!NOTE]
> Make sure you know [what the abbreviations mean](#abbreviations) and understand
> [the relevance of version numbers](#about-version-numbers).

## 4.1 External libraries<a name="external-libraries"></a> <small><sup>[top ▲](#toc)</sup></small>
First of all, here's a few required mods/tools.
These are essentially toolkits that directly alter the game engine, and are required by many other mods.

> [!IMPORTANT]
> These mods should be installed manually.
> They should not be installed with MO2.

> [!IMPORTANT]
> These mods should be installed into `[fo4vr_dir]`, _not_ into `[fo4vr_dir]\Data\`.

1. **[F4SEVR](https://f4se.silverlock.org/)** (v0.6.20) <sub>![required]</sub>  
   This is a framework that allows modders to write custom scripts. Many other mods require this.
   * **Installation instructions:**
     1. Go to [the F4SE website](https://f4se.silverlock.org/), find the "Fallout 4 VR runtime", and click "7z archive".
     2. Use [7-Zip](https://7-zip.org/) to extract the downloaded file into `[fo4vr_dir]`.
     3. If you did this correctly, you should have the file `f4sevr_1_2_72.dll` in the same directory as
        `Fallout4VR.exe`.
        If this is not the case, you probably created the directory `[fo4vr_dir]\f4sevr_0_6_20\`, and you should copy
        the contents of that directory into `[fo4vr_dir]`.
2. **[fo4vr_improvements](https://github.com/fholger/f4ovr_improvements)** (vcas_v2) <sub>![required]</sub>  
   Improves some filters and shaders specifically for VR, and fixes issues the game has with some controllers.
   * **Note:**
     Do not install this mod if you use WMR or Vive Wand controllers.
   * **Installation instructions:**
     1. Go to [the mod's releases page](https://github.com/fholger/f4ovr_improvements/releases), and download the file
        `fo4vr_contrast_adaptive_sharpening_v2.7z`.
     2. Use 7-Zip to extract the downloaded file into `[fo4vr_dir]`.
        When prompted, choose to overwrite existing files.
     3. If you did this correctly, you should have the file `fo4_openvr.cfg` in the same directory as `Fallout4VR.exe`.
   * **Note:**
     If you verify the integrity of your game files in Steam, Steam will (partially) overwrite this mod, and you will
     have to re-install this mod.
3. **[vrperfkit](https://github.com/fholger/vrperfkit)** (v0.3) <sub>![required]</sub>  
   Enables upscaling and foveated rendering, which improves performance by a lot.
   * **Installation instructions:**
     1. Go to [the mod's releases page](https://github.com/fholger/vrperfkit/releases), and download the file
        `vrperfkit_v0.3.zip`.
     2. Extract the downloaded file into `[fo4vr_dir]`.
        When prompted, choose to overwrite existing files.
     3. If you did this correctly, you should have the file `vrperfkit.yml` in the same directory as `Fallout4VR.exe`.
     4. After installing, find the file `vrperfkit.yml`, open it with Notepad, and change `method: cat` to
        `method: fsr`.
        * Otherwise (at least on my machine), the game looks fine on my monitor, but inside my VR headset the screen is
          black.
   * **Note:**
     If you verify the integrity of your game files in Steam, Steam will (partially) overwrite this mod, and you will
     have to re-install this mod.
   * **Untested alternative:** [Fallout4 Upscaler VR](https://www.nexusmods.com/fallout4/mods/73715)
4. **[xSE PluginPreloader F4](https://www.nexusmods.com/fallout4/mods/33946)** (v0.2.5.1) <sub>![required]</sub>  
   Will pre-load F4SEVR scripts before loading a save.
   * **Installation instructions:**
     1. Go to the [NexusMods page](https://www.nexusmods.com/fallout4/mods/33946).
     2. Go to "Files", click "Manual download", and again click "Download".
     3. Extract the downloaded file into `[fo4vr_dir]`.
     4. If you did this correctly, you should have the file `IpHlpAPI.dll` in the same directory as `Fallout4VR.exe`.
5. **[Binaural 3D Surround Sound for Headphones - HRTF](https://www.nexusmods.com/fallout4/mods/39692)** (v2.4) <sub>![recommended]</sub>  
   Adds binaural sound, allowing you to more accurately pinpoint the source of a sound by the sound alone.
   The difference is quite subtle, and people who often play headphones may not even notice the difference, but this might give FO4VR's sound that extra bit of realism that makes the difference for you.
   * **Installation instructions:**
     1. Go to the [NexusMods page](https://www.nexusmods.com/fallout4/mods/39692).
     2. Go to "Files", click "Manual download" at the main file, and again click "Download".
     3. Extract the downloaded file into `[fo4vr_dir]`.
     4. If you did this correctly, you should have the file `x3daudio1_7.dll` in the same directory as `Fallout4VR.exe`.

> [!NOTE]
> From now on, all listed mods should be downloaded and installed through MO2.

## 4.2 Libraries<a name="libraries"></a> <small><sup>[top ▲](#toc)</sup></small>
These mods provide utilities used in other mods.
These do not affect your game directly, but are required by many other mods.

1. **[Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327)** (v1.10.163.0) <sub>![required]</sub>
2. **[VR Address Library for F4SEVR](https://www.nexusmods.com/fallout4/mods/64879)** (v1.6.1) <sub>![required]</sub>
3. **[Fallout4 VR Tools](https://www.nexusmods.com/fallout4/mods/45167)** (v0.1) <sub>![required]</sub>

## 4.3 Stability and Patches<a name="stability-and-patches"></a> <small><sup>[top ▲](#toc)</sup></small>
These mods fix bugs, either in the base game or in other mods.

1. **[Fallout 4 Version Check Patcher](https://www.nexusmods.com/fallout4/mods/42497)** (v1.00) <sub>![required]</sub>  
   [As explained in the introduction](#about-modding-fo4vr), most mods will be created for the wrong game version.
   The game warns you of this in the main menu.
   This mod disables those warnings, because they're annoying and there's not a whole lot you can do about it anyway.
2. **[Unofficial Fallout 4 Patch - UFO4P](https://www.nexusmods.com/fallout4/mods/4598)** (v2.1.5) <sub>![required]</sub>  
   Fixes a bunch of bugs, big and small, in the base game.
   Though there are some incompatibilities because VR is not supported by the mod authors (like with most other mods on
   this list), overall the pros outweigh the cons.
   * **Requires:** all DLC
   * **Patch:** [Unofficial Fallout 4 VR Fix](https://www.nexusmods.com/fallout4/mods/47117) (v1)
   * **Patch:** [VR weapon and armor keyword crash patch](https://www.nexusmods.com/fallout4/mods/79711) (v2.1.5-1.0.3)
3. **[DLCVR - Fallout 4 VR and DLC standalone bug fixes](https://www.nexusmods.com/fallout4/mods/28842)** (v1.0.4) <sub>![required]</sub>  
   Fixes issues specific to FO4FH and FO4NW, relating to invisible floors and so on.
   * **Requires:** FO4FH _or_ FO4NW
   * **Variant:** depends on your DLC
4. **[Edmond's Automatron VR Workbench Rebuild](https://www.nexusmods.com/fallout4/mods/55692)** (v1.0) <sub>![required]</sub>  
   Re-implements parts of FO4AU that did not work in VR. Some parts of FO4AU are still broken even with this mod.
   * **Requires:** FO4AU _and_ FO4NW
   * **Variant:** "No wild edits"
5. **[Buffout 4](https://www.nexusmods.com/fallout4/mods/47359)** (v1.28.6) <sub>![required]</sub>  
   Fixes engine bugs and adds a crash logger.
6. **[Buffout 4 NG with PDB support](https://www.nexusmods.com/fallout4/mods/64880)** (v1.13.1) <sub>![required]</sub>  
   Same as above, but for VR.
7. **[Multiple Floors Sandboxing](https://www.nexusmods.com/fallout4/mods/15608)** (v1.0) <sub>![required]</sub>  
   In locations with multiple storeys, NPCs walk only on the ground storey.
   This mod fixes that behaviour so NPCs walk on all storeys.
8. **[No Aggro Impact Landing (Power Armor)](https://www.nexusmods.com/fallout4/mods/9019)** (v1.0) <sub>![required]</sub>  
   If you wear power armour and fall from a height, you will create a shock wave that damages NPCs around you.
   Friendly NPCs damaged this way may become hostile, even if you do so by accident.
   This mod ensures that you do not accidentally turn friendly NPCs hostile this way.
9. **[Bird Fix](https://www.nexusmods.com/fallout4/mods/45429)** (v1) <sub>![required]</sub>  
   Fixes a bug where birds are _always_ flying into buildings for some reason.
   * **Note:** You can ignore the listed dependencies.
10. **[Radio Reverb Fix](https://www.nexusmods.com/fallout4/mods/16563)** (v1) <sub>![optional]</sub>  
    Applies reverb to your radio when applicable.
    * **Variant:** "Subtle" _or_ main file

## 4.4 Performance<a name="performance"></a> <small><sup>[top ▲](#toc)</sup></small>
FO4VR is notorious for having sub-par performance.
The following mods help improve performance.
If you notice after some playing that you have high FPS, you can consider disabling these for (arguably) more
surrounding more detail around you.

Personally, I eventually disabled these because I preferred higher graphical quality, but they may be useful for you.

1. **[Insignificant Object Remover](https://www.nexusmods.com/fallout4/mods/9835)** (v1.0) <sub>![recommended]</sub>
   * **Installer:** "Full"
2. **[FAR - Faraway Area Reform](https://www.nexusmods.com/fallout4/mods/20713)** (v1.2) <sub>![recommended]</sub>
   * **Variant:** "Default Resolution"

## 4.5 Graphics<a name="graphics"></a> <small><sup>[top ▲](#toc)</sup></small>
1. **[Burst Impact Blast FX](https://www.nexusmods.com/fallout4/mods/57789)** (v9.51 + v0.952) <sub>![recommended]</sub>
   * **Requires:** FO4AU _and_ FO4FH _and_ FO4NW
   * **Variant:** main file _and_ "BIB-FX Fixed Bloatfly's too-large effect"
   * **Installer:**
     Choose whatever.
     If you're lazy, just spam "Next".
2. **[Visible Galaxy 4k and Framework](https://www.nexusmods.com/fallout4/mods/19127)** (v1.0) <sub>![required]</sub>
   * **Variant:** "Visible Galaxy"
   * **Note:** Required only because it's required by the mod below.
3. **[Fallout 4 HD Overhaul 2k](https://www.nexusmods.com/fallout4/mods/65720)** (v1.0 / v1.01) <sub>![required]</sub>  
   FO4VR's default textures are too ugly for VR, and the high-resolution texture pack is (supposedly) too
   VRAM-consuming.
   This texture pack provides a nice balance.
   * **Variant:** All files in section "Main files"
   * **Note:** You can safely download files for which you do not own the required DLC
4. **[Vivid Fallout - All in One](https://www.nexusmods.com/fallout4/mods/25714)** (v1.9) <sub>![recommended]</sub>  
   Adds even nicer textures, but may have some performance impact.
   * **Variant:** "Best choice"
5. **[Water Enhanced](https://www.nexusmods.com/fallout4/mods/3281)** (v1) <sub>![recommended]</sub>  
   Improves water textures.
   * **Variant:** "2K Water"
6. **[Detailed Feral Ghouls](https://www.nexusmods.com/fallout4/mods/20555)** (v3.1) <sub>![recommended]</sub>
   * **Variant:** "Better Performance - Non ESP Version"
7. **[Classic Ghouls Redux](https://www.nexusmods.com/fallout4/mods/57362)** (v1) <sub>![optional]</sub>  
   Changes (non-feral) ghoul textures to look more like ghouls from Fallout 3.
   * **Patch:** [UFO4P and LotC patch](https://www.nexusmods.com/fallout4/mods/79713) (v1-1.0.4)

## 4.6 Lighting<a name="lighting"></a> <small><sup>[top ▲](#toc)</sup></small>
By default, the world looks _really_ overexposed, which makes the outside like outright ugly.
I used a combination of mods recommended by [dropadred](https://www.reddit.com/user/dropadred/), as
[described in this thread](https://www.reddit.com/r/fo4vr/comments/r8rrsm/).

1. **[Darker Nights](https://www.nexusmods.com/fallout4/mods/191)** (v1.11p6) <sub>![recommended]</sub>
   * **Variant:** main file _and_ "No Glow Fix for Far Harbor DLC"
   * **Installer:**
     1. _Darkness level:_ Darkest
     2. _Misc:_ None
     3. _Merged DLC patches:_ depends on your DLC
     4. _Merged overhaul patches:_ None
     5. _Standalone patches:_ None
     6. _Detection:_ Automatic
     7. _Night vision:_ Vanilla
2. **[PhyLight](https://www.nexusmods.com/fallout4/mods/25740)** (v1.1) <sub>![required]</sub>
   * **Variant:** "PhyDark (164)" _and_ "No Interior Dust or Fog"
3. **[Vanilla Eye Adaptation Fix - All DLC](https://www.nexusmods.com/fallout4/mods/52129)** (v1.1) <sub>![required]</sub>
   * **Requires:** all DLC
   * **Variant:** version 1.1
4. **[Fr4nsson's Light Tweaks](https://www.nexusmods.com/fallout4/mods/2139)** (v1.6) <sub>![required]</sub>
   * **Variant:** "plus Bloom Remover"
5. **[Interiors Enhanced - Darker Ambient Light and Fog](https://www.nexusmods.com/fallout4/mods/8768)** (v2.0) <sub>![required]</sub>
   * **Variant:** depends on your DLC

## 4.7 Sound<a name="sound"></a> <small><sup>[top ▲](#toc)</sup></small>
The sound is actually fine in VR.
However, it doesn't hurt to improve sound effects for VR, and to add more high-quality music. 

1. **[Faded Glory - A Post-Apocalyptic Soundscape](https://www.nexusmods.com/fallout4/mods/26014)** (v5-1) <sub>![optional]</sub>
2. **[Fallout Suite - Soundtrack Extension](https://www.nexusmods.com/fallout4/mods/15870)** (v1.1) <sub>![optional]</sub>
3. **[Bleak Beauty - A Fallout 4 Fan Made OST](https://www.nexusmods.com/fallout4/mods/9663)** (v1.2) <sub>![optional]</sub>
4. **[Musical Lore - Wasteland Edition (Soundtrack Mod By Nir Shor)](https://www.nexusmods.com/fallout4/mods/14531)** (v1.6) <sub>![optional]</sub>  
   Adds new high-quality songs to the game's radio.
5. **[Ambient Wasteland - Fallout 4 Edition](https://www.nexusmods.com/fallout4/mods/25343)** (v0.1) <sub>![recommended]</sub>  
   Adds a whole bunch of ambient, distant background sounds to make the world feel more lively.
   * **Patch:** [Realistic Reverb and Ambience Overhaul - VR and FP](https://www.nexusmods.com/fallout4/mods/61140) (v6)
6. **[Project Reality Footsteps FO4](https://www.nexusmods.com/fallout4/mods/35904)** (v1.7) <sub>![recommended]</sub>  
   Adds more different kinds of footstep sounds.
   * **Variant:** "BA2"
7. **[Not Great Not Terrible - Scarier Geiger Counter Sounds](https://www.nexusmods.com/fallout4/mods/45354)** (v1.0) <sub>![optional]</sub>  
   Replaces Geiger counter sounds to be more intense.
   * **Variant:** "Quieter Version" _or_ "Main File"

## 4.8 UI<a name="ui"></a> <small><sup>[top ▲](#toc)</sup></small>
The UI in VR is unintuitive to navigate, and the key bindings shown in the UI are usually incorrect.
Unfortunately, there are currently no good UI mods for VR.
[FallUI](https://www.nexusmods.com/fallout4/mods/48758) (v2.2.1) sort of works, but suffers from a variety of bugs in
VR, like bad contrast between text and background, menus being too small, and some VR-only menus not being replaced at
all.
[MCM](https://www.nexusmods.com/fallout4/mods/21497) (v1.39) also doesn't work; mods that use MCM are fine, but you
can't configure them through MCM.
What we're left with is a single UI mod, which actually works fine.

1. **[Full Dialog VR](https://www.nexusmods.com/fallout4/mods/28516/)** (v1.1) <sub>![recommended]</sub>
   In conversations, you usually have four response options.
   The game summarises these using keywords.
   This is annoying, because your character may say something completely different from what you expected.
   This mod replaces the keywords with the full line your character will say.
   * **Patch:**
     After installing, right-click the mod, click "Open in Explorer", enter the directory `interface`, and delete the
     file `MultiActivateMenu.swf`.
     This fixes a VR-specific bug where no icons are shown when talking with followers.

## 4.9 Gameplay<a name="gameplay"></a> <small><sup>[top ▲](#toc)</sup></small>
1. **[FRIK - Full Player Body with IK](https://www.nexusmods.com/fallout4/mods/53464)** (v0.58) <sub>![required]</sub>  
   Allows you to see your hands.
   Absolutely required for immersion.
   * **Variant:** "alpha 58"
   * **Important:** Download this mod, but **keep it deactivated in MO2 for now**.
   * **Note:** [In-game configuration required.](#configure-mods)
   * **Untested alternative:** [Idle Hands](https://www.nexusmods.com/fallout4/mods/42922)
2. **[Player Collision Options - nocollide actors](https://www.nexusmods.com/fallout4/mods/41866)** (v1.0) <sub>![required]</sub>  
   Normally, when you get close to an NPC in VR, the game will push you back. This is annoying and disorienting when you
   want to roleplay or pet your dog.
   This disables collisions between you and NPCs.
   * **Variant:** "nocollide actors"
3. **[Realistic Death Physics - No Animations](https://www.nexusmods.com/fallout4/mods/4371)** (v1.2) <sub>![recommended]</sub>
   * **Variant:** "Vanilla Animations" (even if you have DLC)
4. **[PipBoy VR light](https://www.nexusmods.com/fallout4/mods/29245)** (v1.1) <sub>![recommended]</sub>  
   In VR, the default Pip-Boy light (the "flashlight") is just a weak glow around you.
   I really liked the flashlight in Half-Life: Alyx.
   This mod changes the shape of the Pip-Boy's light to be like a flashlight, and does so with no performance overhead.
   I personally chose the small light because I want it to be scary, but you can choose any variant you want.
   * **Variant:** main file _and_ one optional file.
     (I chose "Gun style aimed Small Gobo".)
5. **[Everyone's Best Friend](https://www.nexusmods.com/fallout4/mods/13459)** (v3.0.0) <sub>![recommended]</sub>  
   Normally you can only have one follower, but Dogmeat really isn't comparable to the depth of the other companions.
   But Dogmeat is also really cute.
   This mods lets you have both Dogmeat and any other companion at the same time.
   * **Patch:** [EBF UFO4P compatibility fix](https://www.nexusmods.com/fallout4/mods/43409) (v2.1.0)
6. **[Splinterz - Breakable Wooden Doors](https://www.nexusmods.com/fallout4/mods/21521)** (v1.3) <sub>![optional]</sub>  
   Allows you to break doors.
   Pretty cool.
   * **Variant:** depends on your DLC

## 4.10 Combat<a name="combat"></a> <small><sup>[top ▲](#toc)</sup></small>
Combat in VR is a mixed experience.
Many parts are fine, but a few important parts are very, very wrong.
The following selection of mods is a combination of important fixes and subjective rebalancing.

1. **[See-Through-Scopes](https://www.nexusmods.com/fallout4/mods/9476)** (v2.5.3) <sub>![required]</sub>  
   Changes in-game scopes so they are see-through.
   Required for the next mod.
   * **Installer:**
     1. _Add or replace:_ Replace
     2. _DLC:_ depends on your DLC (if you have both, also choose "Install and merge both DLCs")
     3. _Add-ons:_ None
     4. _Tweaks:_ None
     5. Do not choose any patches
2. **[Better Scopes VR](https://www.nexusmods.com/fallout4/mods/61214)** (v0.9) <sub>![required]</sub>  
   This one is _absolutely_ required.
   Without this mod, when you look down a scope, your screen turns black and you get a full-screen 2D projection of what
   you can see through your scope.
   Absolutely horrible and nauseating.
   This mod removes that screen, and just lets you look through the actual scope.
   * **Variant:** main file only, not the optional file.
3. **[Bullet Time VATS VR](https://www.nexusmods.com/fallout4/mods/72502)** (vb1.1) <sub>![required]</sub>  
   In vanilla, VATS is a gameplay mechanic that pauses combat and lets you select body parts to target, which you will
   then automatically shoot at.
   This sucks in VR, because you don't get to aim the gun and pull the trigger yourself.
   This mod replaces VATS with bullet time.
   * **Requires:** FO4FH _and_ FO4NW
   * **Note:** [In-game configuration required.](#configure-mods)
4. **[Critical Hits Outside of VATS](https://www.nexusmods.com/fallout4/mods/12653)** (v1.1.3) <sub>![required]</sub>  
   The above Bullet Time mod internally works by disabling VATS, and thus (almost) completely removes critical hits from the game.
   This mod makes it so all hits have a small chance of being a critical hit, even outside of bullet time.
5. **[Weapon Accuracy Redone for VR](https://www.nexusmods.com/fallout4/mods/40669)** (v1.0) <sub>![required]</sub>  
   In VR it's super annoying if you're clearly aiming at an enemy and then the game decides the shot didn't hit because
   of some random die roll.
   This mod reduces weapon spread and recoil to make accuracy in VR more rewarding.
   * **Variant:** depends on your DLC
6. **[Better Low Health](https://www.nexusmods.com/fallout4/mods/6018)** (v1.0) <sub>![recommended]</sub>  
   Your health bar is visible on the inside of your wrist, but that's also where you're holding your gun, so during
   combat you typically don't really know how much health you have left.
   The game shows some visual effects at 20% health left, but that's usually too late.
   This mod increases that threshold to 50%.
   * **Variant:** "50"
7. **[More Noticeable Hit Effect](https://www.nexusmods.com/fallout4/mods/6157)** (v1.0) <sub>![recommended]</sub>  
   I noticed that during fights I usually had no idea if bullets were flying past me or into me.
   This mod makes it much more noticeable when you are being hit.
   * **Variant:** "aMedium"

## 4.11 Difficulty / Survival<a name="difficulty-survival"></a> <small><sup>[top ▲](#toc)</sup></small>
Fallout 4 is not a difficult game, even at higher difficulties.
In VR, it only gets easier.
Mods in this category affect the difficulty.
Some (but not all) of them assume you play in Survival mode, which I recommend you do anyway.

1. **[Survival Options](https://www.nexusmods.com/fallout4/mods/14650)** (v1.7.1) <sub>![recommended]</sub>  
   Allows you to customise your survival mode experience.
   Lets you re-enable manual saves, configure automatic saves, and change damage multipliers.
   * Recommended even for non-survival playthroughs!
   * **Installer:** everything
   * **Note:** [In-game configuration required.](#configure-mods)
3. **[Settlement Fast Travel Survival Mod](https://www.nexusmods.com/fallout4/mods/58708)** (v1.05) <sub>![recommended]</sub>  
   Re-enables a restricted form of fast travel.
   You can use this together with the above mod.
   * **Requires:** FO4AU _and_ FO4FH _and_ FO4VW _and_ FO4NW
4. **[Campsite](https://www.nexusmods.com/fallout4/mods/11734)** (v1.0.4) <sub>![recommended]</sub>  
   Lets you bring a tent with you so you can sleep anywhere.
   * **Note:** [In-game configuration required.](#configure-mods)
5. **[Loot Logic and Reduction With optional Harvest Restrictions](https://www.nexusmods.com/fallout4/mods/21366)** (v1.5.3.1) <sub>![recommended]</sub>  
   Reduces loot found in containers.
   Otherwise you'll quickly find you'll have so much ammo and chems the game just totally isn't challenging anymore.
6. **[NPC Loot Drop rebalance](https://www.nexusmods.com/fallout4/mods/24163)** (v1.0) <sub>![recommended]</sub>  
   Reduces loot found on NPCs, in line with the above mod.
7. **[Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/29447)** (v1.5.4) <sub>![recommended]</sub>  
   In survival, you have less carrying capacity and heavier items. These backpacks will come in use.
   * **Requires:** FO4AU _and_ FO4FH _and_ FO4NW
   * **Variant:** "1.5.4"
   * **Installer:** "Scripted Level List Inject"
   * **Patch:** [Dirty Edit Patch](https://www.nexusmods.com/fallout4/mods/79705) (v1.5.4-1.0.2)
   * **Note:** [In-game configuration required.](#configure-mods)
8. **[Dogmeat's Backpack](https://www.nexusmods.com/fallout4/mods/10111)** (v2.0) <sub>![recommended]</sub>  
   As above, but now for your companion.
9. **[Dogmeat's Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/62037)** (v1.3) <sub>![recommended]</sub>  
   Re-balances the above mod to be in line with the one above that.
   * **Requires:** The two mods above this one.
9. **[Headshot Damage Multiplier](https://www.nexusmods.com/fallout4/mods/33546)** (v1.0) <sub>![recommended]</sub>
   In survival, your outgoing damage is reduced and enemy health is increased.
   Unfortunately, this results in bullet sponge enemies, where you can unload an entire shotgun magazine into someone's
   face and they somehow survive.
   In VR, your accuracy is much higher, so I found that combat became more interesting if I rewarded myself for making
   headshots.
   The result is a sort of mutual [glass cannon](https://tvtropes.org/pmwiki/pmwiki.php/Main/GlassCannon) situation,
   where every shot matters.
   * **Variant:** "x5"
10. **[Radiation Overhaul - 4x More Radiation Across the Wasteland](https://www.nexusmods.com/fallout4/mods/13790)** (v1.1) <sub>![optional]</sub>  
    Makes radiation actually dangerous.
    * **Variant:** depends on your DLC
    * **Patch:** [UFO4P and item name patch](https://www.nexusmods.com/fallout4/mods/79708) (v1.1-1.0.3)

## 4.12 Settlements<a name="settlements"></a> <small><sup>[top ▲](#toc)</sup></small>
I think Fallout 4's settlements are very flawed.
In VR, they are not necessarily _more_ flawed, so the mods in this section aren't VR-specific.
However, several of these mods require VR-specific tweaks.
That said, this entire section is recommended, because the VR experience is no worse than the non-VR experience with or
without these.
If you don't intend to engage with settlements at all, you can skip this section.

> [!CAUTION]
> If you install Sim Settlements, you **must** choose version 4.1.7.
> Newer versions do not work.

1. **[Sim Settlements](https://www.nexusmods.com/fallout4/mods/21872)** (v4.1.7) <sub>![recommended]</sub>  
   Completely changes the way settlements are built.
   Instead of you building everything, settlers will build and upgrade their own houses in designated locations.
   I especially like the "leaders" feature, where you can appoint a settlement leader who will oversee the placement of
   all buildings in the settlement.
   It just works.
   * **Variant:** "Three In One **v4.1.7**"
   * **Note:** [In-game configuration required.](#configure-mods)
   * **Untested alternative:** [Sim Settlements 2](https://www.nexusmods.com/fallout4/mods/47976)  
     There are guides out there on how to get Sim Settlements 2 working on FO4VR, but these have not been tested with
     this guide.
     I recommend you err on the side of caution and avoid Sim Settlements 2.
2. **[Leaders Of The Commonwealth](https://www.nexusmods.com/fallout4/mods/30495)** (v2) <sub>![recommended]</sub>  
   With basic Sim Settlements, only your followers are leaders.
   Especially at the start of the game, it's frustrating if your settlements can't grow because you don't have enough
   leaders for the number of settlements you find.
   This mod designates several unique settlers from the base game as leaders.
   * **Variant:** "Vanilla Looks No New npcs".
3. **[Salvage Beacons](https://www.nexusmods.com/fallout4/mods/18757)** (v1.0.4) <sub>![optional]</sub>  
   Carrying junk back to your settlement is frankly a waste of time.
   This lets you drop off your junk and whatnot in any container, then mark that container, and your settlers will take
   back your loot to your settlement.
4. **[IDEK's Logistics Station 2](https://www.nexusmods.com/fallout4/mods/48389)** (v2.1.3) <sub>![recommended]</sub>  
   I wasn't sure whether to make this recommended or required.
   In Fallout 4, you can connect your settlements using supply routes, which allows the settlements to share resources.
   Unfortunately, this feature is super annoying to use, hard to get right, and hard to manage.
   This mod automates most of that part:
   You just build one station per settlement, assign a settler, and the mod will handle all the rest.
   There's also a bunch of other really useful features which improve the stability of your trading routes.
   * **Installer:**
     1. Install type: FO4VR
     2. Sim Settlements 1: "Sim Settlements"
     3. Sim Settlements 2: Do not select
   * **Note:** [In-game configuration recommended.](#configure-mods)
5. **[Local Leader Tweaks](https://www.nexusmods.com/fallout4/mods/16661)** (v1.0) <sub>![recommended]</sub>  
   The Local Leader perk is required to unlock some of the most important parts of using settlements.
   I think that it's stupid that these perks, which cost quite some effort to unlock if you don't run a Charisma build,
   don't justify their worth in terms of gameplay impact, but are still vital for using settlements.
   For this reason, I recommend using this mod, which will allow you to do basically everything you can do with Local
   Leader, except you won't need Local Leader.
   * **Variant:** main file _and_ "Crafting add-on"


# 5 Playing the game<a name="playing-the-game"></a> <small><sup>[top ▲](#toc)</sup></small> 
> [!CAUTION]
> Make sure [FRIK](https://www.nexusmods.com/fallout4/mods/53464) remains disabled until you have exited the vault.

> [!WARNING]
> On the right-hand side of MO2, under the tab "Plugins", check that 
> Check that all `.esp` files are actually activated.
> Additionally, sort your load order one more time, just to be sure.

> [!NOTE]
> In MO2, in the list of plugins, some mods will be crossed out (with ~~strikethrough~~).
> This is just MO2's weird way of informing you that it's a textures-only mod.
> Ignore the strikethrough, but keep the mod enabled.

You should now have a good selection of mods from the previous selection installed.
You should have installed all required mods, probably several recommended mods, and maybe some optional mods.

Next up is to learn about a few quirks of FO4VR you need to be aware of during playing.
After that, you can start playing the prologue.
Finally, you'll need to configure a few final mods.
This section will take you through the entire process.

## 5.1 General tips<a href="general-tips"></a> <small><sup>[top ▲](#toc)</sup></small>
### 5.1.1 Launching <small><sup>[top ▲](#toc)</sup></small>
* Always launch F4SEVR, and always launch through MO2.
  Do not launch through Steam.
  Otherwise, your mods will not load.

  The following steps will tell MO2 how to launch F4SEVR.
  1. In MO2, in the main menu, click "Tools" and then "Executables",
  2. in the list on the left, select "Fallout 4 VR",
  3. above the list on the left, click the plus icon, and choose "Clone selected",
  4. on the right, change "Title" to "F4SEVR",
  5. on the right, in "Binary", replace `Fallout4VR.exe` with `f4sevr_loader.exe`, and
  6. in the bottom-right, click "OK" to close the dialog,

  To launch F4SEVR (and thus the game) from MO2, click the dropdown menu with "Fallout 4 VR" and select "F4SEVR".
  Then simply press "Run".
* Unplug any controllers/gamepads you don't want to use before launching the game.
  FO4(VR) does not support multiple controllers at the same time, and gets confused when you try.
* Start your VR controllers before launching the game.
  Otherwise, the game won't respond to some buttons, and you'll have to restart.
* In the main menu, if you choose "Continue" and nothing happens, just press the selection button again.
  This is necessary because the game is trying to show you a warning that you've removed a mod that the save relies on,
  but for some reason this warning is invisible in the main menu (but works correctly after loading another save).

### 5.1.2 Playing <small><sup>[top ▲](#toc)</sup></small>
* Quicksaves are unreliable and are sometimes broken.
  Autosaves are slightly better, but I still wouldn't rely on them.
  Save manually and save often.
  As covered by this guide, I recommend that you install
  [Survival Options](https://www.nexusmods.com/fallout4/mods/14650) and [configure the mod](#configure-mods) to
  automatically create manual saves.
* Do not open your Pip-Boy while your flashlight is on.
  Doing so may cause the game to crash.
* Swimming sucks ass in VR;
  you have to stick out your arms in front of you, hold both triggers, and pull your arms towards you, releasing the
  triggers while your arms are still moving.
  Unlike in Skyrim VR, you cannot disable this.

## 5.2 Configure controls<a name="configure-controls"></a> <small><sup>[top ▲](#toc)</sup></small>
This section applies to Valve Index controllers only.

With the game running, with your headset on, open the SteamVR overlay.
Select "Controller bindings", select "Choose another", and select "Fallout VR Essential Bindings".
Unfortunately, even after configuring your controls, button prompts in the game will not show correctly.
You'll have to learn the buttons by heart.
This is mostly a case of trial and error.

## 5.3 Completing the prologue<a name="complete-prologue"></a> <small><sup>[top ▲](#toc)</sup></small>
You can complete the prologue normally, though the experience can be somewhat buggy.
Here's a small list of troubleshooting tips.

* If your gun aim is completely wrong, just use the baton for now.
  Aiming will be better once you've activated [FRIK](https://www.nexusmods.com/fallout4/mods/53464) after the prologue.
* If the game keeps crashing while leaving the vault using the elevator, temporarily disable UFO4P.
  You should re-enable UFO4P after having left the vault.
* If this all sounds too bothersome, use [SKK Fast Start new game](https://www.nexusmods.com/fallout4/mods/29227)
  (v020).

## 5.4 Configure mods<a name="configure-mods"></a> <small><sup>[top ▲](#toc)</sup></small>
After you've exited the vault, there's a few mods you should configure.

### 5.4.1 Backpacks of the Commonwealth <small><sup>[top ▲](#toc)</sup></small>
As soon as you exit Vault 111, you'll receive a magazine from Backpacks of the Commonwealth.
After that, you'll also be prompted to enter the spawn rate.
Enter the recommended rate of 0%.

### 5.4.2 Survival Options <small><sup>[top ▲](#toc)</sup></small>
The following settings apply to both survival playthroughs and non-survival playthroughs.

Open your inventory, go to Misc, and use the holotape "\[Settings\] Survival Options Holotape".
Apply the following settings.

| Category                                | Option                     | Value               |
|-----------------------------------------|----------------------------|---------------------|
| Combat Options                          | Incoming Damage Multiplier | 3.0                 |
|                                         | Outgoing Damage Multiplier | 1.0                 |
| Save Options > Cell Change Save Options | Toggle                     | Current:On          |
|                                         | Change To                  | Current:Normal Save |
| Save Options > Timed Save Options       | Toggle                     | Current:On          |
|                                         | Change To                  | Current:Normal Save |
|                                         | Interval                   | 7 Minutes           |
| Save Options > Level Up Save Options    | Toggle                     | Current:On          |
|                                         | Change To                  | Current:Normal Save |

Finally, if you are doing a survival playthrough, in the same holotape, under the "Save Options" menu, select "Give Save
Item".
This will add a "Save Item" to your inventory, to be found under Aid.
Favourite the item and put it on your favourite wheel so you can save whenever you want.

### 5.4.3 Bullet Time VATS VR <small><sup>[top ▲](#toc)</sup></small>
Open your inventory, go to Misc, and use the holotape "\[Settings - Bullet Time VATS\]".
Apply the following settings.

| Option                                                 | Value       |
|--------------------------------------------------------|-------------|
| Time Dilation                                          | 50%         |
| Movement Settings Menu > "In Bullet Time V.A.T.S." use | DIRECT MOVE |

### 5.4.4 FRIK <small><sup>[top ▲](#toc)</sup></small>
> [!WARNING]
> Make sure [FRIK](https://www.nexusmods.com/fallout4/mods/53464) remains disabled until you have exited the vault.

Save the game (using the "Save Item" you added using [Survival Options](https://www.nexusmods.com/fallout4/mods/14650)),
exit the game, enable FRIK (and re-enable UFO4P while you're at it, if you disabled it), re-sort your mods with LOOT,
and then re-launch the game.

Open your inventory, go to Misc, and use the holotape "FRIK Configuration".
Apply the following settings.
You will need to re-open the holotape several times.

1. Stand up straight, relaxed, hands by your side.
   Select "CALIBRATE".
2. Select "Toggle Arms Only Mode!".
3. Select "Save Body Position to INI".
   (This also saves your "arms only" setting.)

### 5.4.5 Campsite <small><sup>[top ▲](#toc)</sup></small>
To activate [Campsite](https://www.nexusmods.com/fallout4/mods/11734), you'll need to find a book
[somewhere in Sanctuary](https://youtu.be/E7VLBtH4gyA).
Once you've found the book, you'll be able to craft camping items at any chemistry workbench.

### 5.4.6 Sim Settlements<a href="configure-sim-settlements"></a> <small><sup>[top ▲](#toc)</sup></small>
[Sim Settlements](https://www.nexusmods.com/fallout4/mods/21872) can only be configured after you've played the game 
a bit.
Specifically, you'll need to reach the [Museum of Freedom](https://fallout.fandom.com/wiki/Museum_of_Freedom), which is
one of the earlier storyline locations anyway.
Inside, [you can find the Sim Settlements holotape](https://youtu.be/WQB6FQezJgE).

After having picked up the holotape, open your inventory, go to Misc, and use the holotape "City Manager 2078 Holotape".
Answer the questions to configure Sim Settlements.
(If the prompt becomes invisible, just skip through it.
The actions below will override those choices.)

After having answered these questions, use the holotape again, and select the following options.
1. ASAM Sensor Info
2. Tools > Configuration Tools > Configuration Wizard
3. Tools > Configuration Tools > Performance Wizard

#### How to create a settlement
1. Build a City Planner's Desk (found under "Crafting").
2. Select the City Plan blueprint on top of the City Planner's Desk and assign a leader.
   If no leaders are available, you'll have to continue playing the game until you find more.
   All followers can be leaders,
   [in addition to all NPCs listed in this mod](https://www.nexusmods.com/fallout4/mods/30495).
3. After assigning a leader, a cutscene starts during which your camera will fly around the settlement.
   All items in the settlement will be scrapped, and a new foundation will be built.
   Wait until the camera stops flying around.
4. Build a Logistics Desk (found under "Special").
5. Wait until you have at least three settlers in that settlement.
   (Otherwise your leader will override your assignment in the next step.)
6. Assign a settler to the Logistics Desk.
7. Build a Logistics Locker (found under "Special" after
   [configuring IDEK's Logistics Station 2](#configure-ideks-logistics-station-2)).

Optionally, using the City Planner's Desk (aim to the left of the City Plan blueprint), craft a Packed City Planner's
Desk (found under "Tools") and, using a Chemistry Station, craft a Packed Logistics Desk (found under "Utility"), so you
can quickly set up new settlements whenever you find one.

> [!NOTE]
> You can disable or skip the cutscene that plays when the settlement is initialising.
> However, you then run the risk of breaking the script if you leave the settlement before the script is finished.
> If the cutscene makes you nauseous, I recommend simply taking off your headset and checking your monitor when it's
> done.

### 5.4.7 IDEK's Logistics Station 2<a href="configure-ideks-logistics-station-2"></a> <small><sup>[top ▲](#toc)</sup></small>
The essential parts of this mod require zero configuration.
However, if you want to easily move items between settlements, you'll need to tell this mod what your main settlement
is.
(Don't worry, you can always easily and safely choose a new main settlement.)

1. Go to your main settlement.
2. Build a Logistics Desk.
3. Interact with the Logistics Desk.
   (The desk itself, not the terminal on top of it).
4. Select "Set Up Locker".
5. Read the popup message and select "OK".
6. Go to any workbench or container in this settlement, and transfer the Logistics Storage Designator into the storage
   of your settlement.
7. Read the popup message and select "Yes, keep my stuff safe!"
8. In any other settlement(s), build a Logistics Locker (found under "Special").

From now on, to move items between settlements, simply interact with the Logistics Locker.


# 6 Conclusion <small><sup>[top ▲](#toc)</sup></small>
That's it!
I hope this guide was useful for you :-)

If you don't understand something, experience in-game issues, have suggestions, or just need some help,
[check out the Discussions page](https://github.com/FWDekker/fo4vr-modlist/discussions) or
[open an issue](https://github.com/FWDekker/fo4vr-modlist/issues).


  [required]:    https://img.shields.io/badge/required-red?style=flat-square "required"

  [recommended]: https://img.shields.io/badge/recommended-orange?style=flat-square "recommended"

  [optional]:    https://img.shields.io/badge/optional-blue?style=flat-square "optional"

  [reddit]:      https://img.shields.io/badge/-%2300000000?style=flat-square&logo=reddit "Reddit"
