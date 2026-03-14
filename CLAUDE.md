# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

## Repository Overview

**Repository:** `yanehr/claude-lab`
**Status:** Freshly initialized — no source files yet.

This is a lab/experimental repository. As the codebase grows, update this file to reflect the actual structure, tooling, and conventions.

## Current State

The repository contains only this `CLAUDE.md` file. There is no application code, build system, or test suite yet.

When the project gains structure, document the following sections accordingly:

- Project purpose and architecture
- Directory layout
- Build and run commands
- Test commands
- Linting and formatting rules
- Dependency management

## Git Workflow

### Branch Naming

- Feature branches: `feature/<short-description>`
- Bug fixes: `fix/<short-description>`
- Claude-generated branches: `claude/<task-description>-<session-id>`

### Commits

- Write clear, imperative commit messages (e.g. "Add user authentication module")
- Keep commits focused; one logical change per commit
- Do not commit secrets, credentials, or large binaries

### Pushing

Always push with tracking:

```bash
git push -u origin <branch-name>
```

Never force-push to `main` or `master`.

## Development Conventions

### General

- Prefer editing existing files over creating new ones
- Do not add dead code, unused imports, or speculative abstractions
- Only add comments where logic is non-obvious
- Validate at system boundaries (user input, external APIs); trust internal code

### Security

- Never introduce command injection, XSS, SQL injection, or other OWASP Top 10 vulnerabilities
- Do not commit `.env` files or credentials
- Sanitize all user-supplied input before use

## AI Assistant Guidelines

- Read files before editing them
- Do not create files unless strictly necessary
- Keep changes minimal and focused on the task
- Do not refactor surrounding code when fixing a bug
- Do not add docstrings or type hints to code you did not touch
- Confirm before taking irreversible actions (deleting files, force-pushing, etc.)
- Update this `CLAUDE.md` whenever significant structural changes are made to the project

## Updating This File

As the project evolves, keep this file current:

1. Add actual directory structure once source files exist
2. Document the build system and run commands
3. Add test instructions and CI/CD details
4. Record any project-specific conventions or gotchas
