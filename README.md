# PenguinOS manifest overlay (Lineage base)

`penguin.xml` overrides the Lineage `default.xml` + `snippets/lineage.xml`
with Penguin-OS-LINEAGE-OS-BASE forks.

v1 scope: QS panel + bootable base.
- `frameworks/base` tracks branch `penguin-qs` (additive QS hooks; stock
  behavior without the PenguinSystemUI app).
- `vendor/penguin` provides the product config (ships `PenguinSystemUI`,
  which overrides stock `SystemUI`).
- `packages/apps/PenguinSystemUI` is the Penguin QS panel / Control Centre.

Sync: include this repo's `penguin.xml` after Lineage's `default.xml`.
See `penguin.xml` header for the exact `repo` wiring.
