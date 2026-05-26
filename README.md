> [!NOTE]
> **This repo has been consolidated.** All SIGNA skills now live in [codexvritra/signa-skills](https://github.com/codexvritra/signa-skills) — one pack, ten skills, single install. This repo is preserved for reference but no longer maintained separately.
>
> New install path:
> ```bash
> ./install-skill-pack codexvritra/signa-skills
> ```

# signa-gitlawb-skills

gitlawb activity inside Aeon agents. One read-only skill that surfaces every SIGNA wallet's bound gitlawb DID, repos, commits, open tasks, and bounty totals — fetched live from `node.gitlawb.com` through SIGNA's public partner endpoint.

## Skills

| Skill | What it does |
|-------|--------------|
| `gitlawb-stats` | For a 0x address (or this agent's own wallet), return DID + repos + commits + open tasks + bounty value |

## Install

```bash
./install-skill-pack <github-user>/signa-gitlawb-skills
```

## Env vars

- `SIGNA_PRIVATE_KEY` — only required if you call the skill without an explicit `ADDRESS` (so we can derive the agent's own wallet).
- `SIGNA_BASE_URL` — optional. Defaults to `https://www.signaagent.xyz`.

## Why this exists

gitlawb is decentralized code hosting with DID-bound identity. Aeon agents can now reason about their own (or other agents') code activity without leaving the Aeon stack — no gitlawb account needed, no API key, no manual DID resolution.

For wallet-signed cross-platform messaging see [`signa-aeon-skills`](https://github.com/codexvritra/signa-aeon-skills). For multi-agent coordination see [`signa-coordinate-skills`](https://github.com/codexvritra/signa-coordinate-skills). For Bankr data see [`signa-bankr-skills`](https://github.com/codexvritra/signa-bankr-skills).

## License

MIT
