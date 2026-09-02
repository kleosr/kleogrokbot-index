# Agent Handbook

This handbook is the single canonical source of truth for coding agents operating in this repository. All agents follow the rules and workflows defined here.

## Rules

- **Scope & Codebase Nature**: This repository (`kleogrokbot-index`) is a static coming-soon landing page consisting strictly of `index.html`, `grok-logo.svg`, `README.md`, and `.gitignore`.
- **No Build Step**: There is no build system, package manager, compiler, or test framework. Do not introduce dependencies or build scripts unless explicitly instructed.
- **Minimal Changes**: Keep changes minimal, focused, and scoped strictly to the task. Do not rewrite existing landing page markup, styles, or SVG assets unless requested.
- **Grounding & Evidence**: Encode only what is verified in the repository. Do not invent operational conventions, tools, or configurations that do not exist.
- **No Unused Vendor Files**: Vendor adapter files (`CLAUDE.md`, `.cursorrules`, etc.) must not be added unless that specific tool is actively adopted in the repository. If introduced, they must remain thin adapters pointing to `AGENTS.md`.

## Skills

Reusable task recipes belong in `.agents/skills/`.

- Currently, this repository does not define custom agent skills in `.agents/skills/`.
- Do not create `.agents/skills/` until task recipes are added to the repo.

## Workflows

- **Verification**: Because there are no automated build or test pipelines, verification is done by directly inspecting the static files (`index.html`, `grok-logo.svg`, `README.md`) and checking diffs with `git diff`.
- **Editing**: Make targeted edits directly to the relevant static files. Preserve the existing styling, dark theme, and minimalist structure.

## Memory

Project memory is maintained in versioned markdown files under `docs/`.

- This repository currently does not have a `docs/` directory or existing markdown memory files. Do not create `docs/` until memory or documentation files are introduced.
- Never use vendor-specific proprietary memory systems.
