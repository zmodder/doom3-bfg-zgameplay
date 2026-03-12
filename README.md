# zgameplay - zmodder's gameplay mod for Doom3-BFG

This is a minimal gameplay change to make Doom3 BFG Edition more balanced
and more realistic.

## Features

- More useful armor: absorbs 50% of damage instead of 20%
- Slightly more useful shotguns: less spread so more powerful at
  medium range, despite producing less pellets.  Also increased its
  firing rate.
- Rebalanced super shotgun so that while it has more spread, it produces
  50% more projectiles than two shotgun shots.
- Realistic weapon reloading.  The reloading mechanism of the modern FPS
  is not also unrealistic as it merges the remaining ammo in real time,
  but also repetitive and triggers obsession.  I find it more fun to play
  without preemptive reloading.
  - Allow reloading only when clip is empty (except shotgun)
  - Shotgun reloads one shell at a time (instead of two)
- Realistic and more balanced ammo pickups.  Doom3 BFG increased the
  ammo supplied by almost all pickups, resulting in a serious
  oversupply and threw off gameplay balance.  Even in the original
  Doom 3, small ammo pickups are not in line with the clip size, e.g.,
  picking up a machine gun clip gives you 30 rounds, but a machine gun
  clip holds 60 rounds.  The mod:
  - Increases the volume of ammo pickups so that they align with the
    actual clip size of the weapon.  To mitigate over-supply, cuts
    down the clip size of the machine gun and plasma gun.
  - Changed all large ammo pickups to small pistol bullet pickups,
    effectively making them useless, to further cut down the ammo
    supply brought by BFG edition.


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
