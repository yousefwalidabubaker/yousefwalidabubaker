# Wafeer Product Backlog

This is the Product Owner backlog I created from Wafeer, a team project I worked on as Project Manager during the Global TechBridge Hackathon in Amman.

I wanted this backlog to show how I think about a product, not only list features. It explains the problem, the people we are building for, what I would validate first, how I chose priorities, and what the team would need to deliver each story.

| Project detail | Information |
| --- | --- |
| **Backlog owner** | Yousef AbuBaker |
| **My role in the original project** | Project Manager and major contributor |
| **Last updated** | August 2026 |
| **Backlog size** | 5 epics and 12 user stories |
| **Award** | Wafeer received the Potential to Scale Award at the Global TechBridge Hackathon in Amman, 2026 |
| **Microsoft involvement** | The event was technically supported by Microsoft, and our team received training and mentorship from Microsoft engineers |

> **Important safety rule:** Food can only be sold or offered to charity while it is still safe, edible, properly stored, unexpired, and inside the allowed time window. Expired, damaged, recalled, or unsafe food is never sold or donated.

[View all Wafeer issues on GitHub](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues?q=is%3Aissue+state%3Aopen+Wafeer)

## What is included

* Five clear epics
* Twelve linked user stories
* Priorities and dependencies
* Acceptance criteria for every story
* Task checklists
* Edge cases and test criteria
* A suggested sprint order
* Product metrics and risks
* A Definition of Ready and Definition of Done

Each story is a separate GitHub Issue, so a team could discuss it, estimate it, assign it, and track it.

## What Wafeer does

Wafeer has two connected applications.

| Application | Who uses it | What it does |
| --- | --- | --- |
| **Wafeer** | Customers | Helps people find safe products that are approaching expiry at lower prices |
| **Wafeer Partners** | Stores and retailers | Helps stores manage eligible products, reduce waste, recover value, and coordinate safe charity handoffs |

A store adds its eligible inventory through Wafeer Partners. Customers can then find and reserve available products through Wafeer. If an item is not sold but is still safe and within its valid date, the store can offer it to a verified charity before the safety cutoff.

The two applications must use the same inventory record. This is important because the same unit should never be sold twice or offered to a customer and a charity at the same time.

## My role in the original project

I worked as the Project Manager for Wafeer. My main responsibilities were:

* Helping the team define the problem and target users
* Shaping the value proposition for customers, stores, and charities
* Deciding which features mattered most for the hackathon
* Keeping the business, design, and technical work connected
* Making sure both applications felt like one product
* Leading the final pitch and product demo

This backlog builds on the product thinking I contributed during the project. It does not claim that I built the entire team project alone.

## Product goal

Help stores take action on time sensitive inventory before it becomes waste, while giving customers a simple and trustworthy way to save money on safe food.

## The problem

Stores often notice products too late, after there is little time left to discount, sell, or responsibly redirect them. That creates lost revenue and unnecessary food waste.

Customers want lower prices, but they need clear information before trusting products that are close to expiry. Charities also need enough time to review an offer and collect it safely.

Wafeer connects these three sides through one inventory and eligibility process.

## Who we are building for

| User | What they need |
| --- | --- |
| Customer | Affordable products, clear dates, real availability, and simple pickup |
| Store manager | A way to recover value and see which products need attention |
| Inventory employee | Fast product entry and clear validation |
| Charity coordinator | Safe offers with enough information and time to collect |
| Platform administrator | Strong safety rules, access control, and reliable reporting |

## Questions I would validate first

These are questions I would test before committing the full team to every feature.

| Question | How I would test it | What I would learn |
| --- | --- | --- |
| Do customers understand and trust the product information? | Show a prototype and ask customers to explain the date, discount, and pickup process | Whether the wording and layout are clear enough |
| Can store employees add products without slowing their work? | Observe them completing realistic inventory tasks | Which fields or steps should be simplified |
| Can a charity accept and collect an offer before the cutoff? | Walk through a timed handoff with a store and charity | Whether the offer needs to be sent earlier |
| Are Smart Search and Smart Basket suggestions actually useful? | Test common shopping scenarios with different budgets and needs | Whether the suggestions save time or create confusion |
| Can Smart Analysis make useful suggestions without weakening safety? | Compare its suggestions with known inventory cases and manager decisions | When a simple rule or human decision is better |

## How I prioritized the backlog

I used MoSCoW priorities, but I did not start with the most exciting features.

The first stories create verified stores, accurate inventory, and strict safety rules. Without those foundations, search results, orders, donations, and analytics would not be trustworthy.

The next group creates the smallest complete customer journey: browse a product, understand it, and place a pickup order without overselling stock.

Smart Search, Smart Basket, and Smart Analysis come later because they need reliable inventory and real usage data. The donation flow is a core feature, so it works with clear safety rules even if Smart Analysis is not available.

## Main product metric

The main metric I would watch is:

**The number of eligible units collected by customers or handed to a verified charity before the safety cutoff.**

This connects the customer benefit, the store benefit, and the waste reduction goal. It only counts completed outcomes, not products that were listed or offered but never collected.

## Supporting metrics

| Area | Metric |
| --- | --- |
| Customer savings | Difference between the original price and paid price for completed orders |
| Store recovery | Revenue from completed orders for products approaching expiry |
| Search quality | Search success, searches with no results, and search to order conversion |
| Order reliability | Checkout success, cancellations, and stock conflicts |
| Donation reliability | Quantity collected compared with quantity accepted |
| Safety | Invalid items blocked, override attempts, and reported incidents |
| Repeat use | Returning customers and active returning partner stores |

These are proposed metrics. They are not being presented as results already achieved by the project.

# Epic map

| Epic | Goal | Stories |
| --- | --- | --- |
| **E1: Store and safety foundation** | Create trusted stores and safely managed inventory | US01 to US03 |
| **E2: Customer discovery and trust** | Help customers find and understand eligible products | US04 to US06 |
| **E3: Orders and fulfilment** | Reserve stock once and complete a clear pickup journey | US07 and US11 |
| **E4: Smart features** | Give customers and stores useful recommendations | US08 and US09 |
| **E5: Donation and impact** | Complete safe charity handoffs and measure outcomes honestly | US10 and US12 |

# Prioritized backlog

| Priority | Story | Epic | Depends on |
| --- | --- | --- | --- |
| Must | [US01: Create and verify a partner store](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/1) | E1 | None |
| Must | [US02: Add eligible inventory](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/2) | E1 | US01 |
| Must | [US03: Enforce food safety and eligibility rules](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/3) | E1 | US02 |
| Must | [US04: Browse discounted products](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/4) | E2 | US02 and US03 |
| Should | [US05: Find products with Smart Search](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/5) | E2 | US04 |
| Must | [US06: Review clear product and safety information](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/6) | E2 | US03 and US04 |
| Must | [US07: Reserve and place a pickup order](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/7) | E3 | US03 and US06 |
| Should | [US08: Build a Smart Basket within a budget](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/8) | E4 | US05 and US07 |
| Should | [US09: Prioritize inventory with Smart Analysis](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/9) | E4 | US02, US03, and US07 |
| Must | [US10: Route eligible surplus to verified charities](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/10) | E5 | US02 and US03 |
| Should | [US11: Send useful order and safety notifications](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/11) | E3 | US07 and US10 |
| Could | [US12: Measure savings, recovery, and impact](https://github.com/yousefwalidabubaker/yousefwalidabubaker/issues/12) | E5 | US07 and US10 |

Every linked Issue contains the full user story, acceptance criteria, task checklist, edge cases, test criteria, and dependencies.

# Suggested delivery order

This is a starting point for planning. I would still ask the team to estimate the work and adjust the scope based on what we learn in each sprint.

| Sprint | Goal | Stories |
| --- | --- | --- |
| Sprint 0 | Validate the main workflows, safety rules, and product assumptions | Discovery work |
| Sprint 1 | Let verified stores create safe and accurate inventory | US01, US02, and US03 |
| Sprint 2 | Let customers find and understand eligible products | US04 and US06 |
| Sprint 3 | Complete reliable orders and safe charity handoffs | US07 and US10 |
| Sprint 4 | Improve search and send timely updates | US05 and US11 |
| Sprint 5 | Add Smart Basket and Smart Analysis | US08 and US09 |
| Sprint 6 | Add transparent product and impact reporting | US12 |

## First release

The first usable release would include US01, US02, US03, US04, US06, and US07.

That gives the team one complete journey:

1. A verified store adds a valid product.
2. The platform checks its eligibility.
3. A customer finds and understands the product.
4. The customer places a pickup order.
5. The system reserves the stock so it cannot be sold twice.

US10 can then add the safe charity path using the same inventory and safety rules.

## Important cases the whole product must handle

| Situation | Expected result |
| --- | --- |
| An item passes its safety cutoff | It disappears from sale and donation immediately |
| Two customers try to reserve the final unit | Only one order succeeds |
| Price or quantity changes while a customer is viewing the product | The latest information appears before confirmation |
| A customer order and charity offer request the same stock | The total reserved quantity never exceeds available stock |
| A charity misses the collection deadline | The item is blocked and is not counted as a completed donation |
| A smart feature does not have enough data | It explains the limitation and uses a safe fallback |
| The same notification event arrives twice | The user receives one message and analytics count one event |

## Definition of Ready

A story is ready when:

* The user and problem are clear
* The priority and dependencies are known
* Acceptance criteria can be tested
* Important safety and data questions are answered
* The team has enough information to estimate the work

## Definition of Done

A story is done when:

* The acceptance criteria pass
* Important edge cases are tested
* Safety, privacy, access, and accessibility checks pass
* Error states and analytics events work
* The relevant documentation is updated
* The Product Owner reviews the result and accepts it

## Main risks

| Risk | How I would respond |
| --- | --- |
| Customers do not trust products close to expiry | Make the date, storage, safety, discount, and pickup information clear before checkout |
| An unsafe item enters the system | Use automatic blocks, audit records, and an authorized review process |
| The same item is sold or donated twice | Use one inventory allocation record and check it again before confirmation |
| Store employees find the process too slow | Reduce unnecessary fields and focus alerts on items that need action |
| Charity offers arrive too late | Send offers earlier and use realistic collection windows |
| Smart suggestions are not useful | Explain why an item was suggested and keep human control |
| Reports exaggerate impact | Count completed outcomes only and label estimates clearly |

## Ownership note

Wafeer was a team project. My role was Project Manager, and I was a major contributor to the product direction, feature priorities, coordination, pitch, and demo.

This backlog is my Product Owner portfolio sample based on that real experience. It was created and meaningfully updated in August 2026. It does not claim that I completed the entire team project alone.
