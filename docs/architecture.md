# NeoKube Architecture Overview

## Core Concepts

```
┌─────────────────────────────────────────────┐
│                NeoKube Platform             │
│                                             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  │
│  │  Agents  │  │Workflows │  │Connectors│  │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  │
│       │             │             │         │
│       └─────────────┴─────────────┘         │
│                     │                       │
│              ┌──────▼──────┐                │
│              │  Orchestrator│               │
│              │  (Kubinote) │                │
│              └──────┬──────┘                │
│                     │                       │
│         ┌───────────┴───────────┐           │
│    ┌────▼────┐           ┌──────▼────┐      │
│    │  LLM    │           │  Client   │      │
│    │  Layer  │           │  Stack    │      │
│    │(Mistral)│           │(CRM/ERP..)│      │
│    └─────────┘           └───────────┘      │
└─────────────────────────────────────────────┘
```

## Key Principles

- **Agent-first** — every business action is encapsulated in a traceable, auditable agent
- **Stack-agnostic** — connects to any CRM, ERP, or document system via connectors
- **Sovereign by design** — runs on European infrastructure, compatible with GDPR requirements
- **Subscription-based maintenance** — deployed once, maintained continuously

## Production vs Community

| Feature | Community (this repo) | Production (Kubinote) |
|---|---|---|
| Agent templates | ✅ | ✅ |
| Workflow examples | ✅ | ✅ |
| Full orchestrator | ❌ | ✅ |
| Client stack connectors | Starters only | Full integration |
| SLA & support | ❌ | ✅ |
| Commercial license | Not required (non-prod) | Required |
