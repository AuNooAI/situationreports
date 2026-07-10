# SITUATION REPORT: AfD "Alternita" — a party-run AI system for mass-producing far-right "rage bait"

**Classification:** Unclassified · Open-source intelligence (OSINT)
**As of:** 10 July 2026, 12:00 UTC
**Prepared from:** Correctiv undercover investigation, as reported by The Irish Times (Derek Scally, 8 July 2026), supplemented by Aunoo news-intelligence
**Subject:** The AfD's Alternita platform, which uses commercial AI models from Google, OpenAI, and Anthropic to turn far-right articles into ready-to-post social-media content, and the questions this raises about provider policy enforcement and unlabeled political content ahead of a September German state election

---

## Bottom line up front (BLUF)

Germany's far-right Alternative for Germany (AfD) has built and begun piloting an in-house content system called Alternita that converts far-right news articles into ready-to-post "rage bait" for all major social platforms in a few minutes. An undercover investigation by the German outlet Correctiv, reported by The Irish Times on 8 July 2026, documented the tool generating posts that called for forced deportations, described as "remigration," and a post warning of an LGBT "rainbow dictatorship" accompanied by an AI-generated image of a burning rainbow flag. Correctiv examined Alternita's source code and found it draws on three leading commercial AI engines: Google Gemini, OpenAI's ChatGPT, and Anthropic's Claude.

The platform is registered to the AfD's general secretary, Hans-Holger Malcomeß, and according to Correctiv is already in use on the social-media channels of party co-leader Alice Weidel, where not all of the AI-generated output is labeled as such. Correctiv asked the three technology companies whether this use complies with their terms of service. Google and OpenAI said they are each examining Alternita's use of their engines. Anthropic did not reply to Correctiv's query.

The significance is that this is centralized, party-operated production of automated political propaganda built on mainstream AI tools. Its stated aim is to let AfD headquarters steer messaging while its decentralized base keeps posting, and to extend an online advantage the party already holds. It arrives before a September state-parliament election in an eastern German state where the AfD is polling around 40 percent, and it is an early test of whether AI providers' usage policies can be enforced in practice.

## What is documented

The account below is drawn from Correctiv's investigation as reported by The Irish Times. It reflects a direct product demonstration and an analysis of the platform's source code, not inference.

Alternita markets itself to users as a way to produce social-media posts "in five minutes, with your positions, in your style, your branding." Posing as an AfD regional party member, a Correctiv journalist was given an online tour of the platform by Mario Hau, the social-media chief of the AfD's parliamentary group in the Bundestag. The version demonstrated on a Zoom call automatically pulled in feeds from AfD-friendly far-right outlets, including the site Nius.

Given access to a test account, the Correctiv journalist uploaded a Nius article about revoking citizenship from immigrants. The software generated posts demanding "consequential and involuntary remigration," meaning forced deportations, to prevent "ethnic elections," ending with the tags "#Homeland #Identity #That'sWhyAfD" in translation. Left alone with the test account, the reporters uploaded an article from a neo-Nazi magazine and the tool produced a post warning of an LGBT "rainbow dictatorship," accompanied by an AI-generated image of a burning rainbow flag.

According to Correctiv, Alternita is already running on the channels of AfD co-leader Alice Weidel, and not all content posted through it is flagged as AI-generated. A separate account tied to the effort is "Karl Ranseier," a satirical fictional politician who describes himself as "federal minister for remigration." That account, which Correctiv reports is operated by Hau and followed by Weidel, posts AI-generated images including a "Ministry for Truth" and dark-skinned men boarding a train to a "deportation airport."

The AfD says the software, launched in a pilot phase in the week of 6 July, will be ready for full implementation next year. Hau told the undercover reporter that the platform's content foundation is the current party programme, and that "the whole thing is tailor-made for the AfD." Correctiv examined the source code and found that Alternita draws on Google Gemini, OpenAI's ChatGPT, and Anthropic's Claude.

## Key facts at a glance

| Item | Detail |
|---|---|
| Platform | Alternita, an AfD content-generation tool that turns articles into ready-to-post social content |
| Registered to | Hans-Holger Malcomeß, AfD general secretary |
| Demonstrated by | Mario Hau, social-media chief of the AfD's Bundestag group |
| Exposed by | Correctiv (undercover investigation), reported by The Irish Times, 8 July 2026 |
| AI engines used | Google Gemini, OpenAI ChatGPT, Anthropic Claude (found in the source code) |
| Documented output | Calls for forced "remigration"; an LGBT "rainbow dictatorship" post with an AI burning-flag image |
| Current use | Reportedly running on co-leader Alice Weidel's channels; not all output labeled as AI |
| Provider responses | Google and OpenAI examining the use; Anthropic did not reply |
| Status | Pilot launched w/c 6 July 2026; full rollout planned for 2027 |
| Political context | AfD polling around 40% in an eastern state with a September state-parliament election |

## Indicative timeline

| Date | Event | Significance |
|---|---|---|
| Ongoing | AfD holds a large online lead over rivals on major platforms | The advantage Alternita is designed to scale |
| Week of 6 Jul 2026 | AfD launches Alternita in a pilot phase | The system moves from development to live use |
| 8 Jul 2026 | Correctiv publishes its undercover investigation; The Irish Times reports it | Public exposure of the tool and its AI engines |
| 8 Jul 2026 | Google and OpenAI say they are examining the use; Anthropic does not reply | Opens the provider-enforcement question |
| Sep 2026 | State-parliament election in an eastern German state | Near-term contest where the AfD leads polling |
| 2027 | Planned full implementation of Alternita | Scale-up beyond the pilot |

## Positions of the parties

**The AfD.** The party presents Alternita as an efficiency tool built around its own programme. Hau described it as tailor-made for the AfD, and Correctiv's reporting frames its purpose as letting headquarters keep control of messaging in a subtle way while its decentralized base continues to generate high-engagement posts. The party has not, in the reporting reviewed here, disputed the authenticity of Correctiv's findings.

**The AI providers.** Google and OpenAI told Correctiv they are examining Alternita's use of their engines. Anthropic did not respond. Major providers' usage policies generally prohibit using their models for coordinated political manipulation or deceptive campaigns, and several require that AI-generated political content be disclosed. Whether those policies are being enforced against API-based use of this kind is exactly what is now in question.

**Correctiv.** Correctiv is an established German nonprofit investigative newsroom. It obtained the findings through an undercover approach, a live demonstration, a test account, and an examination of the platform's source code, which is a strong evidentiary basis for the tool's existence and behaviour.

## Implications (second-order effects)

The first effect is the industrialization of political propaganda. Alternita lowers the time and skill needed to turn a partisan article into platform-ready, emotionally charged content, and it does so from a central point while preserving the appearance of an organic, decentralized base. That combination is what makes it more than an ordinary social-media scheduling tool.

The second effect concerns the enforcement of AI-provider policies. Alternita reportedly runs on three mainstream commercial models accessed as services. If a political party can build propaganda tooling on top of these engines, the practical question is whether the providers can detect and stop such use, and how quickly. Enforcement here is reactive, and the exposure came from journalists rather than from the companies' own monitoring.

The third effect is a transparency and labeling gap. Reporting that not all of Alternita's output is marked as AI-generated sits directly against the direction of European regulation, including the AI Act's transparency obligations and platform-level labeling efforts. A party leader's channel carrying unlabeled synthetic political content is a concrete instance of the gap that regulators are trying to close.

The fourth effect is timing and replicability. The pilot is live before a September state election in a region where the AfD already leads, and the design is generic enough that other parties or movements could copy it. A working template is harder to contain than a single campaign.

## Significance

This is a case of a major political party operating its own automated propaganda pipeline on top of mainstream AI infrastructure, rather than a covert network of anonymous accounts. That is what makes it notable. The content is produced centrally and pushed out through a base that looks organic, the tooling is built on services that most organizations can access, and a share of the output is not labeled as machine-generated. Each of those features makes the activity harder to detect, attribute, and regulate than a conventional bot operation.

**Assessment.** On the evidence reported, the existence of Alternita, its documented outputs, and its reliance on Google, OpenAI, and Anthropic models are well supported by Correctiv's direct demonstration and source-code analysis. The scale of current deployment is less certain, since the party describes the system as a pilot, while Correctiv reports it is already active on Weidel's channels. **Confidence: high on the tool's existence, capabilities, and AI engines; moderate on the current scale of live deployment.**

## Consensus and forecast outlook (Aunoo cross-source analysis)

On Aunoo's tracking of the news, coverage of disinformation and influence operations is rising again in early July 2026, running at roughly 28 articles per day and growing at about 12 percent per day, after an earlier lull. The tone of that coverage is strongly negative and has been getting more so, with no sign of a reversal. Across the wider body of reporting, the strongest point of agreement is the need to detect and label AI-generated content as synthetic media spreads across platforms. Recent examples include Google's move to disclose which advertisements are made with AI and the growing volume of reporting on AI-generated content filling social feeds.

Alternita is a concrete instance of the gap that consensus identifies: the ability to generate persuasive political content is outpacing the systems meant to detect or label it. It also connects to the European regulatory thread in the same coverage, where lawmakers are debating message monitoring and content rules, because the tool produces unlabeled synthetic political material inside the EU.

## Outlook and indicators to watch

The near-term question is whether Google, OpenAI, or Anthropic take visible action, such as restricting API access, issuing statements, or changing enforcement, following Correctiv's findings. A second indicator is whether German regulators or EU authorities respond under the AI Act's transparency rules or the Digital Services Act, which would move the matter from journalism to enforcement. A third is whether Alternita advances from pilot to full deployment before the September state election, which would raise its practical effect on that contest. A fourth is whether other parties or movements adopt a similar system, which would turn a single case into a pattern. Finally, platform responses from X and Meta on labeling and coordinated behaviour will indicate whether the distribution side is being addressed at all.

## Source assessment

The core of this report rests on Correctiv's undercover investigation, reported by The Irish Times through its Berlin correspondent Derek Scally. Correctiv is a credible German investigative newsroom, and its findings are based on a live product demonstration, a working test account, and an analysis of Alternita's source code, which together support the existence and behaviour of the tool at high confidence. The specific outputs quoted, including the "remigration" posts and the "rainbow dictatorship" image, are documented by the reporters rather than inferred. The claim that Alternita is already active on Alice Weidel's channels is Correctiv's assessment. The status of provider compliance is characterized through the companies' own responses, where Google and OpenAI said they are examining the use and Anthropic did not reply.

The broader context, that disinformation coverage is re-accelerating and that cross-source consensus centers on AI-content detection and labeling, is Aunoo-derived from its tracking of the disinformation and influence-operations topic. The cited-versus-inferred boundary matters here: the tool and its engines are reported facts, while the judgment that Alternita functions as an industrialized propaganda pipeline, and that it tests provider enforcement, is analysis rather than a claim made by any single source.

**Confidence.** High on the existence, capabilities, and AI engines of Alternita, and on the providers' responses. Moderate to high on the reading of Alternita as centralized, industrialized political-content production. Moderate on the current scale of live deployment. What would raise confidence: independent confirmation beyond Correctiv, a provider statement on enforcement, a regulator's finding, or direct evidence of the volume of Alternita content already posted.

## Sources

- [The Irish Times — AI software that generates 'rage bait' developed by Germany's far-right AfD](https://www.irishtimes.com/world/europe/2026/07/08/ai-software-that-generates-rage-bait-developed-by-germanys-far-right-afd/) (Derek Scally, 8 July 2026)
- Correctiv — the originating undercover investigation into Alternita ([correctiv.org](https://correctiv.org/))
- [TechCrunch — Google will now disclose which ads are made with AI](https://techcrunch.com/2026/07/09/google-will-now-disclose-which-ads-are-made-with-ai/) (context: AI-content disclosure)
- [Pangram — AI Content Is Everywhere on Social Media, Especially LinkedIn](https://www.pangram.com/blog/ai-in-your-feed) (context: scale of AI-generated content)
- [Business Standard — Why AI-generated spam is becoming a bigger threat to online communities](https://www.business-standard.com/technology/artificial-intelligence/why-ai-generated-spam-is-becoming-a-bigger-threat-to-online-communities-126070800806_1.html) (context)

*Compiled via Aunoo news-intelligence. Volume, sentiment, and consensus signals are derived from Aunoo's tracking of the disinformation and influence-operations topic. This SITREP synthesizes open-source reporting and should be verified against the primary Correctiv investigation before use in decision-making. Confidence levels are stated throughout.*
