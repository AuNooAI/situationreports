---
id: ACT-2026-PANZERPARROT
name: AfD Alternita operation
codename: PANZER PARROT
aliases: [Alternita]
actor_type: grassroots-astroturf
country_nexus: [Germany]
operational_status: active
profile_status: tentative
attribution_confidence: high
first_observed: 2026-07
last_active: 2026-07
last_updated: 2026-07-10
tlp: CLEAR
motivations: [domestic-political, ideological]
target_sectors: [elections, public-opinion, minority-communities]
target_geographies: [DE]
frameworks: [DISARM, AUNOO-8T]
aunoo_tactic_vector:
  identity_reframing: 3
  legitimacy_inversion: 1
  severity_minimization: 0
  category_reframing: 1
  whataboutism: 0
  motive_substitution: 0
  agent_swap: 0
  cause_effect_reversal: 0
related_sitreps:
  - SITREP:2026-07-afd-alternita-ai-ragebait
related_actors: []
source_count: 2
admiralty_high_water: B2
analyst: "Aunoo Intelligence"
review_status: in-review
---

# THREAT ACTOR PROFILE: PANZER PARROT — "AfD Alternita operation" (ACT-2026-PANZERPARROT)

**Classification:** Unclassified · TLP:CLEAR
**As of:** 10 July 2026
**Profile status:** tentative · **Attribution confidence:** high
**Prepared from:** 2 sources · Admiralty high-water B2 (Correctiv undercover investigation, reported by The Irish Times)

## BLUF

PANZER PARROT is Aunoo's designation for the AfD's in-house automated content operation built on the platform Alternita, which converts far-right articles into ready-to-post social-media content in minutes. An undercover Correctiv investigation, reported by The Irish Times on 8 July 2026, documented the tool generating calls for forced deportations ("remigration") and an anti-LGBT "rainbow dictatorship" post with an AI-generated burning-flag image, and found the source code draws on Google Gemini, OpenAI's ChatGPT, and Anthropic's Claude. Attribution to the AfD is high, because the operation was demonstrated by a serving party official and the platform is registered to the party's general secretary. The main caveat is evidentiary breadth: the profile currently rests on a single primary investigation, so scale-of-deployment and provider-compliance details are corroborated at only two sources.

The name captures the operation's two defining features. The "Panzer" is the industrial, centralized machine: party headquarters mass-producing message-consistent content at scale. The "Parrot" is the mechanism: the tool ingests AfD-friendly feeds and parrots back templated variations of the same talking points, dressed up as an organic base.

## Quick-reference card

| Field | Value |
| :-- | :-- |
| ID | `ACT-2026-PANZERPARROT` |
| Code name | PANZER PARROT |
| Name / aliases | AfD Alternita operation · Alternita |
| Type | Grassroots-astroturf (operated by an elected political party) |
| Nexus | Germany (domestic) |
| Operational status | Active (pilot live since w/c 6 Jul 2026) |
| First / last seen | 2026-07 / 2026-07 |
| Profile status | Tentative |
| Attribution confidence | High |
| Frameworks | DISARM, Aunoo 8-tactic |

## Attribution & confidence

**Diamond Model.**
- **Adversary:** The Alternative for Germany (AfD). The operation was demonstrated by Mario Hau, social-media chief of the AfD's Bundestag parliamentary group; the Alternita platform is registered to AfD general secretary Hans-Holger Malcomeß.
- **Capability:** The Alternita platform, which turns uploaded articles into platform-ready posts and AI-generated images, built on Google Gemini, OpenAI's ChatGPT, and Anthropic's Claude accessed as services.
- **Infrastructure:** Alternita's application and account system; AfD-controlled social channels, including those of co-leader Alice Weidel; a satirical persona account, "Karl Ranseier."
- **Victim / target:** German public opinion ahead of a September state-parliament election, with content aimed at migrants and LGBT people.

**Confidence statement.** Attribution to the AfD is assessed **high**: the tool was shown by a serving party official, is registered to a party officer, and is described by the party itself as a pilot. Profile status is **tentative** rather than confirmed only because the public evidence is a single primary investigation (Correctiv), reported secondarily by The Irish Times.

**Competing hypotheses.** (1) A third party built Alternita and the AfD is a customer — weakened by the registration to the general secretary and the demonstration by a party official. (2) The demonstrated outputs are cherry-picked and unrepresentative — possible, but the tool's stated design ("tailor-made for the AfD," content foundation is the party programme) points the same way. Neither materially lowers attribution confidence.

Load-bearing claims are graded **B2** (a reputable investigative outlet with direct undercover access and source-code review; corroboration currently limited to secondary reporting of the same investigation).

## History & evolution

The AfD has held a large online lead over its rivals on the major platforms for some time. Alternita is the party's attempt to convert that lead into centrally controlled, high-volume output without visibly centralizing it. Correctiv's investigation caught the tool in its pilot phase.

| Date | Event |
| :-- | :-- |
| Ongoing | AfD holds a large online lead over rivals on major platforms |
| Week of 6 Jul 2026 | Alternita launches in a pilot phase |
| 8 Jul 2026 | Correctiv publishes its undercover investigation; The Irish Times reports it |
| 8 Jul 2026 | Google and OpenAI say they are examining the use; Anthropic does not reply |
| Sep 2026 | State-parliament election in an eastern German state (AfD leads polling) |
| 2027 | Planned full implementation of Alternita |

## Ownership, structure & key personnel

- **Hans-Holger Malcomeß** — AfD general secretary; the Alternita platform is registered to him. Entity resolution: **confirmed** (named in Correctiv/Irish Times). 
- **Mario Hau** — social-media chief of the AfD's Bundestag parliamentary group; demonstrated the tool to the undercover journalist and reportedly operates the "Karl Ranseier" persona. Entity resolution: **confirmed**.
- **Alice Weidel** — AfD co-leader; her channels reportedly already run Alternita output, and she reportedly follows the "Karl Ranseier" account. Entity resolution: **confirmed**.

## Targeting / victimology

The operation targets German domestic public opinion, with the near-term objective of the September state-parliament election where the AfD polls around 40 percent. Content selection is driven by AfD-friendly feeds (for example the site Nius); the documented outputs single out migrants (forced "remigration," "ethnic elections") and LGBT people (an "LGBT rainbow dictatorship").

## Modus operandi

Party headquarters generates message-consistent content centrally and distributes it through a base that continues to look organic. An operator uploads an article from an aligned outlet; Alternita returns platform-ready posts in the party's branding, plus AI-generated images, in a few minutes. Some output is published through official channels, including a party leader's, and not all of it is labeled as AI-generated. A satirical persona account extends reach while giving the operation deniable, "just joking" cover. The design goal, in the party's own framing, is to keep central control of the message while preserving the appearance of a decentralized activist base.

## TTPs

**(a) DISARM.** Predominantly **content-generation and fabrication** techniques: automated creation of persuasive text at scale, generation of synthetic imagery (a burning rainbow flag; men boarding a train to a "deportation airport"), persona development (the fictional "minister for remigration"), and undisclosed AI-generated political content. Distribution relies on an existing owned-channel network rather than covert account creation.

**(b) MITRE ATT&CK.** Poor fit and not forced. ATT&CK describes intrusion tradecraft; this operation involves no compromise of victim systems. Recorded here only to note the non-fit, as the schema requires.

**(c) Aunoo 8-tactic vector.** Signature tactic is **identity_reframing (3)**: recasting policy debate as existential identity conflict ("remigration," "ethnic elections," "rainbow dictatorship"). **Category_reframing (1)** and **legitimacy_inversion (1)** appear occasionally. Note on fit: much of the output is outright **fabrication** (AI-generated images and a fictional persona), which sits **outside** the reframing model and is captured under DISARM above. A low reframing vector alongside heavy fabrication is itself the signal here — this actor manufactures rather than merely reframes.

## Infrastructure & indicators

Structured observables are in `indicators.yaml` (`IOC-1`…). In summary: the Alternita platform (registered to the general secretary); the "Karl Ranseier" satirical persona; AfD-controlled official channels used for distribution; a recurring hashtag cluster in the generated posts; and AfD-friendly outlet feeds (for example Nius) used as content inputs. The operation's engines are commercial AI services from Google, OpenAI, and Anthropic.

## Campaigns & incidents

- **CAMP-PANZERPARROT-01 — Alternita pilot (Jul 2026).** The launch and exposure documented in [SITREP:2026-07-afd-alternita-ai-ragebait](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-07-afd-alternita-ai-ragebait). Provider responses: Google and OpenAI examining; Anthropic did not reply.

## Relationships

No operational links to other profiled actors are established. As a comparison, PANZER PARROT differs from the vendor actors in this registry (BlackCore, Team Jorge) in that it is run by the political principal itself, in-house, rather than sold as a service.

## Detection & monitoring guidance

Aunoo-specific signals that should raise this actor: bursts of near-duplicate posts across AfD-aligned accounts sharing paraphrase structure, hashtag clusters, and coordinated timing; AI-content detection hits on official AfD channels; and image outputs matching the documented synthetic style. Suggested `label_status` workflow: open at `suspected` on a single paraphrase cluster, promote to `tentative` on corroborated multi-account timing, and reserve `confirmed` for analyst-reviewed matches tied to Alternita output. The most useful detector heads here are AI-content detection and coordinated-behaviour clustering rather than the reframing tactic heads, given the fabrication-heavy profile.

## Outlook & watch indicators

Single best early-warning signal: a move from pilot to full deployment before the September state election. Other indicators: enforcement action or statements from Google, OpenAI, or Anthropic; action by German or EU regulators under the AI Act or the Digital Services Act; and adoption of a similar system by other parties or movements, which would turn this from one actor into a pattern.

## Source assessment & confidence

The profile rests on Correctiv's undercover investigation, reported by The Irish Times. Both are credible, and the method (live demonstration, test account, source-code review) is strong for establishing the tool's existence and behaviour. The picture is thin on independent corroboration and on the true scale of live deployment. What would change the assessment: a second independent investigation, a provider statement on enforcement, a regulator's finding, or direct evidence of the volume of Alternita content already posted. Because the profile currently has fewer than three distinct sources, it is held at `review_status: in-review`.

## Changelog

- **2026-07-10** — Initial profile created at tentative status, attribution high, from the Correctiv investigation (via The Irish Times). Code name PANZER PARROT assigned.

## Sources

1. The Irish Times — *AI software that generates 'rage bait' developed by Germany's far-right AfD* (Derek Scally, 8 July 2026). Admiralty B2. https://www.irishtimes.com/world/europe/2026/07/08/ai-software-that-generates-rage-bait-developed-by-germanys-far-right-afd/
2. Correctiv — the originating undercover investigation into Alternita. Admiralty B2. https://correctiv.org/
