Implemented on branch `feat/expand-release-distribution-targets`.

Expanded the release/npm matrix across workflows, runtime helpers, npm metadata, archive staging, Homebrew formula generation, docs, changelog, and tests. The public release workflow now covers `linux-arm64`, `linux-musl-x64`, `windows-arm64`, plus Windows x64 for end-to-end npm support. npm staging now handles Windows `.zip` assets, the wrapper detects musl on Linux x64, and generated Linux platform packages include npm `libc` constraints.

Verification passed:
- `python -m pytest` -> `133 passed`
- `npm pack --dry-run --ignore-scripts`
- YAML parse check for the changed workflows

I used GitHub’s runner docs to confirm `ubuntu-24.04-arm` and `windows-11-arm`, and `actions/setup-python` docs for architecture behavior:
- https://docs.github.com/actions/reference/runners/github-hosted-runners
- https://github.com/actions/setup-python

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/distribution-target-matrix-must-match-published-assets, problems/index, problems/linux-musl-pyinstaller-needs-binutils-objdump, problems/windows-arm-smoke-version-checks-need-full-cli-output, workflows, people/bochengyin/drafts/introducing-new-npm-package-names-needs-a-bootstrap-publish-plan  
AI Wiki Material Effects: reused_convention, applied_musl_setup_guidance, followed_release_workflow, updated_npm_bootstrap_docs  
AI Wiki Missed Memory: npm bootstrap draft was found during final update check and folded into docs

AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/linux-musl-npm-packages-need-libc-metadata-and-runtime-detection.md