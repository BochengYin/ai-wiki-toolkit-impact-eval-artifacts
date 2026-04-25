Implemented the team-memory scaffold expansion.

Key changes:
- Added starter repo areas for `conventions/`, `problems/`, and `features/`.
- Added installer-created skills for `ai-wiki-clarify-before-code` and `ai-wiki-capture-review-learning`.
- Added managed `schema/team-memory-v1.md` guidance.
- Updated managed prompt guidance, doctor checks, catalog doc-kind inference, README, and tests.
- Preserved create-only behavior for user-owned AI wiki docs; managed refreshes stay under `_toolkit/**`.

Verification passed:
- `python -m pytest -q`
- `git diff --check`

`ai-wiki/_toolkit/system.md` materially guided the ownership and end-of-task behavior, so I cited it here but did not log it as reuse.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index, conventions/distribution-target-matrix-must-match-published-assets, problems/windows-arm-smoke-version-checks-need-full-cli-output, problems/linux-musl-pyinstaller-needs-binutils-objdump  
AI Wiki Material Effects: changed_plan, reused_convention, blocked_wrong_path  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None