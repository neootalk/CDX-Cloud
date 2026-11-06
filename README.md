# CDX-Cloud

Reusable development environment for **OpenAI Codex** and **Claude Code**. It provides shared AI engineering rules, agent-specific workspace configuration, safe environment templates, setup and verification scripts, and GitHub Actions checks.

## Included

- `AGENTS.md` — canonical shared instructions for AI coding agents.
- `CLAUDE.md` — Claude Code entry point referencing the shared policy.
- `.codex/config.toml` — conservative Codex workspace defaults.
- `.claude/settings.json` — workspace-level Claude Code permission guardrails.
- `.claude/commands/review.md` — `/review` command for read-only code review.
- `.env.example` — safe local environment template; no credentials.
- `scripts/setup.sh` — environment checks and lockfile-aware dependency setup.
- `scripts/verify.sh` — available project checks and secret-ignore validation.
- `.github/workflows/ci.yml` — automated verification on pushes and pull requests.

## Quick start

```bash
git clone https://github.com/neootalk/CDX-Cloud.git
cd CDX-Cloud
npm run setup
npm run verify
```

Copy `.env.example` to `.env` only when the target project needs environment variables. Replace or remove unused placeholders. Never commit real secrets.

## Use in another project

Copy the agent instruction/configuration files that fit the target project. Read the target project's existing instructions first and merge carefully; do not overwrite its established architecture or configuration. Keep project-specific environment variables in that project's own `.env.example`.

## Supported project types

The template is framework-neutral. It can be adapted to HTML/CSS/JavaScript, Node.js, PHP, and Supabase projects. It does not impose a frontend framework, database schema, build system, or deployment provider.

See [`docs/ENVIRONMENT.md`](docs/ENVIRONMENT.md) for setup and security details.

## License

MIT — see [`LICENSE`](LICENSE).
