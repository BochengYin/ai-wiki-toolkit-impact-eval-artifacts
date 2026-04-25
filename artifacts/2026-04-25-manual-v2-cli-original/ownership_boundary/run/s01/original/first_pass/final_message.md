Implemented on branch `feature/2026_04_25_contributor_pr_helper`.

Added a contributor workflow helper in [contributor_workflow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/src/ai_wiki_toolkit/contributor_workflow.py:14) with enforced branch formats, `main` start checks, push-from-branch checks, and finish-back-to-`main` support. Exposed it as `aiwiki-toolkit contributor branch-name/start/push/finish` in [cli.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/src/ai_wiki_toolkit/cli.py:75).

Updated the contributor docs in [CONTRIBUTING.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/CONTRIBUTING.md:20) and noted the new helper in [CHANGELOG.md](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/CHANGELOG.md:5). Added unit and CLI coverage in [test_contributor_workflow.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/tests/test_contributor_workflow.py:23) and [test_contributor_cli.py](<eval-root>/ownership_boundary/workspaces/20260425-115832/slots/s01/tests/test_contributor_cli.py:10).

Verification:
- `python -m pytest` → `133 passed`
- `git diff --check`
- `PYTHONPATH=src python -m ai_wiki_toolkit.cli contributor branch-name fix "Patch release flow" --date 2026_04_25` → `fix/2026_04_25_patch_release_flow`