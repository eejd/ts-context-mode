# Local patches carried on `local`

Fork of `mksglu/context-mode` (primary upstream). `main` mirrors upstream's default branch;
`local` is the latest upstream release plus the work below, tagged `v<base>-local<NN>`
(docs/development-model.md in eejd/macports-ports-local, "Forks, upstreams and port tiers").

| Change | Branch | Upstream status |
|---|---|---|
| Standalone installs (MacPorts, npm global) get `mcp__context-mode__<tool>` names in hook guidance when `CLAUDE_PLUGIN_ROOT` is absent; plugin installs keep the plugin-namespaced form | `topic/standalone-tool-prefix` | not submitted |

## Retired

- `fix(upgrade): skip settings.json wiring only for true plugin installs` (the former
  `v1.0.169-patch1`): the same fix is merged upstream (mksglu/context-mode `7cc9d3be`, #810, same
  author) and is in `v1.0.169`; the fork's copy only regenerated the committed bundles, which
  already carry the gate. Dropped.
- `chore: gitignore npm pack tarballs (*.tgz)`: only served the former release-asset flow
  (`v1.0.169-patch2`). Dropped.
- The old `main` tip (`66091ac9`, three commits ahead of upstream) is preserved as the tag
  `archive/main-pre-sync-66091ac9`.
