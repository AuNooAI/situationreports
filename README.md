<p align="center">
  <img src="assets/aunoo-logo.svg" alt="Aunoo" width="140">
</p>

<h1 align="center">Aunoo Intelligence — Situation Reports</h1>

<p align="center"><em>Up-to-date situational awareness on breaking AI and technology events.</em></p>

---

Situation Reports are produced by **Aunoo Intelligence**, the research and advisory team at Aunoo. Each report gives a concise, sourced read on a developing event: what happened, why it matters, what to watch, and where the evidence points.

This repository holds two linked products:

- **Situation Reports** (`reports/`) — point-in-time reads on a developing *event*.
- **Threat Actor Profiles** (`actors/`) — durable profiles of the *actors* behind coordinated influence operations, cross-linked to the events they are attributed to.

## Latest

**US export-control suspension of Anthropic's Fable 5 and Mythos 5** — 14 June 2026
[Read the report »](reports/2026-06-anthropic-fable-mythos-export-ban/sitrep.md)

**BlackCore (AMON MIRAGE): Israeli firm and the 2026 French election interference campaign** — 20 June 2026
[Read the report »](reports/2026-06-blackcore-france-elections/sitrep.md) · [Actor profile »](actors/ACT-2026-BLACKCORE/profile.md)

**Fabricated Jeff Bezos quote on prioritising AI water use over humans** — 22 June 2026
[Read the report »](reports/2026-06-bezos-fabricated-ai-water-quote/sitrep.md) — a misinformation incident (assessed LLM hallucination), not a coordinated actor.

**Pro-AI influence operations and the "foreign influence" counter-narrative against data-center opposition** — 2 July 2026
[Read the report »](reports/2026-07-pro-ai-influence-counter-narrative/sitrep.md)

**The Onion's "Palantir Acquires Pentagon" satire misread as a market signal** — 2 July 2026
[Read the report »](reports/2026-07-palantir-onion-pentagon-satire/sitrep.md) — satire misattribution, not a coordinated actor.

**AfD "Alternita" (PANZER PARROT): a party-run AI system for mass-producing far-right "rage bait"** — 10 July 2026
[Read the report »](reports/2026-07-afd-alternita-ai-ragebait/sitrep.md) · [Actor profile »](actors/ACT-2026-PANZERPARROT/profile.md)

**MANASSEH CHORUS (Clock Tower X): a FARA-registered, Israel-funded influencer operation aimed at the American right** — 14 July 2026
[Read the report »](reports/2026-07-manasseh-chorus-parscale-israel/sitrep.md) · [Actor profile »](actors/ACT-2026-MANASSEHCHORUS/profile.md)

**State-actor climate disinformation targeting Europe (IRIS assessment)** — 20 July 2026
[Read the report »](reports/2026-07-state-climate-disinformation-europe/sitrep.md) · [Portal Kombat profile »](actors/ACT-2026-PORTALKOMBAT/profile.md) · [Heartland profile »](actors/ACT-2026-HEARTLAND/profile.md)

## Browse

**Situation reports** live under [`reports/`](reports/), one folder per event. Each folder contains the report itself as `sitrep.md`, and where produced, a shareable bulletin PDF and cover or timeline graphics.

**Threat actor profiles** live under [`actors/`](actors/), one folder per actor. Start with the [actor registry](actors/registry.md) for an index, or the [profile schema](actors/SCHEMA.md) for the format. Actors and reports are cross-linked by stable IDs (e.g. `ACT-2026-BLACKCORE`) in YAML front-matter, so an event and the actor behind it point at each other.

Currently profiled: **BlackCore / AMON MIRAGE** (`ACT-2026-BLACKCORE`), **Team Jorge / AHAB PUPPETEER** (`ACT-2026-TEAMJORGE`), **AfD Alternita / PANZER PARROT** (`ACT-2026-PANZERPARROT`), **Clock Tower X / MANASSEH CHORUS** (`ACT-2026-MANASSEHCHORUS`), **Portal Kombat / POTEMKIN PORTAL** (`ACT-2026-PORTALKOMBAT`), and the **Heartland Institute** (`ACT-2026-HEARTLAND`).

## About Aunoo

Aunoo builds news-intelligence tools that help people stay ahead of fast-moving events.

- **Website** — [aunoo.ai](https://aunoo.ai)
- **Free SaaS** — our news-intelligence platform, free to use at [aunoo.ai](https://saas.aunoo.ai)
- **Free MCP** — connect Aunoo to your own AI agents at [agentic.aunoo.ai](https://agentic.aunoo.ai)
- **Research & advisory** — [research@aunoo.ai](mailto:research@aunoo.ai)

---

Reports and profiles are compiled from open-source reporting and should be verified against primary sources before use in decision-making. Attribution in influence operations is probabilistic; confidence levels are stated throughout. © Aunoo.
