# Yggdrasil Builder — Master Prompt

You are an AI engineer building **Yggdrasil Builder**: MCP Co-Design, Cognitive Reasoning & Execution Platform.

## Goal
Build a system that takes 3 inputs (Problem Statement, Documentation, Constraints), discovers MCP servers, scores them (Mjolnir), applies guardrails (Jataka), builds a Yggdrasil tree, reasons via Thinking Hats + Shatkona, issues Thunderbolt tokens, executes via Bifrost/Stormbreaker, and outputs Integration Suggestions + Collaborative Report + Meeting Mode.

## Stack
- Frontend: Next.js (TypeScript, Tailwind CSS, shadcn/ui)
- Backend: FastAPI (Python) + Node.js (MCP gateway)
- DB: PostgreSQL + Redis + Vector DB (pgvector/weaviate/milvus)
- Infra: Docker + Kubernetes
- Auth: OIDC + MFA
- Policy: OPA/Rego
- Observability: OpenTelemetry + Audit DB

## Core Modules
- Input Layer (parse 3 inputs)
- Intent Extractor (LLM)
- Agent Reach (search GitHub/npm/PyPI/Smithery/Glama/PulseMCP/MCP.so + web)
- Mjolnir Scorer (trust,reliability,relevance,cost,community)
- Jataka Guardrails (Ahimsa/Satya/Asteya/Brahmacharya/Aparigraha)
- Bifrost Router
- Yggdrasil Builder (tree)
- Thinking Hats
- Shatkona Protocol
- Thunderbolt Token (JWT, scoped, TTL, revocation)
- Stormbreaker (normalize)
- Output Generator (3 outputs)
- Audit Service

## MVP Scope
1. Project creation + 3 inputs
2. Agent Reach + dedupe + cache
3. Mjolnir scoring + filtering
4. Jataka validation
5. Yggdrasil tree + co-design UI (swap/prune/graft/lock)
6. Thinking Hats + Shatkona logs
7. Thunderbolt token issuance
8. Execute mocked MCP calls (safe)
9. Generate 3 outputs (export PDF/MD/JSON)
10. Audit log

## Implementation Rules
- Strict types
- Validate all inputs
- Enforce guardrails before execution
- Immutable audit
- Least privilege tokens
- Deterministic scoring first; LLM only for extraction/reports
- Avoid external writes in MVP
- Read-only for discovery
- Add Jataka certificate on every validated answer/plan

## Deliverables
- /backend (FastAPI)
- /frontend (Next.js)
- /mcp-gateway (Node.js)
- /infra (docker-compose, k8s manifests)
- /docs (API, schema, runbook)
- /tests (unit/integration)

## First Task
Scaffold monorepo with above, implement DB schema, and minimal working flow: input -> search -> score -> build tree -> outputs.
