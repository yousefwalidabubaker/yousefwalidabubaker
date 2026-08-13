# Wafeer — Product Backlog & Delivery Strategy

**A two-application product ecosystem designed to reduce food waste, recover value for stores, help customers access affordable food, and redirect eligible surplus safely before expiry.**

| Portfolio information | Detail |
| --- | --- |
| **Backlog owner / Product Owner** | Yousef AbuBaker |
| **Original project role** | Project Manager and major contributor |
| **Artifact status** | Product Owner portfolio sample; meaningfully updated August 2026 |
| **Backlog scale** | 5 epics · 12 ready stories · 7 Must · 4 Should · 1 Could |
| **Recognition** | Recipient of the **Potential to Scale Award** at the international TechBridge Hackathon in Amman, Jordan; developed under training and mentorship from Microsoft engineers |

> **Food-safety commitment:** Wafeer may redirect food to charity only while it is still unexpired, safe, edible, properly stored, and before its configured safety cutoff. Expired, unsafe, damaged, or recalled food is never offered for sale or donation.

[Open the complete GitHub Issue backlog](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues?q=is%3Aissue+state%3Aopen+Wafeer)

## Reviewer quick map

This page is the backlog index and product strategy. Every linked story is a trackable GitHub Issue.

| Product Owner evidence | Where to review it |
| --- | --- |
| Product vision, problem, users, and outcomes | Product strategy below |
| Epics and prioritization | Epic map and prioritized backlog |
| User stories | 12 linked GitHub Issues |
| Actionable tasks | Checkbox task list inside every Issue |
| Acceptance criteria | Testable criteria inside every Issue |
| Dependencies | Backlog dependency column and each Issue |
| Edge cases and test criteria | Every Issue plus the cross-cutting quality matrix |
| Sprint and release goals | Proposed delivery sequence |
| Metrics and product learning | Measurement framework and discovery plan |
| Ownership and recency | Portfolio integrity note |

## Product overview

Wafeer is built around two connected applications and one shared eligibility workflow.

| Product | Primary user | Job to be done |
| --- | --- | --- |
| **Wafeer** | Customers | Discover, understand, reserve, and collect eligible products approaching expiry at meaningful discounts |
| **Wafeer Partners** | Stores and retailers | Create a store, manage eligible inventory, reduce expiry risk, recover value, and coordinate safe charity handoffs |

The customer journey and partner workflow share one source of truth for inventory, eligibility, reservation, and handoff status. This prevents an item from being sold twice, donated twice, or offered after it becomes ineligible.

## Product strategy

### Vision

Make affordable food easier to access while giving stores a practical system to sell or responsibly redirect safe inventory before it expires.

### Problem

Stores lose revenue when action on time-sensitive inventory happens too late. Customers face rising food costs but may not trust near-expiry offers without clear information. Charities need reliable notice, safe eligibility rules, and realistic collection windows. Disconnected processes create waste, overselling, and unclear accountability.

### Target users

| User | Primary need | Product value |
| --- | --- | --- |
| Value-conscious customer | Find trustworthy discounted food quickly | Clear discovery, savings, availability, and pickup details |
| Store manager | Recover value before inventory becomes unsellable | Risk visibility, timely actions, and measurable outcomes |
| Inventory employee | Update time-sensitive products with low effort | Validated entry, clear status, and fewer manual steps |
| Charity coordinator | Receive safe, actionable offers before cutoff | Verified offers, collection deadlines, and handoff records |
| Platform administrator | Protect safety, trust, and data quality | Deterministic controls, auditability, and impact reporting |

### Product outcomes

1. **Prevent avoidable waste safely** by acting before eligibility ends.
2. **Improve affordable access** through transparent discounted offers.
3. **Recover store value** without creating operational complexity.
4. **Create accountable charity handoffs** for eligible, unexpired surplus.
5. **Learn from measurable behavior** instead of treating proposed metrics as completed results.

### Product guardrails and non-goals

- Safety rules always outrank revenue, recommendation, and growth goals.
- Smart features may recommend actions but cannot override eligibility controls.
- Wafeer does not sell or donate expired or unsafe food.
- Estimates are labeled; they are never presented as confirmed impact.
- The product does not make medical, nutritional, or food-safety guarantees.
- Sensitive customer, store, and charity information is visible only to authorized roles.

## Product principles

1. **Safety before savings**
2. **Clarity creates trust**
3. **Act before waste**
4. **Simple store operations**
5. **Human control over consequential recommendations**
6. **Measured impact with honest definitions**

## Core capabilities

### Wafeer customer application

- Browse eligible discounted inventory from verified stores
- **Smart Search** using intent, category, price, location, and availability
- Clear product, discount, expiry, storage, and pickup information
- Inventory-protected reservation and order confirmation
- **Smart Basket** suggestions based on budget, preferences, and eligible stock
- Timely order and collection notifications

### Wafeer Partners application

- Store onboarding and verification
- Validated inventory and eligibility management
- Deterministic sale, donation, and safety cutoffs
- **Smart Analysis** for expiry risk and recommended next actions
- Order preparation and collection status
- Verified charity offer, acceptance, and handoff workflow
- Revenue, savings, recovery, and impact reporting

## Discovery and validation plan

These are proposed validation activities, not claims of completed research.

| Risky assumption | Validation method | Decision rule |
| --- | --- | --- |
| Customers trust near-expiry offers when dates, storage, savings, and pickup are clear | Moderated prototype test and comprehension questions | If users cannot explain eligibility and pickup correctly, revise content before checkout work |
| Store employees can add and update inventory without slowing operations | Observe realistic product-entry and quantity-update tasks | If repeated errors or workarounds appear, simplify fields and automation before scaling |
| Charity partners can decide and collect within the safe window | Service-blueprint walkthrough and timed pilot scenario | If the handoff cannot finish before cutoff, change lead time, routing, or eligibility policy |
| Smart Search and Smart Basket produce helpful choices | Scenario-based relevance and constraint testing | If suggestions violate needs or lack useful alternatives, fall back to transparent rules |
| Smart Analysis improves action without weakening safety | Compare recommendations with curated inventory cases and manager judgment | If explanations or confidence are insufficient, keep human approval and deterministic fallbacks |

## Measurement framework

### North-star metric

**Eligible units successfully collected by customers or handed off to a verified charity before the configured safety cutoff.**

This combines the core customer, store, and impact outcomes while preserving a strict safety boundary.

| Outcome | Metric definition | Product decision supported |
| --- | --- | --- |
| Waste reduction | Confirmed eligible units and estimated weight completed before cutoff; excludes cancellations and uncollected offers | Which categories, stores, and interventions need earlier action |
| Customer affordability | Sum of original price minus paid price for completed quantities | Whether discovery and basket features create meaningful value |
| Store recovery | Revenue from completed near-expiry orders | Which discount and timing strategies recover value |
| Discovery quality | Search-to-product-view, zero-result rate, and search-to-order conversion | How to improve ranking, filters, and inventory coverage |
| Order reliability | Confirmed orders divided by initiated checkouts; cancellation and stock-conflict rate | Where reservation or fulfilment fails |
| Donation reliability | Collected quantity divided by accepted quantity before cutoff | Whether offer timing and handoff operations work |
| Safety and trust | Invalid listings blocked, eligibility overrides attempted, safety incidents, and support reports | Whether release must pause or controls must change |
| Product retention | Returning customer rate and active returning partner stores | Whether value is repeated rather than one-time |

All formulas, sources, owners, refresh times, and exclusions are documented in [US12](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/12). Proposed metrics are not presented as achieved results.

# Epic map

| Epic | Outcome | Stories |
| --- | --- | --- |
| **E1 — Store and safety foundation** | Verified partners can create valid, safely governed inventory | US01–US03 |
| **E2 — Customer discovery and trust** | Customers can find and understand eligible offers | US04–US06 |
| **E3 — Ordering and fulfilment** | Inventory is reserved once and collected through a clear workflow | US07, US11 |
| **E4 — Intelligent experiences** | Customers and stores receive explainable, constraint-aware recommendations | US08–US09 |
| **E5 — Safe donation and impact** | Eligible surplus reaches verified charities and outcomes are measured honestly | US10, US12 |

# Prioritized backlog

**Prioritization method:** MoSCoW, ordered first by safety and dependency, then by customer value and learning. Relative sizes are initial Product Owner hypotheses and must be re-estimated by the delivery team.

| Priority | Story | Epic | Product outcome | Size | Depends on |
| --- | --- | --- | --- | --- | --- |
| Must | [US01 — Create and verify a partner store](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/1) | E1 | Establish a trusted partner identity | M | None |
| Must | [US02 — Add eligible inventory](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/2) | E1 | Create accurate, actionable stock records | M | US01 |
| Must | [US03 — Enforce food safety and eligibility rules](https://github.com/yousefwalidabubaker/yousefwalidabuber/issues/3) | E1 | Block unsafe or invalid sale and donation paths | L | US02 |
| Must | [US04 — Browse discounted products](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/4) | E2 | Make eligible inventory discoverable | M | US02, US03 |
| Should | [US05 — Find products with Smart Search](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/5) | E2 | Reduce effort and zero-result searches | M | US04 |
| Must | [US06 — Review clear product and safety information](https://github.com/yousefwalidabubaker/yousefwalidabaker/issues/6) | E2 | Help customers make informed choices | S | US03, US04 |
| Must | [US07 — Reserve and place a pickup order](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/7) | E3 | Complete an order without overselling | L | US03, US06 |
| Should | [US08 — Build a value-optimized Smart Basket](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/8) | E4 | Create a useful basket within customer constraints | L | US05, US07 |
| Should | [US09 — Prioritize inventory with Smart Analysis](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/9) | E4 | Help stores take earlier, explainable action | L | US02, US03, US07 |
| Must | [US10 — Route eligible surplus to verified charities](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/10) | E5 | Complete accountable handoffs before cutoff | L | US02, US03 |
| Should | [US11 — Send timely order and safety notifications](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/11) | E3 | Reduce missed actions and collections | M | US07, US10 |
| Could | [US12 — Measure savings, recovery, and impact](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/12) | E5 | Turn outcomes into transparent decisions | M | US07, US10 |

> Each linked Issue contains the complete user story, acceptance criteria, task checklist, dependencies, edge cases, and test criteria.

## Priority rationale

- **Safety and eligibility come first:** no discovery, order, recommendation, or donation can be trusted without US01–US03.
- **The smallest customer value path comes next:** browsing, clear information, and inventory-protected ordering validate real demand before complex intelligence.
- **Donation is core, not dependent on AI:** US10 uses deterministic eligibility rules; US09 may recommend donation but is not a blocking dependency.
- **Smart features follow reliable data:** Smart Search, Smart Basket, and Smart Analysis become more useful after inventory and behavioral events exist.
- **Reporting follows stable event definitions:** US12 measures confirmed outcomes only after order and handoff states are trustworthy.

# Proposed delivery sequence

This is a planning hypothesis, not a fixed promise. Scope should be replanned using team capacity, technical discovery, and sprint evidence.

| Sequence | Sprint goal | Stories | Exit evidence |
| --- | --- | --- | --- |
| Sprint 0 | Validate users, workflows, safety rules, and event definitions | Discovery activities | Agreed journey, eligibility states, major risks, and measurable hypotheses |
| Sprint 1 | Allow verified stores to create safely governed inventory | US01, US02, US03 | Invalid inventory is blocked and every state change is auditable |
| Sprint 2 | Help customers discover and understand eligible offers | US04, US06 | A customer can find an eligible item and explain price, expiry, and pickup |
| Sprint 3 | Complete reliable orders and safe charity handoffs | US07, US10 | No double allocation; completed orders and collections have matching records |
| Sprint 4 | Improve discovery and timely action | US05, US11 | Search failures are measurable and critical reminders reach the correct role |
| Sprint 5 | Add explainable intelligence | US08, US09 | Suggestions respect constraints, expose limitations, and keep human control |
| Sprint 6 | Measure outcomes and guide iteration | US12 | Dashboard totals reconcile to source events and estimates are clearly labeled |

## Release cuts

| Release | Included value | Stories |
| --- | --- | --- |
| **MVP — Safe marketplace** | Verified supply, trusted discovery, and protected ordering | US01–US04, US06, US07 |
| **MVP impact extension** | Deterministic, accountable charity handoff | US10 |
| **Reliability and discovery** | Better search and action timing | US05, US11 |
| **Intelligence** | Constraint-aware customer and store recommendations | US08, US09 |
| **Learning** | Transparent product and impact reporting | US12 |

# Quality and acceptance strategy

Issue-level tests appear in every story. The matrix below covers risks that cross multiple stories.

| Scenario | Product rule | Test oracle |
| --- | --- | --- |
| Item crosses the expiry or safety boundary | Remove it from sale and donation automatically | It cannot be discovered, reserved, accepted, or reactivated without authorized review |
| Two users request the final unit | Reserve inventory atomically | Only one confirmation succeeds and total allocation never exceeds stock |
| Price or stock changes while a page is open | Revalidate before basket and checkout actions | The customer sees the current value and cannot confirm stale inventory |
| Customer reservation overlaps a charity offer | Use one allocation ledger | Sale plus donation allocation never exceeds available quantity |
| Charity misses collection | Enforce the cutoff automatically | Uncollected quantity becomes blocked and is excluded from confirmed impact |
| Smart feature has sparse or conflicting data | Explain limitations and use a safe fallback | No false certainty, forbidden item, or automatic safety override appears |
| The same event is received twice | Make notifications and analytics idempotent | One user-facing message and one counted outcome are created |
| Data is delayed, cancelled, or estimated | Preserve event status and metric definitions | Reports reconcile to sources and estimates remain visibly separate |

## Definition of Ready

A story is Ready only when:

- The user, problem, outcome, and priority are clear.
- Acceptance criteria are testable.
- Dependencies, data needs, and safety implications are identified.
- Important edge cases and test criteria are documented.
- Design or policy questions that block estimation are resolved.
- The delivery team can estimate the work.

## Definition of Done

A story is Done only when:

- All acceptance criteria pass and important edge cases are tested.
- Safety, privacy, accessibility, and authorization requirements pass.
- Analytics events and failure states are verified.
- The experience works across supported screen sizes.
- Documentation and operational guidance are updated.
- No critical defect remains open.
- The Product Owner reviews the evidence and accepts the story.

# Key product risks

| Risk | Early signal | Product response |
| --- | --- | --- |
| Customers misunderstand near-expiry food | Confusion in usability tests or repeated support questions | Make date, safety, storage, and pickup information explicit before checkout |
| Unsafe or invalid inventory enters a workflow | Eligibility override attempts or inconsistent statuses | Deterministic blocks, audit records, authorized review, and release guardrails |
| Inventory is sold or donated twice | Reservation conflicts or negative quantity | Atomic allocation, final validation, timeout release, and reconciliation alerts |
| Store work becomes too complicated | Incomplete listings or off-platform workarounds | Reduce fields, integrate updates, and prioritize exceptions by urgency |
| Charity offers arrive too late | Low acceptance or missed collection before cutoff | Earlier triggers, realistic collection windows, and fallback routing |
| Smart recommendations reduce trust | High replacement/rejection or unexplained output | Explain inputs, expose uncertainty, preserve manual approval, and keep rules-based fallback |
| Impact is overstated | Dashboard cannot reconcile to source records | Document formulas, separate estimates, and count only confirmed outcomes |

# Portfolio integrity and ownership

- Wafeer is an original team hackathon product developed in 2026.
- Yousef AbuBaker's original role was **Project Manager and major contributor**; this backlog presents his Product Owner thinking and contribution.
- This portfolio artifact was newly structured and meaningfully updated in **August 2026**.
- It does not claim that the full team build was completed by one person.
- Proposed stories, experiments, release plans, estimates, and metrics are clearly distinguished from completed product results.
- Recognition and mentorship are stated specifically; no employment relationship with Microsoft is implied.
