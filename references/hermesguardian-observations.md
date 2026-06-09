# HermesGuardian Observations

## Background

HermesGuardian is a multi-agent security investigation platform developed to explore agentic workflows, collaborative reasoning, and automated threat analysis.

During development and testing, several recurring challenges emerged that motivated the DSHP research initiative.

---

## Observation 1: Agent Consensus Divergence

Multiple agents frequently reached conclusions that differed from expert human judgment.

Example:

* Agent A: Allow
* Agent B: Allow
* Agent C: Allow
* Human Analyst: Block

This exposed a gap between agent consensus and expert reasoning.

Key Question:

How can humans effectively intervene when agent consensus appears incorrect?

---

## Observation 2: Limited Execution Visibility

During long-running workflows, it became difficult to understand:

* why a decision was made
* which agent influenced the outcome
* what evidence contributed to the final vote

Key Question:

How should agent execution state be represented for human inspection?

---

## Observation 3: Expensive Recovery

When an incorrect decision path was identified, recovery often required:

* restarting execution
* manually modifying workflow state
* replaying previous actions

Key Question:

Can agent workflows recover from incorrect branches without full restart?

---

## Observation 4: Prompt Accumulation

Corrective feedback was often appended to existing context.

This introduced:

* larger context windows
* diluted model attention
* increased token consumption

Key Question:

Can state rehydration outperform append-only correction approaches?

---

## Observation 5: Human Steering Gap

Current agent frameworks optimize for autonomy but provide limited mechanisms for:

* pause
* inspect
* redirect
* resume

long-horizon workflows.

Key Question:

How can humans steer agent execution without corrupting state integrity?

---

## Research Motivation

These observations motivated the creation of DSHP (Dynamic State Hydration Protocol).

DSHP aims to investigate human-guided steering, state recovery, and context rehydration for long-horizon multi-agent systems.
