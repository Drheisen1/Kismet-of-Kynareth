# Authoria - Requiem Reforged — Tool Running Guide

This guide will walk you through howw to run LOD tools for Authoria - Requiem Reforged, in case you modified the list and need to Generate LODs again.

The guide will go through Running Parallaxgen, Grass Cache, xLodGen, Texgen, and Dyndolod.

Any other tools not covered by this guide will be covered in other simpler guides.

---

## When do i need to rerun these tools?

- When adding things that replace vanilla meshes and textures, most likely parallaxgen will need to be rerun, to make sure, you can check the mod you added for conflicts, if it is losing conflicts with the parallaxgen output, then you ill need to rerun parallaxgen

**Note:** rerunning parallaxgen means that xLodGen and Dyndolod will need to be rerun as well.

- When adding things that Edit the worldspace in tamriel, you wwill have to check in xedit for this, you will need to rerun Parallaxgen, Grasscache, xLodgen, and Dyndolod.

---

## Disclaimer

Running tools for Authoria is very different than the usual process, this is because the list contains Seasons of Skyrim, expect this entire process to take two full days at least to complete.

almost 30-40% of the list's size come from the outputs, they total to aroung 160 GBs, plan accordingly.

---

## Index

- Preperation
- Parallaxgen
- Grass Cache
- xLodGen
- Texgen
- Dyndolod

---

# Part 1) Preperation

- You should already have a duplicated profile created, with empty mods for the outputs that corresponds to each tool, if you dont have the space to support having two outputs, feel free to delete the contents of the current outputs and replace them.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005429.png)

- Expand the Flat map Framework Seperator, and Disable everything inside it,

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005437.png)

- Double check the Plugin Panel on the right side of mo2, the last plugins in the load order should be the Synthesis Outputs.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005810.png)

---

# Part 2) Running Parallaxgen  
**est. time : 10 - 15 mins**

- From the Drop Down menu on the right side of mo2, select Parallaxgen, then hit Run.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010119.png)

- Make sure The settings Match the Following Screenshot  
- The Instance Location (2) should match your Wabbajack Installation Directory.  
- for The Output directory (3), select the empty mod you created for the Parallaxgen output, Then hit "Start Patching"

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010334.png)

- After sometime a pop up window will appear titled "set mods", dont change anything and press "Okay"

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010820.png)

- a new window will popup Once parallaxgen Completes, Press "OK".

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011136.png)

- Enable your PG Output Mod, and refresh mo2, 2 new plugins will appear on the right side of mo2, one at the top, and another at the bottom, enable both and place them as low as possible in the load order.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011441.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011528.png)

---

# Part 3 - Running Grass Cache  
**est. time : 9 - 15 Hours**

- Grass cache should be rarely rerun, unless you change or add a very big location overhaul, or a mod that changes landscape drastically, From the author of No Grass in Objects:

"When do I need to regenerate a cache?

If you change grass mods, change your grass setting excluding grass distance, fade range, Dyndolod mode, or extended grass distance you will need to completely regenerate your cache for the changes to take effect.

If add or remove mods that alter location or add locations or the landscape you will need to regenerate a cache either for the changed cells or the whole worldspace depending on what is easier for you."

- Grass cache will need to be run 5 times in total for each corresponding season.

- To get started, Follow [this guide](https://www.youtube.com/watch?v=jH7co25_JIo) starting from the 4:33 minute mark up until 9:50, the "Grass Bounds.esp" plugin is called "Deez Nuts.esp" in Authoria.

- Don't change any Grass Control INI settings other than only-pregenerate-world-spaces if you dont know what they mean.

- Once GrassControl.ini is Sorted, Disable the "Grass Cache Helper NG" mod in mo2, then Enable the "No Grass In Objects" Mod.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013250.png)

- Disable the Following mods in mo2 to prevent crashing while generating Grass cache:
  - Auto Parallax
  - Discord Rich Presence
  - TrueHUD -> Only disabling the plugin on the right panel is enough.
  - Skyrim Souls -> take note of the plugin load order

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013539.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013609.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013641.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014008.png)

- Navigate to the Data tab of MO2, aand search for the po3_seasonsofskyrim.ini, Right click on it and pick reveal in explorer.  
IMPROTANT, if you added a new worldspace, and it has a seasons of skyrim support, then you should delete the po3_seasonsofskyrim.ini and let the game generate a new one by launching the game and getting to the main screen.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014207.png)

- Open the seasons of skyrim ini, and select the season you will geenrate grass cache for, start with 0 (disabled), and save then close the seasons of skyrim ini file.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014319.png)

- Go back to mo2, click the jigsaw icon on the top right and press on precache grass to start the process, you will get a notification window, press yes.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014715.png)

- it will take 2-3 hours for the process to complete, once it's done, you will get a notification window saying that grass cache has egenerated successfully, press ok, then navigate to the overwrite directory in mo2, there should be a folder called "grass" in your overwrite, move it to "Authoria - Grass Cache - Default"

- to Generate the seasonal Grass cache, go back to the po3_seasonsofskyrim.ini, and change the Season Type to 1 (winter), save and exit, then do the exact same process as the two steps above.

- Once it's done, and after moving the winter grass cache to the "Authoria - Grass cache - winter" mod, manually download the [Seasonal Grass Cache File Renamer (like Seasons your Grass)](https://www.nexusmods.com/skyrimspecialedition/mods/142343?tab=files) and place it anywhere outside of the wwabbajack installation.

- extract the Grass Renamer Archive into your winter grass cache folder

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015518.png)

- Run the windows batch file, and enter the number that corresponds to the season you just generated (1 for winter)

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015715.png)

- it will take some time to rename every file, once it's done, press Enter to close out of the Batch File, the grass cache should have a suffix now corresponding to the season you just generated.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015937.png)

- Repeat the same process for Summer, Spring and Autumn.

- Once you are done, Re-enable and Re-sort all the mods that you previously disabled, then disable "No Grass in Objects" and enable "Grass Cache Helper NG"

---

# Part 4 - Running xLodGen  
est. time: 4 hours

- xLodgen has to be run two times, once for the default worldspaces with no seasons, and another time for worldspaces with seasons.

- First, Search for "xLODGen Resource - SSE Terrain Tamriel" mod and enable it

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020450.png)

- Then, Click the gear icon in mo2, and navigate to xLodGen, you can change the output directory of xlodgen here, hit aply then OK.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020646.png)

- For the First run we will Generate non-seasonal xlodgen, pick xLODGen from the dropdown menu of mo2 and run it.

- Once xLodgen loads up, Tick only "Terrain LOD" then configure the settings for every LOD level like the pictures below.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021104.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021109.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021115.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021123.png)

- Right click on the Check box window and press select all, Then from the Seasons Dropdown menu, select only "Default"

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021516.png)

- Finally, Hit Generate, Once it Done it will say "Lod Generation Done.", close out of xLodgen.

- To know what worldspaces are seasons, open the po3_seasonsofskyrim.ini, and find the "Valid Worldspaces" Line  
IMPROTANT, if you added a new worldspace, and it has a seasons of skyrim support, then you should delete the po3_seasonsofskyrim.ini and let the game generate a new one by launching the game and getting to the main screen.

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021844.png)

Copy these into a blank text document, keep in mind that not every worldspace here will be in xlodgen, but you have to select every worldpsace that appears in that list and xlodgen, the following is the list for Authoria:

Tamriel  
MarkarthWorld|  
SkuldafnWorld|  
DeepwoodRedoubtWorld|  
JaphetsFollyWorld|  
LabyrinthianMazeWorld|  
DLC01FalmerValley|  
DLC1HunterHQWorld|  
DLC2SolstheimWorld|  
PalePass|  
zCOBruiantWorld  
zAoMWitchWorld|  
WyrmstoothWorld|  
AXOffshoreIslandWorld|  

- Run xLodgen again, and select the worldspaces that are in the seasonsfoskyrim.ini, then from the Seasons drop down select everything EXCEPT default, and press generate (LOD Level settings are the same):

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20022406.png)

- Once its Done it will say "Lod Generation Done.", close out of xLodgen.

---

# Part 5 - Running Texgen and Dyndolod
