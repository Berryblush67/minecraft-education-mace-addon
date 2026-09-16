# Minecraft Education Edition - Mace Weapon Add-on

## 🔨 Features

This add-on adds a custom **Mace Weapon** to Minecraft Education Edition with special abilities:

### Left-Click (Attack) Abilities:
- ⚔️ **Base Damage**: 8 HP per hit
- 👁️ **Blindness Effect**: Enemies can't see for 3 seconds
- 💪 **Weakness Effect**: Enemies deal less damage for 4 seconds
- 🎯 **Bonus Damage**: Extra 6-8 damage on special hits

### Right-Click (Special Ability):
- 👻 **Teleport Dash**: Move 6 blocks forward in the direction you're looking
- 🫥 **Invisibility Buff**: Become invisible for 3 seconds after using ability
- ⏱️ **12 Second Cooldown**: Wait before using ability again

## 📦 Installation

### Step 1: Download the Add-on
1. Download this repository as a ZIP file
2. Extract the folders: `behavior_pack` and `resource_pack`

### Step 2: Install on Windows/Mac/iPad
1. **Behavior Pack**: Copy the `behavior_pack` folder to:
   - Windows: `%appdata%\.minecraft\behavior_packs\`
   - Mac: `~/Library/Application Support/minecraft/behavior_packs/`
   - iPad: Use Files app → On My iPad → Minecraft → Documents → behavior_packs

2. **Resource Pack**: Copy the `resource_pack` folder to:
   - Windows: `%appdata%\.minecraft\resource_packs\`
   - Mac: `~/Library/Application Support/minecraft/resource_packs/`
   - iPad: Use Files app → On My iPad → Minecraft → Documents → resource_packs

### Step 3: Enable in Game
1. Create a new world in Minecraft Education Edition
2. Go to **World Settings** → **Behavior Packs**
3. Add the "Mace Weapon Behavior Pack"
4. Go to **Resource Packs**
5. Add the "Mace Weapon Resource Pack"
6. Click **Create World**

## 🎮 How to Use

### Getting the Mace:
```
/give @s mace:mace_weapon
```

### Simulating Effects in Command Blocks:

**For hit effects (setup repeating command blocks):**
```
# Blindness effect
effect @s blindness 3 0

# Weakness effect
effect @s weakness 4 0

# Extra damage
damage @s 8
```

**For special ability (on right-click):**
```
# Teleport forward 6 blocks
tp @s ^ ^ ^6

# Give invisibility
effect @s invisibility 3 0

# Play sound effect
playsound block.end_portal.spawn @s ~ ~ ~
```

## 📝 How It Works

Minecraft Education Edition doesn't support full Java modding, so this add-on uses:

1. **Behavior Pack** (`.json` files):
   - Defines the mace item properties
   - Sets up item events
   - Configures damage and enchantability

2. **Resource Pack** (textures):
   - Custom appearance for the mace
   - Item model and textures

3. **Command Blocks** (`.mcfunction` file):
   - Simulates special abilities
   - Creates effects and status effects
   - Handles cooldowns with redstone circuits

## ⚠️ Limitations

- **No automatic effects**: Effects require command block setup
- **No true cooldown system**: Use scoreboards and command blocks for cooldowns
- **No teleportation**: Must use command blocks to simulate teleport
- **Limited automation**: Some features require manual trigger setup

## 🔧 Customization

### Change Mace Color/Texture:
Replace the texture file at:
```
resource_pack/textures/items/mace.png
```

### Adjust Damage:
Edit `behavior_pack/items/mace.json` and change:
```json
"minecraft:damage": 8
```

### Change Effect Duration:
Edit the command blocks and adjust the numbers:
- `effect @s blindness 3` → change `3` to desired seconds
- `effect @s weakness 4` → change `4` to desired seconds

## 📚 Resources

- [Minecraft Education Add-ons Guide](https://educommunity.minecraft.net/)
- [Bedrock Add-on Documentation](https://learn.microsoft.com/en-us/minecraft/creator/)
- [Command Block Tutorial](https://minecraft.fandom.com/wiki/Command)

## 💡 Tips

- Use **Repeating Command Blocks** set to "Always Active" for continuous effects
- Use **Conditional Command Blocks** to create complex logic chains
- Test effects in **Creative Mode** first before using in Survival
- Use **Scoreboards** to track cooldowns:
  ```
  /scoreboard objectives add mace_cooldown dummy
  /scoreboard players add @s mace_cooldown 1
  ```

## 📧 Support

Have questions? Check the [Minecraft Education Community](https://educommunity.minecraft.net/)

---

**Enjoy your Mace Weapon! ⚔️**
