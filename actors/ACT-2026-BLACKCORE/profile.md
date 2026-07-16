---
id: ACT-2026-BLACKCORE
name: BlackCore
codename: AMON MIRAGE
aliases: [Black Core]
actor_type: influence-ops-vendor
country_nexus: [Israel]
operational_status: disrupted
profile_status: tentative
attribution_confidence: moderate
first_observed: 2026-03
last_active: 2026-06
last_updated: 2026-07-15
tlp: CLEAR
motivations: [contract-hire, geopolitical-narrative, data-harvesting]
target_sectors: [elections, political-candidates, civil-society, pro-palestine-advocacy]
target_geographies: [FR, US-NY, GB-SCT, AO, TG]
frameworks: [DISARM, ATT&CK, AUNOO-8T]
aunoo_tactic_vector:
  legitimacy_inversion: 2
  severity_minimization: 0
  category_reframing: 1
  whataboutism: 0
  identity_reframing: 3
  motive_substitution: 1
  agent_swap: 0
  cause_effect_reversal: 0
related_sitreps:
  - SITREP:2026-06-blackcore-france-elections
related_actors:
  - ACT-2026-TEAMJORGE
  - ACT-2026-MANASSEHCHORUS
source_count: 14
admiralty_high_water: B2
analyst: "Aunoo Intelligence"
review_status: published
---

# THREAT ACTOR PROFILE: AMON MIRAGE — "BlackCore" (ACT-2026-BLACKCORE)

**Classification:** Unclassified · OSINT · **TLP:**CLEAR
**Code name:** AMON MIRAGE
**As of:** 20 June 2026, 18:00 UTC
**Profile status:** tentative · **Attribution confidence:** moderate
**Prepared from:** 14 sources · Admiralty high-water B2 (Haaretz/Libération joint investigation, corroborated by Reuters and Viginum)

---

## Bottom line up front (BLUF)

BlackCore is a self-described Israeli "elite influence, cyber and technology" firm exposed between March and June 2026 as the suspected operator of a cross-border, hire-for-service digital-interference business. Its signature campaign smeared three left-wing, pro-Palestinian France Unbowed (LFI) candidates ahead of France's March 2026 municipal elections using fabricated sexual-assault allegations, AI-generated fake nude imagery, sock-puppet personas, and an avatar/bot amplification network. France's disinformation watchdog **Viginum** subsequently attributed the same modus operandi to operations against the 2025 New York City mayoral race, Scotland's First Minister, and activity in Angola and Togo. **The operation is well-evidenced; the corporate identity and the client are not.** No investigator — Reuters included — has found a legal entity named "BlackCore" in any registry, and Viginum could not identify who commissioned the work. Attribution to specific Israeli companies (Galacticos, SNI Digital) and individuals rests on the Haaretz/Libération technical investigation and is **denied by the named parties.** Do not confuse BlackCore with **Black Cube** (a separate, older Israeli private-intelligence firm) or with **Team Jorge / Tal Hanan** (a separate influence-for-hire operation exposed in 2023).

---

## Quick-reference card

| Field | Value |
| :-- | :-- |
| Actor ID | `ACT-2026-BLACKCORE` |
| Code name | **AMON MIRAGE** |
| Aliases | Black Core |
| Type | Influence-operations vendor (hire-for-service) |
| Country nexus | Israel (suspected) |
| Operational status | Disrupted (infrastructure scrubbed; under French investigation) |
| First observed | March 2026 (France); marketing domain registered Aug 2025 |
| Last active | June 2026 |
| Attribution confidence | Moderate (operation), Low (client/sponsor) |
| Frameworks mapped | DISARM · ATT&CK · Aunoo 8-tactic |

---

## Attribution & confidence

**Diamond Model.**

| Vertex | Finding | Confidence |
| :-- | :-- | :-- |
| **Adversary** | "BlackCore" brand operating from an Israeli nexus; technical infrastructure traced to Tel Aviv firms **Galacticos Ltd** and **SNI Digital Ltd**, linked to businessmen **Guy Geyor** and lawyer **Doron Afik** (both deny involvement). **Commissioning client unidentified.** | Tentative (operator) / Low (client) |
| **Capability** | "Political campaign management" product built on ~1,600 AI-generated avatars; fabricated news/blog sites; AI-generated imagery; a fake-charity honeypot. | Confirmed |
| **Infrastructure** | `blackcore[.]online` (anonymous Icelandic registrar, registered Aug 2025); 8 subdomains; a London server on a Finnish cloud provider; further servers in Britain, Germany, Finland, Lithuania; corporate cluster at 103 HaHashmonaim St, Tel Aviv. | Tentative–Confirmed |
| **Victim** | Pro-Palestinian / Gaza-critical political candidates and officials across FR, US (NYC), Scotland; plus Angola/Togo government-linked operations. | Confirmed (FR) / Tentative (others, per Viginum) |

**Confidence statement.** The *existence and tooling* of the operation are **confirmed** — multiple independent outlets, a state watchdog (Viginum), and platform takedowns (Meta, Google, TikTok for coordinated inauthentic behaviour). The *operator identity* "BlackCore" is **tentative**: it is a brand with no found legal registration, attributed via shared digital infrastructure to named Israeli companies whose principals deny knowledge. The *sponsor/client* is **suspected/unknown** — Viginum explicitly could not identify it. Load-bearing source is the Haaretz/Libération joint technical investigation (~B2), corroborated by Reuters (~B2) and Viginum's on-record statements (~B1).

**Competing hypotheses.**
1. *Private vendor acting for an undisclosed client* (best fit with marketed "campaign management" product and mercenary target spread across unrelated geographies). — favoured.
2. *State-directed operation using a commercial front* (consistent with Unit 8200 alumni links and the pro-Israel narrative thrust). — possible; no direct evidence of state tasking.
3. *"BlackCore" is a misdirection brand* layered over the real operators (Galacticos/SNI) to absorb attention. — partially supported by the anonymous registration and rapid teardown.
Discriminating evidence would be: the client contract / payment trail (DGSI probe), or Israeli corporate-registry linkage of the "BlackCore" name itself.

---

## History & evolution

BlackCore surfaced through a chain of reporting in spring 2026. The underlying corporate vehicles are older than the brand: **Galacticos Ltd** was incorporated in Tel Aviv in **April 2022 as "Pagecorn Ltd,"** renamed **"Mycelium Intelligence Networks" (2023)**, then **"Galacticos" (2024)** — the renaming cadence itself a notable pattern. The public "BlackCore" brand appears to date only to **August 2025** (domain registration).

| When | Event |
| :-- | :-- |
| Apr 2022 | "Pagecorn Ltd" incorporated, Tel Aviv (later → Mycelium Intelligence Networks → Galacticos). |
| Aug 2025 | `blackcore[.]online` registered via anonymous Icelandic registrar; site presents firm as long-established. |
| Mar 2026 | France Unbowed (LFI) candidates targeted ahead of municipal elections; first exposed by *Le Monde* (9 Mar). |
| May 2026 | **Reuters** first names "BlackCore"; Haaretz/Libération publish joint technical investigation. |
| ~2 hrs after press contact | BlackCore and Galacticos digital infrastructure pulled offline after principals asked for comment. |
| 11–12 Jun 2026 | **Viginum** (with French PM) attributes same MO to NYC 2025, Scotland, Angola, Togo; sponsor unidentified. |
| Jun 2026 | French government formally asks Israel for explanations; two French probes underway (Paris prosecutors; DGSI). |

---

## Ownership, structure & key personnel

> Entity-resolution status tags mirror the platform's resolver. All denials are on the record.

- **Galacticos Ltd** (Tel Aviv; ex-Pagecorn Ltd → Mycelium Intelligence Networks) — built the avatar-generation product ("Galacticos AI Avatar Generator"). Status: `confirmed` (corporate record) / link-to-BlackCore `tentative`.
- **SNI Digital Ltd** (Tel Aviv) — reportedly hosted the avatar tooling on a London server. Status: `confirmed` (corporate record) / link `tentative`.
- **Guy Geyor** — Israeli tech entrepreneur (former *Survivor*/*The Bachelor* contestant); linked to Galacticos/SNI ownership. **Denies knowledge of BlackCore.** Status: `confirmed` (identity) / involvement `ambiguous`.
- **Doron Afik** — lawyer; firm at the same Tel Aviv address; reported majority stake in Galacticos and trustee via **Benguy Escrow Company Ltd** (distance-inserting structure). **Denies involvement.** Status: `confirmed` (identity) / involvement `ambiguous`.
- **Unit 8200 / Yigal Unna** — investigators reported links to Israel's SIGINT corps (Unit 8200) and to **Yigal Unna**, former head of Israel's National Cyber Directorate. **Unna denies any link.** Status: `unresolved`.
- **Registered address:** 103 HaHashmonaim Street, Tel Aviv–Jaffa (corporate cluster). Status: `confirmed`.

---

## Targeting / victimology

The consistent selection logic is **electorally relevant figures who criticised Israel's conduct in Gaza or championed Palestinian rights.** Targets to date:

- **France (Mar 2026):** Sébastien Delogu (LFI, Marseille), François Piquemal (LFI, Toulouse), and a third LFI candidate in Roubaix.
- **New York City (2025 municipal):** the race won by Zohran Mamdani, an outspoken Palestine supporter (Viginum did not name the target explicitly).
- **Scotland:** First Minister John Swinney, who called Gaza a "man-made humanitarian catastrophe."
- **Angola & Togo:** government-linked operations (BlackCore documents suggested a social-media operation for an African government — a possible *paying-client* footprint rather than the pro-Israel narrative thread).
- **Pro-Palestinian donors/supporters:** harvested via the "Sadaqah Palestine" fake-charity honeypot.

The Africa activity sits oddly against the Gaza-narrative thread, supporting the *mercenary vendor* hypothesis over a purely ideological one.

---

## Modus operandi

BlackCore marketed a **productised, hire-for-service influence capability** — a bilingual (Hebrew/English) mini-site advertising "political campaign management" built on ~1,600 avatars. The operational lifecycle observed:

1. **Brand/front separation.** A clean public brand (BlackCore) over older, repeatedly-renamed companies (Pagecorn → Mycelium → Galacticos; SNI Digital), with a lawyer-trustee/escrow layer to distance activity from ownership.
2. **Jurisdictional laundering of infrastructure.** Anonymous Icelandic registrar; servers across Britain, Germany, Finland, Lithuania; avatar tooling on a London server (Finnish cloud provider) — keeping the technical layer off Israeli soil while the corporate core sits in Tel Aviv.
3. **Manufacture scandal.** Stand-up fake news/blog sites publishing fabricated criminal allegations and AI-generated imagery; sock-puppet personas ("Sophie," a supposed blogger) to launder accusations.
4. **Segment & steer.** Audience-specific deception (a fake "help Muslim voters choose well" site).
5. **Amplify.** Avatar/bot network infiltrating Facebook groups, manipulating trends, skewing TikTok/Instagram polls, plus paid Meta ads.
6. **Harvest.** A fake charity ("Sadaqah Palestine") as a honeypot for donations and donor PII.
7. **Burn down.** On exposure, delete avatars, sites and login portals within ~2 hours of contact — though residual traces enabled attribution.

---

## TTPs

### (a) DISARM techniques

| DISARM (indicative) | Technique | How BlackCore uses it | Evidence |
| :-- | :-- | :-- | :-- |
| T0086 | Develop AI-generated content / synthetic media | AI-generated fake nude images of a candidate | Haaretz/Libération |
| T0087/T0088 | Create inauthentic personas / sock puppets | "Sophie" blogger persona issuing accusations | Haaretz |
| T0085 | Create inauthentic websites / news sites | Multiple fabricated smear sites; fake "Muslim voter guide" | Le Monde, Haaretz |
| T0017 | Conduct fundraising / honeypot | "Sadaqah Palestine" fake charity harvesting money + PII | Haaretz, Drop Site |
| T0049 | Flood / coordinated inauthentic amplification | ~1,600 avatars; Facebook-group infiltration; TikTok/IG poll-skewing | Haaretz, Viginum |
| T0023 | Paid targeted advertising | Paid Meta ads for the charity honeypot and smears | Haaretz |
| T0128/T0129 | Conceal / scrub infrastructure | Anonymous registrar; ~2-hour teardown on exposure | Haaretz/Libération |

> DISARM IDs above are indicative mappings pending analyst confirmation against the current DISARM Red Framework release.

### (b) MITRE ATT&CK (cyber-enabled activity only)

| ATT&CK | Technique | Use | Evidence |
| :-- | :-- | :-- | :-- |
| T1583 (.001 Domains / .004 Server) | Acquire Infrastructure | Anonymous domain + multi-country servers/hosting | Haaretz/Libération |
| T1585 (.001/.002) | Establish Accounts (social/email) | Avatar account fleet; persona accounts | Haaretz |
| T1598 / T1589 | Phishing-for-info / Gather Victim Identity Info | Charity honeypot harvesting donor PII | Haaretz, Drop Site |

> BlackCore performs **no observed intrusion/exploitation** — ATT&CK coverage is limited to resource-development and collection, which is typical for a pure influence-ops actor. The centre of gravity is DISARM, not ATT&CK.

### (c) Aunoo 8-tactic reframing vector

| Tactic | Salience (0–3) | Rationale / example |
| :-- | :-- | :-- |
| Legitimacy Inversion | 2 | Fake blogger + fake charity positioned as authentic, credible voices to launder claims. |
| Severity Minimization | 0 | Not observed. |
| Category Reframing | 1 | Recasting candidates' politics as "pro-Muslim"/extremist framing. |
| Whataboutism | 0 | Not observed. |
| **Identity Reframing** | **3 (signature)** | Branding candidates as "rapists," "pro-Muslim," extremist — false categorical attributes attached to targets. |
| Motive Substitution | 1 | Implying smeared figures act from illegitimate/criminal motives. |
| Agent Swap | 0 | Not observed. |
| Cause-Effect Reversal | 0 | Not observed. |

> **Fabrication flag (outside the reframing model).** BlackCore's most damaging content — AI-generated fake nudes, invented rape allegations, a wholly fictitious charity — is **pure fabrication**, not reframing of a real event. This is captured under DISARM above. The profile of *heavy fabrication + Identity-Reframing-dominant vector + low use of the subtler reframing tactics* is itself a useful BlackCore signature: this is a smear-and-amplify shop, not a narrative-laundering operation in the Russian state-media mould.

---

## Infrastructure & indicators

Core observables: the `blackcore[.]online` brand domain (anonymous Icelandic registrar, Aug 2025) and 8 subdomains; a London-hosted server (Finnish cloud provider) carrying password-protected influence tooling including the "Galacticos AI Avatar Generator" login; additional servers in Britain, Germany, Finland and Lithuania; the Tel Aviv corporate cluster at 103 HaHashmonaim St (Galacticos Ltd, SNI Digital Ltd, Benguy Escrow Company Ltd); the "Sadaqah Palestine" fake-charity web/social/ad assets; and the "Sophie" persona. Most assets were taken down within hours of press contact. Full structured list in [`indicators.yaml`](./indicators.yaml).

---

## Campaigns & incidents

### CAMP-BLACKCORE-01 — France LFI municipal smear (Mar 2026)

Fabricated sexual-assault allegations, AI-generated fake nudes, a fake "Muslim voter guide," and avatar amplification against three LFI candidates ahead of the March 2026 municipals. Removed by Meta/Google/TikTok for coordinated inauthentic behaviour; now under two French investigations.
**Sitrep:** [2026-06-blackcore-france-elections](https://github.com/AuNooAI/situationreports/tree/main/reports/2026-06-blackcore-france-elections)

### CAMP-BLACKCORE-02 — NYC 2025, Scotland, Angola, Togo (per Viginum)

Same MO attributed by Viginum to the 2025 NYC mayoral race, Scotland's FM John Swinney, and activity in Angola and Togo. Sponsor unidentified.

### CAMP-BLACKCORE-03 — "Sadaqah Palestine" honeypot

Fake pro-Palestinian aid charity (web + social + paid Meta ads) built to harvest donations and donor PII; no registry record in UK/US/EU/Israel.

---

## Relationships

- **Galacticos Ltd / SNI Digital Ltd / Benguy Escrow Company Ltd** — the corporate/infrastructure cluster BlackCore's tooling traces to (Tel Aviv).
- **ACT-2026-TEAMJORGE** (Team Jorge / Tal Hanan) — *comparison only*, no established operational link. Same genre (Israeli influence-for-hire, avatar/bot tooling, election clients); useful as an analytic analogue.
- **ACT-2026-MANASSEHCHORUS** (MANASSEH CHORUS / Clock Tower X) — *methodological comparison only*, no established operational link and no shared-attribution claim. Contrasts an overt, FARA-registered US influencer operation run by Brad Parscale with BlackCore's covert fabrication vendor model. Because BlackCore's own commissioning client is unattributed (assessed at low confidence), the comparison is about method, not a common sponsor or objective.
- **Black Cube** — *explicitly NOT related.* Different, older Israeli private-intelligence firm; named here only to prevent conflation.

---

## Detection & monitoring guidance (Aunoo platform)

- **Raise-conditions:** sudden persona clusters attacking a single Gaza-critical candidate with sexual-misconduct or extremism framing; fabricated single-purpose news/blog domains on shared hosting; "charity" assets with manufactured followings and paid amplification; anonymous-registrar domains presenting as long-established.
- **Relevant detectors / tactic-heads:** **Identity Reframing** head (primary signature) and **Legitimacy Inversion** head; the **cluster-detection** and **echo-loop/amplification** modules (avatar fleet + paid ads is a strong coordination signal independent of per-claim score); account-level coordination once that workstream lands (timing synchrony + lexical fingerprinting across the avatar fleet).
- **label_status workflow:** treat new BlackCore-consistent activity as `suspected` on a single-thread match; `tentative` on corroborated infrastructure or persona reuse; `confirmed` only after analyst review with a documented evidence chain (infrastructure overlap + behavioural signature + independent corroboration).
- **Pivots:** from any indicator, pivot on (a) registrar/hosting cluster, (b) the 103 HaHashmonaim corporate address, (c) avatar-generator artefacts/login fingerprints, (d) persona reuse, (e) shared Meta ad-account or payment trails.

---

## Outlook & watch indicators

Infrastructure is down and the firm is under French investigation, but the *capability* (Galacticos avatar tooling, the corporate cluster, the personnel) is intact — **expect re-branding rather than disappearance** (consistent with the Pagecorn → Mycelium → Galacticos history). **Single best early-warning signal:** re-emergence of the avatar-generation tooling fingerprint or 103 HaHashmonaim-linked registrations under a new brand. Secondary: the DGSI probe naming a commissioning client (would move attribution from Low toward Moderate/High and reclassify motivation).

---

## Source assessment & confidence

Anchored on the **Haaretz/Libération joint technical investigation** (high factuality, original digital-forensic work; ~B2) and **Reuters** (~B2), corroborated by **Viginum**'s on-record attributions via the French PM's press conference (~B1) and platform enforcement actions. The operation, tooling, and targeting are well-corroborated (**confirmed**). The "BlackCore" corporate identity is **tentative** (no registry record; attribution via shared infrastructure; principals deny involvement). The commissioning client is **unknown** (Viginum could not identify a sponsor). Thinner, single-thread elements: the Unit 8200 / Yigal Unna links (denied; `unresolved`) and the precise scope of the NYC/Scotland/Angola/Togo operations (asserted by Viginum, limited public technical detail). Attribution would shift materially if the DGSI probe releases the client/payment trail or if Israeli corporate records tie the "BlackCore" name to the Galacticos cluster.

---

## Changelog

| Date | Change |
| :-- | :-- |
| 2026-06-20 | Initial profile created at `tentative` / attribution `moderate`. Worked example for the actor-profile format. |
| 2026-07-14 | Added reciprocal cross-link to ACT-2026-MANASSEHCHORUS (MANASSEH CHORUS / Clock Tower X) as a comparison/counterpart; bumped `last_updated`. |
| 2026-07-15 | Recast the MANASSEH CHORUS link as a methodological comparison only; removed the shared Israel-nexus/Gaza-objective claim (BlackCore's client is unattributed). |

---

## Sources

1. [Haaretz — Israeli Firm BlackCore Suspected of Meddling in NYC, Scotland Elections](https://www.haaretz.com/israel-news/security-aviation/2026-06-11/ty-article/israeli-firm-blackcore-suspected-of-meddling-in-nyc-scotland-elections/0000019e-b7d1-d892-adde-f7df71710000) — B2
2. [Haaretz — The Fake Gaza Charity Linked to the Anti-left Disinformation Campaign in France](https://www.haaretz.com/israel-news/security-aviation/2026-06-11/ty-article-magazine/.premium/the-fake-gaza-charity-linked-to-the-anti-left-disinformation-campaign-in-france/0000019e-b6a8-d7bd-a3bf-beec56f10000) — B2
3. [Middle East Eye — Israeli firm BlackCore meddled in US and Scottish elections, French watchdog says](https://www.middleeasteye.net/news/nyc-and-scotland-elections-also-targeted-israeli-firm-blackcore-french-watchdog-says) — B2
4. [Middle East Eye — 'Attack on our democracy': Inside an Israeli influence campaign in France's local elections](https://www.middleeasteye.net/news/unprecedented-attack-inside-israeli-foreign-influence-campaign-france-local-elections) — B2
5. [The Canary — BlackCore: Inside an Israeli foreign influence operation](https://www.thecanary.co/global/world-analysis/2026/05/19/blackcore-psy-op/) — C2
6. [Times of Israel — France probing if shadowy Israeli firm BlackCore meddled in municipal elections](https://www.timesofisrael.com/france-probing-if-shadowy-israeli-firm-blackcore-meddled-in-municipal-elections-sources/) — B2
7. [Times of Israel — French official accuses Israeli firm of also meddling in NYC, Scotland](https://www.timesofisrael.com/french-official-accuses-israeli-firm-of-also-meddling-in-elections-in-new-york-city-scotland/) — B2
8. [US News / Reuters — France Probes Whether Israeli Firm BlackCore Interfered in Local Elections](https://www.usnews.com/news/world/articles/2026-05-13/exclusive-france-probes-whether-israeli-firm-blackcore-interfered-in-local-elections-sources-say) — B2
9. [The New Arab — France says Israeli spy firm behind fake Palestinian aid charity](https://www.newarab.com/news/france-says-israeli-spy-firm-behind-fake-palestinian-aid-charity) — C2
10. [Palestine Chronicle — Inside the BlackCore Network Linked to a Fake Palestine Aid Operation](https://www.palestinechronicle.com/extremely-grave-inside-the-blackcore-network-linked-to-a-fake-palestine-aid-operation/) — C3
11. [WION — How an Israeli influence operation allegedly targeted elections across multiple countries](https://www.wionews.com/world/blackcore-israel-election-interference-france-scotland-new-york-viginum-report-1781845456022/amp) — C3
12. [Al Arabiya — Israeli firm BlackCore suspected of meddling in New York and Scotland votes](https://english.alarabiya.net/amp/News/world/2026/06/12/israeli-firm-blackcore-suspected-of-meddling-in-new-york-and-scotland-votes-france-says) — C2
