# 0001: Plugins Remain Standalone

- Status: Accepted
- Date: 2026-06-20

## Context

The ecosystem needs shared direction without coupling every plugin's lifecycle,
implementation, and release process into one repository.

## Decision

Each DeLeon Labs plugin remains in a standalone repository. This manual is the
canonical home for ecosystem-level vision, architecture, charters, protocols,
decisions, and roadmap.

## Consequences

Plugins can evolve and ship independently, with clearer ownership and smaller
repository scopes. Shared behavior must be documented as a contract, and changes
that span repositories require deliberate coordination. Some documentation will
necessarily link between this manual and plugin-specific repositories.
