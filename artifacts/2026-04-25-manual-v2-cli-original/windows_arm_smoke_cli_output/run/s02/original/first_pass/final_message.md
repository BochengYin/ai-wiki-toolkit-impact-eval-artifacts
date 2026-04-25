Fixed on branch `fix/windows-arm-smoke-version-output`.

Root cause: both Windows ARM smoke paths ran `aiwiki-toolkit --version`, which returns `ai-wiki-toolkit <version>`, but the workflow compared that output to the bare package version. I updated both checks in [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s02/.github/workflows/release-smoke-windows-arm.yml:84) to expect the full CLI output string.

I also tightened [tests/test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s02/tests/test_release_smoke_workflow.py:31) so it verifies both the release-archive and npm-installed smoke paths use that full-output comparison.

Verification:
- `UV_CACHE_DIR=/tmp/uv-cache uv run pytest tests/test_release_smoke_workflow.py tests/test_cli_version.py` -> 3 passed
- `UV_CACHE_DIR=/tmp/uv-cache uv run pytest` -> 136 passed, 1 skipped

Recorded the durable workflow lesson at `ai-wiki/people/eval-user/drafts/windows-arm-smoke-version-checks-must-match-cli-output.md`.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/linux-musl-pyinstaller-needs-binutils-objdump, features/index, workflows, trails/index, trails/2026-04-18-release-workflow-and-prompt-block-edge-cases  
AI Wiki Material Effects: reused_convention, followed_release_triage, recorded_problem_solution_draft  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/windows-arm-smoke-version-checks-must-match-cli-output.md