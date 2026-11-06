# Claude Code Instructions

Read and follow [`AGENTS.md`](./AGENTS.md) as the canonical project-wide engineering policy.

Before editing, inspect the repository and any more-specific `AGENTS.md` or `CLAUDE.md` files in the target directory. Follow the most specific applicable instructions without violating the root policy.

Use a minimal-diff workflow: inspect → plan scope → edit only necessary files → run relevant checks → review the diff → report verified results. Preserve existing architecture and behavior. Do not invent dependencies, secrets, schemas, endpoints, or deployment outcomes.

Do not run destructive commands, alter production infrastructure, publish releases, or change remote settings unless the user explicitly requests that action.
