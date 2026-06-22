---
id: ACT-YYYY-SHORTNAME
name: <Primary name>
aliases: []
actor_type: unknown                 # §7.1 influence-ops-vendor | state-actor | state-aligned-proxy | hacktivist | cybercrime | commercial-pr-firm | private-intelligence | grassroots-astroturf | unknown
country_nexus: []                   # suspected origin/operating nexus; [] if unknown
operational_status: unknown         # active | dormant | disrupted | defunct | unknown
profile_status: suspected           # suspected | tentative | confirmed
attribution_confidence: low         # low | moderate | high
first_observed: YYYY-MM
last_active: YYYY-MM
last_updated: YYYY-MM-DD
tlp: CLEAR                          # CLEAR | GREEN | AMBER | AMBER+STRICT | RED
motivations: []                     # contract-hire | geopolitical-narrative | domestic-political | financial | reputation-management | data-harvesting | ideological | unknown
target_sectors: []
target_geographies: []              # ISO codes where possible
frameworks: [DISARM, ATT&CK, AUNOO-8T]
aunoo_tactic_vector:                # 0 none | 1 occasional | 2 frequent | 3 signature
  legitimacy_inversion: 0
  severity_minimization: 0
  category_reframing: 0
  whataboutism: 0
  identity_reframing: 0
  motive_substitution: 0
  agent_swap: 0
  cause_effect_reversal: 0
related_sitreps: []                 # SITREP:<folder-slug> — must be reciprocal
related_actors: []                  # ACT-YYYY-... — must be reciprocal
source_count: 0
admiralty_high_water: F6            # best grade among key sources (A1 best … F6 worst)
analyst: "Aunoo Intelligence"
review_status: draft                # draft | in-review | published
---

# THREAT ACTOR PROFILE: <Name> (<ID>)

**Classification:** Unclassified · OSINT · **TLP:**<COLOUR>
**As of:** <DD Mon YYYY, HH:MM UTC>
**Profile status:** <suspected | tentative | confirmed> · **Attribution confidence:** <low | moderate | high>
**Prepared from:** <N> sources · Admiralty high-water <grade>

---

## Bottom line up front (BLUF)

<3–6 sentences. What the actor is; the single most important judgement; the biggest evidentiary caveat. State plainly where the entity is well-evidenced vs. where attribution is thin. If the name may be confused with another actor, say so here.>

---

## Quick-reference card

| Field | Value |
| :-- | :-- |
| Actor ID | `<ID>` |
| Aliases | <…> |
| Type | <actor_type> |
| Country nexus | <…> |
| Operational status | <…> |
| First observed | <…> |
| Last active | <…> |
| Attribution confidence | <…> |
| Frameworks mapped | DISARM · ATT&CK · Aunoo 8-tactic |

---

## Attribution & confidence

**Diamond Model.**

| Vertex | Finding | Confidence |
| :-- | :-- | :-- |
| Adversary | <who — including the "who commissioned it" layer if a vendor> | <…> |
| Capability | <tooling, personas, content> | <…> |
| Infrastructure | <domains, servers, hosting, corporate shells> | <…> |
| Victim | <targets> | <…> |

**Confidence statement.** <What is `confirmed`, what is `tentative`, what is `suspected`, and why. Grade the load-bearing claims (Admiralty).>

**Competing hypotheses.** <List the main alternative explanations and what evidence would discriminate between them. Influence-op attribution is probabilistic — show the fork.>

---

## History & evolution

<Narrative.>

| When | Event |
| :-- | :-- |
| <YYYY-MM> | <…> |

---

## Ownership, structure & key personnel

> Tag every named person/company with an entity-resolution status: `auto · confirmed · ambiguous · unresolved`.

- **<Name>** — <role>. Status: `<…>`. <Basis / source. Note any denial on record.>

---

## Targeting / victimology

<Who they target and the selection logic — sector, geography, political alignment, the common thread.>

---

## Modus operandi

<Prose: how they sell the service, set up infrastructure, run a campaign, amplify, and burn down/scrub on exposure. The operational lifecycle.>

---

## TTPs

### (a) DISARM techniques

| DISARM ID | Technique | How the actor uses it | Evidence |
| :-- | :-- | :-- | :-- |
| <Txxxx> | <…> | <…> | <source> |

### (b) MITRE ATT&CK (cyber-enabled activity only)

| ATT&CK ID | Technique | Use | Evidence |
| :-- | :-- | :-- | :-- |
| <Txxxx> | <…> | <…> | <source> |

> If the actor performs little/no intrusion activity, say so: most pure-IO actors touch only acquisition/collection techniques. Do not force mappings.

### (c) Aunoo 8-tactic reframing vector

| Tactic | Salience (0–3) | Rationale / example |
| :-- | :-- | :-- |
| Legitimacy Inversion | <…> | <…> |
| Severity Minimization | <…> | <…> |
| Category Reframing | <…> | <…> |
| Whataboutism | <…> | <…> |
| Identity Reframing | <…> | <…> |
| Motive Substitution | <…> | <…> |
| Agent Swap | <…> | <…> |
| Cause-Effect Reversal | <…> | <…> |

> Record **fabrication** (invented content/personas/sites) separately here as a note — it is outside the reframing model and belongs under DISARM. A heavy-fabrication / low-reframing profile is itself a signature.

---

## Infrastructure & indicators

<Narrative summary. Full observables in `indicators.yaml`, referenced as `IOC-<n>`.>

---

## Campaigns & incidents

### <CAMP-ID-01> — <Campaign name> (<date>)

<Summary.> **Sitrep:** [<slug>](https://github.com/AuNooAI/situationreports/tree/main/reports/<slug>)

---

## Relationships

- **<Other actor / company>** (`<ID>`) — <nature of relationship: shared infra, lineage, comparison>.

---

## Detection & monitoring guidance (Aunoo platform)

- **Raise-conditions:** <what signals should surface this actor — domains, persona patterns, narrative + amplification signatures>.
- **Relevant detectors / tactic-heads:** <which of the 8 heads + amplification/cluster modules apply>.
- **label_status workflow:** <what moves a hit from suspected → tentative → confirmed for this actor>.
- **Pivots:** <given one indicator, what to pivot on — registrar, hosting cluster, corporate address, persona reuse>.

---

## Outlook & watch indicators

<Forward-looking. Call out the single best early-warning signal.>

---

## Source assessment & confidence

<Overall reliability read. Where the picture is thin or single-sourced. What new evidence would raise/lower confidence or change attribution.>

---

## Changelog

| Date | Change |
| :-- | :-- |
| <YYYY-MM-DD> | Initial profile created at `<profile_status>`. |

---

## Sources

1. [<Title>](<URL>) — <Admiralty grade>
