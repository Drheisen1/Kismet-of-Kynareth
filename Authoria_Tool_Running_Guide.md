# Authoria - Requiem Reforged — Tool Running Guide

This guide will walk you through how to run LOD tools for Authoria - Requiem Reforged, in case you modified the list and need to generate LODs again.

The guide covers:
- ParallaxGen
- Grass Cache
- xLODGen
- TexGen
- DynDOLOD

Any other tools not covered here will be handled in separate guides.

---

## Index
- [Preparation](#part-1-preperation)
- [Running ParallaxGen](#part-2-running-parallaxgen)
- [Running Grass Cache](#part-3---running-grass-cache)
- [Running xLODGen](#part-4---running-xlodgen)
- [TexGen and DynDOLOD](#part-5---running-texgen-and-dyndolod)

---

## When do I need to rerun these tools?

- When adding mods that replace vanilla meshes and textures, ParallaxGen will most likely need to be rerun. To verify, check the mod for conflicts—if it is losing conflicts against the ParallaxGen output, then you must rerun ParallaxGen.

**Note:** Rerunning ParallaxGen requires rerunning xLODGen and DynDOLOD as well.

- When adding mods that edit the worldspace in Tamriel, you must check in xEdit. In this case, you will need to rerun ParallaxGen, Grass Cache, xLODGen, and DynDOLOD.

---

## Disclaimer

Running tools for Authoria is very different from the usual process due to the inclusion of Seasons of Skyrim. Expect the full process to take at least two full days.

Approximately 30–40% of the modlist size comes from outputs, totaling around 160 GB, so plan your storage accordingly.

---

## Part 1 Preperation

- You should already have a duplicated profile created, with empty mods for the outputs corresponding to each tool. If you do not have enough space to support multiple outputs, you can delete the contents of the current outputs and replace them.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005429.png)

- Expand the Flat Map Framework Seperator and disable everything inside it.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005437.png)

- Double check the plugin panel on the right side of MO2. The last plugins in the load order should be the Synthesis Outputs.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005810.png)

---

## Part 2 Running ParallaxGen

**Estimated time: 10–15 minutes**

- From the dropdown menu on the right side of MO2, select ParallaxGen and press Run.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010119.png)

- Ensure the settings match the screenshot:
  - The Instance Location should match your Wabbajack installation directory.
  - The Output directory should be the empty mod you created for ParallaxGen output.
  - Then click "Start Patching".

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010334.png)

- When the "Set Mods" popup appears, do not change anything—just press OK.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010820.png)

- Once ParallaxGen completes, another window will appear—press OK.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011136.png)

- Enable your ParallaxGen output mod and refresh MO2. Two new plugins will appear:
  - One at the top
  - One at the bottom

Enable both and move them as low as possible in the load order.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011441.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011528.png)

---

## Part 3 - Running Grass Cache

**Estimated time: 9–15 hours**

- Grass cache should rarely be rerun unless you change or add a major location overhaul or landscape-altering mod.

From the author of No Grass in Objects:

"When do I need to regenerate a cache?

If you change grass mods or grass settings (excluding grass distance, fade range, DynDOLOD mode, or extended grass distance), you must regenerate the cache.

If you add or remove mods that alter locations or landscapes, regenerate either the affected cells or the entire worldspace depending on what is easier."

- Grass cache must be generated 5 times, once for each season.

- To begin, follow this guide from 4:33 to 9:50:
https://www.youtube.com/watch?v=jH7co25_JIo  
In Authoria, "Grass Bounds.esp" is named "Deez Nuts.esp".

- Do not modify GrassControl INI settings except for only-pregenerate-world-spaces if you do not understand them.

- Once GrassControl.ini is configured:
  - Disable "Grass Cache Helper NG"
  - Enable "No Grass In Objects"

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013250.png)

- Disable the following mods to prevent crashes:
  - Auto Parallax
  - Discord Rich Presence
  - TrueHUD (plugin only)
  - Skyrim Souls (note load order)

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013539.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013609.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013641.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014008.png)

- Navigate to MO2 Data tab and locate po3_seasonsofskyrim.ini, then reveal it in explorer.

IMPORTANT: If you added a new worldspace with Seasons support, delete this file and launch the game to regenerate it.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014207.png)

- Open the INI file, set Season Type to 0 (disabled), then save and close.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014319.png)

- Back in MO2, click the jigsaw icon and run "Precache Grass", then confirm.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014715.png)

- After completion (2–3 hours), move the "grass" folder from overwrite to "Authoria - Grass Cache - Default".

- To generate Seasonal Grass Cache, Repeate the same Process above, but change the Season type to the seasons you want to generate in the po3_seasonsofskyrim.ini beforehand, you will also need the [Grass cache renamer](https://www.nexusmods.com/skyrimspecialedition/mods/142343?tab=files) , the process is explained in the images below.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015518.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015715.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015937.png)

- Re-enable all mods and restore original configuration.

---

## Part 4 - Running xLODGen

**Estimated time: 4 hours**

- xLODGen must be run twice:
  - Default worldspaces
  - Seasonal worldspaces

- Enable "xLODGen Resource - SSE Terrain Tamriel"

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020450.png)

- Configure output directory in MO2 settings.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020646.png)

- First run:
  - Select Terrain LOD
  - Select all worldspaces
  - Seasons = Default

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021516.png)

- For seasonal:
  - Use po3_seasonsofskyrim.ini → Valid Worldspaces

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021844.png)

- Second run:
  - Select seasonal worldspaces
  - Seasons = everything except Default

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20022406.png)

---

## Part 5 - Running TexGen and DynDOLOD

Continue following the same structured workflow.
