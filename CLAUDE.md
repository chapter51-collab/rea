@AGENTS.md

## Claude Code

`AGENTS.md` above is the single source of repository guidance; edit it there,
not here. This file only adds Claude Code specifics.

- Project skills in `.claude/skills/` are symbolic links to
  `.agents/skills/`. Edit the files under `.agents/skills/`; never replace a
  link with a copy. The generated `skills/` directory is an ignored build
  output.
- Load `rea-tool-design` before changing tools, CLI/MCP contracts, provider
  capabilities, or Evidence semantics, and `rea-changelog-update` for release
  notes. `reverse-engineer-anything` is the shipped user-facing skill; use it
  only when actually reverse engineering a target, not for this repository's
  own architecture.
- `turbo` may re-add the managed block at the end of `AGENTS.md`; keep it
  committed rather than deleting it.
- Personal overrides belong in `.claude/settings.local.json` and
  `CLAUDE.local.md`, which are ignored by Git.
