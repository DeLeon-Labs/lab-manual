# DeLeon Labs Manual

This repository is the canonical source of truth for the DeLeon Labs creative
software ecosystem. It explains the shared vision, system boundaries, context
model, plugin charters, architectural decisions, and ecosystem roadmap.

Individual plugins remain in standalone repositories. Their repositories own
implementation, release history, and operational instructions; this manual owns
the explanation of how those products fit together.

## Start here

- [Ecosystem vision](docs/ecosystem-vision.md)
- [Ecosystem architecture](docs/ecosystem-architecture.md)
- [Context protocol](docs/context-protocol.md)
- [Plugin charters](plugins/)
- [Decision records](decisions/)
- [Ecosystem roadmap](roadmap/ecosystem-roadmap.md)

## Documentation principles

1. Name one owner for every ecosystem responsibility.
2. Prefer stable contracts over knowledge of another plugin's internals.
3. Keep user intent, provenance, and reversibility visible.
4. Record consequential architectural choices as decision records.
5. Describe current truth plainly and label future direction explicitly.

## Repository scope

This repository contains documentation only. It does not contain plugin source
code, shared runtime code, generated artifacts, or deployment configuration.
