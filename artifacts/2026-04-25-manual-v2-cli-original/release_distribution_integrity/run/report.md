# Impact Eval Report

- Run dir: `<eval-root>/release_distribution_integrity/runs/cli-original-release-20260425-1246`
- Experiment: `release_distribution_integrity`
- Workspace root: `<eval-root>/release_distribution_integrity/workspaces/20260425-124642`
- Variants: `s01, s02, s03, s04, s05, s06`
- Prompt levels: `original`
- Created at: `2026-04-25T12:46:48`
- Layout: `workflow-primary neutral slots`
- Shareable for causal claims: `yes`
- Notes: `Clean formal Manual v2 release_distribution_integrity run; original prompt, five neutral slots, Codex CLI-first only, run-level caffeinate guard via run_cli_slots.py. Supplemental s06 aiwiki_scaffold_no_adjacent_memory diagnostic added on 2026-04-25 without rerunning s01-s05.`

## Workflow Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s01 | no_aiwiki_workflow | original | partial | pending | 23 |
| s05 | aiwiki_ambient_memory_workflow | original | success | pending | 23 |

## Diagnostic Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s02 | aiwiki_scaffold_no_target_memory | original | success | pending | 23 |
| s03 | aiwiki_linked_raw_only | original | success | pending | 21 |
| s04 | aiwiki_linked_consolidated_only | original | success | pending | 20 |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | success | pending | 24 |

## Variant Summary

| variant | recorded_slots | first_pass_successes | first_pass_failures | first_pass_pending | avg_attempts | avg_human_nudges |
| --- | --- | --- | --- | --- | --- | --- |
| aiwiki_ambient_memory_workflow | 1 | 0 | 0 | 1 | 1.00 | 0.00 |
| aiwiki_linked_consolidated_only | 1 | 0 | 0 | 1 | 1.00 | 0.00 |
| aiwiki_linked_raw_only | 1 | 0 | 0 | 1 | 1.00 | 0.00 |
| aiwiki_scaffold_no_adjacent_memory | 1 | 0 | 0 | 1 | 1.00 | 0.00 |
| aiwiki_scaffold_no_target_memory | 1 | 0 | 0 | 1 | 1.00 | 0.00 |
| no_aiwiki_workflow | 1 | 0 | 0 | 1 | 1.00 | 0.00 |

## Recorded Results

| slot | variant | prompt_level | phase | score | first_pass_success | attempt | human_nudges | changed_file_count | changed_files | untracked_files | final_message_present | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| s01 | no_aiwiki_workflow | original | first_pass | partial | pending | 1 | 0 | 23 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>CHANGELOG.md<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>scripts/check_linux_runtime_matrix.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>src/ai_wiki_toolkit/release_runtime.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>tests/test_release_runtime.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s02 | aiwiki_scaffold_no_target_memory | original | first_pass | success | pending | 1 | 0 | 23 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>scripts/check_linux_runtime_matrix.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>src/ai_wiki_toolkit/release_runtime.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>tests/test_release_runtime.py<br>ai-wiki/people/eval-user/drafts/windows-npm-platform-packages-need-zip-aware-staging.md | ai-wiki/people/eval-user/drafts/windows-npm-platform-packages-need-zip-aware-staging.md | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s03 | aiwiki_linked_raw_only | original | first_pass | success | pending | 1 | 0 | 21 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>src/ai_wiki_toolkit/release_runtime.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>tests/test_release_runtime.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s04 | aiwiki_linked_consolidated_only | original | first_pass | success | pending | 1 | 0 | 20 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>ai-wiki/people/eval-user/drafts/npm-libc-target-tests-should-use-resolved-package-name.md | ai-wiki/people/eval-user/drafts/npm-libc-target-tests-should-use-resolved-package-name.md | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s05 | aiwiki_ambient_memory_workflow | original | first_pass | success | pending | 1 | 0 | 23 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>CHANGELOG.md<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>src/ai_wiki_toolkit/release_runtime.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>tests/test_release_runtime.py<br>ai-wiki/people/eval-user/drafts/linux-musl-npm-packages-need-libc-metadata-and-runtime-detection.md | ai-wiki/people/eval-user/drafts/linux-musl-npm-packages-need-libc-metadata-and-runtime-detection.md | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | first_pass | success | pending | 1 | 0 | 24 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>CHANGELOG.md<br>README.md<br>docs/homebrew-tap.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>npm/platform-targets.json<br>npm/shared.js<br>package.json<br>scripts/build_linux_release_in_container.py<br>scripts/check_linux_runtime_matrix.py<br>src/ai_wiki_toolkit/homebrew_formula.py<br>src/ai_wiki_toolkit/npm_distribution.py<br>src/ai_wiki_toolkit/release_build.py<br>src/ai_wiki_toolkit/release_runtime.py<br>tests/test_distribution_metadata.py<br>tests/test_homebrew_formula.py<br>tests/test_npm_wrapper.py<br>tests/test_release_artifacts.py<br>tests/test_release_build.py<br>tests/test_release_runtime.py<br>ai-wiki/people/eval-user/drafts/alpine-release-containers-need-posix-sh.md | ai-wiki/people/eval-user/drafts/alpine-release-containers-need-posix-sh.md | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |

## Confounds

_No rows._
