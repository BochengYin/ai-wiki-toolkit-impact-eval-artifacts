Implemented a repo-local contributor workflow helper.

Changed:
- Added branch naming and workflow validation in [contributor_workflow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s06/src/ai_wiki_toolkit/contributor_workflow.py:8).
- Added `scripts/contributor_pr.py` with `start`, `push`, `finish`, and `validate` commands in [contributor_pr.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s06/scripts/contributor_pr.py:70).
- Documented the workflow in [README.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s06/README.md:147).
- Added unit and real-git integration coverage in [test_contributor_pr_script.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s06/tests/test_contributor_pr_script.py:47).

Verified:
`python -m pytest` -> 130 passed.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, review-patterns/index, problems/index, features/index  
AI Wiki Material Effects: changed_plan, test_coverage  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None