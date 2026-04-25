Implemented on `feat/expand-release-distribution-matrix`.

Added the expanded release/npm matrix across the workflow, npm metadata/runtime selection, staging, Homebrew formula generation, docs, and tests. The public release/npm target set now covers `linux-arm64`, `linux-musl-x64`, `windows-x64`, and `windows-arm64` in addition to the existing macOS/Linux targets. Windows npm staging now consumes `.zip` release assets, and Linux musl uses npm `libc` metadata plus runtime musl detection.

Verification:
- `python -m pytest` -> 130 passed
- `npm pack --dry-run --ignore-scripts` -> passed

I used official docs to confirm current runner labels and npm `libc` metadata:
- GitHub hosted runners: https://docs.github.com/actions/reference/runners/github-hosted-runners
- npm package.json `libc`: https://docs.npmjs.com/cli/v11/configuring-npm/package-json

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: constraints, workflows, problems/linux-musl-pyinstaller-needs-binutils-objdump, problems/windows-arm-smoke-version-checks-need-full-cli-output, people/bochengyin/drafts/distribution-target-matrix-must-match-published-assets, people/bochengyin/drafts/introducing-new-npm-package-names-needs-a-bootstrap-publish-plan, people/bochengyin/drafts/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline  
AI Wiki Material Effects: aligned_distribution_matrix, avoided_known_failure, expanded_verification, updated_docs  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None