# Impact Eval Run

- Experiment: `release_runtime_compatibility`
- Workspace root: `<eval-root>/release_runtime_compatibility/workspaces/20260425-160315`
- Prompt level: `original`

Formal CLI-first runs should use one run-level sleep guard for the whole slot set. `run_cli_slots.py` starts `caffeinate -dimsu`, runs each neutral slot in sequence, captures first-pass artifacts immediately after each `codex exec`, and stops the sleep guard at the end.

```bash
uv run python evals/impact/scripts/run_cli_slots.py \
  --run-dir "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618" \
  --prompt-level "original"
```
After all slots finish, export sessions and validate the run:

```bash
uv run python evals/impact/scripts/export_codex_sessions.py --workspace-root "<eval-root>/release_runtime_compatibility/workspaces/20260425-160315"
uv run python evals/impact/scripts/validate_run.py --run-dir "<eval-root>/release_runtime_compatibility/runs/cli-original-runtime-20260425-1618"
```
