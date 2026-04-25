Implemented the contributor branch-and-PR helper.

Added [pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s04/src/ai_wiki_toolkit/pr_flow.py:1) with `start`, `create`, and `finish` flows, plus the repo-local wrapper [scripts/pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s04/scripts/pr_flow.py:1). The helper enforces `feature|chore|fix/YYYY_MM_DD_description`, blocks PR creation from `main`, pushes and verifies the remote branch, opens the PR with `gh`, and only switches back to `main` after `gh` reports the PR is merged.

Updated [CONTRIBUTING.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s04/CONTRIBUTING.md:17) with the helper workflow and added tests in [test_pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s04/tests/test_pr_flow.py:1).

Verification:
- `uv run pytest tests/test_pr_flow.py` passed: 17 tests
- `uv run pytest` passed: 135 tests
- `uv run python scripts/pr_flow.py --help` passed
- `git diff --check` passed

I also recorded a local AI wiki draft for the durable workflow refinement: [contributor-pr-flow-helper-enforces-dated-branch-names.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s04/ai-wiki/people/eval-user/drafts/contributor-pr-flow-helper-enforces-dated-branch-names.md:1).

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, workflows, features/index, problems/index  
AI Wiki Material Effects: changed_plan, reused_workflow, preserved_boundary, guided_search  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/contributor-pr-flow-helper-enforces-dated-branch-names.md