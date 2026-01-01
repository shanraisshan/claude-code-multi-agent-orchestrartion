# Claude Code Multi-Agent Orchestration

Run `/orchestrate` in Claude Code CLI to fetch temperatures from Pakistan and India in parallel, then calculate their average.

```
/orchestrate
```

```
┌─────────────────────────────┐
│        /orchestrate         │
└──────────────┬──────────────┘
               │
       ┌───────┴───────┐
       │               │
       ▼               ▼
┌──────────────┐ ┌──────────────┐
│   Weather    │ │   Weather    │
│   Pakistan   │ │    India     │
│    Agent     │ │    Agent     │
└──────┬───────┘ └──────┬───────┘
       │               │
       └───────┬───────┘
               │
               ▼
┌─────────────────────────────┐
│   output/temperatures.md    │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│   Weather Average Agent     │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│     output/average.md       │
└─────────────────────────────┘
```
