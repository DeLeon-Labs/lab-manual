# Cross-Plugin Assumption Inventory

This inventory makes current integration assumptions visible before they harden
into accidental contracts. An assumption is not a serialized protocol guarantee.

| Assumption | Participants | Current basis | Validation needed |
| --- | --- | --- | --- |
| Lighthouse can hand a bounded selection to another plugin without copying the canonical source. | Lighthouse and all receivers | Context invariants | Prototype reference-only and snapshot handoffs. |
| Every source can carry an identity and enough provenance to be recognized after a handoff. | All producers and receivers | Context package concept | Decide identifier scope and cross-device behavior. |
| Receivers can reject unsupported required fields while tolerating unknown optional fields. | Lighthouse and all receivers | Integration rules | Define serialized required/optional field behavior. |
| Note Actions can return a result without directly owning another plugin's storage. | Note Actions, Lighthouse | Accepted ownership decisions | Prototype preview, apply, and recovery boundaries. |
| Voice transcript segments can reference stable time ranges in external audio. | Voice Memo, Lighthouse, Note Actions | Voice Memo charter | Define audio reference and revocation behavior. |
| Graph relationships can be represented without importing a plugin's entire graph model. | Graph Focus, Lighthouse | Graph Focus charter | Define the minimum node-and-edge representation. |
| Citation findings can point to exact claim and source locations. | Citation Integrity, Lighthouse | Citation Integrity charter | Define portable selectors and stale-source behavior. |
| Discovered material remains distinguishable from user-authored material. | Crate Digger, Lighthouse | Crate Digger charter | Define source type and authorship provenance fields. |
| Permissions can narrow during a handoff and are never silently broadened. | All plugins | Context invariants | Define vocabulary, enforcement, and revocation propagation. |

## Maintenance

Add an entry when implementation work reveals an undocumented dependency across
repositories. Remove it only when testing disproves it or an accepted contract
and conformance example replace it. Contract changes follow the decision
workflow.
