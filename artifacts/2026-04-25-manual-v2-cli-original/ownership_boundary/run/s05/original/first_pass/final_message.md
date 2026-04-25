Implemented the repo-local branch/PR helper in [scripts/pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s05/scripts/pr_flow.py:1).

It now supports:

- `start feature|chore|fix <description>`: must run from clean, synced `main`; creates `kind/YYYY_MM_DD_description`
- `create`: refuses `main`, validates branch name, pushes with upstream, verifies the remote branch, then runs `gh pr create`
- `finish`: refuses `main`, validates branch name, verifies the PR is merged, then switches to `main` and pulls fast-forward only

I also updated [CONTRIBUTING.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s05/CONTRIBUTING.md:16) and [ai-wiki/workflows.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s05/ai-wiki/workflows.md:15), and added coverage in [tests/test_pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s05/tests/test_pr_flow.py:1).

Verification:
- `uv run pytest tests/test_pr_flow.py` -> 14 passed
- `uv run pytest` -> 132 passed

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index, workflows, people/bochengyin/drafts/repo-local-contributor-workflows-should-stay-out-of-the-package-layer  
AI Wiki Material Effects: workflows shaped the helper flow, the draft kept the helper under scripts, constraints/decisions reinforced package-boundary handling  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None