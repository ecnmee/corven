# Roadmap

High-level, public view of where Corven is headed. For the full architectural reasoning behind each stage, see the ADRs in the private development monorepo (referenced from internal docs — not all architecture decisions are public yet).

| Stage | What ships | Status |
|---|---|---|
| v1 | Design tokens + atomic utilities (5-layer static core, no build tooling required to consume) | In development |
| v2 | JIT compiler (scans your templates, generates only the CSS you use) + component composition syntax | Planned |
| v3 | Lazy loading of CSS by feature domain | Planned |
| v4 | Full CLI (pattern analysis, build explain mode, performance budgets) | Planned |
| v5+ | Project diagnostics command, dependency graph, browser DevTools inspector, official templates | Planned |

## Current focus

Finishing v1: the Core needs to compile cleanly, have zero duplicate utilities, ship with compilation tests, minimal usage examples, and generated reference documentation before it's considered done. No timeline is published yet — quality gates come before dates.
