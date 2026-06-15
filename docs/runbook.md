# Runbook — Event-Driven Situation Report (Aunoo)

**Purpose:** a repeatable process for turning a breaking AI/tech event into a sourced situation report plus collateral (LinkedIn bulletin, client PDF, web/app page), using Aunoo news-intelligence and supporting skills.
**Owner:** Foresight / intelligence desk
**Reference build:** "US Export-Control Suspension of Anthropic's Fable 5 / Mythos 5," 14 June 2026.
**Time to first draft:** ~30–45 min once scope is set.

---

## 1. Tooling inventory

### Aunoo news-intelligence (MCP)
| Tool | Use in this process |
|---|---|
| `list_capabilities` | Confirm scope, topic IDs, and named playbooks at session start |
| `get_world_state` | Topic baseline: current entities, leadership, ongoing situations (use over training knowledge) |
| `forecast_topic_trajectory` | Lifecycle phase + growth rate (logistic fit, r²); is the story climbing or cresting |
| `forecast_sentiment_inflection` | Sentiment level + CUSUM change-point; is the mood about to flip |
| `get_consensus` | Cross-source consensus: strength, evidence quality, % agreement, sentiment split, optimistic/pessimistic outliers, milestone forecast |
| `get_horizons` | Three-Horizons scenarios (H1/H2/H3) when cached |
| `search_news` | Semantic search for the event and its history |
| `search_articles_by_keywords` | Exact-phrase fallback |
| `get_article_full` | Full text of a specific article (no truncation) — use for key claims |
| `fetch_related_to_article` | Pull the cluster of coverage around a seed article (corroboration breadth) |
| `get_topic_articles` + `sampling_pipeline` | **Bias control.** Pipelines: `high_factuality`, `bias_neutral`, `diverse`, `balanced_topics`, `latest`, `newsletter` |
| `get_entity_wiki` | Entity background when available |

### Supporting skills / tools
| Tool | Use |
|---|---|
| `humanize` MCP — `detect_ai_tells`, `compute_readability` | Quality gate: scan prose for AI tells, em-dash density, readability |
| `humanize` MCP — `deep_scan`, `classify_verdict` | Deeper "faux-insightful voice" scan (requires Ollama; skip if `list_providers` shows it unconfigured) |
| `identify-ai-tells` skill | Wraps the detector into a read-only diagnostic |
| `pdf` skill + WeasyPrint | HTML→PDF for the client bulletin (`pip install weasyprint --break-system-packages`) |
| Task list (`TaskCreate`/`TaskUpdate`) | Track the phases below |
| `present_files` | Deliver outputs to the user |

---

## 2. The process (8 phases)

### Phase 0 — Scope
- Confirm the event, audience, and which deliverables are needed (SITREP, LinkedIn, client PDF, web page).
- Call `list_capabilities`; note the topic ID (here: 1 = AI & Machine Learning).

### Phase 1 — Foresight baseline (run before the event detail)
Pull, in parallel, for the topic:
- `get_world_state` — situational baseline.
- `forecast_topic_trajectory` — phase + growth.
- `forecast_sentiment_inflection` — mood + inflection risk.
- `get_consensus` — quantified cross-source read and forecast.
This gives the analytic frame the event will be slotted into ("where does this sit in the foresight").

### Phase 2 — Event gathering
- `search_news` for the event; `get_article_full` on the 3–5 highest-relevance items.
- `fetch_related_to_article` on the strongest article to map the coverage cluster.
- Identify the **primary source** (company statement, regulator notice) and pull it.
- Build a timeline from datelines; note any pre-event triggers (e.g., the public jailbreak that preceded the order).

### Phase 3 — Bias control (mandatory)
- Re-pull with `get_topic_articles(sampling_pipeline="high_factuality")` (and/or `bias_neutral`).
- Confirm each load-bearing claim appears across **multiple regions and outlets**, not one market.
- **Fix the input, don't caveat the output:** if coverage skews to one region, rebalance the source set rather than writing a disclaimer. (Any note about feed composition stays internal — never in customer-facing collateral.)
- Tag each key claim: primary / multi-source / single-source.

### Phase 4 — Draft in intelligence register
- Structure: **BLUF → What happened → Key facts → Timeline → Anthropic/actor position → Implications → Significance → Consensus & forecast → Outlook → Source assessment + Confidence → Sources.**
- Voice: declarative, assessment-led. End analytic sections with an **Assessment** line and a **Confidence** rating.
- **Sourcing discipline:** separate what is *cited* from what is *inferred*. State causation only when a source asserts it; otherwise label the link "reported sequence" or "inferred."

### Phase 5 — Quality gates
- `detect_ai_tells` + `compute_readability` on the prose. Target: **0 high-signal tells**, low em-dash density, sentence length appropriate to register.
- Watch for register slop the regex misses: narrative framing ("the story read as…"), antithesis ("no longer X, it is Y"), jargon-as-drama ("textbook accelerant"). Rewrite these by hand.
- **Correctness review:** re-query Aunoo for updates and challenge the strongest claims (this is how the public jailbreak and the cited-vs-inferred cause were caught). Verify the primary source.

### Phase 6 — Collateral
- **SITREP** (master): markdown, full detail, internal confidence notes.
- **LinkedIn bulletin:** punchier register is acceptable for this channel.
- **Client PDF (Wiley):** HTML built to the house style, rendered with WeasyPrint. Use flexbox (WeasyPrint's CSS-grid support is incomplete). Visual key-facts cards + timeline cards.
- **Web/app page:** responsive HTML, same facts, customer-safe (no internal caveats).

### Phase 7 — Branding
- Aunoo palette: pink `#ce5e9c`, light mark `#ecedf2`; Wiley house style: navy `#0f172a` + pink `#d6346c`.
- Inline the logo SVG so each file stays self-contained.

### Phase 8 — Internal vs. customer-facing split
- Internal-only: feed-composition/bias notes, raw confidence hedges, methodology asides.
- Customer-facing: balanced framing, primary-sourced facts, no exposure of data-provider limitations.

---

## 3. Conventions

**Confidence ratings.** State explicitly (High / Moderate / Low) and tie to evidence: primary-sourced and multi-region = High; single-source or contested causation = Moderate; flag what would raise it (e.g., release of the regulator's technical justification).

**Cited vs. inferred.** Never let timing imply causation. "The order followed the jailbreak" (sequence) ≠ "the jailbreak caused the order" (claim). If no source asserts the link, say it is inferred.

**Sentiment numbers.** Use Aunoo's figures verbatim (e.g., consensus 70/15/15) rather than estimating.

**AI-tells gate is non-negotiable.** No deliverable ships without a `detect_ai_tells` pass and a manual register check.

**House writing style (all channels, including LinkedIn).** Write as a human analyst in measured, connected prose. Do not use punchy marketing/infomercial register: no staccato one-line drama ("The jailbreak was real and public."), no "X, not Y" headlines, no rule-of-three escalation, no arrow/"from X to Y" constructions, no faux-insight subtitles, no em-dash overuse. The detector misses most of these, so a manual register read is required in addition to it. See `WRITING_STYLE_NOTE.md`.

---

## 4. Reusable prompt seed

> Build an event SITREP on [EVENT] using Aunoo (topic_id [N]). Phase 1: world_state, trajectory, sentiment_inflection, consensus. Phase 2: search_news + get_article_full on top items + fetch_related + primary source. Phase 3: re-pull high_factuality sample, corroborate across regions, tag claims. Phase 4: draft in intel register (BLUF, key facts, timeline, implications, significance, consensus/forecast, outlook, source assessment + confidence). Phase 5: detect_ai_tells + correctness re-query. Phase 6: produce SITREP, LinkedIn, Wiley PDF (WeasyPrint), web page. Keep bias/feed notes internal only.

---

*Maintained by the foresight desk. Update when Aunoo tool names, sampling pipelines, or the Wiley house template change.*
