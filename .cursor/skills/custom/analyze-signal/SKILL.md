---
name: analyze-signal
description: Turn a raw product signal or stakeholder request into a structured investigation without prematurely selecting a solution.
---

# Analyze Product Signal

Use this skill when a task starts from a raw product signal such as:

- a stakeholder request;
- a metric change;
- a customer complaint;
- an interview observation;
- a support pattern;
- a sales request;
- an idea for a feature;
- an operational anomaly.

The purpose of this skill is to determine what is actually known,
what is not known, and what should be investigated next.

Do not convert a raw signal directly into a feature requirement.

## Procedure

### 1. Capture the original signal

Preserve the original meaning of the signal.

Identify:

- source;
- observed event or statement;
- affected user or segment, if known;
- metric or workflow involved, if known;
- time period, if known.

Do not strengthen the signal beyond the available evidence.

Example:

Stakeholder signal:

> Activation is low. Onboarding may be broken.

This establishes that activation is a concern.

It does NOT establish that onboarding is the cause.

### 2. Separate evidence from interpretation

Classify relevant statements as:

- OBSERVATION — directly supported by available evidence;
- INTERPRETATION — a possible explanation of observations;
- ASSUMPTION — believed but not currently supported;
- UNKNOWN — information required but unavailable.

Never present an interpretation or assumption as an observation.

### 3. Inspect available evidence

Identify which evidence sources are currently available.

Examples:

- analytics;
- interviews;
- support conversations;
- CRM;
- logs;
- experiments;
- product behavior;
- external research.

The absence of a particular source does not block analysis.

Work with the evidence that exists and explicitly state what cannot
be concluded from it.

Examples:

If only interviews are available:
- qualitative patterns may be identified;
- prevalence across the population is unknown.

If only analytics are available:
- funnel losses may be identified;
- user motivation or causal explanation may remain unknown.

### 4. Determine whether additional evidence is decision-relevant

Do not request data merely because it could be interesting.

Request additional evidence only when it could materially change:

- problem framing;
- prioritization;
- hypothesis selection;
- experiment design;
- product decision.

Prefer the cheapest evidence that reduces the most important uncertainty.

### 5. Identify investigation paths

When useful, identify independent analysis tracks.

Examples:

- qualitative research;
- quantitative analysis;
- technical/product behavior verification;
- market research.

Use specialized agents when context isolation or independent reasoning
would improve reliability.

Do not force every investigation to use every available agent.

### 6. Produce an investigation brief

The output should contain:

## Original Signal

The raw request or observation.

## What We Know

Only evidence-supported facts.

## What We Do Not Know

Important unresolved questions.

## Initial Interpretations

Possible explanations, explicitly labeled as unvalidated.

## Evidence Available

Sources currently available for investigation.

## Evidence Gaps

Only decision-relevant missing evidence.

## Recommended Investigation

The minimum useful next analysis.

## Constraints

Known scope, business, technical, time, or data constraints.

## Status

ANALYSIS READY

This status does not represent a product decision.

## Guardrails

Do not:

- invent product behavior;
- invent missing metrics;
- infer causality from observational evidence;
- select a solution before the problem is sufficiently understood;
- treat stakeholder opinion as validated evidence;
- write findings into product memory;
- start implementation or OpenSpec.

When evidence is insufficient, say so explicitly.

Uncertainty is an acceptable result.