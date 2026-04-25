# Impact Eval Report

- Run dir: `<eval-root>/ownership_boundary/runs/cli-original-ownership-20260425-1158`
- Experiment: `ownership_boundary`
- Workspace root: `<eval-root>/ownership_boundary/workspaces/20260425-115832`
- Variants: `s01, s02, s03, s04, s05, s06`
- Prompt levels: `original`
- Created at: `2026-04-25T11:58:38`
- Layout: `workflow-primary neutral slots`
- Shareable for causal claims: `yes`
- Notes: `Clean formal Manual v2 ownership_boundary run restarted after adding run-level caffeinate guard; original prompt, five neutral slots, Codex CLI-first only. Supplemental s06 aiwiki_scaffold_no_adjacent_memory diagnostic added on 2026-04-25 without rerunning s01-s05.`

## Workflow Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s01 | no_aiwiki_workflow | original | fail | pending | 6 |
| s05 | aiwiki_ambient_memory_workflow | original | success | pending | 4 |

## Diagnostic Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s02 | aiwiki_scaffold_no_target_memory | original | success | pending | 4 |
| s03 | aiwiki_linked_raw_only | original | success | pending | 4 |
| s04 | aiwiki_linked_consolidated_only | original | fail | pending | 5 |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | fail | pending | 5 |

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
| s01 | no_aiwiki_workflow | original | first_pass | fail | pending | 1 | 0 | 6 | CHANGELOG.md<br>CONTRIBUTING.md<br>src/ai_wiki_toolkit/cli.py<br>src/ai_wiki_toolkit/contributor_workflow.py<br>tests/test_contributor_cli.py<br>tests/test_contributor_workflow.py | src/ai_wiki_toolkit/contributor_workflow.py<br>tests/test_contributor_cli.py<br>tests/test_contributor_workflow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s02 | aiwiki_scaffold_no_target_memory | original | first_pass | success | pending | 1 | 0 | 4 | CONTRIBUTING.md<br>ai-wiki/people/eval-user/drafts/contributor-pr-flow-uses-dated-feature-chore-fix-branches.md<br>scripts/pr_flow.py<br>tests/test_pr_flow.py | ai-wiki/people/eval-user/drafts/contributor-pr-flow-uses-dated-feature-chore-fix-branches.md<br>scripts/pr_flow.py<br>tests/test_pr_flow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s03 | aiwiki_linked_raw_only | original | first_pass | success | pending | 1 | 0 | 4 | CONTRIBUTING.md<br>ai-wiki/workflows.md<br>scripts/pr_flow.py<br>tests/test_pr_flow.py | scripts/pr_flow.py<br>tests/test_pr_flow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s04 | aiwiki_linked_consolidated_only | original | first_pass | fail | pending | 1 | 0 | 5 | CONTRIBUTING.md<br>ai-wiki/people/eval-user/drafts/contributor-pr-flow-helper-enforces-dated-branch-names.md<br>scripts/pr_flow.py<br>src/ai_wiki_toolkit/pr_flow.py<br>tests/test_pr_flow.py | ai-wiki/people/eval-user/drafts/contributor-pr-flow-helper-enforces-dated-branch-names.md<br>scripts/pr_flow.py<br>src/ai_wiki_toolkit/pr_flow.py<br>tests/test_pr_flow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s05 | aiwiki_ambient_memory_workflow | original | first_pass | success | pending | 1 | 0 | 4 | CONTRIBUTING.md<br>ai-wiki/workflows.md<br>scripts/pr_flow.py<br>tests/test_pr_flow.py | scripts/pr_flow.py<br>tests/test_pr_flow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | first_pass | fail | pending | 1 | 0 | 5 | README.md<br>scripts/contributor_pr.py<br>src/ai_wiki_toolkit/contributor_workflow.py<br>tests/test_contributor_pr_script.py<br>tests/test_contributor_workflow.py | scripts/contributor_pr.py<br>src/ai_wiki_toolkit/contributor_workflow.py<br>tests/test_contributor_pr_script.py<br>tests/test_contributor_workflow.py | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |

## Confounds

_No rows._
