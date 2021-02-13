# customplay - a minimum gameplay mod for Doom3-BFG

## Features

- More useful armor: absorbs 50% of damage instead of 20%
- Slightly more useful shotguns: less spread so more powerful at medium
  range.
- Rebalanced super shotgun so that while it has more spread, it produces
  25% more projectiles than two shotgun shots.
- Realistic weapon reloading
  - Allow reloading only when clip is empty (except shotgun)
  - Shotgun reloads one shell at a time (instead of two)
- Realistic ammo pickups
  - Pickup sizes are consistent with weapon clip sizes and pickup models.

## How to use

Because the original BFG executable doesn't support modding, you have
to use a sourceport such as RBDOOM-3-BFG.

Download the whole repo and put it in a subdirectory called
`customplay` under Doom3 BFG's install directory, along with `base`.
For example, using git:

```
Doom3 BFG $ git clone https://github.com/zmodder/doom3-bfg-customplay.git customplay
```

To start, add `+set fs_game customplay +set fs_resourceLoadPriority 0`
to the command line.

It also comes with an optional `autoexec.cfg` that's suitable for
low-end computers that don't handle the default graphics setting. To
use it, rename `optional_autoexec.cfg` to `autoexec.cfg`.
