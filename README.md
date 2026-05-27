# awesome-apm

A curated index of [**APM**](https://github.com/microsoft/apm)-native packages. Add this marketplace once, then `apm search` and `apm install` across the indexed packages from any compatible harness — GitHub Copilot CLI, Claude Code, Cursor, OpenCode, Codex, Gemini.

## Why this exists

APM (the [Agent Package Manager](https://github.com/microsoft/apm)) solves the install primitive beautifully — `apm install <owner>/<repo>` works from any GitHub repo with an `apm.yml`, across every compatible AI harness, with a manifest and lockfile and policy support. What APM doesn't ship yet: a central index. `apm search` works only against a marketplace you've already added. The canonical aggregator the APM README cites is [`github/awesome-copilot`](https://github.com/github/awesome-copilot) — broad, valuable, and intentionally generic across GH Copilot tooling.

`awesome-apm` is a sibling — narrower scope, APM-native focus. Every entry here is a package with a valid `apm.yml` or compatible manifest, installable via `apm install <owner>/<repo>`.

## Use it

```bash
# Register the marketplace (first time only)
apm marketplace add Avyayalaya/awesome-apm

# Search across listed packages
apm search competitive@awesome-apm
apm search azure@awesome-apm

# Install a package (resolves to the source repo)
apm install pm-skills@awesome-apm
apm install azure@awesome-apm
apm install agent-council@awesome-apm
```

## What's listed (v0.2.0)

| Name | Source | Domain | License |
|---|---|---|---|
| `pm-skills` | [`Avyayalaya/pm-skills-arsenal`](https://github.com/Avyayalaya/pm-skills-arsenal) | Product management methodology (12 skills + MCP server + composes_with frontmatter for cross-package routing) | MIT |
| `azure` | [`microsoft/azure-skills`](https://github.com/microsoft/azure-skills) | Azure cloud operations (Microsoft's official Azure capability layer — 27 skills + MCP + Foundry integration) | MIT |
| `agent-council` | [`Avyayalaya/agent-council`](https://github.com/Avyayalaya/agent-council) | Multi-agent quality gate for tier-1 text artifacts (5-deliberator SHIP / REVISE / HOLD adjudication, 4 runtime adapters, bundled MCP + slash commands) | MIT |

awesome-apm is curated, not crowdsourced. v0.2.0 adds `agent-council` — the first quality-gate domain on the index (existing domains are execution / analysis layers). More entries are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) for the PR submission process.

## How to submit a package

1. Confirm your package is **APM-installable** — has a valid `apm.yml` at the repo root or under `.github/plugins/<name>/`, points at real skill files / MCP servers / hooks, has a tagged release.
2. Open a PR against `apm.yml` here adding your entry in the `marketplace.packages` block. The entry shape mirrors the [awesome-copilot external plugins schema](https://github.com/github/awesome-copilot/blob/main/CONTRIBUTING.md#adding-external-plugins).
3. CI runs `apm marketplace check` to verify the source resolves.
4. Curation is non-quality-grading. Listed if: APM-installable, MIT/Apache/BSD-style license, public GitHub repo, not malicious. The reader decides quality.

## What's NOT in scope

- **No managed hosting / paid services** — awesome-apm is a static repo and stays that way.
- **No quality benchmarking** — see each package's own benchmarks.
- **No automation / scrapers** — entries arrive via PR. Curation is intentional.
- **No competing with `github/awesome-copilot`** — they cover the broader Copilot tooling space; this is APM-native specifically.

## License

[MIT](LICENSE)

## Author

[@Avyayalaya](https://github.com/Avyayalaya) — personal research, separate from my day-job at Microsoft.
