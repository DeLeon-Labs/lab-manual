# 0003: Note Actions Owns Transformation

- Status: Accepted
- Date: 2026-06-20

## Context

Many workflows can suggest changes to note material. Allowing every plugin to
apply transformations differently would fragment preview, history, provenance,
and recovery behavior.

## Decision

Note Actions owns explicit transformations of note material. Other plugins may
propose outputs or delegate a transformation, but application to notes follows
the behavior and contract defined by Note Actions.

## Consequences

Users get a consistent boundary between proposals and applied changes, along with
shared expectations for preview, provenance, and reversibility. Note Actions must
support diverse transformation intents without absorbing the domain logic or
identity of every plugin.
