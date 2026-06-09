# Problem Statement

## Introduction

Modern AI agent frameworks increasingly support long-horizon task execution involving multiple collaborating agents, external tools, and autonomous decision-making.

While autonomy has improved significantly, human steering remains underdeveloped.

In practical systems, operators frequently need to:

* inspect execution state
* understand reasoning paths
* correct agent mistakes
* redirect workflows
* recover from incorrect decisions

Most existing frameworks provide limited support for these activities.

---

## Problem

Current agent systems primarily rely on prompt-based corrections.

When an agent drifts from the intended objective, human feedback is typically appended to the conversation history.

This approach introduces several challenges:

* context growth
* attention dilution
* reduced explainability
* difficult recovery paths
* duplicated tool execution risk

As workflows become longer and more complex, these issues become increasingly significant.

---

## Research Question

How can human operators effectively steer long-horizon multi-agent workflows while preserving execution integrity, state consistency, and contextual relevance?

---

## Proposed Direction

DSHP explores a state-centric approach where execution history is represented as structured state transitions rather than an append-only conversational log.

This enables:

* inspection
* interruption
* correction
* recovery
* resumption

while maintaining a verifiable execution history.
