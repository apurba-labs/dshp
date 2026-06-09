# DSHP Architecture Overview

## Design Goal

DSHP aims to enable safe human steering of long-horizon multi-agent workflows without requiring complete workflow restart or excessive prompt accumulation.

The protocol separates execution state management from model inference, allowing workflows to be inspected, interrupted, modified, and resumed.

---

## High-Level Architecture

```text
Human Operator
       │
       ▼
Steering Interface
       │
       ▼
DSHP Middleware
       │
 ┌─────┼─────┐
 ▼     ▼     ▼
State  Agent Tool
Graph Runtime Layer
       │
       ▼
Execution Context
```

---

## Core Components

### Human Steering Interface

Provides capabilities to:

* observe execution progress
* inspect workflow state
* pause execution
* inject corrections
* resume execution

---

### DSHP Middleware

Acts as an orchestration layer between agents and execution state.

Responsibilities:

* state tracking
* event management
* interruption handling
* recovery coordination

---

### State Graph

Execution history is represented as a directed graph containing:

* agent decisions
* tool executions
* observations
* voting outcomes
* environmental responses

Each node represents a recoverable workflow state.

---

### Context Rehydration Engine

Instead of appending corrective prompts indefinitely, DSHP rebuilds execution context from validated workflow state.

Goals:

* reduce context bloat
* improve reasoning quality
* improve intervention effectiveness

---

## Workflow Lifecycle

1. Execute workflow
2. Detect issue or disagreement
3. Pause execution
4. Inspect state graph
5. Inject steering decision
6. Rehydrate context
7. Resume execution

---

## Research Focus

This architecture is intended as a research framework for studying:

* human-agent collaboration
* workflow steering
* state recovery
* explainability
* long-horizon execution
