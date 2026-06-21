# Ecosystem Roadmap

This roadmap describes ecosystem coordination, not implementation schedules for
individual plugins. Dates and release commitments belong in plugin repositories.

## Now: establish the foundation

- Ratify the ecosystem vision and plugin charters.
- Resolve the open questions in the context protocol.
- Add links to each standalone plugin repository as they are established.
- Define the decision-record workflow and maintainers for this manual.
- Inventory existing cross-plugin assumptions before they harden into contracts.

## Next: validate the contracts

- Describe representative handoffs between Lighthouse and every plugin.
- Define a serialized context-package format and compatibility policy.
- Document permissions, revocation, error handling, and provenance behavior.
- Prototype one end-to-end flow without moving plugin code into this repository.
- Add compatibility declarations to participating plugin repositories.

## Later: deepen interoperability

- Publish ecosystem-wide interaction and trust guidelines.
- Define conformance examples for context producers and consumers.
- Establish a cross-plugin release and deprecation process.
- Measure whether handoffs remain understandable, reversible, and useful.
- Revisit ownership decisions when real workflows reveal unclear boundaries.

## Roadmap guardrails

- Plugins remain independently useful and independently released.
- Shared infrastructure is introduced only after a documented contract proves
  insufficient.
- New capabilities receive an explicit owner before implementation begins.
- The roadmap does not substitute for accepted architectural decisions.
