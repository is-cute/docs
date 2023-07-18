---
label: "CurseForge"
icon: package-dependencies
order: -1
---

# CurseForge

CurseForge is a large mod/plugin repository and launcher used by popular modpacks.

!!!info
This page pertains to *Minecraft: Java Edition*.
!!!

## Windows (CurseForge App)

!!!info
Jump to **[Downloading Modpacks](#downloading-modpacks)** if you already have CurseForge installed.
!!!

### Prerequisities

- [Java Runtime Environment](https://www.java.com/en/download/) or [Liberica JRE](https://bell-sw.com/pages/downloads/)
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) or [Liberica JDK](https://bell-sw.com/pages/downloads/)

### Installing

- Download [CurseForge](https://download.curseforge.com/) and run the installer.

[!button variant="primary" icon="download" text="Standard (Overwolf)" margin="0 8 0 0"](https://download.overwolf.com/install/Download?&PartnerId=4047)
[!button variant="secondary" icon="download" text="Standalone"](https://download.overwolf.com/install/Download?Name=CurseForge&ExtensionId=cfiahnpaolfnlgaihhmobmnjdafknjnjdpdabpcm)

- Launch CurseForge. *If you have Minecraft: Java Edition preinstalled, it should automatically detect your installation.*

!!!info
You can manually set your Minecraft modding folder under ***Settings*** > ***Game Specific*** > ***Add*** > ***Minecraft*** > ***Minecraft (Java Edition).***

By default, CurseForge creates this new folder under your system drive, replacing `<your_name>` with the name of your user folder. *Select **Advanced** if you wish to change this location.*

```bash
C:\Users\<your_name>\curseforge\minecraft
```

!!!

![Installing CurseForge](/static/minecraft/curseforge/windows-installing.gif)

### Downloading Modpacks

Modpacks can be installed by browsing the CurseForge website or using the CurseForge app.

==- Using the CurseForge Website

- Launch the [CurseForge](https://www.curseforge.com/minecraft/modpacks) website for Minecraft modpacks.
- Install modpacks using the **Install** button. *It should automatically launch in CurseForge and begin installation.*

![Downloading mods Using the website](/static/minecraft/curseforge/windows-downloading.gif)

- Alternatively, you can specify a specific or older version of a modpack by clicking on the modpack's details > ***Files***.

![Searching for a specific version](/static/minecraft/curseforge/windows-downloading2.gif)

==- Using the CurseForge App

- In the left sidebar, select ***Minecraft*** > ***Browse Modpacks***. Modpacks can be installed using the ***Install*** button.

![Downloading mods using the app](/static/minecraft/curseforge/windows-downloading3.gif)

- Alternatively, you can specify a specific or older version of a modpack by clicking on the modpack's details > ***Versions***.

![Searching for a specific version](/static/minecraft/curseforge/windows-downloading4.gif)

===

### Downloading Extra Mods

- Download the mod(s) and save them to an accessible directory.
- Locate your Minecraft installation folder. In the CurseForge app, this can be found under ***Minecraft*** > ***My Modpacks***. Find your modpack, then right-click and select ***Open Folder***.

![Locating the modpack folder](/static/minecraft/curseforge/windows-extra.gif)

- Navigate to `mods`, then drag or paste in the downloaded mods.

![Installing extra mods](/static/minecraft/curseforge/windows-extra2.gif)

- Launch the game, or relaunch if it is currently open.

### Adding Profiles

==- CurseForge (Official)
By default, CurseForge will automatically make profiles for your modpacks.

- In the launcher, go to ***Minecraft*** > ***My Modpacks***. Hover your mouse over the modpack you want to launch and press ***Play***.

![Launching modpacks with CurseForge](/static/minecraft/curseforge/windows-profiles.gif)

==- SKLauncher
SKLauncher can automatically create profiles while allowing you to launch from CurseForge. *You only need to set this up once for the launcher to work with any future modpacks.*

- Download the [SKLauncher](https://skmedix.pl/downloads) executable and save it to a directory.
- Locate the Minecraft mod folder created by CurseForge and navigate to `Install`.

!!!info
By default, CurseForge creates this new folder under your system drive, replacing `<your_name>` with the name of your user folder.

```bash
C:\Users\<your_name>\curseforge\minecraft
```

!!!

!!!info
Make sure you've enabled ***File name extensions*** in ***File Explorer*** > ***View*** > ***Show/hide***.

![Enabling file name extensions](/static/minecraft/curseforge/windows-profiles3.gif)
!!!

- Delete or rename the existing `minecraft.exe` file (e.g. renaming to `minecraft.exe.bak`). Drag the SKLauncher executable into the directory and rename it to `minecraft.exe`.

![Inserting SKLauncher](/static/minecraft/curseforge/windows-profiles2.gif)

- SKLauncher should now appear instead when you hit ***Play***.

![Launching modpacks with SKLauncher](/static/minecraft/curseforge/windows-profiles4.gif)

===

### Uninstalling Modpacks

- To uninstall a modpack, open the CurseForge app and head to the left sidebar. Select ***Minecraft*** > ***My Modpacks***. Click on the modpack > ***3 Dots*** > ***Delete Profile***.

![Uninstalling modpacks](/static/minecraft/curseforge/windows-uninstalling.gif)
