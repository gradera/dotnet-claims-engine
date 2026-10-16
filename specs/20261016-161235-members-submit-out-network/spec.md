# Feature Specification: Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance

**Feature Branch**: `20261016-161235-members-submit-out-network`

**Created**: 2026-10-16

**Status**: Draft

**Input**: Backlog epic "Members submit out-of-network eyewear claims online with an itemised receipt, reimbursed up to the frame allowance" (gradera:18045612-2be5-4f44-916b-354d1deb7002, approved), drafted by the Gradera Context Engine from its stories, acceptance criteria and the estate of `git:dotnet-claims-engine`

## User Scenarios & Testing *(mandatory)*

### User Story 1 - Submit out-of-network eyewear claims online (Priority: P1)

As a member, I want to submit out-of-network eyewear claims online, so that my claim is reimbursed up to the frame allowance. (gradera:a6ca7b97-bb92-4b11-8147-02d48bb59b65, approved)

**Why this priority**: Ordered as the backlog ranks it.

**Independent Test**: Can be fully tested by the acceptance scenarios below, each of which cites the estate it was drawn from.

**Acceptance Scenarios**:

1. *An out-of-network claim must be received within 12 months of the date...*: **Given** a member who wants to submit out-of-network eyewear claims online, **When** the Claims plan handles the request, **Then** An out-of-network claim must be received within 12 months of the date of service; claims received later are denied. (gradera:595050e6-d3b4-4634-b12b-5b122701d062, approved)
2. *Claims above the listed amounts are paid up to the allowance the...*: **Given** a member who wants to submit out-of-network eyewear claims online, **When** the Claims plan handles the request, **Then** Claims above the listed amounts are paid up to the allowance; the excess is the member's responsibility and is not a reason to deny the claim. (gradera:956c2cf4-5ea2-442d-9944-859f5bb8a28a, approved)
3. *Every out-of-network claim needs an itemised receipt showing the...*: **Given** a member who wants to submit out-of-network eyewear claims online, **When** the Claims plan handles the request, **Then** Every out-of-network claim needs an itemised receipt showing the provider, the date of service, each service and the amount paid. (gradera:4547d011-8360-4917-97e6-30d23a39ecf2, approved)

---

### User Story 2 - Submit out-of-network eyewear claims online with an itemised receipt (Priority: P2)

As a member, I want to submit out-of-network eyewear claims online with an itemised receipt, so that my claim is reimbursed up to the frame allowance. (gradera:bb63d928-3c71-480f-aadb-56e67042f690, approved)

**Why this priority**: Ordered as the backlog ranks it.

**Independent Test**: Can be fully tested by the acceptance scenarios below, each of which cites the estate it was drawn from.

**Acceptance Scenarios**:

1. *Read requests query claim lists with pageSize=20 expecting HTTP 200...*: **Given** a member who wants to submit out-of-network eyewear claims online with an itemised receipt, **When** the Claims portal handles the request, **Then** Read requests query claim lists with pageSize=20 (expecting HTTP 200), retrieve claim stats (expecting HTTP 200), and if items exist, fetch details for a claim by id (expecting HTTP 200). (gradera:f13c1362-869f-4192-a238-38bb53e4fc5c, approved)
2. *The divisor max in the percentage calculation is always at least 1...*: **Given** a member who wants to submit out-of-network eyewear claims online with an itemised receipt, **When** the Claims portal handles the request, **Then** The divisor max in the percentage calculation is always at least 1, preventing division by zero even if all item values are 0 or empty. (gradera:94642327-f5df-4e06-9360-cbff8127f4ea, approved)

---

### User Story 3 - Be reimbursed up to the frame allowance (Priority: P3)

As a member, I want to be reimbursed up to the frame allowance, so that I am paid as the approved rules say. (gradera:ba506ea2-c98f-4fa0-a446-90ac827f43df, approved)

**Why this priority**: Ordered as the backlog ranks it.

**Independent Test**: Can be fully tested by the acceptance scenarios below, each of which cites the estate it was drawn from.

**Acceptance Scenarios**:

1. *Benefit frequencies: eye exam, spectacle lenses, contact lenses and...*: **Given** a member who wants to be reimbursed up to the frame allowance, **When** the Claims plan handles the request, **Then** Benefit frequencies: eye exam, spectacle lenses, contact lenses and retinal imaging once every 12 months; frames once every 24 months; frame allowance or contact lens allowance in a benefit period, not both. (gradera:37e04888-8d29-40f2-9686-3eeb42fe913d, approved)
2. *Out-of-network services are reimbursed up to: eye exam 45, frames 70...*: **Given** a member who wants to be reimbursed up to the frame allowance, **When** the Claims plan handles the request, **Then** Out-of-network services are reimbursed up to: eye exam 45, frames 70, single vision lenses 30, bifocal lenses 50, elective contact lenses 105 (USD). (gradera:f0dbb07f-b644-456b-96b8-e37c4c470c9a, approved)

---

### Edge Cases

- [NEEDS CLARIFICATION: Which filing deadline applies to an out-of-network claim submitted online: the portal's limit, the adjudication engine's limit or the plan's limit?]
- [NEEDS CLARIFICATION: Should a claim that is paid in full up to its allowance be flagged for investigation when it reaches 80 percent of the limit, or be paid without review as the plan says?]
- [NEEDS CLARIFICATION: Which claim type should an eyewear claim use in the portal and in adjudication, given neither lists a vision type today?]
- [NEEDS CLARIFICATION: Who should approve an eyewear claim that is paid up to the frame allowance: nobody (automatic), a person within a delegated limit, or a role-based tier?]
- [NEEDS CLARIFICATION: Should a claim that is paid in full up to its allowance be flagged for investigation when it reaches 80 percent of the limit, or be paid without review as the plan says?]

## Requirements *(mandatory)*

### Functional Requirements

- **FR-001**: System MUST meet this criterion: an out-of-network claim must be received within 12 months of the date... (User Story 1; gradera:595050e6-d3b4-4634-b12b-5b122701d062, approved)
- **FR-002**: System MUST meet this criterion: claims above the listed amounts are paid up to the allowance the... (User Story 1; gradera:956c2cf4-5ea2-442d-9944-859f5bb8a28a, approved)
- **FR-003**: System MUST meet this criterion: every out-of-network claim needs an itemised receipt showing the... (User Story 1; gradera:4547d011-8360-4917-97e6-30d23a39ecf2, approved)
- **FR-004**: System MUST meet this criterion: read requests query claim lists with pageSize=20 expecting HTTP 200... (User Story 2; gradera:f13c1362-869f-4192-a238-38bb53e4fc5c, approved)
- **FR-005**: System MUST meet this criterion: the divisor max in the percentage calculation is always at least 1... (User Story 2; gradera:94642327-f5df-4e06-9360-cbff8127f4ea, approved)
- **FR-006**: System MUST meet this criterion: benefit frequencies: eye exam, spectacle lenses, contact lenses and... (User Story 3; gradera:37e04888-8d29-40f2-9686-3eeb42fe913d, approved)
- **FR-007**: System MUST meet this criterion: out-of-network services are reimbursed up to: eye exam 45, frames 70... (User Story 3; gradera:f0dbb07f-b644-456b-96b8-e37c4c470c9a, approved)

## Success Criteria *(mandatory)*

### Measurable Outcomes

- **SC-001**: Every acceptance scenario of User Story 1 passes in the repository's own test suite.
- **SC-002**: Every acceptance scenario of User Story 2 passes in the repository's own test suite.
- **SC-003**: Every acceptance scenario of User Story 3 passes in the repository's own test suite.

## Assumptions

- Until the business answers, this story waits on: how late a claim may be filed.
- Until the business answers, this story waits on: when a claim is flagged for investigation.
- Until the business answers, this story waits on: which kinds of claim exist.
- Until the business answers, this story waits on: who may approve a claim, and up to what amount.
- Until the business answers, this story waits on: when a claim is flagged for investigation.
- Scope is the backlog epic as the engine holds it; a story or criterion rejected or superseded there is not in this specification.

## Estate Context *(Gradera)*

### Constraints that bind this feature

- Conflict: Claims portal and Claims adjudication and Claims plan disagree: How long after the service or incident can a claim still be filed? (open)
- Conflict: Claims adjudication and Claims plan disagree: When does a claim stop being paid automatically and wait for a person? (open)
- Conflict: Claims portal and Claims adjudication disagree: Which claim types can a member declare, and does a vision claim exist? (open)
- Conflict: Claims portal and Claims adjudication disagree: Who is allowed to approve a payout, and is the limit a person's or a role's? (open)
- Conflict: Claims adjudication and Claims plan disagree: When does a claim stop being paid automatically and wait for a person? (open)

### Estate facts to confirm

- None: every item and criterion here is approved or validated.
