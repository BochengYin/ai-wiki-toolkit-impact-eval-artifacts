Implemented the Linux runtime compatibility guard.

Changed [release-binaries.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s05/.github/workflows/release-binaries.yml:36) so `linux-x64` builds on `ubuntu-22.04`, records the glibc baseline, and must pass a new Linux runtime smoke job in `ubuntu:22.04` and `node:24-bookworm` before GitHub Release assets upload.

Changed [publish-npm.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s05/.github/workflows/publish-npm.yml:116) so the npm publish workflow packs the local Linux platform package plus meta package, installs them globally inside `node:24-bookworm` linux/amd64, and runs `aiwiki-toolkit --version` before any npm publish step.

Updated docs in [docs/releasing.md](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s05/docs/releasing.md:35) and [docs/npm-publish.md](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s05/docs/npm-publish.md:81), and added workflow guardrail tests in [tests/test_distribution_metadata.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s05/tests/test_distribution_metadata.py:69).

Verification:
- `python -m pytest` passed: 86 tests.
- `npm_config_cache=/tmp/aiwiki-npm-cache npm pack --dry-run --ignore-scripts` passed.
- Default `npm pack` hit a local `<home>/.npm` cache permission issue, so I used an isolated temp cache rather than changing ownership.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline, workflows  
AI Wiki Material Effects: changed_plan, reused_convention, followed_workflow  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None