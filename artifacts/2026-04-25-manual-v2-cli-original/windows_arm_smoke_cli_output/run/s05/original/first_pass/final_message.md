Diagnosed and fixed the Windows ARM smoke failure. Both jobs were comparing `--version` output to the bare package version, but the CLI prints `ai-wiki-toolkit <version>`.

Changed [release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s05/.github/workflows/release-smoke-windows-arm.yml:84) so both the release archive smoke path and npm-installed smoke path compare against the full CLI output. Added regression coverage in [test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s05/tests/test_release_smoke_workflow.py:33).

Verification:
`uv run pytest` passed: 137 passed, 1 skipped.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/windows-arm-smoke-version-checks-need-full-cli-output, workflows  
AI Wiki Material Effects: reused_problem_note, reused_convention, followed_workflow  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None