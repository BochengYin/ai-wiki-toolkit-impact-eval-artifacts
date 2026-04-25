Diagnosed and fixed the Windows ARM smoke failure. The workflow was comparing `--version` output to bare `0.1.16`, but the CLI contract is `ai-wiki-toolkit 0.1.16`.

Updated:
- [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s03/.github/workflows/release-smoke-windows-arm.yml:84): both binary and npm smoke paths now compare against `ai-wiki-toolkit <package_version>`.
- [tests/test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s03/tests/test_release_smoke_workflow.py:31): added coverage for the prefixed expected output and guards against the old bare-version comparison.

Verification:
- `uv run pytest tests/test_release_smoke_workflow.py` -> 2 passed
- `uv run pytest` -> 136 passed, 1 skipped
- `npm pack --dry-run --ignore-scripts` -> succeeded
- `git diff --check` -> clean

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/linux-musl-pyinstaller-needs-binutils-objdump, features/index, workflows, trails/index, trails/2026-04-18-release-workflow-and-prompt-block-edge-cases, people/bochengyin/drafts/windows-arm-smoke-version-checks-need-full-cli-output  
AI Wiki Material Effects: reused_convention, followed_repo_workflow, checked_release_history  
AI Wiki Missed Memory: people/bochengyin/drafts/windows-arm-smoke-version-checks-need-full-cli-output was found during the end check after the fix  
AI Wiki Update Candidate: None