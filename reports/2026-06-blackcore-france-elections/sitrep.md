---
related_actors:
  - ACT-2026-BLACKCORE   # code name: AMON MIRAGE
actor_profiles:
  - ../../actors/ACT-2026-BLACKCORE/profile.md
---

# SITUATION REPORT: AMON MIRAGE (BlackCore) — 2026 French Municipal Election Interference Campaign

**Classification:** Unclassified · Open-source intelligence (OSINT) · TLP:CLEAR
**As of:** 20 June 2026, 18:00 UTC
**Prepared from:** Haaretz/Libération joint investigation, Reuters, and Viginum on-record statements, with 12+ corroborating sources
**Subject:** A cross-border digital-interference campaign against pro-Palestinian left-wing candidates in France's March 2026 municipal elections, attributed in open reporting to the Israeli influence firm tracked by Aunoo as **AMON MIRAGE** (self-styled "BlackCore")
**Attributed actor:** [AMON MIRAGE — "BlackCore" (ACT-2026-BLACKCORE)](../../actors/ACT-2026-BLACKCORE/profile.md)

---

## Bottom line up front (BLUF)

**AMON MIRAGE** — the Aunoo code name for the Israeli "elite influence, cyber and technology" firm that styles itself **"BlackCore"** — is the suspected operator of a coordinated online smear campaign run ahead of France's **March 2026 municipal elections** against three left-wing France Unbowed (LFI) candidates. The campaign used fabricated sexual-assault allegations, **AI-generated fake nude imagery**, sock-puppet personas, fake "news" sites, and an avatar/bot amplification network. Meta, Google and TikTok removed assets for **coordinated inauthentic behaviour**. French reporting and the watchdog **Viginum** attribute the operation to BlackCore, whose infrastructure a *Haaretz*/*Libération* joint investigation traced to two Tel Aviv companies (Galacticos Ltd, SNI Digital Ltd). **The operation is well-evidenced; the corporate identity and the commissioning client are not.** No registry record of "BlackCore" has been found, the named principals deny involvement, and Viginum could not identify who paid for the campaign. Two French investigations (Paris prosecutors; DGSI) are ongoing. Full actor tracking: **[AMON MIRAGE / ACT-2026-BLACKCORE](../../actors/ACT-2026-BLACKCORE/profile.md)**.

> **Naming note.** *AMON MIRAGE* is Aunoo's internal code name for this actor (the wicked-king register is a deliberately critical label for a suspected-Israeli influence operation; see the [profile schema](../../actors/SCHEMA.md)). *"BlackCore"* is the name the operation gave itself. Both refer to the same entity, `ACT-2026-BLACKCORE`.

---

## What happened

- Around the **March 2026 municipal elections**, a coordinated operation targeted three LFI (France Unbowed / Jean-Luc Mélenchon's party) mayoral candidates: **Sébastien Delogu** (Marseille), **François Piquemal** (Toulouse), and a third candidate in **Roubaix**.
- The campaign deployed **fabricated criminal allegations** (a sock-puppet "Sophie" persona accused Delogu of rape and violence), **AI-generated fake nude photographs** presented as part of a fake Gaza fundraising effort, a separate site attacking Piquemal, and a fake "help Muslim voters choose well" site steering voters — all amplified by a **network of fake social-media accounts**.
- The operation was **first exposed by *Le Monde* on 9 March 2026**, a week before the vote. Once discovered, operators began deleting avatars and websites, but residual digital traces survived.
- A French special investigative team (General Secretariat for Defence and National Security, Interior Ministry, the election commission, and **Viginum**) picked up the trail and identified **BlackCore** (AMON MIRAGE) as the main suspect. **Reuters first named BlackCore** in mid-May 2026.
- A ***Haaretz*/*Libération* joint investigation** analysed BlackCore's digital footprint — a bilingual marketing site advertising a **"political campaign management"** product built on **~1,600 avatars** — and tied the infrastructure to a London server, multi-country hosting (UK, Germany, Finland, Lithuania), and a Tel Aviv corporate cluster.
- On **11–12 June 2026**, Viginum chief Marc-Antoine Brillant (alongside PM Sébastien Lecornu) said the same modus operandi had also been used against the **2025 New York City** mayoral race, **Scotland** (First Minister John Swinney), and in **Angola** and **Togo** — but that the **sponsor could not be identified**.
- A linked **fake charity, "Sadaqah Palestine,"** operated as a honeypot to harvest donations and donor personal data from Gaza sympathisers.

## Indicative timeline

| When | Event |
|---|---|
| Aug 2025 | `blackcore[.]online` registered via an anonymous Icelandic registrar; site presents the firm as long-established |
| 9 Mar 2026 | *Le Monde* exposes the anonymous smear campaign against LFI candidates, one week before the municipal vote |
| Mar 2026 | Municipal elections held; Meta/Google/TikTok remove assets for coordinated inauthentic behaviour |
| ~13 May 2026 | **Reuters** first names "BlackCore"; reports French probe |
| ~mid-May 2026 | *Haaretz*/*Libération* publish joint technical investigation; principals asked for comment → BlackCore + Galacticos infrastructure pulled offline within ~2 hours |
| 11–12 Jun 2026 | **Viginum** attributes the same MO to NYC 2025, Scotland, Angola, Togo; states the sponsor is unidentified |
| Jun 2026 | French government formally asks Israel for explanations; two French investigations underway (Paris prosecutors; DGSI) |

## Key facts at a glance

| Item | Detail |
|---|---|
| Actor (code name) | **AMON MIRAGE** (`ACT-2026-BLACKCORE`) |
| Primary targets | Sébastien Delogu (LFI, Marseille), François Piquemal (LFI, Toulouse), third LFI candidate (Roubaix) |
| Tactics | Fabricated rape/violence claims, AI fake nudes, sock-puppet personas, fake news/voter-guide sites, avatar/bot amplification, paid Meta ads, fake-charity honeypot |
| Attributed operator | **AMON MIRAGE** — self-styled "BlackCore", an Israeli "elite influence, cyber and technology" firm (no found legal registration) |
| Infrastructure | Anonymous Icelandic-registered domain; London server (Finnish cloud provider); servers in UK/DE/FI/LT; Tel Aviv cluster at 103 HaHashmonaim St |
| Linked companies | Galacticos Ltd (ex-Pagecorn → Mycelium Intelligence Networks); SNI Digital Ltd — principals **deny involvement** |
| Platform action | Meta, Google, TikTok removed assets for coordinated inauthentic behaviour |
| Commissioning client | **Unknown** — Viginum could not identify a sponsor |
| Investigations | Paris prosecutors; DGSI (domestic intelligence) |
| Actor profile | [AMON MIRAGE / ACT-2026-BLACKCORE](../../actors/ACT-2026-BLACKCORE/profile.md) |

---

## Significance

This is a rare, well-documented look inside a **commercial, hire-for-service influence operation** that crossed multiple democracies. Three features stand out. First, the **productisation**: AMON MIRAGE marketed a packaged "political campaign management" capability (an avatar army) to governments and campaigns, rather than running a one-off operation. Second, the **target logic**: across France, NYC, and Scotland, the through-line is electorally relevant figures who criticised Israel's conduct in Gaza or championed Palestinian rights — yet parallel Angola/Togo activity points to a paying-client model rather than purely ideological motivation. Third, the **attribution gap**: the operation is corroborated by a state watchdog and platform takedowns, but the operating entity has no corporate footprint and the client is unknown — the defining difficulty of influence-ops attribution.

## Outlook & indicators to watch

- **DGSI findings on the client.** Identification of who commissioned the campaign would move attribution from low toward moderate/high and clarify motivation. Primary indicator.
- **Re-branding, not disappearance.** The capability (avatar tooling, the Tel Aviv corporate cluster, the personnel) is intact; the firm's history of renaming (Pagecorn → Mycelium → Galacticos) suggests it may resurface under a new brand. Watch for the avatar-generator fingerprint or new registrations linked to 103 HaHashmonaim Street.
- **Spread to other elections.** Any further Viginum/partner attributions would confirm a systematic cross-border service rather than a France-specific event.
- **Israeli response.** Whether Israel's own promised review produces findings.

## Source assessment

Anchored on the **Haaretz/Libération joint investigation** (original digital-forensic work; high factuality) and **Reuters**, corroborated by **Viginum**'s on-record statements via the French PM's press conference and by platform enforcement actions (Meta, Google, TikTok). The operation, tooling, and targeting are well-corroborated. The "BlackCore" corporate identity is **tentative** (no registry record; attribution via shared infrastructure; named principals deny involvement). The commissioning client is **unknown**. Thinner, single-thread elements include the Unit 8200 / Yigal Unna links (denied) and the technical specifics of the NYC/Scotland/Angola/Togo operations (asserted by Viginum with limited public detail). Confidence: **High** on the operation and its terms; **Moderate** on operator attribution; **Low** on the sponsor.

## Sources

- [Haaretz — Israeli Firm BlackCore Suspected of Meddling in NYC, Scotland Elections](https://www.haaretz.com/israel-news/security-aviation/2026-06-11/ty-article/israeli-firm-blackcore-suspected-of-meddling-in-nyc-scotland-elections/0000019e-b7d1-d892-adde-f7df71710000)
- [Haaretz — The Fake Gaza Charity Linked to the Anti-left Disinformation Campaign in France](https://www.haaretz.com/israel-news/security-aviation/2026-06-11/ty-article-magazine/.premium/the-fake-gaza-charity-linked-to-the-anti-left-disinformation-campaign-in-france/0000019e-b6a8-d7bd-a3bf-beec56f10000)
- [Reuters via US News — France Probes Whether Israeli Firm BlackCore Interfered in Local Elections](https://www.usnews.com/news/world/articles/2026-05-13/exclusive-france-probes-whether-israeli-firm-blackcore-interfered-in-local-elections-sources-say)
- [Times of Israel — France probing if shadowy Israeli firm BlackCore meddled in municipal elections](https://www.timesofisrael.com/france-probing-if-shadowy-israeli-firm-blackcore-meddled-in-municipal-elections-sources/)
- [Middle East Eye — Israeli firm BlackCore meddled in US and Scottish elections, French watchdog says](https://www.middleeasteye.net/news/nyc-and-scotland-elections-also-targeted-israeli-firm-blackcore-french-watchdog-says)
- [Middle East Eye — 'Attack on our democracy': Inside an Israeli influence campaign in France's local elections](https://www.middleeasteye.net/news/unprecedented-attack-inside-israeli-foreign-influence-campaign-france-local-elections)
- [The Canary — BlackCore: Inside an Israeli foreign influence operation](https://www.thecanary.co/global/world-analysis/2026/05/19/blackcore-psy-op/)
- [The New Arab — France says Israeli spy firm behind fake Palestinian aid charity](https://www.newarab.com/news/france-says-israeli-spy-firm-behind-fake-palestinian-aid-charity)
- [Al Arabiya — Israeli firm BlackCore suspected of meddling in New York and Scotland votes](https://english.alarabiya.net/amp/News/world/2026/06/12/israeli-firm-blackcore-suspected-of-meddling-in-new-york-and-scotland-votes-france-says)

*Compiled via Aunoo Intelligence. This SITREP synthesises open-source reporting and should be verified against primary statements (Viginum, French judicial authorities) before use in decision-making. Influence-operation attribution is probabilistic; confidence levels are stated so readers can weigh the evidence. Actor tracking: [AMON MIRAGE / ACT-2026-BLACKCORE](../../actors/ACT-2026-BLACKCORE/profile.md).*
