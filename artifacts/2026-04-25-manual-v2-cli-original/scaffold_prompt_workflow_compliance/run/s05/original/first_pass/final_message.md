Implemented the team-memory scaffold expansion.

Key changes:
- Added starter `conventions/`, `problems/`, and `features/` repo wiki areas.
- Added managed `schema/team-memory-v1.md` guidance and updated managed workflow/prompt guidance.
- Added installer templates for `ai-wiki-clarify-before-code` and `ai-wiki-capture-review-learning`.
- Updated `doctor` checks/suggestions, README install docs, and scaffold compatibility tests.

Verification:
- `uv run pytest` passed: `123 passed`
- `git diff --check` passed

AI Wiki Reuse Check: wiki_used  
AI Wiki Reuse Docs: constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index, workflows, trails/index, conventions/package-managed-vs-user-owned-docs, people/bochengyin/drafts/repo-local-codex-skills-should-live-under-dot-agents-skills, people/bochengyin/drafts/toolkit-installed-repo-local-skills-should-skip-existing-files  
AI Wiki Update Candidate: None