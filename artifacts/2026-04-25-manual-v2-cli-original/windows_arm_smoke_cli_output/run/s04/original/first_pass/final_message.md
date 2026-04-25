Fixed the Windows ARM smoke workflow version checks.

Both smoke paths now compare `--version` against the actual CLI output format, `ai-wiki-toolkit <version>`, instead of the bare package version:
- [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s04/.github/workflows/release-smoke-windows-arm.yml:84)
- [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s04/.github/workflows/release-smoke-windows-arm.yml:152)

I also added regression coverage so the workflow must keep checking the full CLI version string in both the release-archive and npm-installed paths:
- [tests/test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s04/tests/test_release_smoke_workflow.py:33)

Verification:
- `uv run pytest tests/test_release_smoke_workflow.py tests/test_cli_version.py` passed
- `uv run pytest` passed: `137 passed, 1 skipped`
- `git diff --check` passed

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/windows-arm-smoke-version-checks-need-full-cli-output, features/index, workflows, trails/index  
AI Wiki Material Effects: reused existing Windows ARM smoke diagnosis, aligned release smoke check with distribution convention, scoped release-facing tests  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None