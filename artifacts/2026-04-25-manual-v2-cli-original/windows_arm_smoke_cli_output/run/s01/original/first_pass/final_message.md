Diagnosed and fixed the Windows ARM smoke failure.

The workflow was comparing `--version` output to only `0.1.16`, but the CLI contract is `ai-wiki-toolkit 0.1.16`. That made both the direct release binary and npm-installed smoke paths fail even though the binary existed and ran.

Changed:
- [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s01/.github/workflows/release-smoke-windows-arm.yml:84): compare against `ai-wiki-toolkit ${{ steps.release.outputs.package_version }}`
- [tests/test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s01/tests/test_release_smoke_workflow.py:29): updated workflow coverage for the full expected version line

Verification:
- `python -m pytest tests/test_release_smoke_workflow.py tests/test_cli_version.py` passed
- `python -m pytest` passed: `136 passed, 1 skipped`
- `git diff --check` passed