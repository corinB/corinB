# Repository Guidelines

## Project Structure & Module Organization
The repository currently centres on `README.md`, which presents the public profile. Place reusable assets in `assets/` (images, diagrams) and additional long-form notes in `docs/`. If prototypes or sample code are added, prefer `src/<domain>` and mirror tests under `tests/<domain>` so contributors can navigate quickly.

## Build, Test, and Development Commands
Use Markdown tooling to keep docs consistent. Install once with `npm install` to pull linting utilities. Run `npm run lint:md` (or `npx markdownlint "**/*.md"`) before opening a pull request. For link validation, run `npx markdown-link-check README.md` to catch stale URLs.

## Coding Style & Naming Conventions
Write in concise English with optional Korean context to match the README tone. Headings should use ATX style (`#`), with title case at level one and sentence case elsewhere. Keep emoji usage purposeful and group badges in logical rows. Name media files descriptively (`assets/jetson-nano-demo.png`) and store code snippets in fenced blocks tagged with the language (` ```python `). Preserve 120-character line wrapping for readability.

## Testing Guidelines
Treat lint passes as required tests. Ensure all Markdown files pass `markdownlint` with no warnings, and add comments disabling a rule only when justified inline. When contributing sample code, add lightweight unit checks in `tests/` and document how to execute them so others can reproduce results.

## Commit & Pull Request Guidelines
Commits in this project are short and imperative (e.g., `Update README.md`); follow that style but expand the verb to describe the change (`Add CV links`, `Refine badges`). Include scoped commits rather than batching unrelated edits. Pull requests should link any relevant issue, list screenshots for visual changes, and confirm lint commands were run. Provide a brief checklist outlining what reviewers should verify before merging.
