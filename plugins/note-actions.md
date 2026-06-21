# Note Actions

## Charter

Note Actions owns explicit transformations of note material: turning selected
content into a new form while preserving the source and explaining the change.

## Owns

- User-invoked note transformations
- Transformation previews, results, and history
- Reversible application of changes where practical
- Clear distinction between source text and generated output

## Does not own

- General context assembly
- Source discovery or citation verification
- Silent background rewriting of user material
- Storage models belonging to other plugins

## Integration expectations

Note Actions consumes context packages, identifies the selected note material,
and returns results with transformation metadata and source references. It may
request richer context from Lighthouse but must not assemble hidden ambient
context independently.

## Success criteria

Users can predict what an action will affect, inspect what changed, and recover
the original material.

