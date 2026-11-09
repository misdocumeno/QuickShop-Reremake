# Release tags (misplease QuickShop-Reremake fork)

Permanent fork: buy-from-shulker (and any other) patches on the Reremake line.

Upstream version we keep is the Reremake **pluginver** (`5.1.2.5` in `pom.xml` today), not Hikari’s `6.3.x`.

```text
v{pluginver}-misplease.{N}
```

Examples:

- first ship of our patches on `5.1.2.5` → `v5.1.2.5-misplease.1`
- next change on same base → `v5.1.2.5-misplease.2`
- after bumping `pluginver` to match a newer upstream base → `v5.1.2.6-misplease.1`

Jars:

- Upstream / stock Reremake: `QuickShop-5.1.2.5.jar` (or whatever Maven produces for that `pluginver`).
- Ours: same build pipeline, our commits; release tag `v5.1.2.5-misplease.N`. Older tag `v5.1.2.5-shulker` was a one-off name — prefer `-misplease.N` going forward.

Rules: never re-use a tag; never overwrite assets; bump then `plugin-lock update --only QuickShop` (or the lock name you use).
