# Contributing to awesome-apm

awesome-apm is a curated index of [APM](https://github.com/microsoft/apm)-native packages. We accept PR submissions for entries that meet the criteria below.

## What we accept

- **APM-installable packages** — the source repo must have a valid `apm.yml` (or compatible `.claude-plugin/marketplace.json`) and resolve cleanly under `apm install <owner>/<repo>`.
- **Public GitHub repo** — private or non-GitHub hosts are out of scope for v0.x.
- **OSI license** — MIT, Apache-2.0, BSD-2/3-Clause, or another OSI-approved license. Send an issue first if you're unsure.
- **A tagged release** — recommended but not required. Pinned `#ref` installs prevent drift.

## What we don't accept

- **Generic LLM tasks** without methodological uplift (matches the [`github/awesome-copilot`](https://github.com/github/awesome-copilot) policy)
- **Paid services** as a hard dependency
- **Malicious or RAI-violating content**
- **Duplicates** of existing entries

## How to submit

1. Fork this repo.
2. Add your entry to `apm.yml` under `marketplace.packages`. Follow the schema of existing entries — `name`, `description`, `source`, `homepage`, `version`, `license`, `keywords` (~6–10 lowercase hyphenated terms).
3. Mirror the entry into `.claude-plugin/marketplace.json` so APM clients can read both files. Both files must stay in sync.
4. Open a PR with title `[Add Plugin]: <name>`.

## Entry shape (copy-paste template)

```yaml
- name: your-plugin-name
  description: One or two sentences. What it is + what users can do.
  source: owner/repo
  homepage: https://github.com/owner/repo
  version: 1.0.0
  license: MIT
  keywords:
    - keyword1
    - keyword2
```

```json
{
  "name": "your-plugin-name",
  "description": "...",
  "version": "1.0.0",
  "license": "MIT",
  "author": { "name": "...", "url": "..." },
  "repository": "https://github.com/owner/repo",
  "homepage": "https://github.com/owner/repo",
  "keywords": ["..."],
  "source": {
    "source": "github",
    "repo": "owner/repo",
    "ref": "refs/tags/vX.Y.Z"
  }
}
```

## Review

Reviews are best-effort by [@Avyayalaya](https://github.com/Avyayalaya). Expect days, not minutes. If your PR sits idle for >7 days, comment on it.

## License

Submissions are accepted under [MIT](LICENSE).
