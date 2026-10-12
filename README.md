# PenguinOS manifest (Lineage base)

https://github.com/Penguin-OS-LINEAGE-OS-BASE/manifest

`penguin.xml` overrides the Lineage `default.xml` + `snippets/lineage.xml`
with Penguin-OS-LINEAGE-OS-BASE forks.

v1 scope: QS panel + bootable base.
- `frameworks/base` tracks branch `penguin-qs` (additive QS hooks; stock
  behavior without the PenguinSystemUI app).
- `vendor/penguin` provides the product config (ships `PenguinSystemUI`,
  which overrides stock `SystemUI`).
- `packages/apps/PenguinSystemUI` is the Penguin QS panel / Control Centre.

## Sync

```bash
repo init -u https://github.com/Penguin-OS-LINEAGE-OS-BASE/android -b lineage-24.0
mkdir -p .repo/local_manifests
curl -o .repo/local_manifests/penguin.xml \
  https://raw.githubusercontent.com/Penguin-OS-LINEAGE-OS-BASE/manifest/lineage-24.0/penguin.xml
repo sync
```

See `penguin.xml` header for the exact `repo` wiring.
