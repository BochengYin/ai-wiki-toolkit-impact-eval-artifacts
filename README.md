# AI Wiki Toolkit Impact Eval Artifacts

This repository contains public artifacts for the `ai-wiki-toolkit` Manual v2 CLI-first impact eval
run from 2026-04-25.

Main toolkit repository:

- https://github.com/BochengYin/ai-wiki-toolkit

## Scope

This is an artifact-backed pilot evaluation, not a statistically powered benchmark. The run has one
primary control sample and one primary treatment sample per family:

- `no_aiwiki_workflow`
- `aiwiki_ambient_memory_workflow`

Diagnostic variants are included for mechanism analysis, but they are not the main causal
comparison.

## Contents

```text
benchmark_materials/
  evals/impact/
    README.md
    TODO.md
    families/
    notes/
    public/
    prompts/
    reports/
    runbooks/
    scripts/

artifacts/
  2026-04-25-manual-v2-cli-original/
    ownership_boundary/
    release_distribution_integrity/
    windows_arm_smoke_cli_output/
    release_runtime_compatibility/
    scaffold_prompt_workflow_compliance/
    raw_session_hashes.sha256
```

Each family directory contains:

- `run/`: run metadata, validator output, aggregate report, slot scores, and first-pass artifacts
- `codex_sessions/`: exported visible session artifacts, including `manifest.json`,
  `visible_session.jsonl`, `visible_transcript.md`, `prompt.md`, and session metadata

The raw `session_without_reasoning.jsonl` files are not published in this repository. They can include
local filesystem paths, sandbox configuration, and tool/plugin inventory. Their SHA-256 hashes are
published in:

- `artifacts/2026-04-25-manual-v2-cli-original/raw_session_hashes.sha256`

## Formal Families

| family | primary control | primary treatment | interpretation |
| --- | --- | --- | --- |
| `ownership_boundary` | fail | success | Strongest positive signal for AI wiki workflow changing implementation surface. |
| `release_distribution_integrity` | partial | success | Narrow positive signal for coordinated release/npm completeness and known-hazard handling. |
| `windows_arm_smoke_cli_output` | success | success | Neutral; useful as deterministic harness coverage, not as AI wiki advantage evidence. |
| `release_runtime_compatibility` | partial | success | Narrow positive signal for release runtime baseline and pre-publish verification quality. |
| `scaffold_prompt_workflow_compliance` | partial | success | Workflow-discipline signal for scaffold names, routing, docs, and tests. |

## Reading Order

1. `benchmark_materials/evals/impact/public/ai_wiki_impact_eval_pilot.md`
2. `benchmark_materials/evals/impact/reports/current.md`
3. `benchmark_materials/evals/impact/notes/index.md`
4. The specific family note under `benchmark_materials/evals/impact/notes/`
5. The matching artifact directory under `artifacts/2026-04-25-manual-v2-cli-original/`

## Validity Boundaries

Do not treat these artifacts as evidence of statistical significance. The main defensible claim is
directional: in this pilot suite, ambient AI wiki workflow produced better primary outcomes than the
no-AI-wiki workflow in four of five historical task families and tied in one.

Known limitations include:

- one primary sample per condition per family
- manually scored outcomes
- tasks derived from the same project that produced the memories
- no seed or temperature capture
- no actual GitHub Actions release execution for some release-family slots

## Integrity

Run:

```bash
shasum -a 256 -c checksums.sha256
```

to verify the files committed in this repository.
