# hermes-agent — AGENTS.md

> ANN-Mesh parity repo. Canonical system spec: https://github.com/Thelastlineofcode/ANN-Mesh/blob/main/AGENTS.md

## Role in ANN-Mesh
Growing memory pattern (NousResearch) — reference implementation for Qdrant + Neo4j dual-brain writes.
Skill file: `.ann-core/skills/agent-memory-persistence.md`
Primary agents: **Pairan** (Qdrant/Neo4j writes) · **Madea** (memory synthesis)

## Key Rules
- Load `agent-memory-persistence.md` skill before operating
- Boot: `ann health` → `ann context hydrate --agent ann-agent-pairan`
- Close loop: `ann context store` after every session
- No self-merges. Scooter opens PRs. Roids gates.

## Connections
- rickd: `http://localhost:8080`
- Qdrant: `http://localhost:6333`
- Neo4j: `bolt://localhost:7687`
- ANN-Mesh: https://github.com/Thelastlineofcode/ANN-Mesh
