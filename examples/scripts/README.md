# MSM Script Examples

![Picture](picture.png)

What scripts can do: scheduled effects, action handlers, scripted effects, counters kept across restarts, set bonuses, teleporting, boss bars and commands.

- **Category:** Scripts
- **Made for:** Minecraft 26.3 (MSM target `mc-26.3`)
- **Made by:** the MCSuperMods library (an example that ships with the app)
- **Licence:** MIT, like MCSuperMods

## What is in it (8 examples)

- **Script: scheduled effects:** A script that turns using an amethyst shard into a rising spiral of particles over two seconds, one msm.schedule step after another.
- **Script: action handler:** A chime block whose use event runs a script through a run_script action, and the script that defines that handler.
- **Script: scripted effect:** An Antidote status effect whose tick event runs a script: it cures poison and heals more at higher levels.
- **Script: kill counter:** A script that counts each player's kills in saved player data and the world's total in msm.storage, and tells players their count when they join.
- **Script: full set bonus:** A script that checks the armour of every player once a second and gives Haste and Luck to those wearing a full set of golden armour.
- **Script: teleport staff:** A script that turns a breeze rod into a teleport staff: use it to blink to the block you look at, sneak-use it to mark home or, from another dimension, to go home.
- **Script: boss fight bar:** A script that summons a ravager boss with a nether star and shows its health on a boss bar to every player, with a title and a reward when it falls.
- **Server helper:** Commands for a server: /helpme for everyone, /hub to jump to a lobby and /boost with a number for operators, with a rule book that points new players at /helpme.

## How to open it

1. Download this folder (or the whole repository as a zip from the green **Code** button).
2. In MCSuperMods, choose **File > Open Project…** and pick this folder (the one with `msm.project.json` in it).
3. Look around, change things, then use **Play** or **Export** to try it in the game.

For another Minecraft version, use **File > Upgrade Project Target…** in MCSuperMods. The checks of this repository open the example on mc-26.4 (Minecraft 26.4-snapshot-7) that way too.

This folder is made from the MCSuperMods `examples/` folder by `tools/community-repo/sync.ts`; change the example there, not here.
