---
name: spec-driven-doc-bootstrap
description: Create and maintain spec-driven software project documents. Use when Codex needs to define or update software planning and execution docs such as SPECS.md, specs/*/SPEC.md, PLAN.md, TASKS.md, DECISIONS.md, CONTRACTS.md, TESTING.md, or OPERATIONS.md for backend, API, CLI, library, or service projects, especially when a change is too large for ad-hoc notes.
---

# Spec Driven Doc Bootstrap

## Overview

Use this skill to set up or refresh a software-oriented document set that separates requirements, implementation approach, execution state, testing policy, and operational guidance.

Keep long-lived project context separate from feature-level work and avoid letting spec documents drift into logs or vague notes.

## Core Document Set

Always treat the following as the core document set for spec-driven software work.

- `AGENTS.md` or `CLAUDE.md`
  - Project-wide working rules and document maintenance rules.
- `PROJECT.md`
  - Product goal, scope, constraints, and success criteria.
- `STATUS.md`
  - Current project snapshot and next work at project level.
- `ARCHITECTURE.md`
  - Current system structure and active design decisions.
- `SPECS.md`
  - Index of active and completed specs.
- `specs/<id-slug>/SPEC.md`
  - Problem definition, scope, requirements, and acceptance criteria.
- `specs/<id-slug>/PLAN.md`
  - Implementation approach, impact areas, rollout, compatibility, and risk handling.
- `specs/<id-slug>/TASKS.md`
  - Execution checklist, verification progress, and open blockers.

## Optional Documents

Create these only when they solve repeated documentation needs.

- `DECISIONS.md`
  - Add when technical decisions need to survive across multiple specs.
- `CONTRACTS.md`
  - Add when APIs, events, CLI I/O, file formats, or database boundaries need a stable contract summary.
- `TESTING.md`
  - Add when the project needs a shared testing policy beyond one feature's acceptance criteria.
- `OPERATIONS.md`
  - Add when the project is deployed or operated as a service and needs deployment, rollback, or monitoring guidance.
- `fixtures/contracts/`
  - Add only when example payloads or contract fixtures help prevent ambiguous interpretations.

## Workflow

### 1. Ground in the Current Project

- Inspect repository structure and existing docs before adding anything.
- Read `AGENTS.md` or `CLAUDE.md` first if present.
- Read `PROJECT.md`, `STATUS.md`, and `ARCHITECTURE.md` to understand product scope and current structure.
- Reuse existing documents when their role is already clear and current.

### 2. Decide Whether a New Spec Is Needed

- Do not create a new spec for a trivial bug fix or tiny refactor.
- Create a new spec package for non-trivial feature work, structural changes, or contract changes.
- Use the next available numeric prefix for `specs/<id-slug>/`.
- Add or update the corresponding row in `SPECS.md`.

### 3. Create or Refresh the Spec Package

- Start from the templates in `templates/`.
- Fill `SPEC.md` with the problem, goals, non-goals, scope, requirements, and acceptance criteria.
- Fill `PLAN.md` with the implementation path, affected areas, migration or compatibility concerns, validation plan, and rollout notes.
- Fill `TASKS.md` with concrete tasks and verification checks.
- Keep these three files focused on different jobs. Do not duplicate large sections across them.

### 4. Add Optional Documents Only When Triggered

- Add `DECISIONS.md` when a design choice will outlive one feature or should not be rediscovered later.
- Add `CONTRACTS.md` when interface changes affect other systems, clients, or stored files.
- Add `TESTING.md` when test expectations should be shared across many specs.
- Add `OPERATIONS.md` only for software that is deployed, scheduled, monitored, or manually operated.
- Prefer linking to machine-readable sources of truth when they already exist instead of copying them into prose.

### 5. Synchronize After Implementation

- Update `TASKS.md` to reflect what was actually completed and verified.
- Update `SPECS.md` status so the index matches reality.
- Promote durable structural changes into `ARCHITECTURE.md`.
- Promote project-wide testing changes into `TESTING.md`.
- Promote long-lived contract or operational changes into `CONTRACTS.md` or `OPERATIONS.md`.

## Document Boundaries

- `PROJECT.md` answers why the project exists and what success looks like.
- `STATUS.md` answers where the project stands right now.
- `ARCHITECTURE.md` answers what the current system looks like.
- `SPEC.md` answers what this change must do.
- `PLAN.md` answers how the change will be implemented.
- `TASKS.md` answers what remains and what has been verified.
- `DECISIONS.md` answers why a durable technical choice was made.
- `CONTRACTS.md` answers what external or cross-boundary interfaces must remain true.
- `TESTING.md` answers how the project is generally validated.
- `OPERATIONS.md` answers how the running system is deployed or supported.

## Anti-Patterns

- Do not turn `TASKS.md` into an unbounded dated work log.
- Do not copy the same requirement text into `SPEC.md`, `PLAN.md`, and `TASKS.md`.
- Do not create `OPERATIONS.md` for a project that is not actually operated.
- Do not duplicate generated schemas or OpenAPI files into `CONTRACTS.md`.
- Do not keep stale or superseded decisions as if they were still active.
- Do not leave acceptance criteria vague.

## Templates and Examples

- Use these templates when creating or rewriting documents:
  - `templates/SPECS.template.md`
  - `templates/SPEC.template.md`
  - `templates/PLAN.template.md`
  - `templates/TASKS.template.md`
  - `templates/DECISIONS.template.md`
  - `templates/CONTRACTS.template.md`
  - `templates/TESTING.template.md`
  - `templates/OPERATIONS.template.md`
- Use the examples in `examples/` to check how the skill should react to new or existing software projects.
