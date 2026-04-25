Implemented the release guard for this runtime class.

Linux `linux-x64` now builds in `python:3.11-bookworm`, then the release archive is executed in `node:24-bookworm` before upload in [.github/workflows/release-binaries.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s02/.github/workflows/release-binaries.yml).

The npm publish workflow now runs a pre-publish Linux install smoke via [scripts/smoke_npm_linux_install.sh](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s02/scripts/smoke_npm_linux_install.sh): it packs the staged `linux-x64` platform package plus the meta package, installs both globally in `node:24-bookworm`, and checks `aiwiki-toolkit --version`.

Docs and release-facing tests were updated in `docs/` and [tests/test_distribution_metadata.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s02/tests/test_distribution_metadata.py).

Verified:
- `python -m pytest` -> 86 passed
- `bash -n scripts/smoke_npm_linux_install.sh`
- `npm pack --dry-run --ignore-scripts`
- `git diff --check`

AI Wiki Reuse Evidence: wiki_used
AI Wiki Eligibility: eligible
AI Wiki Reuse Docs: constraints, conventions/distribution-target-matrix-must-match-published-assets, problems/linux-musl-pyinstaller-needs-binutils-objdump, workflows, people/bochengyin/index
AI Wiki Material Effects: reused_convention, expanded_smoke_coverage, followed_release_workflow_expectations
AI Wiki Missed Memory: none known
AI Wiki Update Candidate: Draft
AI Wiki Update Path: ai-wiki/people/bochengyin/drafts/linux-npm-runtime-compatibility-needs-bookworm-smoke-before-publish.md