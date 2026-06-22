# Threat Actor Profile — Schema & Authoring Specification

**Version:** 0.1 · **As of:** 2026-06-20 · **Maintainer:** Aunoo Intelligence

This document defines the structure, controlled vocabularies, framework mappings, and cross-linking rules for actor profiles in this repository. It is the contract that keeps profiles consistent, machine-indexable, and synchronised with the [situationreports](https://github.com/AuNooAI/situationreports) repo and with the platform's detection data model.

---

## 1. Design principles

1. **Entity, not event.** A profile is the durable record of an *actor*. Events are documented as situation reports and linked in. The profile is updated over time; sitreps are point-in-time.
2. **Same language as the detectors.** Confidence, status, and tactic vocabularies are reused verbatim from the platform (`label_status`, entity-resolution statuses, the 8-tactic taxonomy) so a profile and a detector output are directly comparable.
3. **Evidence over assertion.** Every load-bearing claim carries a source and, where attribution-critical, an Admiralty grade. Claims that cannot be graded `confirmed` are published at `suspected`/`tentative` and labelled.
4. **Honest about framework fit.** Influence actors rarely map cleanly to MITRE ATT&CK, and not every behaviour is a "reframing" tactic. The schema requires noting where a framework does *not* fit rather than forcing a mapping.
5. **Human-readable first, machine-readable alongside.** `profile.md` is for analysts; `meta.yaml` and `indicators.yaml` carry the same facts in structured form for indexing and tooling.

---

## 2. Folder layout per actor

```
actors/<ID>/
├─ profile.md        # narrative profile — the primary deliverable (§5)
├─ meta.yaml         # machine-readable actor record — mirrors profile front-matter (§4)
└─ indicators.yaml   # structured observables / IOCs (§6)
```

The folder name **is** the canonical actor ID (§3).

---

## 3. Identifier scheme

**Canonical actor ID:** `ACT-<YYYY>-<SHORTNAME>`

- `ACT` — fixed prefix (Actor).
- `<YYYY>` — year the actor was **first profiled** by Aunoo (not founded; not first active). Stable forever once assigned.
- `<SHORTNAME>` — uppercase, hyphen-free slug of the primary name. Keep ≤ 16 chars.

Examples: `ACT-2026-BLACKCORE`, `ACT-2026-TEAMJORGE`.

Rules:
- The ID never changes, even if the actor renames. Renames go in `aliases` and the changelog.
- If two profiled clusters later prove to be one actor, **merge** into the older ID and leave a `merged_into:` tombstone in the newer `meta.yaml`.
- Numbered collisions (two actors, same year + shortname) get a `-2` suffix.

### 3.1 Code names (CIOPS)

In addition to the canonical ID, a coordinated-influence-operations (CIOPS) actor may be assigned a human-memorable **code name** in the `codename` field — a two-word, all-caps handle (e.g. `AMON MIRAGE`). Code names aid briefing and recall and are independent of the ID (the ID is for tooling; the code name is for humans). The code-name *theme* may encode the actor's suspected nexus — e.g. an Egyptian/Levantine deity prefix (`AMON …`) for a Middle-East-nexus actor — but the theme is advisory, not a controlled vocabulary. One code name maps to exactly one ID; never reuse a code name across actors.

**Related cross-reference IDs:**
- **Situation reports** are referenced by their repo folder slug, e.g. `2026-06-blackcore-france-elections`, prefixed `SITREP:` in front-matter.
- **Indicators** get local IDs `IOC-<n>` within `indicators.yaml`.
- **Campaigns** (a named operation by the actor) get `CAMP-<ID>-<n>`, e.g. `CAMP-BLACKCORE-01`.

---

## 4. Front-matter / `meta.yaml` fields

`profile.md` opens with a YAML front-matter block. `meta.yaml` carries the identical fields (single source of truth for tooling). Required fields are marked **R**.

```yaml
id: ACT-2026-BLACKCORE            # R  canonical ID (= folder name)
name: BlackCore                   # R  primary display name
codename: AMON MIRAGE             #    Aunoo CIOPS code name (see §3.1); optional
aliases: [Black Core]             #    other spellings / cover names
actor_type: influence-ops-vendor  # R  controlled vocab §7.1
country_nexus: [Israel]           # R  suspected origin/operating nexus; [] if unknown
operational_status: disrupted     # R  active|dormant|disrupted|defunct|unknown §7.2
profile_status: tentative         # R  suspected|tentative|confirmed §7.3
attribution_confidence: moderate  # R  low|moderate|high §7.4
first_observed: 2026-03           # R  YYYY or YYYY-MM of earliest known activity
last_active: 2026-06              #    most recent known activity
last_updated: 2026-06-20          # R  date this profile was last edited
tlp: CLEAR                        # R  CLEAR|GREEN|AMBER|AMBER+STRICT|RED §7.5
motivations: [contract-hire, geopolitical-narrative]   # §7.6
target_sectors: [elections, political-candidates, civil-society]
target_geographies: [FR, US-NY, GB-SCT, AO, TG]        # ISO where possible
frameworks: [DISARM, ATT&CK, AUNOO-8T]   # which mappings the profile carries
aunoo_tactic_vector:              #    primary reframing tactics, 0–3 salience §7.7
  identity_reframing: 3
  legitimacy_inversion: 2
  severity_minimization: 0
  category_reframing: 1
  whataboutism: 0
  motive_substitution: 0
  agent_swap: 0
  cause_effect_reversal: 0
related_sitreps:                  #    reciprocal links — §8
  - SITREP:2026-06-blackcore-france-elections
related_actors:                   #    other profiled actors (relationship in body)
  - ACT-2026-TEAMJORGE   # comparison/lineage, not necessarily linked operationally
source_count: 14                  #    number of distinct sources underpinning the profile
admiralty_high_water: C3          #    best (most reliable) grade among key sources
analyst: "Aunoo Intelligence"     # R
review_status: published          #    draft|in-review|published
```

---

## 5. `profile.md` section order

The narrative profile follows a fixed section order so profiles are skimmable and diffable. Sections marked *(opt)* may be omitted when empty, with a one-line "no current data" note.

1. **Title** — `# THREAT ACTOR PROFILE: <Name> (<ID>)`
2. **Header block** — Classification/TLP, As of, Profile status, Attribution confidence, Prepared from (source count + Admiralty high-water).
3. **BLUF** — 3–6 sentences. What the actor is, the single most important judgement, and the biggest evidentiary caveat.
4. **Quick-reference card** — a table: ID, aliases, type, nexus, operational status, first/last seen, attribution confidence, frameworks.
5. **Attribution & confidence** — the **Diamond Model** (Adversary / Capability / Infrastructure / Victim), plus an explicit confidence statement and the key competing hypotheses. Admiralty-grade the load-bearing claims.
6. **History & evolution** — narrative + a timeline table.
7. **Ownership, structure & key personnel** — each named person/company tagged with an entity-resolution status (§7.8) and a source.
8. **Targeting / victimology** — who they hit and the selection logic.
9. **Modus operandi** — how they sell, set up, run, and burn down operations (prose).
10. **TTPs** — three mapped subsections: **(a) DISARM**, **(b) MITRE ATT&CK**, **(c) Aunoo 8-tactic vector** with rationale. Note non-fit explicitly.
11. **Infrastructure & indicators** — narrative summary; details live in `indicators.yaml`, referenced by `IOC-<n>`.
12. **Campaigns & incidents** — one subsection per campaign, each cross-linked to its sitrep(s).
13. **Relationships** — links to other actors/companies (lineage, shared infra, comparison).
14. **Detection & monitoring guidance** — *Aunoo-specific*: what signals should raise this actor on the platform, which detectors/tactic-heads apply, suggested `label_status` workflow, and watch indicators.
15. **Outlook & watch indicators** — forward-looking, with the single best early-warning signal called out.
16. **Source assessment & confidence** — overall reliability read; where the picture is thin; what would change the assessment.
17. **Changelog** — dated revisions (append-only).
18. **Sources** — numbered markdown links, ideally Admiralty-graded.

---

## 6. `indicators.yaml` structure

Observables are typed, graded, and dated so they can be tracked, expired, and matched against live telemetry.

```yaml
indicators:
  - id: IOC-1
    type: domain                # domain|subdomain|ip|server|persona|fake-outlet|
                                # fake-charity|company|address|registrar|wallet|
                                # email|handle|hash|ad-account|other
    value: "blackcore.online"
    status: confirmed           # suspected|tentative|confirmed (mirrors label_status)
    confidence: high            # low|moderate|high
    first_seen: 2025-08
    last_seen: 2026-05
    state: inactive             # active|inactive|taken-down|sinkholed|unknown
    context: "Primary marketing site; anonymous Icelandic registrar."
    source: "Haaretz/Libération, 2026-05"
```

Conventions: prefer **defanged** values for live malicious infrastructure (`blackcore[.]online`). Every indicator carries a `status` and `confidence`; do not list ungraded indicators. Group related observables with a shared `campaign:` or `cluster:` key where useful.

---

## 7. Controlled vocabularies

### 7.1 `actor_type`
`influence-ops-vendor` (hire-for-service) · `state-actor` · `state-aligned-proxy` · `hacktivist` · `cybercrime` · `commercial-pr-firm` · `private-intelligence` · `grassroots-astroturf` · `unknown`

### 7.2 `operational_status`
`active` · `dormant` · `disrupted` (infrastructure taken down / under investigation, may resurface) · `defunct` · `unknown`

### 7.3 `profile_status` *(mirrors platform `label_status`)*
`suspected` (plausible, single-thread evidence) · `tentative` (corroborated, attribution not settled) · `confirmed` (analyst-reviewed, multi-source, defensible in public)

### 7.4 `attribution_confidence`
`low` · `moderate` · `high`. This is distinct from `profile_status`: a profile can be `confirmed` as a real operation while attribution of *who runs it* remains `low`.

### 7.5 `tlp`
Standard FIRST TLP: `CLEAR` · `GREEN` · `AMBER` · `AMBER+STRICT` · `RED`.

### 7.6 `motivations`
`contract-hire` · `geopolitical-narrative` · `domestic-political` · `financial` · `reputation-management` · `data-harvesting` · `ideological` · `unknown`

### 7.7 `aunoo_tactic_vector` — salience scale
Per the platform's 8-tactic taxonomy. Salience per tactic: `0` not observed · `1` occasional · `2` frequent · `3` signature. Tactics: `legitimacy_inversion`, `severity_minimization`, `category_reframing`, `whataboutism`, `identity_reframing`, `motive_substitution`, `agent_swap`, `cause_effect_reversal`.

> **Note on fit.** The 8-tactic taxonomy describes *reframing of a real or partly-real event*. Pure **fabrication** (e.g. AI-generated fake nudes, invented charities) is **out of the reframing model** and must be recorded under DISARM (fabrication techniques) and flagged in the profile body. Recording a low/zero tactic vector alongside heavy fabrication is itself a useful signal about the actor.

### 7.8 Entity-resolution status *(mirrors platform entity resolution)*
On every named person/company: `auto` (machine-resolved, ≥0.85) · `confirmed` (analyst-verified) · `ambiguous` (multiple candidates) · `unresolved` (named in sourcing, identity not established).

### 7.9 Admiralty grading
Each load-bearing source/claim may carry a NATO Admiralty code: reliability `A`–`F` (A = completely reliable) × credibility `1`–`6` (1 = confirmed by other sources). E.g. a major newspaper joint-investigation finding corroborated elsewhere ≈ `B2`; an anonymous single-source social post ≈ `E4`.

---

## 8. Cross-linking convention

Links are **reciprocal** and keyed by stable IDs.

**In an actor profile** (`meta.yaml` / front-matter):
```yaml
related_sitreps:
  - SITREP:2026-06-blackcore-france-elections
```
and inline in §12 as markdown links to the sitrep folder.

**In a situation report** (front-matter, to be added to the situationreports schema):
```yaml
related_actors:
  - ACT-2026-BLACKCORE
```
and inline in the sitrep's actor/attribution section as a markdown link to `actors/ACT-2026-BLACKCORE/`.

**Integrity rule.** A link is only valid if it exists on both ends. `registry.yaml` is the authority for which IDs exist; a CI check (future) should fail any `related_*` pointing at an unknown ID or any one-directional link.

---

## 9. Minimum bar to publish

A profile may move to `review_status: published` only when: BLUF, quick-reference card, at least one TTP framework mapping, source assessment, and ≥ 3 distinct sources are present; every `confirmed` claim has an analyst-reviewed evidence trail; and all `related_*` links are reciprocal. Anything below that bar stays `draft`/`in-review` and is marked accordingly.
