# Optional planning and assignment usage

[AGENTS.md](../AGENTS.md) owns all common duties and review triggers. This guide supplies examples only. No model family must read it, classify through Laya, run preflight, or call planning agents merely to begin work.

## Short plans
The main decides the approach. Explain a material decision briefly and proceed within approval. Use a structured plan only when it helps a complex task; this is not a fixed pre-tool format.

Example: “I will reproduce the lost Back state, fix its initialization, and check the original path plus adjacent search.”

A high-risk example may name goal, owned scope, ordered checks, and required review. Do not ask for approval of an already authorized plan.

## Ownership and delegation
Default to one main owner. Parallelize independent work only when it helps; serialize shared files, devices, and release state.

A needed brief can contain:
- Goal and Done when.
- Owned files, prohibited scope, and relevant sources.
- Requested role/model/effort and actual support or unknowns.
- Relevant checks, expected results, and failure boundary.

Simple repeated replacements normally use batch editing. If a delegated pattern needs an example, the main completes one first. Unknown causes and unclear ownership stay with the main until narrowed.

User-selected Claude may serve as main, implementation, planning/instruction, or review owner when supported. Selecting the main does not select additional Claude/Grok subagents. Fixed roles and actual permission boundaries remain binding.

## Needed review
Apply [review triggers](../AGENTS.md#7-review-triggers-and-holds) first. Use [dispatch](../review/dispatch.md) and review/1.4 only for actual required or concretely needed review. Preserve the main's permissions; review runs in its separate actual read-only session.

The existing run_readonly_review.py supports requested native roles and model/effort values; inspect its current help and logs rather than inventing support. No smoke test or demo is triggered by an instruction edit or installed skill.

Recheck changed findings with the original reviewer as described in dispatch. An unavailable optional reviewer adds no completion gate.

## Cleanup
Apply the central [cleanup conditions](../AGENTS.md#generated-file-cleanup) and [maintenance usage](../guides/maintenance.md#cleanup-usage). Inventory relevant roots and verify usage/reference/copy evidence and protected ancestors; labels and age alone do not prove disposal.

Report actual moved/deleted bytes separately from whole-disk free-space changes. This example grants no new deletion, installation, or remote-write approval.

## Optional tools
- callgraph: useful for locating symbols, callers/callees, shared widgets, and paths from screen to backend. Use absolute project paths and supplement dynamic edges with source inspection.
- context7: useful for confirming unfamiliar version-specific contracts. Use official/local evidence, not guessed APIs.
- preflight.py: optional support/ownership/dependency/capacity inspection when useful, not approval or review clearance.
- laya_classify.py: optional classification/recording aid only when deliberately selected. Its old decision table is not a mandatory route for any main.
- API specifications: use the api-spec skill when requested or a real frontend/backend contract needs documentation; a copy/spacing change alone creates no spec.
- Tool-enforced safety limits still apply. A graph score is evidence to investigate concrete effects, not permission or automatic review clearance.

For CLI data formats and observed usage records, consult [local contracts](../harness/README.md) only when using those helpers.
