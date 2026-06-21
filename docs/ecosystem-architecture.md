# Ecosystem Architecture

## Architectural model

DeLeon Labs is a federation of standalone plugins joined by documented contracts.
There is no shared implementation repository and no assumption that one plugin
may reach into another plugin's internal storage.

The ecosystem has four conceptual layers:

1. **Capture and sources** — material enters through notes, voice, references, or
   discovery workflows.
2. **Context** — Lighthouse assembles and exposes portable context packages.
3. **Action and interpretation** — specialized plugins transform, inspect, or
   navigate that context.
4. **Evidence and output** — results retain links to sources, transformations,
   and responsible plugins.

## Responsibility map

| Capability | Owner |
| --- | --- |
| Context assembly and handoff | Lighthouse |
| Explicit note transformations | Note Actions |
| Source discovery and collection | Crate Digger |
| Claim and citation verification | Citation Integrity |
| Voice capture and transcript handoff | Voice Memo |
| Entropy-oriented exploration | Entropeon |
| Focused graph navigation | Graph Focus |

Ownership means defining the behavior and contract for a capability. It does not
prevent another plugin from presenting an entry point that delegates to the owner.

## Integration rules

- Plugins integrate through versioned, documented payloads or user-visible links.
- A receiver validates what it understands and ignores optional unknown fields.
- The sender identifies itself and preserves source references.
- Material changes require explicit user intent and a reversible path when
  practical.
- Failure in one plugin must not corrupt another plugin's source material.
- Cross-plugin behavior belongs in this manual before it becomes an implicit
  dependency in code.

## Source-of-truth boundaries

This manual owns ecosystem intent, responsibility, and shared contracts. Each
plugin repository owns its implementation, plugin-specific documentation,
testing, releases, and compatibility declarations. When these disagree, the
disagreement should be resolved explicitly and captured here when it affects the
ecosystem.

## Evolution

Architecture changes begin as decision records. Accepted decisions update the
relevant vision, protocol, charter, and roadmap documents so readers do not need
to reconstruct current truth from historical records alone.
