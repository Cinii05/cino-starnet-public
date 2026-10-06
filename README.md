# Cino StarNet

Cino StarNet is a provider-neutral multi-agent reliability and orchestration plugin.

Release candidate: **v1.1.0**

Public surface: **13 skills**.

This package is derived from the sealed Agent 02B StarNet skill/fleet optimisation candidate at 12140279eebd33736d326cd6e941c18837fa235c. Project-specific TMC adapters and private runtime configuration are intentionally excluded.

## Accepted optimisation baseline

- routing accuracy: 100%
- activation precision: 100%
- activation recall: 100%
- misses: 0
- unnecessary activations: 0
- authority leakage: 0
- precedence: 24/24
- aggregate query-index estimate: -59.83%
- activated skill-body estimate: -43.17%

Publication of this package does not grant external mutation authority. Individual skills preserve their own authority and read/write boundaries.

## v1.1.0

Adds **Cino Overseer Mission Prompt Builder**, a pre-launch StarNet skill that interviews the Commander only where material ambiguity remains and compiles one self-contained CALLUS/overseer launch prompt. It deliberately leaves live decomposition, routing, execution, replanning and QA to the existing StarNet stack.

The original 12 v1.0.0 skill bodies remain unchanged.
