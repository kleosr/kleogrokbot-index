# Agent Handbook

This handbook is the single canonical source of truth for coding agents operating in this repository. All agents follow the rules and workflows defined here.

## Rules

- **Scope & Codebase Nature**: This repository (`kleogrokbot-index`) is a static coming-soon landing page consisting of `index.html`, `grok-logo.svg`, `README.md`, and `.gitignore`. There is currently no build system, package manager, or compilation step.
- **Minimal Changes**: Keep changes minimal, focused, and scoped strictly to the task. Do not rewrite existing landing page markup or styles unless explicitly instructed.
- **Grounding & Evidence**: Encode only what is verified in the repository. Do not invent scripts, dependencies, build configurations, or operational conventions that do not exist.
- **Git & Branches**: Work on feature branches prefixed with `cursor/` and suffixed with `-a2aa` (e.g. `cursor/<descriptive-name>-a2aa`). Commit with clear, descriptive messages. Never force-push or rewrite public history.
- **Pull Requests**: Open pull requests against `main` using repository-standard branch workflows. Ensure all PR descriptions detail what was changed, what was excluded, and how the changes were verified.
- **No Unused Vendor Files**: Vendor adapter files (`CLAUDE.md`, `.cursorrules`, etc.) must only exist if that specific tool is actively adopted in the repo, and must remain thin adapters pointing to `AGENTS.md`.

## Skills

Reusable task recipes belong in `.agents/skills/`.

- Currently, this repository does not define custom agent skills in `.agents/skills/`.
- If custom skills are added in the future, document their interface and entry points here.

## Workflows

### Local Inspection & Verification
Because there are no Node, Rust, Python, or Makefile build steps in this repo:
- Inspect changes directly in the static files (`index.html`, `grok-logo.svg`, `README.md`).
- Validate HTML structure and syntax directly or via standard static file checks if added.
- Verify git status and diffs using standard git operations:
  ```bash
  git status
  git diff
  ```

### Development & Review Flow
1. Check out a dedicated branch: `git checkout -b cursor/<task-name>-a2aa`.
2. Inspect the existing files before editing.
3. Keep edits surgical and preserve the existing minimalist design.
4. Stage and commit changes:
  ```bash
  git add <files>
  git commit -m "Clear and descriptive commit message"
  ```
5. Push the branch and open a PR against `main`.

## Memory

Project memory is maintained in versioned markdown files under `docs/`.

- This repository currently does not have a `docs/` directory or existing markdown memory files.
- Vendor-specific proprietary memory systems must not be used; any long-term memory or architectural decision records should be committed as plain markdown files under `docs/` when introduced.
