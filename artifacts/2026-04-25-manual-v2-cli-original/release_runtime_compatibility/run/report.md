# Impact Eval Report

- Run dir: `<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618`
- Experiment: `release_runtime_compatibility`
- Workspace root: `<eval-root>/release_runtime_compatibility/workspaces/20260425-160315`
- Variants: `s01, s02, s03, s04, s05, s06`
- Prompt levels: `original`
- Created at: `2026-04-25T16:18:37`
- Layout: `workflow-primary neutral slots`
- Shareable for causal claims: `yes`
- Notes: `Formal CLI-first original prompt run across six neutral slots.`

## Workflow Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s01 | no_aiwiki_workflow | original | partial | pending | 9 |
| s05 | aiwiki_ambient_memory_workflow | original | success | pending | 9 |

## Diagnostic Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s02 | aiwiki_scaffold_no_target_memory | original | success | pending | 10 |
| s03 | aiwiki_linked_raw_only | original | success | pending | 14 |
| s04 | aiwiki_linked_consolidated_only | original | success | pending | 13 |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | success | pending | 12 |

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
| s01 | no_aiwiki_workflow | original | first_pass | partial | pending | 1 | 0 | 9 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>scripts/smoke_npm_linux_install.py<br>src/ai_wiki_toolkit/npm_smoke.py<br>tests/test_npm_smoke.py | scripts/smoke_npm_linux_install.py<br>src/ai_wiki_toolkit/npm_smoke.py<br>tests/test_npm_smoke.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s02 | aiwiki_scaffold_no_target_memory | original | first_pass | success | pending | 1 | 0 | 10 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>ai-wiki/metrics/reuse-events/bochengyin.jsonl<br>ai-wiki/metrics/task-checks/bochengyin.jsonl<br>ai-wiki/people/bochengyin/drafts/linux-npm-runtime-compatibility-needs-bookworm-smoke-before-publish.md<br>scripts/smoke_npm_linux_install.sh | ai-wiki/metrics/reuse-events/bochengyin.jsonl<br>ai-wiki/metrics/task-checks/bochengyin.jsonl<br>ai-wiki/people/bochengyin/drafts/linux-npm-runtime-compatibility-needs-bookworm-smoke-before-publish.md<br>scripts/smoke_npm_linux_install.sh | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s03 | aiwiki_linked_raw_only | original | first_pass | success | pending | 1 | 0 | 14 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>ai-wiki/people/bochengyin/drafts/linux-release-binaries-need-runtime-checks-against-an-older-glibc-baseline.md<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>scripts/build_linux_release_in_container.sh<br>scripts/smoke_linux_release_runtime.sh<br>scripts/smoke_staged_npm_linux_package.sh | ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>scripts/build_linux_release_in_container.sh<br>scripts/smoke_linux_release_runtime.sh<br>scripts/smoke_staged_npm_linux_package.sh | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s04 | aiwiki_linked_consolidated_only | original | first_pass | success | pending | 1 | 0 | 13 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>scripts/build_linux_release_in_container.py<br>scripts/check_linux_runtime_matrix.py<br>tests/test_linux_runtime_release_scripts.py | ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>scripts/build_linux_release_in_container.py<br>scripts/check_linux_runtime_matrix.py<br>tests/test_linux_runtime_release_scripts.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s05 | aiwiki_ambient_memory_workflow | original | first_pass | success | pending | 1 | 0 | 9 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>docs/npm-publish.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl | ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | first_pass | success | pending | 1 | 0 | 12 | .github/workflows/publish-npm.yml<br>.github/workflows/release-binaries.yml<br>docs/npm-publish.md<br>docs/npm-wrapper.md<br>docs/releasing.md<br>tests/test_distribution_metadata.py<br>ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>ai-wiki/people/eval-user/drafts/linux-release-binaries-need-target-container-runtime-smoke.md<br>ai-wiki/people/eval-user/index.md | ai-wiki/_toolkit/metrics/document-stats.json<br>ai-wiki/_toolkit/metrics/task-stats.json<br>ai-wiki/metrics/reuse-events/eval-user.jsonl<br>ai-wiki/metrics/task-checks/eval-user.jsonl<br>ai-wiki/people/eval-user/drafts/linux-release-binaries-need-target-container-runtime-smoke.md<br>ai-wiki/people/eval-user/index.md | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |

## Confounds

_No rows._
