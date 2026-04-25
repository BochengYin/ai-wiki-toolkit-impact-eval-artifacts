Implemented on branch `feature/2026_04_25_pr_flow_helper`.

Added [scripts/pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s03/scripts/pr_flow.py:1) with:

- `start <branch>`: requires `main`, clean worktree, valid branch name, then creates the branch
- `create [--draft]`: refuses `main`, validates branch name, pushes the branch, opens a PR with `gh`
- `finish`: requires merged PR, switches to `main`, pulls, deletes the local topic branch

Updated [CONTRIBUTING.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s03/CONTRIBUTING.md:17) and [ai-wiki/workflows.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s03/ai-wiki/workflows.md:15) to document the enforced branch forms. Added coverage in [tests/test_pr_flow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s03/tests/test_pr_flow.py:1).

Verification:
`uv run pytest` passed: 135 tests.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index, workflows, index, people/bochengyin/drafts/repo-local-contributor-workflows-should-stay-out-of-the-package-layer  
AI Wiki Material Effects: changed_plan, selected_helper_path, avoided_package_surface  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None