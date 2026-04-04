# Authoria - Requiem Reforged — Tool Running Guide

This guide explains how to properly run all LOD-related tools for **Authoria - Requiem Reforged**.  
You should follow this guide whenever you modify the modlist and need to regenerate LODs.

The tools covered in this guide:
- ParallaxGen
- Grass Cache
- xLODGen
- TexGen
- DynDOLOD

Any tools not listed here are covered in separate, simpler guides.

---

## When Do You Need to Rerun These Tools?

### 1. Mesh / Texture Changes
If you add mods that replace **vanilla meshes or textures**:
- You will most likely need to rerun **ParallaxGen**.

To confirm:
- Check conflicts of the mod you added.
- If it is **losing conflicts to ParallaxGen output**, you must rerun ParallaxGen.

**Important:**
Rerunning ParallaxGen requires:
- xLODGen → must be rerun
- DynDOLOD → must be rerun

---

### 2. Worldspace Edits (Tamriel)
If you add mods that **edit the worldspace**:
- Check changes in **xEdit**
- You must rerun:
  - ParallaxGen
  - Grass Cache
  - xLODGen
  - DynDOLOD

---

## Disclaimer

Running tools for Authoria is **not a standard process** due to the inclusion of **Seasons of Skyrim**.

- Expect the full process to take **at least two full days**
- Outputs make up **30–40% of the modlist size**
- Total output size: **~160 GB**

Plan your storage accordingly.

---

## Index

1. Preparation  
2. ParallaxGen  
3. Grass Cache  
4. xLODGen  
5. TexGen  
6. DynDOLOD  

---

# Part 1 — Preparation

### Profile Setup
- You should already have:
  - A duplicated profile
  - Empty output mods for each tool

If you do not have enough space:
- You can delete existing output contents and regenerate them

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005429.png)

---

### Disable Flat Map Framework Separator
- Expand the **Flat Map Framework Separator**
- Disable everything inside it

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005437.png)

---

### Verify Plugin Load Order
- Open MO2 → Plugin Panel (right side)
- Ensure the **last plugins** are:
  - Synthesis Outputs

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20005810.png)

---

# Part 2 — Running ParallaxGen  
**Estimated Time: 10–15 minutes**

### Step 1 — Launch
- In MO2 dropdown → select **ParallaxGen**
- Click **Run**

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010119.png)

---

### Step 2 — Configure Settings
- Ensure settings match the reference screenshot
- **Instance Location**:
  - Must match your Wabbajack installation directory
- **Output Directory**:
  - Select your empty ParallaxGen output mod

Then click:
- **Start Patching**

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010334.png)

---

### Step 3 — Set Mods Prompt
- When “Set Mods” popup appears:
  - Do not change anything
  - Click **OK**

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20010820.png)

---

### Step 4 — Completion
- After generation finishes:
  - Click **OK**

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011136.png)

---

### Step 5 — Enable Output
- Enable your **ParallaxGen Output Mod**
- Refresh MO2

You will see:
- One plugin at the top
- One plugin at the bottom

Actions:
- Enable both
- Move both to the **bottom of the load order**

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011441.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20011528.png)

---

# Part 3 — Running Grass Cache  
**Estimated Time: 9–15 hours**

### When to Rerun

From the author of No Grass in Objects:

> If you change grass mods or settings (excluding distance/fade/DynDOLOD mode), you must regenerate the cache.  
> If you add/remove landscape or location mods, regenerate either affected cells or the full worldspace.

---

### Key Notes
- Must be run **5 times (one per season)**

---

### External Setup Guide
Follow:
https://www.youtube.com/watch?v=jH7co25_JIo  
(Start at 4:33 → 9:50)

Note:
- "Grass Bounds.esp" = **"Deez Nuts.esp"** in Authoria

---

### GrassControl.ini Rules
- Do NOT change settings unless you understand them
- Only allowed change:
  - `only-pregenerate-world-spaces`

---

### Required Mod Setup

Disable:
- Grass Cache Helper NG  

Enable:
- No Grass In Objects  

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013250.png)

---

### Disable Mods to Prevent Crashes

Disable:
- Auto Parallax
- Discord Rich Presence
- TrueHUD (plugin only)
- Skyrim Souls (note load order)

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013539.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013609.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20013641.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014008.png)

---

### Seasons Setup

Locate:
- `po3_seasonsofskyrim.ini`

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014207.png)

If adding new worldspace:
- Delete the file
- Launch game → reach main menu → regenerate

---

Set initial season:
- `Season Type = 0`

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014319.png)

---

### Generate Grass Cache

- MO2 → jigsaw icon → **Precache Grass**
- Confirm prompt

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20014715.png)

- Wait 2–3 hours
- Move `/overwrite/grass` →  
  `Authoria - Grass Cache - Default`

---

### Seasonal Generation

Repeat for:
- Winter (1)
- Summer
- Spring
- Autumn

---

### Rename Seasonal Cache

Download:
https://www.nexusmods.com/skyrimspecialedition/mods/142343?tab=files  

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015518.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015715.png)
![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20015937.png)

---

### Final Step
- Re-enable all disabled mods
- Disable No Grass In Objects
- Enable Grass Cache Helper NG

---

# Part 4 — Running xLODGen  
**Estimated Time: 4 hours**

### Overview
Run twice:
1. Non-seasonal
2. Seasonal

---

### Setup

Enable:
- xLODGen Resource - SSE Terrain Tamriel

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020450.png)

---

Configure output path:

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20020646.png)

---

### First Run — Default Only

- Select Terrain LOD
- Select All worldspaces
- Seasons → Default

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021516.png)

- Click Generate

---

### Seasonal Worldspaces

Check:
- `po3_seasonsofskyrim.ini`

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20021844.png)

Use listed worldspaces:
(Tamriel, MarkarthWorld, etc.)

---

### Second Run — Seasonal

- Select only seasonal worldspaces
- Seasons → everything except Default

![Screenshot](https://raw.githubusercontent.com/Drheisen1/Authoria-Requiem-Reforged/main/Resources/Tool%20Guide/Screenshot%202026-04-04%20022406.png)

- Generate

---

# Part 5 — Running TexGen and DynDOLOD

Continue with the same workflow pattern.