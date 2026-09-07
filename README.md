# Fields of Mistria Mods

Mods for [Fields of Mistria](https://store.steampowered.com/app/2142790/Fields_of_Mistria/), built with [MOMI](https://github.com/Fields-Of-Mistria-Modding-Discord/MOMI) (Mod Manager / Fiddle format).

## Repo layout

- Each top-level folder is a standalone mod, structured for MOMI: a `manifest.toml` plus `fiddle/` (data overrides in TOML) and `animations/` (sprite overrides) as needed.

## Mods

### [WanderersRing](WanderersRing)

Adds a craftable Wanderer's Ring (blacksmithing) that grants a permanent movement-speed boost via the game's `hasty` infusion. The recipe is delivered by mail once the player reaches floor 80 of the mines.

### [InfusionBoost](InfusionBoost) / [InfusionBoost20](InfusionBoost20) / [InfusionBoost50](InfusionBoost50)

Static rebalance of the general-purpose craftable infusions (Hasty, Fortified, Tireless, Sharp, Leeching, Lightweight, Quality, Speedy, Stacking Speed). There's no in-game way to adjust these live, so each folder is a separate, mutually-exclusive strength tier a player picks instead — install only one:

- **InfusionBoost (+10)**: ~2.5x vanilla (Hasty 4% → 10%)
- **InfusionBoost20 (+20)**: 5x vanilla (Hasty 4% → 20%)
- **InfusionBoost50 (+50)**: 12.5x vanilla (Hasty 4% → 50%, Lightweight's drop chance capped at 100%)

Packaged zips for upload live in `dist/` (gitignored, built from the mod folders — see below).

## Development notes

- Changes are verified against the vanilla `assets.zip` contents in `game/` before being written into a mod's `fiddle/` files, since the item/recipe/UI format is data-driven and behavior isn't always obvious from the format alone.
- See the comments at the top of each mod's TOML files for the reasoning behind specific choices (e.g. why a category is its own file, why a recipe is delivered by mail instead of a scroll item).
