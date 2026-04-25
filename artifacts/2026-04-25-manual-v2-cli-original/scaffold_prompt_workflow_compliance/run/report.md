# Impact Eval Report

- Run dir: `<eval-root>/scaffold_prompt_workflow_compliance/runs/cli-original-scaffold-20260425-1618`
- Experiment: `scaffold_prompt_workflow_compliance`
- Workspace root: `<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315`
- Variants: `s01, s02, s03, s04, s05, s06`
- Prompt levels: `original`
- Created at: `2026-04-25T16:18:37`
- Layout: `workflow-primary neutral slots`
- Shareable for causal claims: `yes`
- Notes: `Formal CLI-first original prompt run across six neutral slots.`

## Workflow Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s01 | no_aiwiki_workflow | original | partial | pending | 10 |
| s05 | aiwiki_ambient_memory_workflow | original | success | pending | 10 |

## Diagnostic Result

| slot | variant | prompt_level | score | first_pass_success | changed_file_count |
| --- | --- | --- | --- | --- | --- |
| s02 | aiwiki_scaffold_no_target_memory | original | success | pending | 11 |
| s03 | aiwiki_linked_raw_only | original | success | pending | 11 |
| s04 | aiwiki_linked_consolidated_only | original | success | pending | 11 |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | success | pending | 11 |

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
| s01 | no_aiwiki_workflow | original | first_pass | partial | pending | 1 | 0 | 10 | README.md<br>docs/doctor-proposal.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>src/ai_wiki_toolkit/wiki_schema.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_wiki_schema.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s02 | aiwiki_scaffold_no_target_memory | original | first_pass | success | pending | 1 | 0 | 11 | README.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>src/ai_wiki_toolkit/wiki_schema.py<br>tests/test_compatibility_scenarios.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_prompt_scenarios.py<br>tests/test_wiki_schema.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s03 | aiwiki_linked_raw_only | original | first_pass | success | pending | 1 | 0 | 11 | README.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>src/ai_wiki_toolkit/wiki_schema.py<br>tests/test_compatibility_scenarios.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_prompt_scenarios.py<br>tests/test_wiki_schema.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s04 | aiwiki_linked_consolidated_only | original | first_pass | success | pending | 1 | 0 | 11 | README.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>src/ai_wiki_toolkit/wiki_schema.py<br>tests/test_compatibility_scenarios.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_prompt_scenarios.py<br>tests/test_wiki_schema.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s05 | aiwiki_ambient_memory_workflow | original | first_pass | success | pending | 1 | 0 | 10 | README.md<br>ai-wiki/_toolkit/workflows.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>tests/test_compatibility_scenarios.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_prompt_scenarios.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |
| s06 | aiwiki_scaffold_no_adjacent_memory | original | first_pass | success | pending | 1 | 0 | 11 | README.md<br>src/ai_wiki_toolkit/content.py<br>src/ai_wiki_toolkit/doctor.py<br>src/ai_wiki_toolkit/scaffold.py<br>src/ai_wiki_toolkit/wiki_schema.py<br>tests/test_compatibility_scenarios.py<br>tests/test_doctor.py<br>tests/test_init_scenarios.py<br>tests/test_install_uninstall_scenarios.py<br>tests/test_prompt_scenarios.py<br>tests/test_wiki_schema.py | - | yes | Captured by run_cli_slots.py; Codex CLI return code: 0. Run-level sleep guard metadata is in sleep_guard.json. |

## Confounds

_No rows._
