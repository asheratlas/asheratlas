# Asher "Ashi" Atlas

**From problem to working product.**

I'm a Senior Product Manager with eight years leading consumer platforms, directly building working products that span deterministic systems and evaluated AI products. I enter before the solution is clear, determine what should be built, and take it through validation and launch. The technology follows the problem — sometimes AI creates meaningful value; sometimes conventional software is the more reliable answer.

## Selected Commercial Proof

Team and company outcomes from commercial product leadership — not solo builds:

- Eight years in product leadership
- eMusic Live: concept to 100+ events
- Platform capacity scaled from 2K to 8K concurrent viewers before a major festival
- Multi-currency checkout expanded from 4 to 120+ currencies
- Search/discovery rebuild increased album purchases by 15% after a roughly 30% catalog loss

## Products I Built Directly

### Atlas Trade — Multi-Party Board Game Trading Platform

**[GitHub Repository](https://github.com/asheratlas/atlas-trade-portfolio)**

Board game communities run math trades — multi-party exchange events where circular trade loops are computed algorithmically. The incumbent tool's matching works, but its browse, assignment, and submit flows drive new participants away.

**Defining decision:** Fix broken UX flows, not the algorithm. TradeMaximizer (MIT, Chris Okasaki) owns matching; I built the surrounding product. The core trading workflow is deterministic and does not depend on AI.

- **Completed first live pilot:** ~40 participants, 732 items catalogued, with modern catalog browse and per-game assignment panels
- **Historical replay validation:** 78/79 trade loops verified; both systems produced trades for the same 26 users on the replay data — distinct from the live pilot outcome
- **Email-only authentication** replaced the BGG account requirement that blocked new participants

First live pilot complete; updating from pilot feedback before the next trade. An external organizer has joined as a design partner and is preparing to use the platform for future trades.

### Atlas Realms — AI Recommendation System for Group Board Game Decisions

**[Live Product](https://www.atlasrealms.com) · [GitHub Repository](https://github.com/asheratlas/atlas-realms-portfolio)**

Groups struggle to pick the right board game for a specific table — different players, time budgets, and experience levels. Atlas Realms turns a natural-language situation into a ranked shortlist with explainable reasons.

**Defining decision:** Models judge where language interpretation matters; code enforces every mechanical constraint. Validation rebuilt around casual players after early feedback overrepresented power users.

- **5–10s end-to-end latency**, down from 31–35s (~78% reduction through caching and architecture changes)
- **~$0.0012 per query** for the main user segment through cost engineering
- **100% consistency** on a 10-prompt regression suite (regression discipline, not a universal accuracy claim)

### Career Copilot — Evidence-First AI Career System

**[GitHub Repository](https://github.com/asheratlas/career-copilot-portfolio)**

PM job search mixes slow profile construction with fast per-role tailoring — and most AI resume tools hallucinate experience or silently drop gaps. Career Copilot separates knowledge building from per-job work and keeps every claim tied to approved evidence.

**Defining decision:** Verbatim evidence selection by ID with human approval — no hallucinated experience, no silent omissions, gap flags for every unsupported requirement.

- **13-JD regression set** with ~9–11/13 directional agreement on founder-labeled ground truth
- **11 completed model responses compared** on failure severity rather than benchmark averages
- **~$0.019 cold / ~$0.013 warm per tailoring**, down from ~$0.042 through model selection and caching

First external product manager actively testing in private beta.

Currently building: an AI-assisted invoicing pilot for an operating business — message capture, constrained extraction, deterministic tax math, human review before anything is issued.

## Products I Led at Commercial Scale

### eMusic Live — 0→1 Livestream Commerce Platform

Led concept-to-launch with real engineering teams, stakeholders, and operational workflows across 100+ live events. Owned product definition, user experience, payments integration, and ongoing optimization ahead of major festival launches.

### eMusic — Multi-Currency Subscription Platform Modernization

Shipped multi-currency checkout and led retention, monetization, and fraud prevention over multiple years in a commercial environment with real engineering constraints and stakeholder accountability.

## How I Work

**Decode the problem before choosing the solution.** Research the existing process and validate pain before defining what to build.

**Use models for judgment, code for invariants.** AI handles language understanding; deterministic code owns rules that must never fail.

**Evaluate failure severity, not averages.** Build regression suites around the failures that break user trust.

**Unit economics are architecture.** If model cost doesn't work at intended usage, the product design isn't finished.

**Validate with the right users against real data.** Power users and casual users diverge; mock data hides integration failures.

**Scope discipline saves projects.** Defend the core mission; change course when evidence wins.

## Currently

Senior product leadership day job. Independent products in active use and private beta. Open to senior product leadership opportunities and selective product-building collaborations where the scope and operating model are compatible.

## Contact

**Email:** [asher@asheratlas.com](mailto:asher@asheratlas.com)  
**LinkedIn:** [linkedin.com/in/asheratlas](https://linkedin.com/in/asheratlas)  
**Portfolio:** [https://www.asheratlas.com](https://www.asheratlas.com)  
**Location:** New York, NY
