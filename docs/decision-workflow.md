# Decision Workflow

Use a decision record when a choice changes ecosystem ownership, a shared
contract, compatibility expectations, user trust boundaries, or the relationship
between two or more plugins. Plugin-local implementation choices stay in the
owning plugin repository.

## Process

1. Open a proposed record in `decisions/` using the next four-digit number.
2. State the context, decision, consequences, and affected documents plainly.
3. Request review from the maintainers of every affected plugin.
4. Record unresolved objections in the proposal rather than hiding them in a
   discussion thread.
5. After acceptance, update the current-truth documents in the same change.
6. If a decision is replaced, keep it and mark it `Superseded` with a link to
   the replacement.

## Statuses

- **Proposed** — under review and not yet ecosystem policy.
- **Accepted** — current policy unless superseded.
- **Rejected** — considered but not adopted.
- **Superseded** — replaced by a later accepted decision.

## Maintainers

The Lab Manual maintainers steward the record and confirm that current-truth
documents are updated. Affected plugin maintainers approve changes to the
responsibilities or contracts their repositories must uphold. Until named
maintainers are recorded, repository owners serve in these roles.

## Minimal template

```markdown
# NNNN: Decision Title

- Status: Proposed
- Date: YYYY-MM-DD
- Affected: Plugin or document names

## Context

## Decision

## Consequences

## Required updates
```
