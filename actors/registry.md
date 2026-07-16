# Threat Actor Registry

Human-readable index of profiled actors. Generated from [`registry.yaml`](./registry.yaml). See [SCHEMA.md](./SCHEMA.md) for field definitions.

**Status legend** — Profile: `suspected` → `tentative` → `confirmed` · Attribution: `low` / `moderate` / `high` · Operational: `active` / `dormant` / `disrupted` / `defunct`.

| ID | Code name | Name | Type | Nexus | Operational | Profile | Attribution | First seen | Profile |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| `ACT-2026-BLACKCORE` | AMON MIRAGE | BlackCore | Influence-ops vendor | Israel | Disrupted | Tentative | Moderate | 2026-03 | [profile](./ACT-2026-BLACKCORE/profile.md) |
| `ACT-2026-TEAMJORGE` | AHAB PUPPETEER | Team Jorge | Influence-ops vendor + cyber | Israel | Disrupted | Confirmed | High | 2015 | [profile](./ACT-2026-TEAMJORGE/profile.md) |
| `ACT-2026-PANZERPARROT` | PANZER PARROT | AfD Alternita operation | Grassroots-astroturf | Germany | Active | Tentative | High | 2026-07 | [profile](./ACT-2026-PANZERPARROT/profile.md) |
| `ACT-2026-MANASSEHCHORUS` | MANASSEH CHORUS | Clock Tower X (Parscale) | Influence-ops vendor | United States · Israel | Active | Tentative | High | 2025-09 | [profile](./ACT-2026-MANASSEHCHORUS/profile.md) |

## Linked situation reports

| Sitrep | Actor(s) | Status |
| :-- | :-- | :-- |
| [2026-06-blackcore-france-elections](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-06-blackcore-france-elections) | `ACT-2026-BLACKCORE` | ✓ linked (reciprocal) |
| [2026-07-afd-alternita-ai-ragebait](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-07-afd-alternita-ai-ragebait) | `ACT-2026-PANZERPARROT` | ✓ linked (reciprocal) |
| [2026-07-manasseh-chorus-parscale-israel](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-07-manasseh-chorus-parscale-israel) | `ACT-2026-MANASSEHCHORUS` | ✓ linked (reciprocal) |

## Not yet profiled (referenced as comparisons)

_None — all referenced actors are now profiled._
