Implemented on branch `feat/expand-release-distribution`.

Expanded the release/npm matrix to include `linux-arm64`, `linux-musl-x64`, `windows-x64`, and `windows-arm64`; added Windows zip extraction for npm platform package staging; added Linux libc-aware npm target resolution; and extended Homebrew to include `linux-arm64`. Docs, changelog, and tests are updated.

Verification passed:

- `python -m pytest` -> `129 passed`
- `npm pack --dry-run --ignore-scripts`
- `PYTHONPATH=src python scripts/check_release_version.py v0.1.11`
- workflow YAML parse check

Reference checks used: GitHub runner labels, npm `libc` metadata, and PyInstaller platform support from official/current docs:
[GitHub hosted runners](https://docs.github.com/actions/reference/runners/github-hosted-runners), [npm package.json](https://docs.npmjs.com/cli/v11/configuring-npm/package-json), [PyInstaller](https://pypi.org/pypi/PyInstaller).

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, constraints, conventions/index, conventions/package-managed-vs-user-owned-docs, decisions, review-patterns/index, problems/index, features/index, workflows, trails/index  
AI Wiki Material Effects: changed_plan, reused_distribution_rules, followed_branch_and_test_workflow  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: Draft  
AI Wiki Update Path: ai-wiki/people/eval-user/drafts/alpine-release-containers-need-posix-sh.md