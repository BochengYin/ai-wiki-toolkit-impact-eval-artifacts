Implemented the team coding memory scaffold.

Changes include:
- New repo starter areas: `ai-wiki/conventions/`, `ai-wiki/problems/`, `ai-wiki/features/`
- New managed schema: `ai-wiki/_toolkit/schema/team-memory-v1.md`
- New repo-local skills: `ai-wiki-clarify-before-code` and `ai-wiki-capture-review-learning`
- Updated managed prompt/system/workflow guidance, README, doctor checks, catalog doc kinds, and scaffold tests
- Preserved create-if-missing behavior for user-owned wiki docs and skip-if-existing behavior for repo-local skill files

Verification:
- `uv run pytest -q` passed
- `git diff --check` passed
- `uv` printed the existing `VIRTUAL_ENV` mismatch warning, but tests completed successfully

Managed AI wiki docs that shaped the implementation: `ai-wiki/_toolkit/system.md` and `ai-wiki/_toolkit/schema/team-memory-v1.md` were used as managed guidance and not logged as reuse events.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: constraints, conventions/package-managed-vs-user-owned-docs, decisions, workflows, people/bochengyin/drafts/repo-local-codex-skills-should-live-under-dot-agents-skills, conventions/index, problems/index, features/index, review-patterns/index, index  
AI Wiki Material Effects: changed_plan, reused_constraint, reused_workflow, reused_structure  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None