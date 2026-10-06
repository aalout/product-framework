---
name: generate-product-hypotheses
description: Generate evidence-grounded product hypotheses and choose the cheapest useful way to reduce uncertainty before committing to implementation.
---

# Generate Product Hypotheses

Use this skill when a product problem has been framed but the correct
intervention is still uncertain.

The purpose is not to generate the largest number of ideas.

The purpose is to identify a small set of testable hypotheses that
could explain or improve the observed product outcome.

## Core Principle

A hypothesis is not a fact.

A hypothesis is not a decision.

A hypothesis is not a specification.

A plausible hypothesis must remain explicitly unvalidated until evidence
supports it.

## Procedure

### 1. Start from the problem, not from a feature

Read the current problem brief and relevant accepted product context.

Identify:

- affected user;
- observed behavior;
- desired outcome;
- strongest evidence;
- important uncertainty.

Do not begin with:

> How can we use AI to solve this?

Begin with:

> What mechanism may be causing this outcome?

### 2. Generate problem hypotheses first

Create competing explanations for the observed behavior.

Example:

H1:
Users abandon configuration because they do not understand
which account/assets and permissions to select.

H2:
Users abandon because they lack required client access.

H3:
Users abandon because technical integration failures prevent completion.

Competing hypotheses reduce confirmation bias.

### 3. Generate solution hypotheses only when useful

For a supported problem hypothesis, formulate the smallest plausible
intervention.

Use:

> We believe [intervention]
> for [user/segment]
> will change [behavior/outcome]
> because [mechanism].

Example:

> We believe showing recommended configuration and explaining
> permissions before completion will increase connection completion
> for small self-serve agencies because it reduces uncertainty
> about client-account risk.

This remains unvalidated.

### 4. Consider non-AI alternatives

AI must compete with simpler solutions.

For each relevant hypothesis consider whether the uncertainty could be
reduced through:

- copy or information;
- UX changes;
- defaults;
- deterministic recommendations;
- instrumentation;
- operational process;
- concierge/manual assistance;
- prototype;
- AI capability.

Do not prefer AI unless probabilistic or generative capability provides
meaningful additional value.

### 5. Identify assumptions

For each hypothesis list the assumptions required for it to work.

Examples:

- users actually see the proposed guidance;
- users possess sufficient account permissions;
- uncertainty rather than technical failure causes abandonment;
- the target behavior predicts downstream product value.

### 6. Define falsification evidence

Ask:

> What evidence would make us reject or substantially weaken this hypothesis?

A hypothesis that cannot fail is not useful.

### 7. Select the cheapest useful test

Prefer reducing uncertainty before building the complete solution.

Possible tests:

- additional analysis;
- targeted interviews;
- usability test;
- fake-door test;
- prototype;
- concierge test;
- information-only intervention;
- A/B experiment;
- technical spike.

Choose based on:

- uncertainty reduced;
- cost;
- speed;
- reversibility;
- risk;
- expected decision value.

### 8. Define success criteria before results

When an experiment is appropriate, define in advance:

- primary metric;
- secondary metrics;
- guardrails;
- target segment;
- evaluation window;
- decision threshold when justified;
- important confounders.

Do not invent statistical precision unsupported by the available data.

### 9. Prioritize

Prioritize hypotheses using:

- evidence strength;
- potential impact;
- uncertainty;
- cost to validate;
- cost to implement;
- reversibility;
- strategic fit.

Do not use a numerical scoring model unless the inputs are meaningful.

### 10. Output

# Product Hypotheses

For each hypothesis:

## H[n] — Name

### Problem Mechanism

What may be causing the observed outcome.

### Evidence For

Traceable supporting evidence.

### Evidence Against

Contradicting or weakening evidence.

### Assumptions

What must be true.

### Confidence

LOW / MEDIUM / HIGH

Confidence represents current evidence strength, not probability of success.

### Proposed Test

Cheapest useful validation approach.

### Primary Metric

If applicable.

### Guardrails

If applicable.

### Falsification Criteria

What result would weaken or reject the hypothesis.

### Status

UNVALIDATED

Finish with:

## Recommended Next Step

Which uncertainty should be reduced first and why.

## Human Decision Required

State whether approval is needed before proceeding.

## Guardrails

Never:

- describe an unvalidated hypothesis as a learning;
- write it to durable product memory as fact;
- create implementation requirements from it without approval;
- assume AI is required;
- optimize for idea quantity over decision quality.