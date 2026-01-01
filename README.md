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
│   (yellow)   │ │   (yellow)   │
└──────┬───────┘ └──────┬───────┘
       │               │
       └───────┬───────┘
               │
               ▼
┌─────────────────────────────┐
│    Weather Writer Agent     │
│            (red)            │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│   Weather Average Agent     │
│           (green)           │
└─────────────────────────────┘
```

## Agents

| Agent | Color | Description |
|-------|-------|-------------|
| Weather Pakistan Agent | 🟡 Yellow | Fetches temperature for Islamabad, Pakistan |
| Weather India Agent | 🟡 Yellow | Fetches temperature for New Delhi, India |
| Weather Writer Agent | 🔴 Red | Writes temperatures to `output/temperatures.md` |
| Weather Average Agent | 🟢 Green | Calculates average and writes to `output/average.md` |

## Output Files

- `output/temperatures.md` - Contains temperatures for each country
- `output/average.md` - Contains the calculated average
