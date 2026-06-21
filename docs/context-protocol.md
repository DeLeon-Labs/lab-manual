# Context Protocol

## Status

This document defines the conceptual contract for context exchanged between
DeLeon Labs plugins. It intentionally does not prescribe a code format yet.

## Goals

The protocol makes context portable, inspectable, attributable, and safe to
extend. A plugin should be able to accept useful context without knowing the
internal model of the plugin that produced it.

## Context package

A context package should communicate:

- a stable package identifier;
- the producing plugin and protocol version;
- the user's stated intent, when known;
- one or more source items or references;
- provenance for each source;
- relevant selections, relationships, and ordering;
- creation time and optional freshness information;
- permissions, sensitivity, or sharing constraints;
- transformations already applied; and
- optional receiver hints that do not bind the receiver.

## Roles

**Lighthouse** owns context assembly, package semantics, and handoff behavior.
Producing plugins contribute source material and provenance. Receiving plugins
declare the context they can use and remain responsible for validating inputs
before acting.

## Invariants

1. A package never silently becomes the canonical copy of its source material.
2. Provenance survives every handoff and transformation.
3. Missing optional context reduces capability rather than causing fabrication.
4. Sensitive context is not broadened beyond its stated permission boundary.
5. Transformations append history; they do not rewrite the history of the source.
6. Receivers identify unsupported or ambiguous required fields to the user.

## Versioning

The protocol will use explicit versions once a serialized format exists.
Compatible additions should be additive. Breaking semantic changes require a new
major version, a migration note, and an ecosystem decision record.

## Open questions

- Which identifiers must remain stable across devices and repositories?
- How should source revocation propagate to derived context?
- What is the minimum portable representation for graph relationships?
- Which permission vocabulary is shared across all plugins?
- How should large or binary sources be referenced without embedding them?
