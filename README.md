# PenguinOS manifest (Lineage base)

https://github.com/Penguin-OS-LINEAGE-OS-BASE/manifest

Lineage-style manifest repo: `repo init` straight against it.
Our forks are pinned inline (`penguin` remote); everything else tracks
LineageOS (`lineage` remote) or AOSP.

Scope: QS panel + bootable base.
- `frameworks/base` tracks branch `penguin-qs` (additive QS hooks; stock
  behavior without the PenguinSystemUI app).
- `vendor/penguin` provides the product config (ships `PenguinSystemUI`,
  which overrides stock `SystemUI`).
- `packages/apps/PenguinSystemUI` is the Penguin QS panel / Control Centre.

## Sync

```bash
repo init -u https://github.com/Penguin-OS-LINEAGE-OS-BASE/manifest -b lineage-24.0
repo sync
```
