# Evaluation Plan

## Objective

Evaluate whether DSHP improves human-agent collaboration during long-horizon multi-agent execution.

---

## Benchmark A: HermesGuardian Investigation Workflows

Purpose:

Evaluate intervention effectiveness using real-world multi-agent security investigation scenarios.

Metrics:

* intervention count
* recovery success rate
* disagreement reduction
* workflow completion rate

Example Scenario:

Agent voting recommends an incorrect action.

Human operator intervenes.

DSHP attempts state recovery and workflow continuation.

---

## Benchmark B: Long-Horizon Software Engineering Tasks

Purpose:

Evaluate workflow steering during complex engineering operations.

Example Tasks:

* multi-step deployment
* infrastructure provisioning
* repository refactoring
* CI/CD workflow execution

Metrics:

* successful completion rate
* recovery latency
* execution cost
* token usage

---

## Benchmark C: Multi-Agent Decision Systems

Purpose:

Evaluate consensus correction and decision steering.

Metrics:

* consensus accuracy
* intervention effectiveness
* state recovery success
* decision quality improvement

---

## Baseline Comparison

DSHP will be compared against traditional append-only correction workflows.

Baseline:

Human correction is appended to existing conversation history.

DSHP:

Human correction triggers state recovery and context rehydration.

---

## Success Criteria

DSHP will be considered successful if experiments demonstrate:

* improved task completion
* reduced disagreement
* reduced token consumption
* improved explainability
* lower recovery cost

while maintaining execution integrity.
