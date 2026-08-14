# Ashes of Sanctuary

A Diablo-style 2.5D isometric action arena game in a single HTML file. No build step, no dependencies, no server — open `index.html` in a browser and play.

**Play it:** https://thientu.github.io/simple-game-glm-5.3/

## Gameplay

Fight through waves of demons across five rotating realms. Five waves clear a realm, then the way opens to the next. Shatter chests, drink from shrines, and mind the lava.

- **Sword** — free melee swing with knockback; damage scales with level
- **Fireball** — piercing ranged bolt, costs essence
- **Frost Nova** — chills enemies with a 55% slow
- **Leap** — gap closer; detonates for area damage with the Earthshaker boon
- **Level-up boons** — pick 1 of 3 upgrade cards each level (crit, lifesteal, quake leaps, and more)
- **Shop** — spend gold between waves on potions, whetstones, armor, essence, and boots
- **Loot** — chests, breakables, and shard drops from elites

### Realms

| Realm | Mood |
|---|---|
| Ossuary Court | Bone and stone |
| Crimson Chapel | Hymns long gone |
| Frostfell Wastes | Where heroes froze |
| Ember Hollow | The mountain's heart |
| Mirefen Bog | It swallows all |

### Enemies

Imps, skeletons, and ghouls rush you; cultists keep their distance and throw dodgeable bile bolts; brutes telegraph charging dashes; elites summon imps every few seconds.

## Controls

| Action | Keyboard / Mouse |
|---|---|
| Move | `WASD` or arrow keys |
| Sword | `LMB` or `J` |
| Fireball | `RMB` or `K` (auto-aim) |
| Leap | `Space` |
| Frost Nova | `1` |
| Potion | `Q` |
| Shop (intermission) | `B` |
| Mute | `M` |
| Pause | `Esc` or `P` |

Touch devices get an on-screen joystick and buttons automatically.

## Run locally

Just open `index.html` in a browser, or:

```bash
python3 -m http.server
# then visit http://localhost:8000
```

## GitHub Pages

The game is fully static (one file, no build). To publish:

1. Push this repo to GitHub
2. Repo **Settings → Pages**
3. Source: **Deploy from a branch** → `main` / `/ (root)`
4. The game goes live at `https://<user>.github.io/<repo>/`

## Design references

The `design/` folder holds the Open Design mockups the game was built from (UI, arena, isometric layouts). They are not needed to play.
