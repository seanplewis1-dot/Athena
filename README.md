# Athena

A 3D first-person zombies FPS built in Unreal Engine 5.8. Solo-dev project, currently a mechanics foundation: movement, combat, inventory, health, and enemy systems.

## Layout

- `Source/Athena/` — core C++: first-person character, game mode, player controller, camera manager (First Person template base)
- `Source/Athena/Variant_Shooter/` — shooter sample code: weapons, projectiles, pickups, AI (StateTree), NPC spawner, EQS
- `Source/Athena/Variant_Horror/` — horror sample code (kept for reference, not in active scope)
- `Content/` — FirstPerson template content, mannequin characters (placeholder enemies), weapons, variant maps

## Building

Open `Athena.uproject` in Unreal Engine 5.8. The editor generates project files and builds the `Athena` module on first open.

## Conventions

- Game logic that needs to be reviewed or diffed lives in C++; Blueprints stay thin (wiring, not logic).
- Work lands on branches and gets merged after review — `master` stays playable.
- Large binary assets: this repo does not use Git LFS. Keep `Content/` lean; anything approaching tens of MB per file should be reconsidered.
