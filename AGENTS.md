# Repository Guidelines

## Project Structure & Module Organization

This repository is at its initial stage and currently contains only `README.md`.
Keep the root focused on project metadata and configuration. As implementation is
added, prefer a simple layout:

- `src/` for application or library source code.
- `tests/` for automated tests that mirror `src/` structure.
- `assets/` for static files, fixtures, or sample data.
- `docs/` for longer design notes or contributor documentation.

Update this guide when the actual structure or toolchain changes.

## Build, Test, and Development Commands

No build system, package manager, or test runner is configured yet. Do not invent
project commands without adding the corresponding configuration files.

Useful repository commands:

- `git status --short` checks local changes before editing or committing.
- `git log --oneline -n 12` reviews recent commit style.
- `cat README.md` verifies the current project description.

When a language stack is introduced, document the exact setup, run, build, lint,
and test commands here.

## Coding Style & Naming Conventions

Follow the conventions of the language and framework added to the project. Until
tooling exists, keep files small, readable, and consistently formatted. Use
descriptive names for modules and tests, such as `src/evaluator.*` and
`tests/evaluator_test.*`, matching the chosen ecosystem.

Prefer automated formatting and linting once a stack is selected, and commit the
formatter or linter configuration with the first code changes.

## Testing Guidelines

There is no test framework configured yet. New functionality should include
automated tests in `tests/` or the standard test location for the chosen stack.
Name tests after the behavior under test, and keep fixtures isolated from source
code. Add the canonical test command to this document when tests are introduced.

## Commit & Pull Request Guidelines

The current history uses a Conventional Commit-style message:
`feat: Project started`. Continue with concise, imperative messages such as
`feat: add evaluator entrypoint`, `fix: handle empty input`, or
`docs: expand setup instructions`.

Pull requests should include a brief summary, the reason for the change, test
results or a note explaining why tests are not applicable, and screenshots only
when UI changes are involved. Link related issues when available.
