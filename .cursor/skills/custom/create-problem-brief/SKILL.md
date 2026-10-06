---
name: create-problem-brief
description: Synthesize product evidence into a decision-ready problem brief while preserving traceability, uncertainty, and competing explanations.
---

# Create Problem Brief

Use this skill after relevant product evidence has been analyzed.

The purpose is to transform distributed analysis into a compact,
decision-ready description of the product problem.

A problem brief is not a product decision and not a feature specification.

## Inputs

Prefer canonical analysis artifacts over replaying all raw evidence.

Typical inputs:

- qualitative findings;
- quantitative findings;
- technical/product facts;
- existing accepted product memory;
- relevant constraints.

Return to raw evidence when:

- an important claim cannot be traced;
- analyses conflict;
- provenance is unclear;
- verification is necessary.

## Procedure

### 1. Define the observed problem

Describe the undesirable user or business outcome.

Prefer:

> Small self-serve agencies have a substantially lower
> ad-account connection completion rate.

Avoid:

> Users need an AI onboarding assistant.

The second statement already assumes a solution.

### 2. Establish evidence strength

For every important claim distinguish:

- MEASURED FACT;
- QUALITATIVE OBSERVATION;
- CALCULATION;
- INTERPRETATION;
- ASSUMPTION;
- UNKNOWN.

Do not combine these categories into a single confident narrative.

### 3. Triangulate independent evidence

Look for agreement or disagreement between sources.

Examples:

Analytics may identify WHERE users abandon.

Interviews may suggest WHY.

Support may reveal recurring operational friction.

Technical verification may establish WHAT the product actually does.

Agreement strengthens a hypothesis but does not automatically prove causality.

### 4. Surface conflicting evidence

Do not silently reconcile incompatible sources.

For conflicts:

- identify the conflicting claims;
- identify source and definition differences;
- mark dependent conclusions as unreliable;
- recommend reconciliation when decision-relevant.

### 5. Define affected users

State the segment only when supported.

Separate:

- confirmed affected segment;
- suspected affected segment;
- segments with insufficient evidence.

### 6. Describe candidate explanations

List plausible explanations without selecting one prematurely.

For each explanation include:

- supporting evidence;
- contradicting evidence;
- important missing evidence;
- current confidence.

### 7. Estimate product significance

When supported, describe:

- size of affected population;
- funnel or business impact;
- downstream value;
- urgency;
- reversibility;
- strategic relevance.

Do not invent estimates when the required data is absent.

### 8. Identify the highest-value uncertainty

Ask:

> What unknown most affects what we should do next?

Prefer reducing this uncertainty before committing expensive engineering work.

### 9. Produce the brief

Use this structure:

# Problem Brief

## Problem

Concise problem statement.

## Affected Users

Who appears affected and how confidently this is known.

## Evidence

Traceable evidence supporting the problem.

## Magnitude

Known quantitative impact, if available.

## Candidate Explanations

Competing hypotheses, not solutions.

## Contradicting Evidence

Evidence that weakens the current framing.

## Critical Unknowns

Unknowns that could change the decision.

## Constraints

Business, product, technical, data, or timing constraints.

## Recommended Next Step

The cheapest useful action to reduce important uncertainty.

## Decision Required

If a human decision is required, state exactly what is being decided.

## Status

PENDING HUMAN DECISION

if a decision is requested.

Otherwise:

ANALYSIS

## Traceability

Reference the canonical evidence and analysis artifacts used.

## Guardrails

Do not:

- introduce unsupported product-specific facts;
- hide conflicting evidence;
- convert correlation into causation;
- turn a hypothesis into a requirement;
- select AI as the default solution;
- write an unapproved recommendation into product memory;
- begin Spec-Driven Delivery without explicit human approval.