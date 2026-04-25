Fixed the Windows ARM smoke failure. The binary and npm-installed wrapper were returning the documented CLI output, `ai-wiki-toolkit <version>`, but the workflow compared that to the bare semver. Both smoke paths now build `$expectedVersion = "ai-wiki-toolkit ${{ steps.release.outputs.package_version }}"` before comparing.

Updated:
- [.github/workflows/release-smoke-windows-arm.yml](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s06/.github/workflows/release-smoke-windows-arm.yml:81)
- [tests/test_release_smoke_workflow.py](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s06/tests/test_release_smoke_workflow.py:31)
- [ai-wiki draft](<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s06/ai-wiki/people/eval-user/drafts/release-smoke-version-checks-must-match-cli-output.md:1)

Verification: `uv run pytest` passes with `137 passed, 1 skipped`.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, decisions, review-patterns/index, problems/index, workflows, trails/index, features/index, people/bochengyin/index, people/bochengyin/drafts/distribution-target-matrix-must-match-published-assets, people/bochengyin/drafts/npm-postinstall-must-not-delete-its-own-download-archive  
AI Wiki Material Effects: changed_plan, guided_release_failure_triage, faster_resolution  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/release-smoke-version-checks-must-match-cli-output.md