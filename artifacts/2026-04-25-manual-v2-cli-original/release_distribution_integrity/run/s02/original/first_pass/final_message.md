Implemented the expanded release/npm distribution support on branch `feat/expand-release-distribution-targets`.

Key changes:
- Release matrix now builds `linux-arm64`, `linux-musl-x64`, `windows-x64`, and `windows-arm64`, alongside existing macOS/Linux targets.
- Linux container build helper now supports target-specific image/platform/shell/setup, including Alpine musl with root `binutils` setup.
- npm platform map now covers glibc Linux, musl Linux, and Windows `.exe` packages.
- npm staging now extracts both Unix `.tar.gz` and Windows `.zip` release assets.
- Runtime wrapper now detects Linux musl vs glibc and resolves the correct optional dependency.
- Homebrew formula generation now includes `linux-arm64`.
- Docs and tests were updated for the new public matrix and first-publish bootstrap caveat for new npm package names.

Verification:
- `python -m pytest` -> `131 passed`
- `npm_config_cache=/tmp/aiwiki-npm-cache npm pack --dry-run --ignore-scripts` -> passed
- Ruby YAML parse for `.github/workflows/release-binaries.yml` and `publish-npm.yml` -> passed

Sources checked: GitHub hosted runner labels from [GitHub Docs](https://docs.github.com/actions/reference/runners/github-hosted-runners), npm `libc` package metadata from [npm package.json docs](https://docs.npmjs.com/cli/v11/configuring-npm/package-json).

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/package-managed-vs-user-owned-docs, decisions, review-patterns/index, review-patterns/shared-prompt-files-must-be-user-agnostic, problems/index, problems/linux-musl-pyinstaller-needs-binutils-objdump, problems/windows-arm-smoke-version-checks-need-full-cli-output, features/index, workflows, trails/index, people/bochengyin/drafts/introducing-new-npm-package-names-needs-a-bootstrap-publish-plan  
AI Wiki Material Effects: changed_plan, reused_problem_memory, avoided_user_doc_churn, added_bootstrap_docs  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/windows-npm-platform-packages-need-zip-aware-staging.md