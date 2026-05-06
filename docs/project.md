# MEMTRACE Project Overview

MEMTRACE is a compact benchmark and protocol for separating immediate retrieval-context failures, poisoned-memory admission, delayed memory-mediated unsafe execution, and execution-format failure in memory-enabled tool agents.

## Submission Scope

The NeurIPS E&D submission reports one audited pilot packet:

- 12 synthetic enterprise-assistant tasks.
- 3 memory-system variants: `S0`, `S1`, and `S2`.
- 324 main traces under `traces/v1_main_324/`.
- 72 oracle-retrieved-memory calibration traces under `traces/calibration_oracle_memory_72/`.
- One actor/backend pair: `mlx-community/Qwen2.5-7B-Instruct-4bit` with MLX writer/planner backends.

The main S0/S1/S2 metrics exclude calibration traces.
The calibration condition `S1-ORACLE-RETRIEVED-MEMORY` inserts the poisoned memory record, forces retrieval at the trigger turn, disables current-turn poison retrieval at the trigger, and measures whether the benchmark and scorer detect delayed memory-mediated unsafe execution.

## Reproducibility Surface

The artifact includes:

- synthetic corpus, allowlist, episode specifications, and gold labels;
- prompts, deterministic tools, traces, run summaries, metrics, and attribution reports;
- validation scripts that regenerate metrics from packaged traces without model inference;
- Croissant metadata and documentation cards for dataset, evaluation, third-party assets, and release scope.

Full model reruns require Apple Silicon, `mlx-lm`, `sentence-transformers`, the referenced MLX actor model, and the dense retrieval model.
The `profile` backend is a smoke-test fixture and is not a reported result backend.

## Claim Discipline

The artifact supports a validity-first benchmark claim for one actor/backend pair.
It does not make broad cross-model claims, does not claim that persistent memory is safe, and treats `S2` as a provenance-aware reference writer rather than a complete deployed defense.
