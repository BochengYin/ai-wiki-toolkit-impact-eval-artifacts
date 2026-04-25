Implemented the release/npm matrix expansion.

Key changes:
- Expanded `Release Binaries` to build `linux-arm64`, `linux-musl-x64`, `windows-x64`, and `windows-arm64`, with Linux runtime verification for glibc and musl targets in [.github/workflows/release-binaries.yml](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s04/.github/workflows/release-binaries.yml:36).
- Added npm target metadata for Linux ARM64, musl x64, and Windows x64/ARM64 in [npm/platform-targets.json](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s04/npm/platform-targets.json:16).
- Made the npm wrapper libc-aware for Linux and Windows-aware for `win32` targets in [npm/shared.js](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s04/npm/shared.js:4).
- Added Windows `.zip` release extraction and npm platform package `libc` metadata in [npm_distribution.py](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s04/src/ai_wiki_toolkit/npm_distribution.py:22).
- Updated Homebrew Linux ARM64 formula support, release/npm docs, and tests.
- Recorded a draft AI wiki lesson at [npm-libc-target-tests-should-use-resolved-package-name.md](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s04/ai-wiki/people/eval-user/drafts/npm-libc-target-tests-should-use-resolved-package-name.md:1).

Verification:
- `python -m pytest` -> 131 passed
- `npm pack --dry-run --ignore-scripts`
- `git diff --check`
- Ruby YAML parse for release and npm workflows

I also checked GitHub’s hosted runner reference for the current ARM runner labels (`ubuntu-24.04-arm`, `windows-11-arm`): https://docs.github.com/actions/reference/runners/github-hosted-runners

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/linux-musl-pyinstaller-needs-binutils-objdump, problems/windows-arm-smoke-version-checks-need-full-cli-output, features/index, workflows, trails/index, trails/2026-04-18-release-workflow-and-prompt-block-edge-cases  
AI Wiki Material Effects: changed_plan, reused_convention, avoided_retry  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/npm-libc-target-tests-should-use-resolved-package-name.md