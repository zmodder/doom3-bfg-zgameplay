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
  ammo supplied by almost all pickups, and added more pickups in the
  maps, resulting in a serious oversupply and threw off gameplay
  balance.  The mod:
  - Reduced the clip sizes of machine gun (60->40) and plasma gun
    (50->30)
  - Reduced ammo pick up sizes in general
      - Small bullets: 24 -> 12 (in line with pistol clip size)
      - Large bullets: 48 -> 12 (just don't need that many bullets)
      - Small shells: 12 -> 6 (only 6 shells are shown on the model)
      - Large shells: 24 -> 12 (doubling the small pick up)
      - Small clip: 60 -> 40 (in line with the machine gun clip size)
      - Large clip: 90 -> 0 (can't be picked up)
      - Grenedes: 8 -> 4 (only 4 are shown on the model)
      - Small rockets: 5 -> 4 (only 4 are shown on the model)
      - Large rockets: 20 -> 8 (only 8 are shown on the model)
      - Cell: 50 -> 30 (in line with the plasma gun clip size)
      - Double cell: 75 -> 0 (can't be picked up)
      - Ammo belt: 90 -> 60 (in line with chain gun clip size)
      - BFG cell: 6 -> 4 (in line with BFG clip size)


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
