# MCSuperMods Community

Mods made with [MCSuperMods](https://github.com/MEZTKING/MCSuperMods) (MSM), the desktop mod maker for Minecraft Java Edition, that anyone can open, learn from and play.

- [`examples/`](examples/) holds every example that ships with MCSuperMods, each as a project folder with a picture and a README. See the [list of examples](examples/README.md).
- [`mods/`](mods/) holds mods people made and shared. See [what is there](mods/README.md), and add yours.

Every project here is checked automatically: it must open in MCSuperMods and export with no errors on every Minecraft version MCSuperMods supports.

## Open a mod in MCSuperMods

1. Get the files: click the green **Code** button and **Download ZIP**, then unzip it. (Or clone the repository with git.)
2. Start MCSuperMods and choose **File > Open Project…**.
3. Pick the mod's folder: the one with `msm.project.json` in it, for example `examples/popular/glowshard`.
4. Look around, change what you like, and press **Play** to try it in Minecraft, or **Try it** for a quick look inside MCSuperMods.

A project is made for one Minecraft version (its README says which). For another version, use **File > Upgrade Project Target…** in MCSuperMods.

Copy a folder somewhere of your own before you change it, so your changes stay yours when you download the repository again.

## Share your own mod

Made something with MCSuperMods? Share it here so others can play it and learn from it. You need a free GitHub account. In short:

1. Copy your project folder into `mods/<your-mod-name>/`.
2. Add a `README.md` (copy [the template](mods/_template/README.md)), a `picture.png` and a `LICENSE`.
3. Open a pull request. The checks run by themselves and say in plain words if anything needs fixing.

[CONTRIBUTING.md](CONTRIBUTING.md) explains every step for a first-timer, including how to do it all in the browser without installing git.

## The rules

- **Only your own pictures and sounds.** Never Mojang's textures or sounds from the game, and nobody else's work unless its licence lets you share it (say so in your README). The checks refuse files under Minecraft's own names (`assets/minecraft/`) and pictures or sounds nothing in the project uses.
- **Nothing that harms players**: no scripts or functions that delete worlds, break saves on purpose, spam, trick players or try to reach outside the game.
- **The project must pass the checks**: it opens and exports with no errors on every supported Minecraft version. Warnings are fine.
- **Keep it small**: at most 2 MiB a file (8 MiB for a sound) and 25 MiB a mod.
- **Be kind** in pull requests and reviews. Anyone may share, beginners most of all.

## Licences

- **The examples** in `examples/` and the files that run this repository (READMEs, the template and the checks) are under the [MIT licence](LICENSE), like MCSuperMods itself.
- **Each mod in `mods/`** has its own licence, which its folder states (a `LICENSE` file and a line in its README). You choose it when you share. **If a mod states no licence, it is shared under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)**: anyone may use, change and share it, also commercially, as long as they credit the author. By opening a pull request you agree to that default if you name no other licence.
- Minecraft is a trademark of Mojang Studios. This repository is not an official Minecraft product and is not approved by or associated with Mojang or Microsoft.

## How the checks work

The workflow in [`.github/workflows/check.yml`](.github/workflows/check.yml) checks out this repository and MCSuperMods (`main`), installs it, and runs MCSuperMods' `tools/check-project` on every changed folder under `mods/` and `examples/`, for every Minecraft version. The checker opens the project with the app's own code, moves it to each version as **File > Upgrade Project Target…** does, runs every validator, and exports the resource pack, the data pack and the Fabric mod jar. It also runs `tools/community-repo/sync.ts --check`, which fails when `examples/` no longer matches the examples of MCSuperMods `main`.

To run the same check on your own computer, in a checkout of MCSuperMods (after `pnpm install`):

```sh
node tools/check-project/index.ts <path to your mod folder>
```

The `examples/` folders are made by `node tools/community-repo/sync.ts --repo <this repository>` in MCSuperMods; change examples there, not here.
