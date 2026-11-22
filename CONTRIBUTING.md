# Sharing your mod

Thank you for sharing! This page walks you through it step by step. You do not need to know git: everything can be done in the browser on GitHub. If you get stuck, open a pull request anyway and ask; someone will help.

You need:

- a mod you made in MCSuperMods;
- a free [GitHub account](https://github.com/signup).

## 1. Get your project folder

Every MCSuperMods project is a folder on your computer with a file called `msm.project.json` in it, next to the folders `content/` and `assets/`. That folder is what you share, not the exported `.jar` or `.zip`.

- Not sure where it is? It is the folder you chose when you made the project; **File > Open Recent** lists the projects you opened lately.
- Save the project first (**File > Save**), and check it in **Things to fix** (Very easy) or the Problems tab: it must have no errors.
- Pack the folder up as it is. Leave out anything that is not part of the project; you may leave the hidden `.msm` folder out too.

## 2. Make your mod's folder

Choose a short folder name for your mod: lower-case letters, digits and hyphens, for example `glow-berries` or `castle-pack`. Your mod goes in `mods/<that name>/` and holds:

| File | What it is |
|---|---|
| `msm.project.json`, `content/`, `assets/` | Your project, copied as it is. |
| `README.md` | About your mod. Copy [`mods/_template/README.md`](mods/_template/README.md) and fill it in. |
| `picture.png` | A picture of your mod: a screenshot from the game, or one of your textures. Keep it under 2 MiB. |
| `LICENSE` | Your licence (see step 4). |

Nothing else may be in the folder (no `.jar`, `.zip`, `.exe` or other files); the checks refuse it.

## 3. Write the README

Open [the template](mods/_template/README.md), copy it into your folder as `README.md` and replace each part in brackets: the title, your name (or GitHub name), the Minecraft version your project is made for (Easy and Advanced mode show it in the status bar, for example 26.3), what your mod adds, how to play it, and the licence. Write in any language you like; plain English helps the most people. British spelling is not required.

## 4. Choose a licence

The licence says what others may do with your mod.

- If you are not sure, use **CC BY 4.0**: anyone may play, change and share it, as long as they credit you. This is also the default: a mod that states no licence is shared under CC BY 4.0.
- **MIT** is a common choice too (it is what MCSuperMods and its examples use).
- **CC BY-NC 4.0** if you do not want others to sell it.

Put the licence's name in your README and its text in `LICENSE`. You can copy the text from [creativecommons.org](https://creativecommons.org/licenses/) or [choosealicense.com](https://choosealicense.com/licenses/mit/).

## 5. Open a pull request

In the browser:

1. On this repository's page, click **Fork** (top right) to make your own copy.
2. In your fork, open the `mods` folder, click **Add file > Upload files**, and drag your mod's folder in (GitHub keeps its folders). Check that the files land in `mods/<your-mod-name>/`.
3. Write a short message such as "Add Glow Berries" and choose **Commit changes**.
4. Click **Contribute > Open pull request**, fill in the checklist in the description, and click **Create pull request**.

With git, the same in a terminal: fork, clone your fork, copy the folder into `mods/`, commit, push, and open the pull request on GitHub.

## 6. Wait for the checks

A few minutes after you open the pull request, the **Check mods** workflow shows a tick or a cross at the bottom of the page. It opens your project with MCSuperMods' own code on every Minecraft version MCSuperMods supports and exports it. If it fails, click **Details**: each problem names the file or element and says what is wrong in plain words. Fix it in MCSuperMods, copy the changed files into your fork again, and the checks run again by themselves. Warnings do not fail the check.

Then someone looks at your mod, may ask a question, and merges it. Your mod is shared!

## The rules

- **Your own pictures and sounds only.** Never Mojang's textures or sounds from the game. Using someone else's work is fine only if its licence lets you share it; say whose it is and under which licence in your README. MCSuperMods projects keep pictures in your own namespace (`assets/<your namespace>/`): the checks refuse anything under `assets/minecraft/`, and pictures or sounds nothing in the project uses.
- **No mod that harms players**: nothing that deletes or damages worlds on purpose, spams, tricks players, or tries to reach outside the game.
- **It must pass the checks**: no errors on any supported Minecraft version.
- **Size**: at most 2 MiB per file, 8 MiB per sound, 25 MiB per mod.
- **One mod per folder**, and one or a few mods per pull request.
- **Be kind.** Everyone starts somewhere.

To change your mod later, open a new pull request that changes its folder. To have it removed, open an issue or a pull request that deletes the folder.

## Examples

The `examples/` folder is made automatically from MCSuperMods' own examples; please do not change it here. Ideas for new examples are welcome as issues in [MCSuperMods](https://github.com/MEZTKING/MCSuperMods/issues).
