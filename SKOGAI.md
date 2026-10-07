---
routes:
  - AGENTS.md
  - CLAUDE.md
  - DEVELOPMENT.md
---

OpenWiki turns a codebase into a linked Markdown wiki that an agent can
search and read for just-in-time context. This checkout is a fork
(`skogai/openwiki`, upstream `langchain-ai/openwiki`) vendored into the
skogai monorepo.

For contribution rules, build/test commands, and how this repo's own
generated `openwiki/` evidence index should be used, don't read this
file further — go to `AGENTS.md` (`CLAUDE.md` just routes there) and
`DEVELOPMENT.md`.

Why this fork is vendored here, and the skogai-specific angle on it, is
undocumented in this repo — nothing in-tree explains it. The
`openwiki` MCP server registered elsewhere in the skogai monorepo runs
as a locally spawned `openwiki mcp` subcommand (see `src/cli/commands.ts`),
not a hosted service; if it fails to connect, that points at the local
`openwiki` install/build in this environment rather than this repo's code.
