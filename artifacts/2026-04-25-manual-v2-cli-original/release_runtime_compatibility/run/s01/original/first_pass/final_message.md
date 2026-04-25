Implemented the release guard.

Changed:
- Added a Linux binary smoke test in [release-binaries.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s01/.github/workflows/release-binaries.yml:72), before archive creation.
- Added a pre-publish npm install smoke test in [publish-npm.yml](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s01/.github/workflows/publish-npm.yml:116).
- Added [scripts/smoke_npm_linux_install.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s01/scripts/smoke_npm_linux_install.py:1), which packs the staged Linux platform package plus a temporary meta package, installs it globally inside `node:24-bookworm` on `linux/amd64`, then runs `aiwiki-toolkit --version`.
- Added helper coverage in [npm_smoke.py](<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s01/src/ai_wiki_toolkit/npm_smoke.py:1) and workflow-order tests.
- Updated npm/release docs to describe the new compatibility gate.

Verification:
- `python -m pytest` -> `87 passed`
- `PYTHONPATH=src python scripts/smoke_npm_linux_install.py --help` passed.