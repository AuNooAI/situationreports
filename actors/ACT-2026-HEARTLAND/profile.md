---
id: ACT-2026-HEARTLAND
name: Heartland Institute (incl. Heartland UK/Europe)
codename: null
aliases: [Heartland UK/Europe]
actor_type: influence-advocacy-network
country_nexus: [United States]
operational_status: active
profile_status: confirmed
attribution_confidence: high
first_observed: 1984
last_active: 2026-07
last_updated: 2026-07-20
tlp: CLEAR
motivations: [policy-influence, climate-policy-opposition]
target_sectors: [climate-policy, energy-policy, eu-legislation]
target_geographies: [US, GB, EU, PL, AT, HU]
frameworks: [AUNOO-8T]
aunoo_tactic_vector:
  legitimacy_inversion: 1
  severity_minimization: 3
  category_reframing: 2
  whataboutism: 0
  identity_reframing: 0
  motive_substitution: 1
  agent_swap: 0
  cause_effect_reversal: 1
related_sitreps:
  - SITREP:2026-07-state-climate-disinformation-europe
related_actors: []
source_count: 5
admiralty_high_water: B1
analyst: "Aunoo Intelligence"
review_status: published
---

# THREAT ACTOR PROFILE: Heartland Institute (ACT-2026-HEARTLAND)

**Classification:** Unclassified · OSINT · **TLP:**CLEAR
**Code name:** none assigned. The organisation operates openly under its own name; Aunoo reserves code names for covert or deceptive actors.
**As of:** 20 July 2026
**Profile status:** confirmed · **Attribution confidence:** high
**Prepared from:** the organisation's own publications and announcements, IRIS climate-disinformation assessment, DeSmog network mapping, E&E News/POLITICO reporting

## Bottom line up front (BLUF)

The Heartland Institute is a US nonprofit think tank, founded in 1984 and known since the 2000s for rejecting the scientific consensus on human-caused climate change. It is profiled here because IRIS's May 2026 assessment names it as a channel for climate disinformation aimed at Europe, and because its European activity is recent, organised, and documented: it opened Heartland UK/Europe in London on 17 December 2024, at an event attended by former Prime Minister Liz Truss and Nigel Farage, with the stated aim of engaging policymakers in the UK and continental Europe.

Since then, reporting by DeSmog and others documents coordination with politicians from Austria, Hungary, and Poland against renewable-energy subsidies and EU environmental legislation, including the Nature Restoration Law and the Corporate Sustainability Due Diligence Directive, activity in Brussels with far-right MEPs, and an affiliated climate-skeptic group launched in Poland in May 2026 by an adviser to Reform UK.

Everything in this profile is public. The organisation publishes its positions and its leadership, and announced its European expansion itself. What distinguishes it from the covert actors in this repository is exactly that openness; what places it in the repository is the IRIS assessment and the documented, coordinated campaign against European climate policy. Reported funding includes fossil-fuel companies such as ExxonMobil and Republican donors, per IRIS and prior public reporting.

## Quick-reference card

| Field | Value |
| :-- | :-- |
| Actor ID | `ACT-2026-HEARTLAND` |
| Code name | none (overt actor) |
| Type | Influence-advocacy network |
| Nexus | United States; European arm in London |
| Operational status | Active |
| First / last seen | 1984 / 2026-07 |
| Profile status | Confirmed |
| Attribution confidence | High (activity is self-announced) |
| Frameworks | Aunoo 8-tactic |

## Attribution & confidence

There is no attribution problem in the usual sense: the organisation operates under its own name and announces its own campaigns. The analytic questions are alignment and funding. IRIS places Heartland within US-aligned climate disinformation directed at Europe; the organisation's positions align with the current US administration's, and DeSmog titles its network mapping accordingly. Reported funding from fossil-fuel companies and Republican donors is drawn from IRIS and earlier public reporting; current funding composition is not fully public. **Confidence: high on activities, structure, and European expansion, which are self-documented; moderate on funding composition; the characterisation of its output as disinformation is IRIS's assessment and Aunoo reports it as such.**

## History & evolution

| Date | Event |
| :-- | :-- |
| 1984 | Founded in Chicago as a free-market policy institute |
| 2008–2014 | Hosts International Conferences on Climate Change; becomes a leading platform for climate-consensus rejection |
| 17 Dec 2024 | Heartland UK/Europe launches in London; Truss and Farage attend |
| 2025 | Brussels activity with far-right MEPs from Austria, Poland, Hungary against EU environmental legislation (per DeSmog) |
| May 2026 | Reform UK adviser launches affiliated climate-skeptic group in Poland (per DeSmog) |
| May 2026 | IRIS names Heartland as a channel for climate disinformation aimed at Europe |

## Modus operandi

Openly branded advocacy: reports, conferences, media appearances, and direct engagement with sympathetic politicians. The European operation follows the US model, building relationships with national politicians and MEPs who oppose climate legislation, supplying them with materials and platforms, and establishing local affiliates. The London office gives the network a European base; the Polish launch extends it into a member state. The output disputes the scientific consensus on human-caused climate change and opposes decarbonisation policy, including the European Green Deal and specific EU directives.

## TTPs

**(a) DISARM.** Poor fit and not forced. The organisation does not use covert accounts, fabricated personas, or concealed infrastructure. Noted per schema to record the non-fit.

**(b) Aunoo 8-tactic vector.** Signature tactic is **severity_minimization (3)**: the consistent output minimises the severity and human causation of climate change. **Category_reframing (2)** recurs in reframing climate policy as an economic-liberty and sovereignty issue. **Cause_effect_reversal (1)** appears in arguments attributing warming to non-human causes.

## Infrastructure & indicators

Structured observables are in `indicators.yaml`. In summary: the Chicago headquarters and the London office (Heartland UK/Europe, launched December 2024, executive director Lois Perry); the Brussels engagement channel with aligned MEPs; the Polish affiliate (May 2026); and the publication and conference apparatus through which the material reaches policymakers and media.

## Campaigns & incidents

- **European expansion (Dec 2024– ).** The London launch and subsequent coordination with politicians in Austria, Hungary, and Poland against renewable subsidies and EU environmental law. Documented in [SITREP:2026-07-state-climate-disinformation-europe](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-07-state-climate-disinformation-europe).
- **EU legislative opposition (2025– ).** Brussels activity against the Nature Restoration Law and the Corporate Sustainability Due Diligence Directive, per DeSmog.

## Detection & monitoring guidance (Aunoo platform)

This actor's output is attributable on its face, so detection is about tracking rather than unmasking. Raise-conditions: Heartland-sourced climate claims surfacing in European parliamentary debates or national media without attribution to the institute; synchronised messaging between the institute and aligned European politicians around specific EU votes; and new national affiliates. The severity_minimization head is the primary detector for the content itself.

## Outlook & watch indicators

Watch for further national affiliates on the Polish model; activity around upcoming EU legislative fights on Green Deal implementation; any disclosure that clarifies current funding composition; and whether European institutions begin treating the network's activity as foreign influence rather than domestic lobbying, which is the question the IRIS report raises.

## Changelog

| Date | Change |
| :-- | :-- |
| 2026-07-20 | Initial profile created at `confirmed` / attribution `high`. No code name assigned (overt actor). |

## Sources

1. [The Heartland Institute — announcement of Heartland UK/Europe](https://heartland.org/opinion/the-heartland-institute-solidifies-its-global-impact-by-founding-heartland-uk-europe/) (December 2024). Admiralty B1 (self-published, against interest for concealment claims).
2. [E&E News / POLITICO — Heartland Institute opens European branch](https://www.eenews.net/articles/heartland-institute-opens-european-branch/). Admiralty B2.
3. [DeSmog — Mapped: Pro-Trump Heartland Institute's European Network](https://www.desmog.com/2025/12/10/mapped-donald-trump-heartland-institute-european-network/) (December 2025). Admiralty B2.
4. [DeSmog — Reform 'Advisor' Launches Climate Denial Group in Poland](https://www.desmog.com/2026/05/20/reform-advisor-launches-climate-denial-group-in-poland/) (May 2026). Admiralty B2.
5. [IRIS / Observatoire Défense et Climat — Climate Disinformation and Information Warfare](https://defenseclimat.fr/wp-content/uploads/2026/06/ObsDefClim_2026_04_Desinformation_Note_EN.pdf) (May 2026). Admiralty B2.
