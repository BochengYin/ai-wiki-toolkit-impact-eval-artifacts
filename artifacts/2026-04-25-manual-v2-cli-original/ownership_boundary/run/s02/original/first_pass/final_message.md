Added the repo-local PR flow helper on branch `feature/2026_04_25_pr_flow_helper`.

Implemented [scripts/pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s02/scripts/pr_flow.py:14) with `start`, `create`, and `finish` commands. It enforces `feature|chore|fix/YYYY_MM_DD_description`, refuses PR creation from `main`, pushes/verifies the topic branch, opens the PR through `gh`, and only returns to `main` after the PR is merged.

Updated [CONTRIBUTING.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s02/CONTRIBUTING.md:20) with the helper workflow and added focused tests in [tests/test_pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s02/tests/test_pr_flow.py:29).

Verification:
- `uv run pytest tests/test_pr_flow.py` passed: 7 tests
- `UV_CACHE_DIR=/tmp/uv-cache uv run pytest` passed: 125 tests
- `git diff --check` passed

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index, workflows, trails/index, people/bochengyin/drafts/impact-eval-no-target-aiwiki-slots-must-exclude-task-specific-workflow-memory, people/bochengyin/drafts/adjacent-consolidated-guidance-can-underperform-task-specific-raw-drafts-in-impact-evals  
AI Wiki Material Effects: changed_plan, chose_repo_local_script, preserved_ownership_boundary, confirmed_repo_local_surface, avoided_package_surface  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/contributor-pr-flow-uses-dated-feature-chore-fix-branches.md