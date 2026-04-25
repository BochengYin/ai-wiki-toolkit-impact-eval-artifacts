# Result Slot

- Experiment: `release_runtime_compatibility`
- Slot: `s03`
- Variant: `aiwiki_linked_raw_only`
- Prompt: `original`
- Workspace: `<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s03`

Preferred formal path: run the whole slot set once with the run-level sleep guard from the run directory README. For this prompt level, the command is:

```bash
uv run python evals/impact/scripts/run_cli_slots.py \
  --run-dir "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618" \
  --prompt-level "original"
```
Run the prompt with Codex CLI first, then capture the first-pass result:

```bash
mkdir -p "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618/s03/original/first_pass"
codex exec \
  --model "gpt-5.5" \
  --config 'model_reasoning_effort="xhigh"' \
  --full-auto \
  --cd "<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s03" \
  --output-last-message "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618/s03/original/first_pass/final_message.md" \
  - < "<repo-root>/evals/impact/prompts/release_runtime_compatibility/original.md"
uv run python evals/impact/scripts/save_result.py \
  --run-dir "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618" \
  --variant "aiwiki_linked_raw_only" \
  --slot "s03" \
  --prompt-level "original" \
  --workspace "<eval-root>/release_runtime_compatibility/workspaces/20260425-160315/slots/s03" \
  --final-message "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618/s03/original/first_pass/final_message.md" \
  --phase first_pass
```

The standard run expects the exported session metadata to show `source=exec`, `model=gpt-5.5`, and `reasoning_effort=xhigh`.

Add `--first-pass-success` or `--first-pass-failure` only if you want to judge correctness now. If you omit both, the result stays pending for later analysis.

If there is a later human nudge or repair, capture it separately with `--phase final`.
After all slots finish, export Codex sessions and run `validate_run.py`; the run is not shareable for causal claims without a complete `codex_sessions/manifest.json`.
