Implemented the release guard.

- Linux release builds now use `ubuntu-22.04`, then run standalone `--version`, package the archive, and smoke-test the archived binary in `node:24-bookworm` before upload: [.github/workflows/release-binaries.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s06/.github/workflows/release-binaries.yml:36)
- npm publish now packs the Linux platform package plus meta package, installs them through the global wrapper path in `node:24-bookworm`, and runs `aiwiki-toolkit --version` before any `npm publish`: [.github/workflows/publish-npm.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s06/.github/workflows/publish-npm.yml:116)
- Added workflow guardrail tests: [tests/test_distribution_metadata.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s06/tests/test_distribution_metadata.py:67)
- Updated release/npm docs to document the Bookworm runtime gate and Linux glibc baseline.

Verification:
- `python -m pytest` passed: 85 tests
- `npm pack --dry-run --ignore-scripts` passed
- `git diff --check` passed
- `actionlint` was not installed locally

Managed `ai-wiki/_toolkit/system.md` drove the required AI wiki evidence flow.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/package-managed-vs-user-owned-docs, decisions, review-patterns/index, problems/index, features/index, workflows, trails/index, metrics/index  
AI Wiki Material Effects: kept_distribution_source_of_truth, followed_release_workflow, recorded_reuse_evidence  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/linux-release-binaries-need-target-container-runtime-smoke.md