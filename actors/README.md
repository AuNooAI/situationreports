<p align="center">
  <img src="assets/aunoo-logo.svg" alt="Aunoo" width="140">
</p>

<h1 align="center">Aunoo Intelligence — Threat Actor Profiles</h1>

<p align="center"><em>Structured, sourced, analyst-gated profiles of coordinated influence-operation actors.</em></p>

---

Threat Actor Profiles are produced by **Aunoo Intelligence**. Each profile gives a concise, sourced read on a coordinated-influence or information-operations actor: who they are, who runs them, who they target, how they operate, and what to watch. Profiles are **cross-linked** with the [Situation Reports](../) in this repo — a sitrep documents an *event*; an actor profile documents the *entity* behind one or more events.

This `actors/` subsystem is the actor-tracking counterpart to the `reports/` situation reports. It uses the same house style (BLUF, evidence tables, explicit confidence, source assessment) and the same curation discipline: **nothing is asserted as confirmed without an analyst-reviewed evidence trail.**

## How it fits together

```
reports/   ──  one folder per EVENT     (what happened)
actors/    ──  one folder per ACTOR      (who did it / how they operate)
     │
     └─ cross-linked by stable IDs in YAML front-matter (see SCHEMA.md §4)
```

A situation report names suspected actors; an actor profile lists the campaigns/sitreps attributed to it. The two are joined by stable IDs so that, e.g., the BlackCore profile and the France-election sitrep point at each other and stay in sync.

## Layout

```
situationreports/
├─ reports/                     ← situation reports (one folder per event)
└─ actors/
   ├─ README.md                 ← this file
   ├─ SCHEMA.md                 ← the profile specification (fields, vocab, frameworks, cross-linking)
   ├─ registry.yaml             ← machine-readable index of all actors
   ├─ registry.md               ← human-readable index table
   ├─ TEMPLATE/
   │  └─ actor-template.md      ← blank profile with inline authoring guidance
   └─ ACT-2026-BLACKCORE/       ← one folder per actor (folder name = canonical ID)
      ├─ profile.md             ← the narrative profile (primary deliverable)
      ├─ meta.yaml              ← machine-readable actor record (mirrors front-matter)
      └─ indicators.yaml        ← structured IOCs / observables
```

## Frameworks used

Influence-operations TTPs are described against three complementary frameworks, so each profile is legible to both the disinformation-research community and the cyber-threat-intel community, and so it plugs directly into Aunoo's detection model:

| Framework | Role in a profile |
| :-- | :-- |
| **[DISARM](https://disarmframework.herokuapp.com/)** (Red Framework) | Primary TTP taxonomy for influence operations — the ATT&CK-equivalent for disinformation. Every behaviour gets a DISARM technique ID where one exists. |
| **[MITRE ATT&CK](https://attack.mitre.org/)** | Secondary, for any *cyber-enabled* activity (infrastructure acquisition, data harvesting, credential/PII collection). Most pure-IO actors touch only a few ATT&CK techniques; that is expected and noted honestly. |
| **Aunoo 8-tactic reframing taxonomy** | Aunoo's own narrative-manipulation model (Legitimacy Inversion, Severity Minimization, Category Reframing, Whataboutism, Identity Reframing, Motive Substitution, Agent Swap, Cause-Effect Reversal). Each actor gets a **tactic vector** describing which reframing moves it favours, so profiles connect directly to the platform's detector outputs. |

## Curation model (inherited from the platform)

Profiles use the platform's own confidence vocabulary so a profile and the detectors that feed it speak the same language:

- **`profile_status`** ∈ `suspected → tentative → confirmed` — the attribution-maturity of the *actor entity*, mirroring `label_status` on detected networks.
- **Entity-resolution status** on every named person/company ∈ `auto · confirmed · ambiguous · unresolved`.
- **Attribution confidence** ∈ `low · moderate · high`, with NATO **Admiralty** source-reliability/credibility grades on load-bearing claims.
- **TLP** marking on every profile.
- **Code names** for CIOPS actors — a human-memorable two-word handle (e.g. BlackCore → **AMON MIRAGE**) alongside the canonical ID; see SCHEMA.md §3.1.

No public attribution, named-entity call, or network claim appears at `confirmed` without an analyst-reviewed evidence chain. Suspected and tentative material is published as such, clearly marked.

## Adding an actor

1. Copy `TEMPLATE/actor-template.md` to `actors/<ID>/profile.md` (repo-relative; see SCHEMA.md §3 for the ID scheme).
2. Fill the YAML front-matter and mirror it into `meta.yaml`.
3. Record observables in `indicators.yaml`.
4. Add a row to `registry.yaml` and `registry.md`.
5. Add reciprocal `related_*` links in any referenced situation reports.

## About Aunoo

Aunoo builds news-intelligence tools that help people stay ahead of fast-moving events.

- **Website** — [aunoo.ai](https://aunoo.ai)
- **Situation Reports** — [github.com/AuNooAI/situationreports](https://github.com/AuNooAI/situationreports)
- **Research & advisory** — [research@aunoo.ai](mailto:research@aunoo.ai)

---

Profiles are compiled from open-source reporting and should be verified against primary sources before use in decision-making. Attribution in influence operations is probabilistic; confidence levels and source grades are stated so readers can weigh the evidence themselves. © Aunoo.
