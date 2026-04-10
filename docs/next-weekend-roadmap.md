# Fredsidian Next-Weekend Roadmap

## Goal

Use the scheduled Fredsidian implementation window to ship a clean V1 foundation, not a sprawling prototype.

## Definition of Success

By the end of the implementation weekend, Fredsidian should have:
- a basic code scaffold
- operational memory loading
- scoped vault reading
- simple retrieval/ranking
- privacy-aware retrieval policy hooks
- a small CLI or test harness proving the flow works

## Scope Guardrails

Do:
- build the boring core
- keep retrieval inspectable
- favor deterministic heuristics over fancy claims
- prove the architecture end to end on sample notes

Do not:
- add embeddings unless clearly needed
- add plugin dependencies early
- build autonomous broad writeback
- promise perfect semantic memory

## Day 1 Plan

### 1. Scaffold the package
Create:
- `src/fredsidian/config.py`
- `src/fredsidian/models.py`
- `src/fredsidian/memory_core.py`
- `src/fredsidian/vault_reader.py`
- `src/fredsidian/search.py`
- `src/fredsidian/retrieval.py`
- `src/fredsidian/policies.py`
- `src/fredsidian/synthesize.py`

### 2. Implement operational memory loading
Support:
- `MEMORY.md`
- daily memory files

### 3. Implement vault reading
Support:
- markdown file discovery
- basic frontmatter parsing
- heading/body extraction

### 4. Implement simple search
Score on:
- title/path exactness
- keyword frequency
- note recency when available
- note type relevance

## Day 2 Plan

### 5. Implement retrieval orchestration
Flow:
- operational memory first
- Obsidian scope second
- assemble minimal context pack

### 6. Implement privacy policy layer
Support:
- allowlisted folders
- blocked paths
- shared-context restrictions

### 7. Implement synthesis contract
Return:
- facts
- relevant context
- uncertainty
- next checks

### 8. Add a small proof harness
Example forms:
- simple CLI query runner
- local script against sample notes

## Stretch Goals

Only if core flow is clean:
- limited source citations formatting
- template-based note parsing improvements
- narrow assistant draft writeback hooks

## Deliverables

Minimum weekend deliverables:
- working scaffold
- retrieval demo on sample notes
- one or two tests for core parsing/retrieval paths
- updated README usage section

## Decision Rule

If a task makes Fredsidian feel smarter but less understandable, delay it.

The point of V1 is trust and clarity, not magic tricks.
