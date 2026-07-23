---
id: ACT-2026-PORTALKOMBAT
name: Portal Kombat (Pravda network)
codename: POTEMKIN PORTAL
aliases: [Pravda network, Portal Combat]
actor_type: state-aligned-amplification-network
country_nexus: [Russia]
operational_status: active
profile_status: confirmed
attribution_confidence: high
first_observed: 2022-02
last_active: 2026-07
last_updated: 2026-07-20
tlp: CLEAR
motivations: [geopolitical-narrative, destabilisation]
target_sectors: [public-opinion, elections, climate-policy, ukraine-support]
target_geographies: [FR, EU, UA, US]
frameworks: [DISARM, AUNOO-8T]
aunoo_tactic_vector:
  legitimacy_inversion: 3
  severity_minimization: 1
  category_reframing: 1
  whataboutism: 2
  identity_reframing: 0
  motive_substitution: 1
  agent_swap: 2
  cause_effect_reversal: 1
related_sitreps:
  - SITREP:2026-07-state-climate-disinformation-europe
related_actors: []
source_count: 4
admiralty_high_water: A1
analyst: "Aunoo Intelligence"
review_status: published
---

# THREAT ACTOR PROFILE: POTEMKIN PORTAL — "Portal Kombat" (ACT-2026-PORTALKOMBAT)

**Classification:** Unclassified · OSINT · **TLP:**CLEAR
**Code name:** POTEMKIN PORTAL
**As of:** 20 July 2026
**Profile status:** confirmed · **Attribution confidence:** high
**Prepared from:** Viginum technical reports (primary, state-agency), French Foreign Ministry statements, EU disinformation monitoring, IRIS climate-disinformation assessment

## Bottom line up front (BLUF)

POTEMKIN PORTAL is Aunoo's designation for Portal Kombat, a pro-Russian network of automated news portals exposed by Viginum, France's service against foreign digital interference, in February 2024. Viginum documented 193 portals at exposure. The sites produce no original content. They republish and amplify material from pro-Russian public figures, Russian news agencies, and official Russian government communications, using automation and search-engine optimisation. Viginum tied the network's creation and administration to TigerWeb, a web-development company based in Crimea and founded by Yevgeny Shevchenko.

After public exposure, the network expanded. Viginum observed new domains and subdomains targeting every EU member state, several African and Asian countries, and French political figures including President Macron. In 2026, IRIS identified the network as a channel for climate disinformation aimed at Europe, including content circulating around the 2024 Valencia floods.

The code name pairs Potemkin, a front built to look like something it is not, with the network's vehicle. The portals present as local news outlets and are automated republication infrastructure.

## Quick-reference card

| Field | Value |
| :-- | :-- |
| Actor ID | `ACT-2026-PORTALKOMBAT` |
| Code name | **POTEMKIN PORTAL** |
| Aliases | Portal Kombat · Pravda network |
| Type | State-aligned automated amplification network |
| Nexus | Russia (infrastructure in Crimea) |
| Operational status | Active |
| First / last seen | 2022-02 / 2026-07 |
| Profile status | Confirmed |
| Attribution confidence | High |
| Frameworks | DISARM · Aunoo 8-tactic |

## Attribution & confidence

**Diamond Model.**
- **Adversary:** The network operates in support of Russian state narratives. Viginum tied site creation and administration to TigerWeb (Crimea); the founder has built and maintained websites since at least 2013. Formal state tasking is not publicly documented; alignment with Russian government communications is.
- **Capability:** Automated republication at scale across 193+ portals; SEO optimisation; rapid creation of new domains after exposure; language- and country-targeted subdomains.
- **Infrastructure:** The portal fleet; TigerWeb hosting and administration; domain generation targeting individual EU states and political figures.
- **Victim / target:** European publics, originally on the war in Ukraine, extended to elections, political figures, and climate and energy policy.

**Confidence statement.** Existence, scale, behaviour, and infrastructure are **high**, resting on Viginum's technical investigation, a primary state-agency source, corroborated by the French Foreign Ministry and EU monitors. State direction of specific narrative choices, including the climate content IRIS describes, is **moderate**: the network demonstrably amplifies Russian official communications, but per-narrative tasking is not publicly documented.

## History & evolution

| Date | Event |
| :-- | :-- |
| Pre-2022 | Portal infrastructure covers Russian and Ukrainian news for Russian-speaking audiences |
| Feb 2022 | After the invasion of Ukraine, the network reorients toward Ukrainian and Western audiences |
| Feb 2024 | Viginum publishes its investigation; the French Foreign Minister names the network publicly |
| 2024–2025 | Expansion: new domains targeting all EU member states, African and Asian countries, French political figures |
| Oct 2024 | Valencia floods: Russian sources amplify false emergency numbers and casualty figures (per IRIS) |
| May 2026 | IRIS identifies the network as a channel for climate disinformation aimed at Europe |
| Jul 2026 | HAARP heatwave conspiracy recirculates through pro-Russian accounts during France's third heatwave of the year |

## Modus operandi

The network does not create content. It ingests material from pro-Russian figures, Russian state media, and official government communications, republishes it across portals styled as local or regional news sites, and uses automation and SEO so the content surfaces in search results and can be cited as apparently independent reporting. Country-targeted domains give the content a local appearance in each market. After exposure, the operators replaced and multiplied domains rather than shutting down.

## TTPs

**(a) DISARM.** Coordinated inauthentic amplification through fabricated news-site personas; narrative laundering of state communications through apparently independent outlets; SEO manipulation; rapid infrastructure replacement after exposure.

**(b) Aunoo 8-tactic vector.** Signature tactic is **legitimacy_inversion (3)**: state messaging presented as independent local journalism. **Agent_swap (2)** and **whataboutism (2)** recur in the amplified content. The vector reflects the amplified material as much as the network itself, since the network republishes rather than writes.

## Infrastructure & indicators

Structured observables are in `indicators.yaml`. In summary: the portal fleet (193 domains at exposure, more since); TigerWeb (Crimea) as builder and administrator; country- and language-targeted subdomains across the EU; SEO-optimised republication with no bylined original journalism; and the behavioural signature of near-simultaneous republication of identical pro-Russian content across nominally unrelated local-news domains.

## Campaigns & incidents

- **Ukraine war narratives (2022– ).** The network's founding purpose per Viginum: defending the invasion, denigrating Ukrainian leadership, and criticising Western governments supporting Kyiv.
- **Valencia floods (Oct 2024).** Amplification of false emergency numbers and inflated casualty figures during a live disaster, per IRIS. Documented in [SITREP:2026-07-state-climate-disinformation-europe](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-07-state-climate-disinformation-europe).
- **European climate policy (2024– ).** Climate disinformation targeting the European Green Deal and EU decarbonisation, per IRIS.

## Detection & monitoring guidance (Aunoo platform)

Raise-conditions: near-simultaneous appearance of identical pro-Russian content across multiple low-traffic "local news" domains; new news-styled domains with no masthead, no bylines, and no original reporting; republication chains that trace to Russian state media or official communications; and spikes of this activity in the hours after a European disaster or ahead of a European vote. The cluster-detection and echo/amplification modules are the primary detectors; the legitimacy_inversion head applies to the local-news presentation.

## Outlook & watch indicators

Viginum's post-exposure observation is that the network grows when named. Watch for new country-targeted domain batches ahead of European elections; climate-event exploitation within hours of the next major European disaster; and any technical reporting that ties narrative selection, rather than just infrastructure, to Russian state entities, which would raise the state-direction confidence from moderate to high.

## Changelog

| Date | Change |
| :-- | :-- |
| 2026-07-20 | Initial profile created at `confirmed` / attribution `high`. Code name POTEMKIN PORTAL assigned. |

## Sources

1. [Viginum — Portal Kombat: A Pro-Russian Propaganda Network (technical report)](https://policycommons.net/artifacts/11331813/20240212_np_sgdsn_viginum_portal-kombat-network_eng_vf/12220740/) (February 2024). Admiralty A1.
2. [Ministère de l'Europe et des Affaires étrangères — Result of Viginum investigations into the Portal Kombat network](https://www.diplomatie.gouv.fr/en/french-foreign-policy/security-disarmament-and-non-proliferation/news/2024/article/foreign-digital-interference-result-of-investigations-into-the-russian) (February 2024). Admiralty A1.
3. [EU DisinfoLab / EDMO — Portal Kombat expansion monitoring](https://ec.europa.eu/newsroom/edmo/newsletter-archives/52424) (April 2024). Admiralty B2.
4. [IRIS / Observatoire Défense et Climat — Climate Disinformation and Information Warfare](https://defenseclimat.fr/wp-content/uploads/2026/06/ObsDefClim_2026_04_Desinformation_Note_EN.pdf) (May 2026). Admiralty B2.
