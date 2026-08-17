# Ashes of Sanctuary

A Diablo-style 2.5D isometric action arena game in a single HTML file. No build step, no dependencies, no server — open `index.html` in a browser and play.

**Play it:** https://thientu.github.io/simple-game-glm-5.3/

## Gameplay

Fight through waves of demons across nine rotating realms. Five waves clear a realm — the fifth wakes its **realm guardian** (a boss with its own skill kit and a phase-shift "super appearance" at a life threshold). Shatter chests, drink from shrines, and mind the lava.

- **Sword** — free melee swing with knockback; damage scales with level
- **Fireball** — piercing ranged bolt, costs essence
- **Frost Nova** — chills enemies with a 55% slow
- **Leap** — gap closer; detonates for area damage with the Earthshaker boon
- **Level-up boons** — pick 1 of 3 upgrade cards each level (crit, lifesteal, quake leaps, and more); boons stack — a second pick adds to the first, and each card shows its level, cooldown, essence cost, and exact current → next values
- **Hero sheet** — a compact stat panel (power, skill damage, crit, armor, speed) sits on the left edge during play; press `C` for the full sheet: DPS, crit, armor, essence, and a per-skill damage breakdown
- **Shop** — spend gold between waves; every item shows the real stat change (current → new) before you buy
- **Bestiary** — press `B` in the field to open the tome: every guardian and new monster with lore, stats, threat, their three skills, and an interactive **Awaken** button that plays the super-appearance transformation
- **Loot** — chests, breakables, and shard drops from elites and guardians

### Realms

The last four realms are shaped — a ring, a hexagon, a crossing, and a long span — with the arena, spawns, and rim all conforming to the footprint.

| Realm | Mood | Guardian |
|---|---|---|
| Ossuary Court | Bone and stone | Madrega, the Marrow Saint |
| Crimson Chapel | Hymns long gone | The Unheard Choir |
| Frostfell Wastes | Where heroes froze | The Unheard Choir |
| Ember Hollow | The mountain's heart | Vhalgrim, the Ash Tyrant |
| Mirefen Bog | It swallows all | Madrega, the Marrow Saint |
| Ashen Caldera | A ring around the fire | Vhalgrim, the Ash Tyrant |
| Hexfound Court | Six walls, one verdict | The Unheard Choir |
| Tomb Crossing | Four roads to rest | Madrega, the Marrow Saint |
| The Gloomspan | A road over nothing | The Unheard Choir |

### Enemies

Imps, skeletons, and ghouls rush you; cultists keep their distance and throw dodgeable bile bolts; chargers telegraph their dashes; elites summon imps every few seconds. The new courts add:

- **Hollow Wisp** — a lantern caster that kites you with rime bolts, leaves freezing snare runes, and blinks away when cornered
- **Bloodsworn Zealot** — a fast zealot that dashes in bleeding arcs, channels an interruptible Blood Tithe, and whips itself into a damage-exposed frenzy
- **Gravehide Brute** — a heavy that slams shockwaves, hurls corpses that rise as remnants when they miss, and tucks into a breakable Hide of Graves shell
- From wave 7, any of the three can spawn **awakened** (rare-elite): bigger, glowing, 2.5× life, and carrying its own ultimate

### Guardians

Wave 5 of every realm summons its guardian: a named boss with a top-screen health bar, three telegraphed skills, and a phase shift at a life threshold (Vhalgrim 50%, Madrega 40%, the Choir 60% and 30%) that transforms it and unlocks a once-per-phase ultimate. Killing the guardian opens the way deeper.

## Controls

| Action | Keyboard / Mouse |
|---|---|
| Move | `WASD` or arrow keys |
| Sword | `LMB` hold or `1` (auto-aim) |
| Fireball | `RMB` or `2` (auto-aim) |
| Frost Nova | `3` |
| Leap | `Space` |
| Potion | `4` |
| Hero sheet | `C` |
| Bestiary | `B` (in the field) |
| Pick boon card | `Tab` / arrows, `Enter` to take |
| Shop buy | `Tab` / arrows, `Enter` to buy |
| Shop (intermission) | `B` |
| Mute | `M` |
| Pause | `Esc` or `P` |
| Debug overlay | `` ` `` (backtick) — with it open, `[` / `]` cycle realms and `N` skips a wave |

Touch devices get an on-screen joystick and buttons automatically. The game is designed for landscape: tapping **Enter the Realms** (or **Rise Again**) requests fullscreen and locks landscape where the browser allows it (Android Chrome). On browsers that can't lock orientation (iOS Safari), a "rotate your device" prompt covers the screen in portrait, and the game auto-pauses if you rotate mid-run.

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
