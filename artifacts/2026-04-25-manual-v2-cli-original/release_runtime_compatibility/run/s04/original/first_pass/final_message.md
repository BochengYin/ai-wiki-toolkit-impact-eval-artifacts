Implemented the Linux runtime compatibility gate.

Changed:
- [release-binaries.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s04/.github/workflows/release-binaries.yml): builds `linux-x64` inside `python:3.11-bullseye`, then runs the binary in `debian:bullseye-slim` and `node:24-bookworm` before packaging.
- [publish-npm.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s04/.github/workflows/publish-npm.yml): runs the staged Linux npm package binary in `node:24-bookworm` before any `npm publish`.
- Added [build_linux_release_in_container.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s04/scripts/build_linux_release_in_container.py) and [check_linux_runtime_matrix.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s04/scripts/check_linux_runtime_matrix.py).
- Updated release/npm docs and added workflow/script tests.

Verification:
- `uv run pytest` passed: 88 tests.
- `npm pack --dry-run --ignore-scripts` passed.
- The actual Docker smoke is wired into CI; locally I covered command construction and workflow ordering with tests.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, decisions, review-patterns/index, problems/index, problems/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline, workflows  
AI Wiki Material Effects: changed_plan, reused_convention, followed_repo_workflow  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None