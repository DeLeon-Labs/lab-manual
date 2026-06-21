# 0002: Lighthouse Owns Context

- Status: Accepted
- Date: 2026-06-20

## Context

Several plugins need relevant material from elsewhere in the ecosystem. If each
plugin independently gathers ambient context, users cannot easily understand or
control what is shared, and incompatible context models will emerge.

## Decision

Lighthouse owns context assembly, context package semantics, scope controls, and
cross-plugin handoff. Other plugins may produce source references or consume
context, but they do not create competing ecosystem-wide context authorities.

## Consequences

Context behavior has one accountable owner and receivers can integrate against a
stable conceptual contract. Lighthouse becomes a critical integration surface
and must remain transparent, permission-aware, and resilient. Domain plugins
retain responsibility for validating context before acting on it.
