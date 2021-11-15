# zgameplay - zmodder's gameplay mod for Doom3-BFG

This is a minimal gameplay change to make Doom3 BFG Edition more balanced
and more realistic.

## Features

- More useful armor: absorbs 50% of damage instead of 20%
- Slightly more useful shotguns: less spread so more powerful at medium
  range.
- Rebalanced super shotgun so that while it has more spread, it produces
  25% more projectiles than two shotgun shots.
- Realistic weapon reloading.  The reloading mechanism of the modern FPS
  is not also unrealistic as it merges the remaining ammo in real time,
  but also repetitive and triggers obsession.  I find it more fun to play
  without preemptive reloading.
  - Allow reloading only when clip is empty (except shotgun)
  - Shotgun reloads one shell at a time (instead of two)
- Realistic and more balanced ammo pickups.  Doom3 BFG increased the ammo
  supplied by almost all pickups, resulting in a serious oversupply and
  threw off gameplay balance.  The mod reverted such change to be more
  consistent with the original Doom3.
  - Pickup sizes are consistent with weapon clip sizes and pickup models.
    Also adjusted some weapons' clip sizes to avoid over-supply of ammo:
    - Reduce machinegun clip size from 60 to 30 because there are just
      too much ammo supply.
    - All machinegun large clip pickups (45) are changed to small (30).
    - Reduce plasma gun clip size from 50 to 25 to be consistent with
      the original Doom3.  Clip size of 50 also results in too much
      supply.

## How to use

Because the original BFG executable doesn't support modding, you have
to use a sourceport such as RBDOOM-3-BFG.

Download the whole repo and put it in a subdirectory called
`zgameplay` under Doom3 BFG's install directory, along with `base`.
For example, using git:

```
Doom3 BFG $ git clone https://github.com/zmodder/doom3-bfg-zgameplay.git zgameplay
```

To start, add `+set fs_game zgameplay +set fs_resourceLoadPriority 0`
to the command line.

It also comes with an optional `autoexec.cfg` that's suitable for
low-end computers that don't handle the default graphics setting. To
use it, rename `optional_autoexec.cfg` to `autoexec.cfg`.
