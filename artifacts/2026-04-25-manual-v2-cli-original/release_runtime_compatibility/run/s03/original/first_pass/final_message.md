Implemented the release gate.

Key changes:
- Linux `linux-x64` release binaries now build in `python:3.11-bookworm`, not directly on `ubuntu-24.04`.
- `Release Binaries` now runs the built Linux archive in `node:24-bookworm` and `node:24-trixie` before uploading release assets.
- `Publish npm Package` now packs staged local npm tarballs, installs them globally with `npm install -g --offline` in `node:24-bookworm`, and runs `aiwiki-toolkit --version` before any npm publish.
- Added static regression tests and updated release/npm docs.
- Marked the existing Linux runtime compatibility AI wiki draft as a promotion candidate.

Verification:
- `python -m pytest` passed: 86 tests.
- `bash -n` passed for the new shell scripts.
- `git diff --check` passed.
- `npm pack --dry-run --ignore-scripts` passed.

The actual Docker smoke scripts are wired into CI; I did not run them locally against a real release archive.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: constraints, conventions/distribution-target-matrix-must-match-published-assets, workflows, problems/linux-musl-pyinstaller-needs-binutils-objdump, people/bochengyin/drafts/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline  
AI Wiki Material Effects: changed_plan, reused_convention, reused_workflow  
AI Wiki Missed Memory: none known  
AI Wiki Update Path: ai-wiki/people/bochengyin/drafts/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline.md  
AI Wiki Update Candidate: PromotionCandidate