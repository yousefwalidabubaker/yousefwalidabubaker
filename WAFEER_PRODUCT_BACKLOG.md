# Wafeer Product Backlog

**An AI assisted marketplace designed to reduce food waste, recover value for stores, and help customers access safe food at lower prices**

> **Recognition:** Award winner at the international TechBridge Hackathon in Amman, Jordan, developed under training and mentorship from Microsoft engineers.

**Product role:** Yousef AbuBaker, Project Manager

## Product overview

Wafeer is a connected two application ecosystem built around one goal: helping safe food reach people before it becomes waste.

| Product | Primary user | Purpose |
| --- | --- | --- |
| **Wafeer** | Customers | Discover and purchase safe products approaching their expiry date at significantly reduced prices |
| **Wafeer Partners** | Stores and retailers | Create a store, manage eligible inventory, apply timely discounts, analyze expiry risk, and coordinate responsible donations |

When an eligible food item approaches the end of its sellable window but remains safe, edible, and within its valid expiry date, Wafeer Partners can redirect it to a verified charity. Expired or unsafe food is never offered for sale or donation.

## My role

As Project Manager, I helped turn the initial problem into a focused product concept. My responsibilities included:

* Defining target users, the core problem, and the value proposition
* Prioritizing features around customer value, store usability, food safety, and social impact
* Coordinating the business, design, and technical workstreams
* Aligning both applications into one connected product journey
* Leading the final pitch and product demonstration
* Presenting Wafeer's growth potential to mentors and judges

## Product vision

Make affordable food easier to access while giving stores a practical system to sell or responsibly redirect safe inventory before it expires.

## The problem

Stores lose revenue when products approach their expiry dates, while customers face rising food costs and charities need reliable access to safe donations. Existing inventory workflows often identify the problem too late.

Wafeer connects customer demand, store inventory decisions, intelligent discovery, and responsible redistribution in one product system.

## Target users

| User | Need |
| --- | --- |
| Value conscious customer | Find safe products at meaningful discounts without a complicated search |
| Store manager | Recover value from inventory before it becomes unsellable |
| Inventory employee | Add products and make time sensitive updates quickly |
| Charity coordinator | Receive clear information about safe, eligible donations before expiry |
| Platform administrator | Protect trust, monitor activity, and measure impact |

## Product principles

1. **Safety before savings:** Every sale and donation must meet food safety and validity rules.
2. **Clarity builds trust:** Customers see the price, discount, expiry information, and collection details before committing.
3. **Act before waste:** Stores receive useful warnings and recommendations early enough to take action.
4. **Simple store operations:** Wafeer Partners reduces work instead of adding another complicated process.
5. **Measurable impact:** Revenue recovered, customer savings, successful donations, and food diverted from waste remain visible.

## Core features

### Wafeer customer application

* **Smart Search:** Finds relevant products using customer intent, category, price, location, and remaining shelf life
* **Smart Basket:** Suggests useful combinations of available discounted products based on needs and budget
* Clear original price, discounted price, expiry information, availability, and pickup details
* Product reservation or purchase with inventory protection
* Notifications for confirmed orders and collection windows

### Wafeer Partners application

* Store creation and onboarding
* Product and inventory management
* Rules for discounts and eligibility
* **Smart Analysis:** Highlights expiry risk, recommends timely actions, and tracks sales, savings, and waste reduction
* Safe donation workflow for products that remain edible and valid but are approaching the end of their eligible window
* Handoff records for verified charity partners

## Proposed success metrics

These metrics define how the product should be evaluated. They are measurement goals, not completed results.

| Goal | Metric |
| --- | --- |
| Reduce food waste | Units and estimated weight redirected from waste |
| Recover store value | Revenue recovered from near expiry inventory |
| Help customers save | Total and average savings per completed basket |
| Improve discovery | Search to product view and search to purchase conversion |
| Encourage repeat use | Returning customers and repeat store activity |
| Support responsible donation | Safe donation handoffs completed before expiry |
| Protect trust | Safety reports, cancellations, and invalid listings |

# Prioritized backlog

| Priority | ID | Epic | User story | Status | Depends on |
| --- | --- | --- | --- | --- | --- |
| Must | US01 | Store foundation | Create and verify a store in Wafeer Partners | Ready | None |
| Must | US02 | Inventory | Add eligible products with price, quantity, and expiry data | Ready | US01 |
| Must | US03 | Safety rules | Block expired, unsafe, or ineligible products | Ready | US02 |
| Must | US04 | Customer discovery | Browse available discounted products | Ready | US02, US03 |
| Must | US05 | Smart Search | Find relevant products quickly using intent and filters | Ready | US04 |
| Must | US06 | Product trust | Review price, discount, expiry, and collection information | Ready | US04 |
| Must | US07 | Order flow | Reserve or purchase an available product | Ready | US03, US06 |
| Should | US08 | Smart Basket | Receive a useful basket recommendation from available items | Ready | US05, US07 |
| Should | US09 | Smart Analysis | Identify expiry risk and recommended store actions | Ready | US02, US07 |
| Must | US10 | Safe donation | Redirect eligible food to charity before expiry | Ready | US03, US09 |
| Should | US11 | Notifications | Receive order, pickup, inventory, and donation updates | Ready | US07, US10 |
| Could | US12 | Impact reporting | Measure store, customer, and community outcomes | Ready | US07, US10 |

## Epic 1: Store and inventory foundation

### US01: Create and verify a store

**User story**

As a store manager, I want to create a Wafeer Partners store profile so that I can manage eligible inventory and make it visible to customers.

**Acceptance criteria**

* The manager can enter the store name, address, contact information, operating hours, and pickup location.
* Required information is validated before submission.
* The store remains inactive until required verification is complete.
* Customers cannot see unverified stores.
* The manager can update store information after verification.

**Tasks**

* Design the store onboarding flow.
* Define required and optional store fields.
* Add validation and clear error messages.
* Create verification and activation states.
* Test incomplete, duplicate, and invalid submissions.

### US02: Add eligible inventory

**User story**

As an inventory employee, I want to add products with price, quantity, expiry date, and storage information so that the store can act before products become waste.

**Acceptance criteria**

* A product includes its name, category, original price, discounted price, quantity, expiry date, and storage requirements.
* The discounted price must be lower than the original price.
* Quantity cannot be negative.
* Invalid or past expiry dates are rejected.
* Inventory changes appear in Wafeer without exposing ineligible products.

**Tasks**

* Create the product entry form.
* Define product validation rules.
* Add inventory quantity controls.
* Connect eligible inventory to the customer catalogue.
* Test incorrect dates, prices, and quantities.

### US03: Enforce safety and eligibility rules

**User story**

As a platform administrator, I want listings to follow safety and eligibility rules so that expired or unsafe food is never sold or donated.

**Acceptance criteria**

* A product cannot be published if its expiry date has passed.
* A store confirms that a product remains safe, properly stored, and compliant before activation.
* Products automatically leave customer discovery when they exit the eligible sales window.
* Donation eligibility ends before or at the configured safety cutoff.
* Expired, damaged, recalled, or unsafe items are blocked from both sale and donation.
* Every eligibility status change is recorded.

**Tasks**

* Define sale and donation eligibility states.
* Create automatic status transitions.
* Add store safety confirmation.
* Add blocked item reasons and an audit record.
* Test boundary dates and invalid status changes.

## Epic 2: Customer discovery and trust

### US04: Browse discounted products

**User story**

As a customer, I want to browse available products from nearby verified stores so that I can find useful food at a lower price.

**Acceptance criteria**

* Only active, in stock, eligible products are displayed.
* Customers can filter by category, store, price, discount, and pickup location.
* Out of stock or ineligible products disappear from results.
* Product cards show essential information without requiring extra clicks.
* An empty state suggests changing filters or location.

**Tasks**

* Design the catalogue and filter experience.
* Define product card content.
* Connect catalogue availability to partner inventory.
* Add loading, empty, and error states.
* Test catalogue changes when inventory is updated.

### US05: Use Smart Search

**User story**

As a customer, I want Smart Search to understand what I need and return relevant available products so that I spend less time looking through listings.

**Acceptance criteria**

* Search supports product names, categories, common needs, and natural language phrases.
* Results prioritize relevance and current availability.
* Filters refine results by price, store, distance, discount, and remaining shelf life.
* Ineligible or out of stock products never appear.
* If no exact match exists, the system suggests safe and relevant alternatives.
* Customers can clear or change their search easily.

**Tasks**

* Define supported search intents and filters.
* Create ranking logic.
* Add spelling tolerance and alternative suggestions.
* Protect results with inventory and eligibility checks.
* Test common, ambiguous, and empty queries.

### US06: Review product information

**User story**

As a customer, I want clear product, price, expiry, and pickup information so that I can make a confident decision.

**Acceptance criteria**

* The customer sees the original price, discounted price, percentage saved, expiry information, quantity, store, and pickup window.
* The page explains that the item is offered before expiry and must meet eligibility rules.
* Storage and collection instructions are visible when relevant.
* Unavailable products cannot be added to the basket.
* Any material product update appears before checkout.

**Tasks**

* Design the product detail page.
* Calculate and display savings.
* Add expiry and pickup information.
* Add availability validation.
* Test changes between product view and checkout.

## Epic 3: Basket and order flow

### US07: Reserve or purchase an item

**User story**

As a customer, I want to reserve or purchase available products so that the store holds them for my collection window.

**Acceptance criteria**

* Availability is checked again before confirmation.
* Confirmed quantities are deducted or temporarily reserved.
* The customer receives a clear order summary and collection window.
* Failed payments or expired reservations release the inventory.
* The same final unit cannot be confirmed twice.
* The store can view and prepare confirmed orders.

**Tasks**

* Design basket, checkout, and confirmation states.
* Add a final inventory check.
* Define reservation timeout rules.
* Update store inventory after confirmation or cancellation.
* Test competing orders for limited inventory.

### US08: Build a Smart Basket

**User story**

As a customer, I want Smart Basket suggestions based on my needs, budget, and available products so that I can save more and discover useful combinations.

**Acceptance criteria**

* Customers can enter a budget, preferences, household need, or excluded items.
* Suggestions contain only available and eligible products.
* The basket displays total original price, discounted total, and savings.
* Customers can remove, replace, or add individual items.
* Replacements respect the customer's budget and exclusions.
* The basket is revalidated before confirmation.

**Tasks**

* Define basket inputs and recommendation rules.
* Create basket generation and replacement flows.
* Calculate total savings.
* Add availability and safety validation.
* Test low inventory, exclusions, and price changes.

## Epic 4: Partner intelligence and responsible redistribution

### US09: Use Smart Analysis

**User story**

As a store manager, I want Smart Analysis to identify inventory at risk and recommend timely actions so that I can recover value before products become waste.

**Acceptance criteria**

* The dashboard groups products by urgency and remaining eligible time.
* The manager sees current quantity, sales activity, discount, and projected risk.
* The system recommends actions such as adjusting the discount, featuring a product, or preparing an eligible donation.
* Recommendations never override safety rules or publish changes without store confirmation.
* The manager can filter analysis by category, date range, and action status.
* Completed actions are reflected in the dashboard.

**Tasks**

* Define expiry risk levels.
* Design the analysis dashboard.
* Create recommendation rules.
* Add manager approval for suggested actions.
* Test products near each safety threshold.

### US10: Redirect safe food to charity before expiry

**User story**

As a store manager, I want to offer eligible food to a verified charity before it expires so that safe food can support people instead of becoming waste.

**Acceptance criteria**

* Only food that is within its valid expiry date, properly stored, safe, and edible can enter the donation workflow.
* Expired, unsafe, damaged, or recalled products are never eligible.
* The store confirms quantity, condition, expiry information, and collection deadline.
* Only verified charity partners can accept a donation.
* Acceptance creates a handoff record with the responsible parties and time.
* Unaccepted items remain subject to the safety cutoff and are automatically blocked when no longer eligible.
* Customer listings and donation availability cannot allocate the same unit twice.

**Tasks**

* Define donation eligibility and verification rules.
* Design the charity offer and acceptance flow.
* Add quantity locking to prevent double allocation.
* Create the handoff record.
* Add automatic cutoff and blocked status.
* Test rejected, expired, and partially accepted donations.

### US11: Send useful notifications

**User story**

As a customer, store employee, or charity coordinator, I want timely updates about actions that require attention so that orders and safe handoffs happen on time.

**Acceptance criteria**

* Customers receive confirmation, collection reminders, changes, and cancellation updates.
* Stores receive low inventory, approaching cutoff, new order, and donation acceptance updates.
* Charity coordinators receive eligible offer, acceptance, and pickup reminders.
* Notifications contain only the information needed by the recipient.
* Users can manage optional notification preferences.
* Safety and cutoff warnings cannot be disabled for responsible store users.

**Tasks**

* Define notification events and recipients.
* Write clear message templates.
* Add preference controls.
* Prevent duplicate notifications.
* Test timing and role based visibility.

## Epic 5: Impact and learning

### US12: Measure product impact

**User story**

As a store manager or platform administrator, I want clear product and impact metrics so that I can understand business value and improve future decisions.

**Acceptance criteria**

* Stores can view revenue recovered, products sold before expiry, successful donations, and estimated waste avoided.
* Customer reporting includes savings and repeat purchase behavior without exposing private information.
* Donation reporting distinguishes offered, accepted, collected, expired, and rejected quantities.
* Metrics use documented definitions and time ranges.
* Administrators can identify missing or inconsistent data.
* Reports do not present estimates as exact measurements.

**Tasks**

* Define every metric and data source.
* Design store and administrator reports.
* Add date and store filters.
* Separate estimates from verified counts.
* Test incomplete and inconsistent records.

# Release plan

| Phase | Product outcome | Included backlog |
| --- | --- | --- |
| Discovery | Validate customer, store, and charity workflows | Interviews, journey maps, safety review |
| MVP 1 | Stores can publish eligible inventory safely | US01, US02, US03 |
| MVP 2 | Customers can discover and understand products | US04, US05, US06 |
| MVP 3 | Customers can complete a reliable order | US07, US11 |
| Growth | Improve value through intelligent experiences | US08, US09 |
| Impact | Enable responsible donation and measurement | US10, US12 |

# Suggested sprint sequence

| Sprint | Goal | Stories |
| --- | --- | --- |
| Sprint 0 | Validate workflows, safety rules, and product assumptions | Discovery and policy definition |
| Sprint 1 | Activate verified stores and safe inventory | US01, US02, US03 |
| Sprint 2 | Launch customer discovery and Smart Search | US04, US05, US06 |
| Sprint 3 | Complete reservations, purchases, and notifications | US07, US11 |
| Sprint 4 | Add Smart Basket and Smart Analysis | US08, US09 |
| Sprint 5 | Add safe charity handoffs and impact reporting | US10, US12 |

## Definition of ready

A story is ready when:

* The user and problem are clear.
* Acceptance criteria are testable.
* Dependencies and safety implications are identified.
* Design or content questions are resolved.
* The team can estimate the work.

## Definition of done

A story is done when:

* Acceptance criteria pass.
* Important edge cases are tested.
* Safety and privacy rules are satisfied.
* The experience works across supported screen sizes.
* Product documentation is updated.
* The Product Owner accepts the completed story.

## Key product risks

| Risk | Product response |
| --- | --- |
| Customer confusion about near expiry food | Display clear dates, eligibility, storage, and collection information |
| Unsafe or expired items entering the system | Enforce automatic blocks, store confirmation, audit records, and clear cutoffs |
| Inventory sold twice | Revalidate and lock quantities during order or donation confirmation |
| Stores receive too many alerts | Prioritize notifications by urgency and required action |
| Smart features make poor recommendations | Keep eligibility rules deterministic and require store control over business actions |
| Donations are misunderstood | State clearly that only safe, edible, valid food can be donated before expiry |

## Portfolio note

This backlog is a Product Owner portfolio artifact based on Wafeer, an award winning team hackathon product. It documents the product thinking, prioritization, user stories, acceptance criteria, dependencies, metrics, and delivery plan behind the concept. It does not present the full team build as solo work.
