# Result Slot

- Experiment: `windows_arm_smoke_cli_output`
- Slot: `s02`
- Variant: `aiwiki_scaffold_no_target_memory`
- Prompt: `original`
- Workspace: `<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s02`

Preferred formal path: run the whole slot set once with the run-level sleep guard from the run directory README. For this prompt level, the command is:

```bash
uv run python evals/impact/scripts/run_cli_slots.py \
  --run-dir "<eval-root>/windows_arm_smoke_cli_output/runs/cli-original-windows-arm-20260425-1618" \
  --prompt-level "original"
```
Run the prompt with Codex CLI first, then capture the first-pass result:

```bash
mkdir -p "<eval-root>/windows_arm_smoke_cli_output/runs/cli-original-windows-arm-20260425-1618/s02/original/first_pass"
codex exec \
  --model "gpt-5.5" \
  --config 'model_reasoning_effort="xhigh"' \
  --full-auto \
  --cd "<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s02" \
  --output-last-message "<eval-root>/windows_arm_smoke_cli_output/runs/cli-original-windows-arm-20260425-1618/s02/original/first_pass/final_message.md" \
  - < "<repo-root>/evals/impact/prompts/windows_arm_smoke_cli_output/original.md"
uv run python evals/impact/scripts/save_result.py \
  --run-dir "<eval-root>/windows_arm_smoke_cli_output/runs/cli-original-windows-arm-20260425-1618" \
  --variant "aiwiki_scaffold_no_target_memory" \
  --slot "s02" \
  --prompt-level "original" \
  --workspace "<eval-root>/windows_arm_smoke_cli_output/workspaces/20260425-160315/slots/s02" \
  --final-message "<eval-root>/windows_arm_smoke_cli_output/runs/cli-original-windows-arm-20260425-1618/s02/original/first_pass/final_message.md" \
  --phase first_pass
```

The standard run expects the exported session metadata to show `source=exec`, `model=gpt-5.5`, and `reasoning_effort=xhigh`.

Add `--first-pass-success` or `--first-pass-failure` only if you want to judge correctness now. If you omit both, the result stays pending for later analysis.

If there is a later human nudge or repair, capture it separately with `--phase final`.
After all slots finish, export Codex sessions and run `validate_run.py`; the run is not shareable for causal claims without a complete `codex_sessions/manifest.json`.
