# Lighthouse

## Charter

Lighthouse is the ecosystem's context authority. It helps a user identify what
matters now, assemble relevant material, and pass a bounded context package to
another plugin.

## Owns

- Context package semantics and lifecycle
- Context assembly, selection, and handoff
- Provenance continuity across handoffs
- User-visible controls for context scope

## Does not own

- Transforming note content
- Verifying citations or factual claims
- Capturing voice or discovering source material
- The receiving plugin's domain-specific action

## Integration expectations

Lighthouse accepts references from source-producing plugins and emits context
packages conforming to the context protocol. It must show what will be shared and
with whom before a handoff when the scope is not already evident.

## Success criteria

Users can understand, adjust, and reuse a context package without needing to know
how the contributing plugins store their data.

