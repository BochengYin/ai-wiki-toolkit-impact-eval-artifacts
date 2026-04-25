Implemented the team-memory scaffold extension.

Changed:
- Added repo-local starter areas: `ai-wiki/conventions/`, `ai-wiki/problem-solutions/`, and `ai-wiki/features/`.
- Added managed schema guidance: `ai-wiki/_toolkit/schema/team-memory-v1.md`.
- Added repo-local starter skills for clarification and PR review learning under `.agents/skills/`.
- Updated managed prompt guidance, installer scaffolding, catalog classification, doctor checks, README, and doctor proposal docs.
- Expanded tests for scaffold snapshots, user-owned overwrite protection, installer behavior, catalog kinds, doctor suggestions, and schema guidance.

Verification:
- `uv run pytest` passed: `124 passed`
- `git diff --check` passed

The changes preserve the existing boundary: user-owned AI wiki docs are only created when missing, while `_toolkit/**` remains the refreshable managed layer.