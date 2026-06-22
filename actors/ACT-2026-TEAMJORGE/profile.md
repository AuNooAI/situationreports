---
id: ACT-2026-TEAMJORGE
name: Team Jorge
codename: AHAB PUPPETEER
aliases: [Jorge, AIMS team, Tal Hanan group]
actor_type: influence-ops-vendor
country_nexus: [Israel]
operational_status: disrupted
profile_status: confirmed
attribution_confidence: high
first_observed: 2015
last_active: 2023
last_updated: 2026-06-20
tlp: CLEAR
motivations: [contract-hire, financial]
target_sectors: [elections, political-campaigns, corporate-disputes]
target_geographies: [global, Africa-heavy]
frameworks: [DISARM, ATT&CK, AUNOO-8T]
aunoo_tactic_vector:
  legitimacy_inversion: 2
  severity_minimization: 0
  category_reframing: 0
  whataboutism: 0
  identity_reframing: 1
  motive_substitution: 0
  agent_swap: 0
  cause_effect_reversal: 0
related_sitreps: []
related_actors:
  - ACT-2026-BLACKCORE
source_count: 8
admiralty_high_water: A1
analyst: "Aunoo Intelligence"
review_status: published
---

# THREAT ACTOR PROFILE: AHAB PUPPETEER — "Team Jorge" (ACT-2026-TEAMJORGE)

**Classification:** Unclassified · OSINT · **TLP:**CLEAR
**Code name:** AHAB PUPPETEER
**As of:** 20 June 2026, 18:00 UTC
**Profile status:** confirmed · **Attribution confidence:** high
**Prepared from:** 8 sources · Admiralty high-water A1 (subject recorded on camera by the journalist consortium that exposed him)

---

## Bottom line up front (BLUF)

Team Jorge is an Israeli private "influence-for-hire" outfit led by **Tal Hanan** (a former Israeli special-forces operative who used the alias "Jorge"), exposed in **February 2023** by the *Story Killers* investigation — a 30-outlet consortium coordinated by **Forbidden Stories**, whose undercover reporters recorded Hanan on camera in Tel Aviv pitching his services. Hanan boasted of involvement in **33 presidential-level campaigns, 27 of them "successful,"** many in Africa, with activity dating to at least 2015. Team Jorge's signature capability is **AIMS** (Advanced Impact Media Solutions), a control panel for **tens of thousands of fabricated social-media avatars** across X/Twitter, Facebook, LinkedIn, Telegram, Gmail, Instagram, YouTube and more — each with a constructed backstory. Beyond avatars, the group runs **offensive cyber operations** (hacking Gmail/Telegram accounts via telecom/SS7 weaknesses) for hack-and-leak operations. **Unlike most pure-IO actors, Team Jorge is a genuine hybrid** — disinformation *and* intrusion — which is why MITRE ATT&CK carries real weight in this profile. It is included here primarily as a **lineage/comparison anchor** for newer Israeli vendors such as [BlackCore (ACT-2026-BLACKCORE)](../ACT-2026-BLACKCORE/profile.md); the two are the same genre but have **no established operational link.**

---

## Quick-reference card

| Field | Value |
| :-- | :-- |
| Actor ID | `ACT-2026-TEAMJORGE` |
| Code name | **AHAB PUPPETEER** |
| Aliases | "Jorge", AIMS team, Tal Hanan group |
| Type | Influence-operations vendor (hire-for-service) + offensive cyber |
| Country nexus | Israel |
| Operational status | Disrupted (publicly exposed 2023; reported Israeli investigation) |
| First observed | ≥ 2015 |
| Last active | 2023 (exposure) |
| Attribution confidence | High (principal recorded on camera; consortium-verified) |
| Frameworks mapped | DISARM · ATT&CK · Aunoo 8-tactic |

---

## Attribution & confidence

**Diamond Model.**

| Vertex | Finding | Confidence |
| :-- | :-- | :-- |
| Adversary | Tal Hanan ("Jorge"), ex-Israeli special forces; brother Zohar Hanan reported in a management/finance role; corporate vehicle reported as **Demoman International Ltd** (Modi'in, Israel). | High |
| Capability | **AIMS** avatar-management platform (tens of thousands of personas); offensive hacking of Gmail/Telegram via SS7-class telecom weaknesses; hack-and-leak; bot amplification. | High |
| Infrastructure | AIMS SaaS back-end; large avatar fleets with backstories, payment cards and phone numbers across many platforms. | High |
| Victim | Political campaigns and candidates (≈33 countries claimed, Africa-heavy), plus corporate-dispute targets. | High (self-claimed scope; specific cases vary) |

**Confidence statement.** This is one of the **best-evidenced** actors of its kind: the principal was filmed demonstrating his own tooling by undercover journalists, and the findings were cross-checked by ~30 outlets. The *existence, leadership and capability* are **confirmed** (Admiralty A1–B2). The one area to treat with care is the **scope of impact**: the "33 campaigns / 27 successful" figure is **Hanan's own sales boast**, not independently verified per-election — treat as `tentative` claim-level evidence.

**Competing hypotheses.** Little genuine ambiguity on *who*; the open question is *how much actually worked* vs. marketing exaggeration. Treat operational outcomes as unproven.

---

## History & evolution

Active since at least **2015**. Operated quietly as a cyber-mercenary service to political and corporate clients until undercover reporters from **TheMarker (Gur Megiddo)**, **Haaretz (Omer Benjakob)** and **Radio France (Frédéric Métézeau)**, posing as consultants for a "politically unstable African country that wanted to delay an election," recorded ~6 hours of meetings with Hanan between **July and December 2022**. The findings were published **February 2023** as part of *Story Killers*.

| When | Event |
| :-- | :-- |
| ≥ 2015 | Team Jorge active in election-manipulation contracting |
| Jul–Dec 2022 | Undercover consortium reporters record Hanan in Tel Aviv; he demonstrates AIMS and live-hacks accounts |
| Feb 2023 | *Story Killers* exposé published by Forbidden Stories + ~30 outlets (Guardian, Haaretz, Der Spiegel, Le Monde, OCCRP, El País, etc.) |
| 2023 → | Reporting of an Israeli investigation; platforms move against AIMS-linked accounts |

---

## Ownership, structure & key personnel

- **Tal Hanan** — founder/leader; alias "Jorge"; former Israeli special forces. Status: `confirmed`.
- **Zohar Hanan** — Tal's brother; reported management/financial role. Status: `confirmed` (identity) / role `confirmed` per reporting.
- **Demoman International Ltd** — corporate vehicle reportedly associated with Tal Hanan (Modi'in, Israel). Status: `confirmed` (entity) / operational link `tentative`.

---

## Targeting / victimology

Primarily **electoral**: candidates and campaigns in ≈33 countries (Hanan's claim), heavily in **Africa**, plus Latin America and elsewhere. Also **corporate/commercial disputes**. Clients are reported to include intelligence services, corporations and political actors — i.e. a true mercenary model where targeting follows the paying client rather than a fixed ideology.

---

## Modus operandi

A **mercenary, full-service** model. Team Jorge sold an integrated package: (1) **AIMS** to stand up and orchestrate large fleets of believable fake personas across platforms; (2) **offensive intrusion** to compromise targets' Gmail/Telegram accounts (exploiting telecom/SS7 weaknesses), enabling **hack-and-leak** operations timed to damage a target; (3) **amplification and narrative seeding** through the avatar fleet; (4) **sabotage/blackmail** elements. Hanan demonstrated the avatar interface live — choosing nationality, gender, and matching a profile photo to a generated name in seconds — and demonstrated account compromise on real accounts during the undercover meetings.

---

## TTPs

### (a) DISARM techniques

| DISARM (indicative) | Technique | Use | Evidence |
| :-- | :-- | :-- | :-- |
| T0090/T0091 | Create / recruit inauthentic personas at scale | AIMS tens-of-thousands avatar fleet with backstories | Story Killers |
| T0085 | Develop inauthentic content | Persona posts, seeded narratives | Story Killers |
| T0049 | Coordinated amplification / flood | Cross-platform avatar amplification | Story Killers |
| T0019/T0023 | Hack-and-leak / paid promotion | Compromised-account leaks timed to elections | Story Killers |

### (b) MITRE ATT&CK (this actor genuinely intrudes)

| ATT&CK | Technique | Use | Evidence |
| :-- | :-- | :-- | :-- |
| T1583 | Acquire Infrastructure | AIMS back-end, avatar phone numbers / payment cards | Story Killers |
| T1585 | Establish Accounts | Mass fabricated social/email accounts | Story Killers |
| T1586 | Compromise Accounts | Hijacking targets' Gmail/Telegram | Story Killers |
| T1598 / SS7 abuse | Phishing-for-info / telecom-signalling abuse | Account takeover via telecom weaknesses | Story Killers |
| T1567 | Exfiltration / leak | Hack-and-leak against political targets | Story Killers |

> Contrast with BlackCore: BlackCore's ATT&CK footprint is thin (resource development only); **Team Jorge actively compromises accounts**, so its ATT&CK mapping is substantive.

### (c) Aunoo 8-tactic reframing vector

| Tactic | Salience (0–3) | Rationale |
| :-- | :-- | :-- |
| Legitimacy Inversion | 2 | Avatar fleet manufactures the appearance of authentic grassroots voices. |
| Identity Reframing | 1 | Smear content against targets in some campaigns. |
| (others) | 0 | Not characteristic. |

> **Fabrication + intrusion dominant.** Team Jorge's core is *manufactured personas and hacking*, not reframing of real events. The low reframing vector alongside heavy fabrication and a real ATT&CK footprint is the signature.

---

## Infrastructure & indicators

Headline observables in [`indicators.yaml`](./indicators.yaml): the **AIMS** platform; the **"Jorge"** alias; **Tal Hanan** and **Zohar Hanan**; **Demoman International Ltd** (Modi'in); avatar fleets characterised by constructed backstories, attached phone numbers and payment cards across X/Twitter, Facebook, LinkedIn, Telegram, Gmail, Instagram, YouTube, Amazon and Airbnb.

---

## Campaigns & incidents

### CAMP-TEAMJORGE-01 — *Story Killers* exposure (2022–2023)

Undercover consortium documented AIMS and live account-hacking; ~33 claimed presidential-level campaigns surfaced. No Aunoo situation report yet; create one if a specific campaign is worked in depth.

---

## Relationships

- **ACT-2026-BLACKCORE** (BlackCore / AMON MIRAGE) — *comparison / lineage anchor*, **no established operational link.** Same ecosystem: Israeli influence-for-hire, avatar tooling, election clients. Useful as the canonical prior-art example when assessing newer entrants.

---

## Detection & monitoring guidance (Aunoo platform)

- **Raise-conditions:** large persona fleets with synchronized cross-platform posting and shallow backstories; sudden hack-and-leak dumps timed to an election; clusters whose accounts share creation-pattern or phone-number fingerprints.
- **Relevant detectors / tactic-heads:** account-level coordination (timing synchrony, lexical fingerprinting) once that workstream lands; Legitimacy Inversion head; cluster + echo-loop modules. Hack-and-leak content needs provenance handling, not reframing detection.
- **label_status workflow:** historical/known actor → treat fresh AIMS-consistent fleets as `tentative` on tooling/fingerprint overlap; `confirmed` only on analyst-reviewed corroboration.

---

## Outlook & watch indicators

Publicly burned in 2023, but the tradecraft (AIMS-style avatar orchestration + hack-and-leak) is now a template copied by successors. **Watch for:** rebranded successors reusing AIMS-style fingerprints; any resurfacing of Hanan-linked entities. Team Jorge's main ongoing value is as the **reference pattern** against which new Israeli IO vendors (BlackCore included) are assessed.

---

## Source assessment & confidence

Exceptionally well-evidenced for this category: the principal was **filmed demonstrating his own tooling** by an undercover consortium of ~30 outlets (Admiralty A1 on the recordings; B1–B2 on downstream reporting). Leadership, capability and methods are **confirmed**. The **scope-of-impact** claim ("33 campaigns / 27 successful") is the subject's own **sales boast** and should be treated as `tentative` at the per-election level.

---

## Changelog

| Date | Change |
| :-- | :-- |
| 2026-06-20 | Initial profile created at `confirmed` / attribution `high`. Second worked example; lineage anchor for BlackCore. Code name AHAB PUPPETEER assigned. |

---

## Sources

1. [Team Jorge — Wikipedia (overview + consortium list)](https://en.wikipedia.org/wiki/Team_Jorge) — C3
2. [Forbidden Stories — "Team Jorge": In the heart of a global disinformation machine](https://forbiddenstories.org/team-jorge-disinformation/) — A2 (primary consortium report)
3. [OCCRP — Hacks, Bots and Blackmail: How Secret Cyber Mercenaries Disrupt Elections](https://www.occrp.org/en/project/story-killers/hacks-bots-and-blackmail-how-secret-cyber-mercenaries-disrupt-elections) — A2
4. [The Times of Israel — Exposé unmasks Israel-led disinformation team that meddled in dozens of elections](https://www.timesofisrael.com/expose-unmasks-israel-led-disinformation-team-that-meddled-in-dozens-of-elections/) — B2
5. [Gizmodo — A Secretive Israeli Company Says It Manipulated More Than 30 Elections Worldwide](https://gizmodo.com/team-jorge-election-meddling-tal-hanan-misinformation-1850120328) — C3
6. [Peoples Dispatch — Team Jorge: The Israeli contractors behind disinformation and election interference](https://peoplesdispatch.org/2023/02/17/team-jorge-the-israeli-contractors-behind-disinformation-and-election-interference/) — C3
7. [Business & Human Rights Resource Centre — summary + responses](https://www.business-humanrights.org/en/latest-news/israel-team-of-contractors-claim-to-have-manipulated-elections-around-the-world-using-hacking-sabotage-social-media-disinformation/) — C2
