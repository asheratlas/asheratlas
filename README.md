# Asher "Ashi" Atlas

**I build AI products designed to survive unit economics.**

Product leader with hands-on experience shipping a consumer-facing AI decision support tool from zero to open beta. I make real decisions about when to use an LLM, when JavaScript is the right answer, and how to build trust between users and systems that make recommendations.

---

## What I've Built

**[Atlas Realms](https://www.atlasrealms.com)** — An AI-powered decision support tool that helps groups find the right board game for their specific situation. Not a filter. Not a ranked list. A system that understands social context: who's at the table, how they want to feel, what kind of evening they're trying to have.

The architecture is a hybrid: two LLMs handling what only language models can do (intent extraction and semantic enrichment), with deterministic JavaScript owning filtering, scoring, and explainability. Same query, same results, every time. Traceable reasons for every recommendation.

- **5–10s end-to-end latency** (down from 31–35s)
- **~$0.0004 per query** (vs ~$0.08–0.40 for a pure LLM approach)
- **100% consistency** on 10-prompt validation suite
- **1,000+ games** enriched across 15 taxonomy dimensions using a 3-model consensus pipeline

---

## This Repository

Architecture documentation, scoring logic, product decisions, and production code artifacts — without the proprietary data and infrastructure. Everything in this repo is designed to be read, not run.

| Document | What it covers |
|---|---|
| [README](./README.md) | Architecture overview and real performance numbers |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Full pipeline: all 7 nodes, filtering logic, design decisions |
| [ADR_hybrid_llm_architecture.md](./ADR_hybrid_llm_architecture.md) | Why hybrid beats pure LLM: unit economics, consistency, explainability |
| [SCORING_SYSTEM.md](./SCORING_SYSTEM.md) | How 14+ dimensions combine to rank results |
| [PRODUCT_DECISIONS.md](./PRODUCT_DECISIONS.md) | The product thinking: assumptions, tests, reversals, and what changed |
| [ENRICHMENT_PIPELINE.md](./ENRICHMENT_PIPELINE.md) | 3-model consensus pipeline for enriching a 1,100-item catalog |
| [analytics/README.md](./analytics/README.md) | PostHog + GA4 dual tracking with UTM attribution in Framer |
| [workers/api-proxy-worker.js](./workers/api-proxy-worker.js) | Cloudflare Worker: CORS proxy + KV-backed catalog cache |

---

## How I Think About AI Products

**Use LLMs for what they're uniquely good at.** Natural language understanding, fuzzy intent extraction, filling gaps where structured data doesn't exist. Not for sorting, filtering, or explaining results — those jobs belong to deterministic code.

**Design for consistency from the start.** A recommendation system that returns different results for the same input is a product that users can't trust. Consistency is an engineering constraint, not a nice-to-have.

**Unit economics are a product constraint.** If the cost per query doesn't work at the scale you're targeting, the architecture is wrong — not the pricing. Build with real numbers from the beginning.

**Real users break things that structured tests don't.** The most valuable feedback I've collected came from watching people use the product in ways I never designed for. Ship to real users as early as possible, with the right instrumentation to learn from what they do.

---

## Background

Building Atlas Realms allowed me to combine five years of board game domain expertise (800+ sales, 3,000+ titles catalogued) with the product management fundamentals I developed at eMusic — a digital music platform where I designed save cancellation journeys, recommendation systems, multi-currency checkout flows, and artist engagement features that drove measurable behavior change. It was also a deliberate choice to develop hands-on AI product skills by shipping something real, with real users, real costs, and real decisions about trust, explainability, and what "correct" means when the user is a group of people negotiating a game night.

---

## Contact

**Email:** atlas.ash8@gmail.com  
**LinkedIn:** [linkedin.com/in/asheratlas](https://linkedin.com/in/asheratlas)  
**Live product:** [atlasrealms.com](https://www.atlasrealms.com)  
**Location:** New York, NY
