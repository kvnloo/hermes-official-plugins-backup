# Detached mirror of [NousResearch/hermes-official-plugins](https://github.com/NousResearch/hermes-official-plugins)

A backup that has **left the fork network**: it survives upstream being deleted, made private or taken down.

- Upstream branches and tags are under their normal names. This branch (`_mirror`) only holds the sync workflow.
- Rewritten or deleted upstream refs are kept under `_gone/<name>-<date>`. Nothing is ever dropped.
- Each run also fast-forwards [kvnloo/hermes-official-plugins](https://github.com/kvnloo/hermes-official-plugins) `main` (FF only, never force).
- Problems show up as issues labelled `mirror-alert`.

Sync logic: kvnloo/home tools/fork-standard (private). Git LFS objects aren't mirrored (pointer files only).
