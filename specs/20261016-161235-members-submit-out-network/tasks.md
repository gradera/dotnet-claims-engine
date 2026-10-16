---

description: "Task list for Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance, drafted from the backlog"
---

# Tasks: Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance

**Input**: Design documents from `/specs/20261016-161235-members-submit-out-network/`

**Prerequisites**: plan.md (required), spec.md (required for user stories)

**Tests**: Included. Every acceptance scenario in spec.md is a test written first.

**Organization**: Tasks are grouped by user story, each naming the promoted kit skill it follows.

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (US1, US2, ...)

## Phase 1: Setup (Shared Infrastructure)

- [ ] T001 Confirm every NEEDS CLARIFICATION in spec.md and plan.md with `/speckit.clarify` and `/speckit.plan`
- [ ] T002 [P] Read the impact of each module the plan names with `get_impact` before changing it

---

## Phase 2: User Story 1 - Submit out-of-network eyewear claims online (Priority: P1) 🎯 MVP

**Goal**: As a member, I want to submit out-of-network eyewear claims online, so that my claim is reimbursed up to the frame allowance.

**Independent Test**: the acceptance scenarios of User Story 1 in spec.md pass.

### Tests for User Story 1

- [ ] T003 [P] [US1] Write a failing test for: An out-of-network claim must be received within 12 months of the date... (gradera:595050e6-d3b4-4634-b12b-5b122701d062, approved)
- [ ] T004 [P] [US1] Write a failing test for: Claims above the listed amounts are paid up to the allowance the... (gradera:956c2cf4-5ea2-442d-9944-859f5bb8a28a, approved)
- [ ] T005 [P] [US1] Write a failing test for: Every out-of-network claim needs an itemised receipt showing the... (gradera:4547d011-8360-4917-97e6-30d23a39ecf2, approved)

### Implementation for User Story 1

- [ ] T006 [US1] Implement Submit out-of-network eyewear claims online, following skill `add-request-validator` (`.github/skills/add-request-validator/SKILL.md`)
- [ ] T007 [US1] Make every test of this story pass and keep to the rules the plan's Estate Impact names

**Checkpoint**: User Story 1 works and is testable on its own

---

## Phase 3: User Story 2 - Submit out-of-network eyewear claims online with an itemised receipt (Priority: P2)

**Goal**: As a member, I want to submit out-of-network eyewear claims online with an itemised receipt, so that my claim is reimbursed up to the frame allowance.

**Independent Test**: the acceptance scenarios of User Story 2 in spec.md pass.

### Tests for User Story 2

- [ ] T008 [P] [US2] Write a failing test for: Read requests query claim lists with pageSize=20 expecting HTTP 200... (gradera:f13c1362-869f-4192-a238-38bb53e4fc5c, approved)
- [ ] T009 [P] [US2] Write a failing test for: The divisor max in the percentage calculation is always at least 1... (gradera:94642327-f5df-4e06-9360-cbff8127f4ea, approved)

### Implementation for User Story 2

- [ ] T010 [US2] Implement Submit out-of-network eyewear claims online with an itemised receipt, following skill `add-query-handler` (`.github/skills/add-query-handler/SKILL.md`)
- [ ] T011 [US2] Make every test of this story pass and keep to the rules the plan's Estate Impact names

**Checkpoint**: User Story 2 works and is testable on its own

---

## Phase 4: User Story 3 - Be reimbursed up to the frame allowance (Priority: P3)

**Goal**: As a member, I want to be reimbursed up to the frame allowance, so that I am paid as the approved rules say.

**Independent Test**: the acceptance scenarios of User Story 3 in spec.md pass.

### Tests for User Story 3

- [ ] T012 [P] [US3] Write a failing test for: Benefit frequencies: eye exam, spectacle lenses, contact lenses and... (gradera:37e04888-8d29-40f2-9686-3eeb42fe913d, approved)
- [ ] T013 [P] [US3] Write a failing test for: Out-of-network services are reimbursed up to: eye exam 45, frames 70... (gradera:f0dbb07f-b644-456b-96b8-e37c4c470c9a, approved)

### Implementation for User Story 3

- [ ] T014 [US3] Implement Be reimbursed up to the frame allowance, following skill `add-request-validator` (`.github/skills/add-request-validator/SKILL.md`)
- [ ] T015 [US3] Make every test of this story pass and keep to the rules the plan's Estate Impact names

**Checkpoint**: User Story 3 works and is testable on its own

---

## Phase 5: Polish & Cross-Cutting Concerns

- [ ] T016 Run `/speckit.analyze` and resolve every finding against the estate
- [ ] T017 [P] Update the documentation the change reaches

## Dependencies & Execution Order

- Setup (Phase 1) first; each user story phase then stands on its own, in priority order.
- Within a story, tests are written and fail before the implementation.
