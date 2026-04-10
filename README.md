# Fredsidian

**Fredsidian** is an open source architecture for building **Obsidian-style memory** for AI assistants.

It combines:
- **assistant operational memory** for high-signal continuity and assistant-specific state
- **Obsidian knowledge graph memory** for linked notes, projects, research, decisions, and long-term context

If you are looking for:
- Obsidian memory for AI agents
- Obsidian second brain for assistants
- markdown-based long-term memory
- local knowledge graph memory for autonomous assistants
- hybrid assistant memory architecture

that is exactly what Fredsidian is designed to explore.

The goal is simple:
- keep Fred operationally reliable
- gain the benefits of an Obsidian second brain
- avoid mixing volatile assistant state with the entire personal knowledge vault too early

## What Fredsidian Is

Fredsidian is a design for using an **Obsidian-style second brain as long-term assistant memory** without losing the safety and clarity of a smaller operational memory core.

Instead of forcing an AI assistant to rely only on chat history or a single flat memory file, Fredsidian proposes:
- a trusted assistant memory layer for operational truth
- an Obsidian-compatible markdown knowledge graph for broader long-term context
- scoped retrieval rules for privacy, accuracy, and maintainability

This makes Fredsidian useful for people building:
- AI personal assistants
- local-first memory systems
- Obsidian-integrated agent workflows
- markdown knowledge graph memory systems
- retrieval-augmented memory for autonomous agents

## Design Principles

- assistant memory and PKM are related, but not identical
- operational truth should stay small, explicit, and trusted
- Obsidian should provide rich linked context, not replace core safety and continuity rules
- retrieval should be scoped, evidence-based, and privacy-aware
- start read-mostly, expand to write workflows later

## Core Model

Fredsidian uses a **two-tier memory system**:

### Tier 1: Fred Core Memory
Used for:
- assistant operating rules
- delivery preferences
- safety boundaries
- recurring assistant tasks
- short, durable user preferences
- daily operational logs
- high-signal curated memory

Suggested storage:
- `MEMORY.md`
- `memory/YYYY-MM-DD.md`

### Tier 2: Obsidian Graph Memory
Used for:
- projects
- research
- people and entities
- decision records
- reference notes
- long-form planning
- linked daily/project context

Suggested storage:
- Obsidian vault folders and markdown notes

## Retrieval Order

When Fred needs context:

1. Check **core assistant memory** first for operational truth
2. Check **Obsidian graph memory** for broader context and linked knowledge
3. Distinguish between:
   - facts
   - hypotheses
   - next checks
4. Return the smallest useful synthesis with source references when possible

## Write Policy

### Core assistant memory writes
Allowed for:
- explicit remember-this requests
- durable preferences
- important assistant-operational facts
- daily logs

### Obsidian writes
Preferred for:
- project summaries
- research notes
- linked plans
- decision notes
- reusable references
- draft artifacts

### Guardrails
- do not silently rewrite broad vault content
- do not write secrets unless explicitly required
- do not expose personal vault content in shared contexts
- require approval before broad externalized or high-impact changes

## Recommended V1 Scope

Fredsidian v1 should be:
- read-mostly
- scoped to specific folders
- explicit about privacy boundaries
- usable without vector databases or plugin sprawl

V1 should **not** try to:
- replace all assistant memory
- automatically rewrite the whole vault
- infer trust across every note in the vault

## Future Expansion

Potential v2/v3 additions:
- scoped write-back into `Assistant/` folders
- Local REST API integration for structured vault access
- semantic indexing / embeddings for improved retrieval
- note templates for project, person, and decision pages
- retrieval confidence ranking
- provenance and citation support

## Open Source Project Structure

```text
fredsidian/
  README.md
  docs/
    architecture.md
    note-schema.md
    retrieval-policy.md
    privacy-model.md
    roadmap.md
  examples/
    vault-structure.md
    sample-notes/
      project-note.md
      person-note.md
      decision-note.md
      research-note.md
      daily-note.md
```

## Search Keywords / Discovery

Relevant terms this project intentionally addresses:
- Obsidian memory for AI
- Obsidian-style memory
- Obsidian second brain for agents
- AI assistant memory architecture
- markdown memory system
- local-first AI memory
- knowledge graph memory for assistants
- personal assistant memory graph
- hybrid memory architecture for AI agents

## Status

This repo is currently a design/spec project, not an implementation release.
