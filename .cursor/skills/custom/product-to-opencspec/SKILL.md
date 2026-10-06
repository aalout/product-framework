---
name: product-to-openspec
description: Convert an explicitly human-approved product behavior change into an OpenSpec-ready engineering handoff while preserving product intent, scope, non-goals, acceptance behavior, and evidence traceability.
---

# Product to OpenSpec

Use this skill only when a product decision has been explicitly approved
by the human Product Owner and the decision requires a behavior-changing
product or engineering change.

This skill is the boundary between Product Discovery and
Spec-Driven Delivery.

It must not be used to turn an unvalidated hypothesis or agent
recommendation directly into implementation work.

## Preconditions

Before creating or proposing an OpenSpec change, verify all of the following:

1. A specific product decision exists.
2. The human explicitly approved that specific decision.
3. The approved behavior is identifiable.
4. Scope is sufficiently clear to specify.
5. Important product ambiguity has been resolved or can be surfaced.
6. The change requires behavior-changing engineering work.

If explicit human approval cannot be verified:

STOP.

Return:

PENDING HUMAN DECISION

Do not create an OpenSpec change.

## Approval Verification

Valid approval must come from an explicit human message approving
the specific product decision.

Do not infer approval from:

- permission to investigate;
- permission to recommend;
- previous agent output;
- completed analysis;
- absence of objection;
- approval of a different decision;
- an agent-generated status label.

Human approval authorizes only the approved scope.

It does not authorize adjacent improvements.

## Procedure

### 1. Load the approved decision

Use the canonical decision artifact when available.

Capture:

- decision ID;
- approved behavior;
- target user/segment;
- product goal;
- rationale;
- relevant evidence;
- explicit constraints;
- non-goals.

Do not reinterpret the decision to make implementation easier.

### 2. Verify traceability

The product premise should be traceable to:

- accepted product memory;
- approved decision;
- supporting analysis/evidence.

Do not copy the entire discovery history into OpenSpec.

Preserve references instead.

OpenSpec should receive the minimum authoritative context necessary
to implement the approved behavior.

### 3. Separate Product from Engineering

Product owns:

- WHY the change exists;
- WHO it is for;
- WHAT observable behavior should change;
- scope;
- non-goals;
- success criteria;
- product constraints.

Engineering owns:

- architecture;
- components;
- libraries;
- APIs;
- data structures;
- implementation strategy;
- internal technical design.

Do not encode implementation choices as product requirements unless
they were explicitly part of the approved decision.

### 4. Define behavioral requirements

Translate the approved decision into observable behavior.

Prefer requirements that can be verified.

Example:

Approved decision:

> Users must retain control over recommended ad-account configuration.

Behavioral requirement:

> The system SHALL require explicit user confirmation before applying
> a recommended configuration.

Avoid:

> Use a React confirmation modal.

The latter is an implementation choice.

### 5. Define scenarios and acceptance criteria

For each important behavior include:

- starting condition;
- user/system action;
- expected observable result.

Cover:

- primary path;
- important edge cases;
- failure states;
- approved safety/control constraints.

Do not invent product behavior for unspecified edge cases.

If an edge case requires a product decision:

STOP and ask the human.

### 6. Preserve non-goals

Explicitly include behavior that is NOT part of the approved change.

Non-goals protect against agentic scope expansion.

Example:

- no automatic configuration;
- no campaign import;
- no changes to post-connection campaign workflow;
- no AI-generated recommendation in this version.

### 7. Define success separately from implementation acceptance

Distinguish:

PRODUCT SUCCESS

Example:
connection completion improves for the target segment.

from:

IMPLEMENTATION ACCEPTANCE

Example:
required permissions are shown before confirmation.

Engineering can verify implementation acceptance.

Product success may require post-release measurement.

Do not treat shipping as validation of the product hypothesis.

### 8. Detect ambiguity

Before creating the OpenSpec change, ask:

> Could two reasonable implementers produce materially different
> product behavior from this description?

If yes, determine whether the ambiguity is:

TECHNICAL:
leave it to Engineering.

PRODUCT:
stop and request a human decision.

Do not silently resolve product ambiguity.

### 9. Create the OpenSpec change

Use the repository's installed/generated OpenSpec workflow.

Do not recreate OpenSpec conventions manually when generated
OpenSpec skills provide the canonical procedure.

The change should preserve:

- decision traceability;
- behavioral requirements;
- scenarios;
- scope;
- non-goals;
- acceptance criteria.

### 10. Handoff

After the OpenSpec change is ready:

- architecture may determine HOW;
- implementation may execute approved tasks;
- deterministic checks should validate formal correctness;
- an independent judge should verify implementation against the spec.

The implementer must not be the sole authority approving its own work.

## Output Contract

Before handoff, report:

# Product → OpenSpec Handoff

## Approved Decision

Decision ID and concise approved behavior.

## Product Goal

Why the change exists.

## Target User

Who the behavior is for.

## Behavioral Requirements

Observable approved behavior.

## Non-Goals

Explicit exclusions.

## Acceptance Criteria

Behavior that implementation must satisfy.

## Product Success Criteria

Post-release outcome, if known.

## Traceability

References to decision and supporting product artifacts.

## Open Questions

Only unresolved questions that materially affect product behavior.

## OpenSpec Change

Path/name of the created change.

## Status

READY FOR SPEC-DRIVEN DELIVERY

or, if product ambiguity remains:

BLOCKED — HUMAN PRODUCT DECISION REQUIRED

## Guardrails

Never:

- create OpenSpec from an unapproved recommendation;
- convert hypotheses into requirements;
- expand approved product scope;
- invent missing product behavior;
- encode arbitrary implementation choices as Product requirements;
- treat implementation completion as product validation;
- treat agent approval as human approval.