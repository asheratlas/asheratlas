# Asher "Ashi" Atlas

**I build AI products designed to survive unit economics.**

Product manager with hands-on experience shipping a consumer-facing AI decision support tool from zero to open beta. I make real decisions about when to use an LLM, when JavaScript is the right answer, and how to build trust between users and systems that make recommendations.

---

## What I've Built

**[Atlas Realms](https://www.atlasrealms.com)** — An AI-powered decision support tool that helps groups find the right board game for their specific situation. Not a filter. Not a ranked list. A system that understands social context: who's at the table, how they want to feel, what kind of evening they're trying to have.

The architecture is a hybrid: LLMs handle intent extraction and result explanation; deterministic JavaScript owns filtering, scoring, and explainability; pre-computed semantic embeddings (Gemini Embedding 001, 768-dim, stored in Cloudflare KV) extend vocabulary coverage for language the synonym dictionary can't reach — without adding LLM cost. Filtering, scoring, and ranking are fully deterministic. Traceable reasons for every recommendation.

- **5–10s end-to-end latency** (down from 31–35s)
- **~$0.0012 per query** mid-tier (vs ~$0.08–0.40 for a pure LLM approach)
- **100% on 10-prompt validation suite** (up from 62.5%) — deterministic scoring pipeline; the suite is small, consistency is an ongoing engineering discipline not a fixed ceiling
- **1,000+ games** enriched across 15 taxonomy dimensions using a 3-model consensus pipeline

---

## This Repository

Architecture documentation, scoring logic, product decisions, and production code artifacts — without the proprietary data and infrastructure. Everything in this repo is designed to be read, not run.

| Document | What it covers |
|---|---|
| [README](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/README.md) | Architecture overview and real performance numbers |
| [ARCHITECTURE.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/ARCHITECTURE.md) | Full pipeline: all 8 nodes, filtering logic, design decisions |
| [ADR_hybrid_llm_architecture.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/ADR_hybrid_llm_architecture.md) | Why hybrid beats pure LLM: unit economics, consistency, explainability |
| [SCORING_SYSTEM.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/SCORING_SYSTEM.md) | How 14+ dimensions combine to rank results |
| [PRODUCT_DECISIONS.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/PRODUCT_DECISIONS.md) | The product thinking: assumptions, tests, reversals, and what changed |
| [ENRICHMENT_PIPELINE.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/ENRICHMENT_PIPELINE.md) | 3-model consensus pipeline for enriching a 1,100-item catalog |
| [analytics/README.md](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/analytics/README.md) | PostHog + GA4 dual analytics tracking — async initialization, UTM attribution, session-level event modeling (standalone Framer pattern) |
| [workers/flowise-proxy.js](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/workers/flowise-proxy.js) | Cloudflare Worker: CORS enforcement, routes requests to the Flowise pipeline |
| [workers/catalog-cache.js](https://github.com/asheratlas/atlas-realms-portfolio/blob/main/workers/catalog-cache.js) | Cloudflare Worker: KV-backed game catalog cache, cron-triggered refresh |

---

## How I Think About AI Products

**Use LLMs for what they're uniquely good at.** Natural language understanding, fuzzy intent extraction, filling gaps where structured data doesn't exist. Not for sorting, filtering, or explaining results — those jobs belong to deterministic code.

**Design for consistency from the start.** A recommendation system that returns different results for the same input is a product that users can't trust. Consistency is an engineering constraint, not a nice-to-have.

**Unit economics are a product constraint.** If the cost per query doesn't work at the scale you're targeting, the architecture is wrong — not the pricing. Build with real numbers from the beginning.

**Real users break things that structured tests don't.** The most valuable feedback I've collected came from watching people use the product in ways I never designed for. Ship to real users as early as possible, with the right instrumentation to learn from what they do.

---

## Background

Building Atlas Realms allowed me to combine five years of board game domain expertise (800+ sales, 3,000+ titles catalogued) with the product management fundamentals I developed at TriPlay — a digital music platform where I designed save cancellation journeys, recommendation systems, multi-currency checkout flows, and artist engagement features that drove measurable behavior change. It was also a deliberate choice to develop hands-on AI product skills by shipping something real, with real users, real costs, and real decisions about trust, explainability, and what "correct" means when the user is a group of people negotiating a game night.

---

## Contact

**Email:** asher@asheratlas.com
**LinkedIn:** [linkedin.com/in/asheratlas](https://linkedin.com/in/asheratlas)  
**Portfolio Site:** [asheratlas.com](https://www.asheratlas.com)
**Live product:** [atlasrealms.com](https://www.atlasrealms.com)  
**Location:** New York, NY
