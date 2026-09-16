# 🎮 Complete Setup Guide for Mace Add-on

## What You're Installing

This add-on adds a custom **Mace Weapon** to Minecraft Education Edition that:
- Deals 8 damage per hit
- Applies Blindness + Weakness effects to enemies
- Can teleport you forward (with invisibility buff)
- Has a 12-second cooldown on special ability

## Prerequisites

✅ Minecraft Education Edition installed  
✅ Administrator access to your computer  
✅ Ability to enable experimental features (some versions)  

---

## Installation Steps

### **Option 1: Automatic Installation (Easiest)**

1. Download the `.mcaddon` file (when available)
2. Double-click it
3. Minecraft Education should open and import automatically
4. Create a new world and enable the packs

### **Option 2: Manual Installation (Recommended)**

#### **Windows:**

1. Extract this ZIP file
2. Open File Explorer
3. Type in address bar: `%appdata%\.minecraft\`
4. Create folders if they don't exist:
   - `behavior_packs`
   - `resource_packs`
5. Copy `behavior_pack` folder → paste into `behavior_packs`
6. Copy `resource_pack` folder → paste into `resource_packs`
7. Open Minecraft Education Edition
8. Create new world → enable both packs in world settings

#### **Mac:**

1. Extract this ZIP file
2. Open Finder → Press `Cmd + Shift + G`
3. Type: `~/Library/Application Support/minecraft/`
4. Create folders if missing:
   - `behavior_packs`
   - `resource_packs`
5. Copy `behavior_pack` → paste into `behavior_packs`
6. Copy `resource_pack` → paste into `resource_packs`
7. Open Minecraft Education Edition
8. Create new world → enable both packs

#### **iPad/Chromebook:**

1. Extract ZIP (use Files app or email)
2. Open **Files** app
3. Navigate to **On My iPad** → **Minecraft** → **Documents**
4. Create `behavior_packs` and `resource_packs` folders
5. Copy extracted folders into correct locations
6. Open Minecraft Education
7. Create world and enable packs

---

## Testing the Add-on

### **Test 1: Get the Mace**

1. Create a test world with the add-on enabled
2. Enable **Cheats**
3. Open chat (press `/` or `T`)
4. Type: `/give @s mace:mace_weapon`
5. You should receive a Mace item

### **Test 2: Hit an Enemy**

1. Spawn a mob (zombie, skeleton, etc.)
2. Hit it with the mace
3. You should see:
   - Mob takes damage
   - Mob appears blinded (black screen effect)
   - Mob gets weakness effect (moves slower, less damage)

### **Test 3: Special Ability**

1. Hold the mace
2. Right-click (on PC) or tap and hold (on tablet)
3. You should:
   - Move forward 6 blocks
   - Become invisible
   - Hear a "whoosh" sound
4. Wait 12 seconds before ability resets

---

## Troubleshooting

### **Problem: Add-on doesn't appear in world settings**

**Solution:**
- Make sure manifest.json files are valid JSON (no typos)
- Check folder names are exactly: `behavior_pack` and `resource_pack`
- Restart Minecraft Education Edition
- Try creating a new world

### **Problem: Mace doesn't appear when using /give command**

**Solution:**
- Check that item identifier is: `mace:mace_weapon`
- Make sure behavior pack is enabled in world
- Try enabling cheats if not already enabled

### **Problem: Effects don't appear**

**Solution:**
- Command blocks may need manual setup
- Create repeating command blocks with:
  ```
  effect @e[name=YourName] blindness 3 0
  ```
- Place blocks near where mace is used
- Connect with redstone for activation

### **Problem: "Pack is incompatible" error**

**Solution:**
- Update Minecraft Education Edition to latest version
- Check `min_engine_version` in manifest.json
- Try removing and re-importing add-on

---

## Command Block Setup (Advanced)

To make effects more automatic, set up these command blocks:

### **Setup for Blindness Effect:**

1. Place a Repeating Command Block
2. Set to "Always Active"
3. Enter command:
   ```
   effect @e[type=zombie] blindness 3 0
   ```

### **Setup for Teleport Ability:**

1. Place Repeating Command Block
2. Set to "Always Active"
3. Connect to a Button/Lever
4. On activate, run:
   ```
   tp @s ^ ^ ^6
   ```
5. Then run:
   ```
   effect @s invisibility 3 0
   ```

---

## Tips for Success ✅

- **Start in Creative Mode** to test without worrying about survival
- **Use command blocks** for automatic effect triggers
- **Enable experimental features** if some features don't work
- **Check console logs** (F3 key on PC) for error messages
- **Join Education community** for advanced help

---

## Frequently Asked Questions

**Q: Can I use this on regular Minecraft Java Edition?**  
A: No, this is Education Edition only. For Java, use Forge mods.

**Q: Can I modify the mace appearance?**  
A: Yes! Replace textures in `resource_pack/textures/items/mace.png`

**Q: How do I increase the cooldown timer?**  
A: Modify command blocks to add more ticks between uses

**Q: Can I add more abilities?**  
A: Yes! Add more command blocks and JSON event handlers

---

## Need More Help?

📖 Visit: https://educommunity.minecraft.net/  
💬 Join Discord: Minecraft Education Community  
🎥 Watch Tutorials: Search "Minecraft Education add-ons tutorial"  

---

**Enjoy your custom Mace Weapon! Have fun in Minecraft Education Edition! 🔨⚔️**
