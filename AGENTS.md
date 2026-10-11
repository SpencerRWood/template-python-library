# Repository Guidance

## Purpose and boundaries
- Keep this typed Python library baseline reusable after package rename.
- The template provides packaging and quality gates, not a domain API.

## Development
- Put public library behavior in `src/` and compatibility tests in `tests/`.
- Keep README rename instructions, package metadata, and coverage target aligned.

## Validation
- Run `uv sync --frozen --group dev`, `uv run ruff check .`, `uv run ruff format --check .`, `uv run mypy`, `uv run pytest`, and `uv run pre-commit run --all-files`.
- Run `uv build` for packaging changes.

## Architecture constraints
- Preserve strict typing and the importable `src/` layout.
- Keep sample code generic enough for a new library after rename.

## Safety
- Keep distribution metadata and examples free of personal infrastructure details.

## Branching strategy

- This repository uses **trunk-based development**. Create short-lived change branches from current `main` and target PRs to `main`.
- Follow the [canonical branching and delivery policy](https://github.com/SpencerRWood/codex-config/blob/main/docs/branching-policy.md), available through the installed codex-config source path. Verify the strategy, release association, fetched base and PR target before implementation and record them in Story evidence. Story completion does not authorize publication or deployment; retain existing review, CI, security and rollback requirements.
- This classification applies to maintenance of the template repository. Replace it with the new repository's classification during project creation; applications must use release-branch integration before Story development begins.
