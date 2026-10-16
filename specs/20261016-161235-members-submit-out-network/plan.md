# Implementation Plan: Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance

**Branch**: `20261016-161235-members-submit-out-network` | **Date**: 2026-10-16 | **Spec**: [spec.md](./spec.md)

**Input**: Feature specification from `/specs/20261016-161235-members-submit-out-network/spec.md`

## Summary

Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance.

## Technical Context

<!-- Drafted by the Gradera Context Engine. `/speckit.plan` fills each field from the estate through the gradera MCP server; nothing here is guessed. -->

**Language/Version**: NEEDS CLARIFICATION

**Primary Dependencies**: NEEDS CLARIFICATION

**Storage**: NEEDS CLARIFICATION

**Testing**: NEEDS CLARIFICATION

**Project Type**: NEEDS CLARIFICATION

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

Checked by `/speckit.plan` against `.specify/memory/constitution.md`, which is the team's; the engine never writes it.

## Project Structure

### Documentation (this feature)

```text
specs/20261016-161235-members-submit-out-network/
├── spec.md
├── plan.md
├── tasks.md
└── checklists/
    └── requirements.md
```

### Source Code (repository root)

**Structure Decision**: NEEDS CLARIFICATION. No impacted code is recorded for the epic; `/speckit.plan` reads it with `get_impact`.

## Estate Impact *(Gradera)*

### What the change reaches

- Not recorded on the backlog.

### Kit skills this plan follows

| Skill | Path | Used by |
|---|---|---|
| `add-query-handler` | `.github/skills/add-query-handler/SKILL.md` | US2 |
| `add-request-validator` | `.github/skills/add-request-validator/SKILL.md` | US1, US3 |

### Unknowns the engine reported

- Open question: Which filing deadline applies to an out-of-network claim submitted online: the portal's limit, the adjudication engine's limit or the plan's limit?
- Open question: Should a claim that is paid in full up to its allowance be flagged for investigation when it reaches 80 percent of the limit, or be paid without review as the plan says?
- Open question: Which claim type should an eyewear claim use in the portal and in adjudication, given neither lists a vision type today?
- Open question: Who should approve an eyewear claim that is paid up to the frame allowance: nobody (automatic), a person within a delegated limit, or a role-based tier?
- Open question: Should a claim that is paid in full up to its allowance be flagged for investigation when it reaches 80 percent of the limit, or be paid without review as the plan says?
- no impacted code is recorded for the epic, so the plan cannot name the modules it changes
