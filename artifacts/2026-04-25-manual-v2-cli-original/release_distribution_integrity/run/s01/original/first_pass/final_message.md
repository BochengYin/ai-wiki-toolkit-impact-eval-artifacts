Implemented the expanded release/npm matrix.

Key changes:
- Added npm targets for `linux-arm64`, `linux-musl-x64`, `win32-x64`, and `win32-arm64` in [npm/platform-targets.json](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s01/npm/platform-targets.json:16).
- Added musl detection and Windows target resolution in [npm/shared.js](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s01/npm/shared.js:4).
- Added Windows `.zip` extraction and npm `libc` metadata generation in [npm_distribution.py](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s01/src/ai_wiki_toolkit/npm_distribution.py:57).
- Expanded release workflow to build Linux x64/arm64/musl, macOS x64/arm64, and Windows x64/arm64 in [release-binaries.yml](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s01/.github/workflows/release-binaries.yml:36). I used GitHub’s runner reference for `ubuntu-24.04-arm` and `windows-11-arm`: https://docs.github.com/actions/reference/runners/github-hosted-runners
- Updated Linux runtime verification so Alpine/musl checks can use `sh -c` instead of bash in [release_runtime.py](<eval-root>/release_distribution_integrity/workspaces/20260425-124642/slots/s01/src/ai_wiki_toolkit/release_runtime.py:50).
- Updated Homebrew to include `linux-arm64`, plus docs, changelog, package metadata, and distribution tests.

Verification passed:
- `python -m pytest` -> `132 passed`
- `npm pack --dry-run --ignore-scripts`
- `git diff --check`