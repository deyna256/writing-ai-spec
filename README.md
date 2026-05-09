# writing-ai-spec

Claude Code skill for writing **AI-first design documents** — specifications optimised for LLM implementation.

## What it does

Guides Claude through a two-phase process to produce a `SPEC.md` that maximises implementation quality when the implementer is an LLM.

**Six target properties of the output code:** cleanliness, simplicity, observability, testability, adaptability, best practices.

## Structure

Every spec follows this standard:

| Section | Content |
|---------|---------|
| §1 Overview | Goal, scope, architectural requirements, constraints, non-goals |
| §3 Entities & Data Types | Fields with justifications tied to §1 requirements |
| §4 Processes & Functions | Input / Output / Invariants / Side Effects → Functions |
| §5 Public Contract | Everything crossing the system boundary |

## Process

```
Phase 0: Context Gathering
  Scans existing materials → interviews only for gaps

Phase 1: Foundation
  §1 Architecture → §3 Entities
  [Gate: all fields justified, all invariants present]

Phase 2: Derivation
  §4 Processes → §5 Contract

Phase 3: Validation
  Traceability + 6 quality properties + completeness checklist
```

## Installation

```bash
# Add marketplace
/marketplace add github:deyna256/writing-ai-spec

# Install plugin
/install writing-ai-spec@writing-ai-spec
```

## Usage

Invoke via:
```
/writing-ai-spec
```

Or Claude auto-triggers on: `"напиши спеку"`, `"write spec"`, `"write design doc"`, `"create specification"`, `"дизайн документ"`.
