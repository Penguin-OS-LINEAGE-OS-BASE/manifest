# PenguinOS (Lineage base)

https://github.com/Penguin-OS-LINEAGE-OS-BASE/manifest

PenguinOS rebased onto LineageOS (`lineage-24.0`, Android 17) — same
Penguin identity (Liquid Glass QS panel, Control Centre, PenguinSystemUI,
Laboratory, DeX) on a Lineage foundation.

## Sync

```bash
repo init -u https://github.com/Penguin-OS-LINEAGE-OS-BASE/manifest -b lineage-24.0
repo sync
```

Lineage-style manifest repo: `default.xml` + `snippets/lineage.xml`.
Our forks are pinned inline via the `penguin` remote; everything else
tracks LineageOS (`lineage` remote) or AOSP.

## Build

```bash
source build/envsetup.sh
lunch penguin_<device>-userdebug
m
```

Device trees point at `vendor/penguin` (not `vendor/lineage`, not `vendor/aospa`).

## Layout

- `default.xml` — full project list (Lineage upstream + our forks:
  `frameworks/base` on `penguin-qs`, `vendor/penguin`, Dialer, PenguinSystemUI…)
- `snippets/lineage.xml` — Lineage additions, rerouted to our org where forked

## Status

v1: QS panel + bootable base. Settings, Launcher, island, volume panel and
DeX framework pieces land as follow-up branches (see PORT_MAP in the
workspace). First builds may surface Dagger/Kotlin nits in the QS hook
files — they are additive-only and isolated to SystemUI.

## Credits

LineageOS and AOSPA for the foundation; PenguinOS team for the panel,
Laboratory, DeX and design work.
