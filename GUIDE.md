# 🚀 MASTER PRODUCT DEVELOPMENT GUIDE
### Industry Best Practice Standard — From Idea to Launch

> **Scope:** Any tech product (web app, mobile app, SaaS, platform, API, or internal tool)
> **Standard:** Industry-grade, production-ready
> **Methodology:** Lean + Agile + Shape Up hybrid
> **Last updated:** 2025

---

## 📖 Table of Contents

1. [Product Discovery & Definition](#1-product-discovery--definition)
2. [Feature Scoping (MVP First)](#2-feature-scoping-mvp-first)
3. [User Flow & Journey Mapping](#3-user-flow--journey-mapping)
4. [Data Modeling & Database Design](#4-data-modeling--database-design)
5. [System Architecture](#5-system-architecture)
6. [Authentication & Authorization](#6-authentication--authorization)
7. [Business Logic Definition](#7-business-logic-definition)
8. [API Design (Contract First)](#8-api-design-contract-first)
9. [UI/UX Design](#9-uiux-design)
10. [Edge Case & Failure Planning](#10-edge-case--failure-planning)
11. [Project Structure & Coding Standards](#11-project-structure--coding-standards)
12. [Development Roadmap](#12-development-roadmap)
13. [Testing Strategy](#13-testing-strategy)
14. [Deployment Plan](#14-deployment-plan)
15. [Monitoring & Observability](#15-monitoring--observability)
16. [Security Checklist](#16-security-checklist)
17. [Post-Launch & Iteration](#17-post-launch--iteration)
18. [Master Reference Library](#-master-reference-library)

---

## Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | TODO / Action Item |
| 📌 | Output / Deliverable |
| 📚 | References (Books) |
| 🔗 | Online Resources |
| ⚠️ | Warning / Critical Note |
| 💡 | Tips & Best Practices |

---

## 1. Product Discovery & Definition

> **Goal:** Validate the problem before writing a single line of code.
>
> 💡 *"Fall in love with the problem, not the solution."*
> — Uri Levine, Co-founder of Waze

### Why This Matters

Most products fail not because of bad code, but because they solve a problem nobody has, or solve the wrong problem for the wrong audience. This phase exists to prevent that.

According to CB Insights (2021), the **#1 reason startups fail (42%)** is building something the market does not need. Discovery is the antidote.

### ✅ TODO

- [ ] **Write a clear problem statement** — Describe the problem in 1–2 sentences without mentioning any solution
- [ ] **Conduct user research** — Minimum 5 user interviews using the Jobs-to-be-Done (JTBD) framework
- [ ] **Define target user persona** — Include: demographics, goals, pain points, behaviors, and current workarounds
- [ ] **Write a Value Proposition** — Use the Value Proposition Canvas (Osterwalder)
- [ ] **Perform competitor analysis** — Map competitors across: features, pricing, target users, strengths, and weaknesses
- [ ] **Define product scope** — Explicitly document what is IN scope and what is OUT of scope
- [ ] **Define success metrics (KPIs)** — Examples: conversion rate, DAU/MAU, retention rate, task completion rate, NPS
- [ ] **Write a Problem Hypothesis:**
  > *"We believe [user type] has [problem]. We will solve it by [solution]. We'll know it works when [measurable outcome]."*
- [ ] **Validate hypothesis before building** — Options: landing page test, survey, paper prototype, Wizard of Oz test, or concierge MVP

### 📌 Output

- `docs/product-brief.md` — 1–2 page document: problem, persona, value prop, scope, KPIs
- `docs/personas.md` — Detailed user persona profiles
- `docs/competitor-analysis.md` — Competitor comparison matrix

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Inspired* (2nd Ed) | Marty Cagan | 2018 | Industry-standard product management methodology used by top tech companies |
| *The Lean Startup* | Eric Ries | 2011 | Build-Measure-Learn loop; validated learning before building |
| *Continuous Discovery Habits* | Teresa Torres | 2021 | Modern framework for continuous, weekly user research |
| *Value Proposition Design* | Osterwalder, Pigneur, et al. | 2014 | Structured canvas for defining and testing value |
| *The Mom Test* | Rob Fitzpatrick | 2013 | How to conduct user interviews that reveal truth, not flattery |

### 🔗 Online Resources

- [Jobs-to-be-Done Framework — Intercom](https://www.intercom.com/resources/books/intercom-jobs-to-be-done)
- [Google Ventures Design Sprint](https://www.gv.com/sprint/) — 5-day framework to answer critical business questions
- [Value Proposition Canvas Tool — Strategyzer](https://www.strategyzer.com/library/the-value-proposition-canvas)
- [CB Insights: Why Startups Fail](https://www.cbinsights.com/research/startup-failure-reasons-top/)

---

## 2. Feature Scoping (MVP First)

> **Goal:** Ship the smallest version of the product that delivers genuine value to real users.
>
> 💡 *"If you're not embarrassed by the first version of your product, you've launched too late."*
> — Reid Hoffman, Co-founder of LinkedIn

### Why This Matters

Scope creep is one of the leading causes of delayed and over-budget software projects. The Standish Group CHAOS Report (2020) found that only **31% of software projects** are delivered on time and on budget. Disciplined scoping is the primary counter-measure.

### ✅ TODO

- [ ] **List ALL possible features** — Brain dump with zero filtering at this stage
- [ ] **Apply MoSCoW prioritization:**
  - **Must Have** — Core value; the product is not viable without this
  - **Should Have** — Important but not launch-blocking
  - **Could Have** — Nice-to-have; low effort, low risk additions
  - **Won't Have (this cycle)** — Explicitly deferred; removes ambiguity
- [ ] **Write user stories per feature:**
  > *"As a [role], I want [goal] so that [benefit]."*
- [ ] **Write acceptance criteria per story** — Use Given/When/Then (Gherkin) format:
  > *"Given [context], When [action], Then [expected outcome]."*
- [ ] **Create a feature dependency map** — Identify which features must be built before others
- [ ] **Estimate complexity per feature** — T-shirt sizing: XS / S / M / L / XL
- [ ] **Validate MVP scope against Problem Statement** — Does the MVP actually solve the core problem?
- [ ] **Remove anything not critical for MVP** — If in doubt, leave it out

### 📌 Output

- `docs/feature-list.md` — Prioritized feature list with MoSCoW labels, complexity, and owner
- `docs/user-stories.md` — User stories with acceptance criteria

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Shape Up* (Free online) | Ryan Singer, Basecamp | 2019 | Appetite-based scoping; fixes time, flexes scope |
| *The Lean Product Playbook* | Dan Olsen | 2015 | Systematic MVP definition using the Product-Market Fit Pyramid |
| *User Story Mapping* | Jeff Patton | 2014 | Visual technique for mapping user journeys to buildable features |
| *Escaping the Build Trap* | Melissa Perri | 2018 | Outcome-over-output thinking; avoid building for the sake of building |

### 🔗 Online Resources

- [Shape Up — Free Book by Basecamp](https://basecamp.com/shapeup)
- [MoSCoW Prioritization — Atlassian](https://www.atlassian.com/agile/project-management/moscow-prioritization)
- [Writing Good User Stories — Mountain Goat Software](https://www.mountaingoatsoftware.com/agile/user-stories)
- [Gherkin Syntax — Cucumber Docs](https://cucumber.io/docs/gherkin/)
- [CHAOS Report Summary — Standish Group](https://www.standishgroup.com/sample_research_files/CHAOSReport2015-Final.pdf)

---

## 3. User Flow & Journey Mapping

> **Goal:** Map every path a user can take through the product before designing or coding anything.
>
> 💡 *"Know the complete journey before building any single screen."*

### Why This Matters

Designing screens without flows leads to disconnected UX, missed edge cases, and expensive rework. A flow diagram is cheaper to change than code.

### ✅ TODO

#### Journey Mapping
- [ ] **Map the end-to-end user journey** — From first awareness to core task completion
- [ ] **Create a flow diagram for each user role** — e.g., end user, admin, operator, guest
- [ ] **Identify all decision points** — Every branching condition in the journey (IF/ELSE moments)
- [ ] **Map the emotional journey** — Where does the user feel confused, frustrated, or delighted?

#### Edge Cases Per Flow
- [ ] **Add all non-happy-path scenarios:**
  - Empty states (first-time use, no data)
  - Error states (network failure, validation error, server error)
  - Loading and skeleton states
  - Permission-denied states
  - Cancellation and timeout flows
  - Partial completion states

#### Screen Inventory
- [ ] **Convert flows into a complete screen list** — Every unique screen or state that needs to be built
- [ ] **Validate flows against all user stories** — Every story must have a corresponding flow step
- [ ] **Review flows with stakeholders** — Walk through with a non-technical person before proceeding

### 📌 Output

- `docs/flows/` — Flow diagrams per role (user, admin, etc.)
- `docs/screen-inventory.md` — Complete list of all screens/states to build
- `docs/journey-map.md` — Emotional journey map

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Don't Make Me Think* (3rd Ed) | Steve Krug | 2014 | Web usability fundamentals; cognitive load, navigation clarity |
| *Mapping Experiences* | James Kalbach | 2016 | Journey mapping techniques from industry practitioners |
| *About Face* (4th Ed) | Alan Cooper | 2014 | Interaction design principles and goal-directed design |

### 🔗 Online Resources

- [UX Flowcharts — Nielsen Norman Group](https://www.nngroup.com/articles/ux-flowcharts/) — Evidence-based guide
- [Customer Journey Mapping — NNGroup](https://www.nngroup.com/articles/customer-journey-mapping/)
- [Lucidchart — Free Flow Templates](https://www.lucidchart.com/pages/templates/flowchart)
- [FigJam — Collaborative Diagramming](https://www.figma.com/figjam/)

### 💡 Recommended Tools

| Tool | Best For |
|------|----------|
| FigJam / Miro | Collaborative, real-time flow diagramming |
| Lucidchart | Formal, documentation-grade flow diagrams |
| draw.io (free) | Simple diagrams that live in your repo as XML |

---

## 4. Data Modeling & Database Design

> **Goal:** Design a normalized, performant, and scalable data schema that accurately reflects your domain.
>
> 💡 *"Data outlives code. Get the data model right before writing application logic."*

### Why This Matters

A poor data model is the hardest type of technical debt to fix in production. Schema changes on live systems with real users can be dangerous and expensive. Martin Kleppmann, author of *Designing Data-Intensive Applications*, notes that data models are often the most long-lived artifact in a software system.

### ✅ TODO

#### Entity Design
- [ ] **Identify all domain entities** — List every significant noun in your domain (e.g., User, Product, Order, Invoice, etc.)
- [ ] **Define attributes per entity** — Field name, data type, constraints (required, unique, default value)
- [ ] **Define relationships between entities:**
  - One-to-One (1:1)
  - One-to-Many (1:N)
  - Many-to-Many (M:N) — define explicit join/bridge tables

#### Normalization
- [ ] **Apply normalization rules:**
  - **1NF** — Atomic values only; no repeating groups or arrays in columns
  - **2NF** — No partial dependency; every non-key attribute depends on the whole primary key
  - **3NF** — No transitive dependency; non-key attributes depend only on the primary key

#### Indexing & Performance
- [ ] **Define indexes:**
  - Primary keys on every table
  - Foreign key indexes
  - Composite indexes for common query patterns
  - Full-text indexes where search is required
- [ ] **Plan for query patterns** — Design schema around how data will be read, not just stored

#### Data Integrity
- [ ] **Define soft delete strategy** — Use a `deleted_at` timestamp instead of hard deletes where history matters
- [ ] **Add audit fields to critical tables** — `created_at`, `updated_at`, `created_by`, `updated_by`
- [ ] **Define data retention policy** — How long is data kept? When is it purged?

#### Multi-tenancy (if applicable)
- [ ] **Define tenant isolation strategy:**
  - **Row-level** — All tenants in one table, filtered by `tenant_id` (simpler, most common)
  - **Schema-level** — Separate schema per tenant (stronger isolation)
  - **Database-level** — Separate database per tenant (maximum isolation, highest cost)

#### Validation
- [ ] **Validate schema against all user flows** — Can every use case be served by this model?
- [ ] **Plan migration strategy** — How will schema changes be applied safely in production?

### 📌 Output

- `docs/erd.png` or `docs/erd.pdf` — Entity Relationship Diagram
- `docs/data-dictionary.md` — Description of every table, column, and relationship
- Database schema file (ORM schema or raw SQL DDL)

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Designing Data-Intensive Applications* | Martin Kleppmann | 2017 | The definitive guide to scalable, reliable data systems |
| *Database Design for Mere Mortals* (4th Ed) | Michael Hernandez | 2020 | Practical normalization and ER modeling from first principles |
| *SQL Antipatterns* | Bill Karwin | 2010 | 24 common database design mistakes and how to avoid them |

### 🔗 Online Resources

- [Database Normalization Guide — GeeksforGeeks](https://www.geeksforgeeks.org/normal-forms-in-dbms/)
- [ER Diagram Basics — Lucidchart](https://www.lucidchart.com/pages/er-diagrams)
- [Multi-tenancy Patterns — Microsoft Azure Architecture](https://learn.microsoft.com/en-us/azure/architecture/guide/multitenant/overview)
- [DB Diagram Tool (Free)](https://dbdiagram.io/) — Browser-based ERD tool with code-like syntax

---

## 5. System Architecture

> **Goal:** Choose a technical architecture that balances current needs with future scalability.
>
> 💡 *"Make it work, make it right, make it fast — in that order."*
> — Kent Beck, creator of Extreme Programming

### Why This Matters

Architecture decisions are expensive to reverse. The goal is not to pick the most sophisticated architecture — it is to pick the most appropriate one. Netflix, Shopify, and Stack Overflow have all published that they started as monoliths.

### ✅ TODO

#### Architecture Style Selection
- [ ] **Choose an architecture style based on team size and complexity:**
  - **Monolith** — Recommended for MVPs, solo devs, and teams under 5 engineers
  - **Modular Monolith** — Modules with clear boundaries inside one deployable unit; good default for growing products
  - **Microservices** — Only justified when team scale and domain complexity are both high; significant operational overhead
- [ ] **Document your choice and rationale** in an Architecture Decision Record (ADR)

#### Tech Stack Decision
- [ ] **Define each layer of the stack:**
  - Frontend (rendering strategy: CSR, SSR, SSG, or hybrid)
  - Backend / API layer
  - Primary database
  - Cache layer (if needed)
  - File/object storage
  - Search engine (if needed)
  - Message queue / background jobs (if needed)
- [ ] **Write justification for each technology choice** — Include tradeoffs, not just benefits

#### Architecture Documentation
- [ ] **Create an architecture diagram using the C4 Model:**
  - **Level 1 — Context:** System and its external actors
  - **Level 2 — Container:** Applications, services, and databases
  - **Level 3 — Component:** Internal modules within a container
  - **Level 4 — Code:** (Optional) Class-level detail for complex areas
- [ ] **Define the data flow** — How data moves from client → server → database → cache → client

#### Strategy Decisions
- [ ] **Define caching strategy:**
  - Static content caching (CDN)
  - API response caching
  - Database query caching
  - Client-side caching
- [ ] **Define state management approach** — Client state vs. server state vs. URL state
- [ ] **Define third-party integrations** — Payment, email, SMS, analytics, etc.
- [ ] **Define infrastructure approach** — Cloud provider, region selection, scaling strategy

#### Twelve-Factor App Compliance
- [ ] **Review against the 12-Factor methodology** (Heroku, 2011 — industry standard for cloud-native apps):
  - Codebase in version control
  - Explicitly declare dependencies
  - Config stored in environment (not code)
  - Backing services as attached resources
  - Strictly separate build and run stages
  - Stateless processes
  - Export services via port binding
  - Scale out via process model
  - Fast startup and graceful shutdown
  - Dev/staging/production parity
  - Treat logs as event streams
  - Admin tasks as one-off processes

### 📌 Output

- `docs/architecture.md` — Architecture overview and diagram
- `docs/tech-stack.md` — Technology choices with rationale
- `docs/adr/` — Folder containing Architecture Decision Records

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Clean Architecture* | Robert C. Martin | 2017 | Dependency rule, separation of concerns, screaming architecture |
| *Designing Data-Intensive Applications* | Martin Kleppmann | 2017 | Distributed systems, replication, caching, streaming |
| *Building Microservices* (2nd Ed) | Sam Newman | 2021 | When and how to decompose services — and when NOT to |
| *Fundamentals of Software Architecture* | Mark Richards & Neal Ford | 2020 | Architecture styles, tradeoffs, and decision-making |

### 🔗 Online Resources

- [C4 Model for Architecture Diagrams](https://c4model.com/) — Used by ThoughtWorks, Spotify, and others
- [Architecture Decision Records (ADR)](https://adr.github.io/) — Standard ADR format and tooling
- [The 12-Factor App](https://12factor.net/) — Cloud-native application methodology
- [System Design Primer — GitHub](https://github.com/donnemartin/system-design-primer) — 270k+ stars; comprehensive system design reference
- [ThoughtWorks Technology Radar](https://www.thoughtworks.com/radar) — Biannual industry tech landscape assessment

---

## 6. Authentication & Authorization

> **Goal:** Implement secure, role-based access control from the very beginning.
>
> 💡 *"Security is not a feature you add. It is a property you build in."*

### Why This Matters

Broken Access Control is the **#1 web application security risk** according to OWASP Top 10 (2021). Retrofitting auth and permissions into an existing system is significantly more expensive and error-prone than designing them upfront.

### ✅ TODO

#### Role & Permission Design
- [ ] **Define all user roles** — e.g., `super_admin`, `admin`, `editor`, `member`, `guest`
- [ ] **Create a permissions matrix** — Role × Resource × Action (Create, Read, Update, Delete)
- [ ] **Apply principle of least privilege** — Every role gets only the permissions it needs, nothing more
- [ ] **Design permission inheritance** — If roles are hierarchical, define how permissions cascade

#### Authentication Implementation
- [ ] **Choose an authentication method:**
  - **Session-based (Stateful)** — Server stores session; easier to invalidate; good for web apps
  - **JWT (Stateless)** — Token carries claims; good for APIs, mobile, distributed systems
  - **OAuth2 / OpenID Connect** — For social login (Google, GitHub) or enterprise SSO
- [ ] **Secure token storage:**
  - Store session tokens or JWTs in **`httpOnly` cookies** — Never in `localStorage` or `sessionStorage`
  - Set `Secure` and `SameSite=Strict` flags on cookies
- [ ] **Define token lifecycle:**
  - Short-lived access tokens (e.g., 15 minutes)
  - Long-lived refresh tokens with rotation
  - Token revocation strategy on logout

#### Authorization Implementation
- [ ] **Enforce RBAC (Role-Based Access Control) at the server/API layer** — Never rely on UI-only restrictions
- [ ] **Protect all routes** — Both client-side (navigation) and server-side (API endpoints)
- [ ] **Deny by default** — Require explicit permission grant; implicit access should not exist

#### Security Hardening
- [ ] **Implement account lockout** — After N consecutive failed login attempts
- [ ] **Rate limit authentication endpoints** — Prevent brute-force attacks
- [ ] **Log all authentication events** — Successful logins, failures, logouts, role changes
- [ ] **Handle session expiry gracefully** — Silent refresh or redirect to login with return URL
- [ ] **Offer Multi-Factor Authentication (MFA)** — TOTP (e.g., Google Authenticator) or magic link

### 📌 Output

- `docs/auth-flow.md` — Authentication flow diagram with token lifecycle
- `docs/rbac-matrix.md` — Role × Permission matrix
- Implementation in `src/auth/` or equivalent

### 📚 References

| Resource | Author/Source | Year | Why Relevant |
|----------|--------------|------|-------------|
| *OAuth 2 in Action* | Richer & Sanso | 2017 | Deep understanding of OAuth2 and OpenID Connect flows |
| [OWASP Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html) | OWASP | 2024 | Definitive, maintained guide to secure auth implementation |
| [OWASP Session Management Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) | OWASP | 2024 | Session security best practices |
| [RFC 8725 — JWT Best Practices](https://datatracker.ietf.org/doc/html/rfc8725) | IETF | 2020 | Official IETF standard for secure JWT usage |

### 🔗 Online Resources

- [OWASP Top 10: A01 — Broken Access Control](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
- [OWASP Top 10: A07 — Auth Failures](https://owasp.org/Top10/A07_2021-Identification_and_Authentication_Failures/)
- [Auth0 Identity Fundamentals](https://auth0.com/docs/get-started/identity-fundamentals) — Vendor-neutral conceptual guides

---

## 7. Business Logic Definition

> **Goal:** Document all domain rules explicitly before implementation to reduce ambiguity and bugs.
>
> 💡 *"The domain model is the heart of the software."*
> — Eric Evans, *Domain-Driven Design*

### Why This Matters

Undocumented business logic lives only in someone's head. When that person leaves, the logic either gets lost or misimplemented. Bugs in business logic (wrong calculation, invalid state transition, missing validation) are often the most damaging bugs in production.

### ✅ TODO

#### Domain Modeling
- [ ] **Identify all domain entities** — Significant nouns in your business domain
- [ ] **Identify aggregates** — Groups of entities treated as a single unit (e.g., an Order and its line items)
- [ ] **Identify domain events** — Things that happen: OrderPlaced, PaymentFailed, UserVerified

#### State Machine Design
- [ ] **Define state machines for all stateful entities:**
  - List all possible states
  - Define all valid transitions between states
  - Define what triggers each transition
  - Define what is NOT a valid transition
- [ ] **Draw state diagrams** — Visualize the machine before implementing it

  Example for a generic Order entity:
  ```
  draft → submitted → confirmed → processing → completed
                    ↘ cancelled              ↗ refunded
  ```

#### Business Rules Documentation
- [ ] **Document all business rules explicitly:**
  - Calculation rules (pricing, tax, discounts, fees)
  - Eligibility rules (who can access what, under what conditions)
  - Constraint rules (limits, quotas, restrictions)
  - Sequencing rules (what must happen before what)
- [ ] **Define validation rules per entity:**
  - Required fields
  - Format constraints (email, phone, date ranges)
  - Business constraints (age restriction, region eligibility, minimum values)
- [ ] **Define failure handling per business scenario:**
  - What happens when a critical operation fails?
  - Is the failure recoverable or terminal?
  - What is the rollback behavior?
- [ ] **Document all calculations with explicit formulas** — Do not leave math implicit in code
- [ ] **Handle race conditions explicitly:**
  - Identify operations that can conflict when executed concurrently
  - Choose a concurrency control strategy: optimistic locking, pessimistic locking, or queue-based serialization

#### Validation
- [ ] **Review all business rules with a domain expert or stakeholder** before writing any code

### 📌 Output

- `docs/business-rules.md` — Full documentation of all domain rules
- `docs/state-machines.md` — State diagrams and transition tables
- `docs/calculations.md` — Formula documentation for all computed values

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Domain-Driven Design* | Eric Evans | 2003 | Foundational book on modeling complex business domains in software |
| *Implementing Domain-Driven Design* | Vaughn Vernon | 2013 | Practical DDD with real code examples and patterns |
| *Patterns of Enterprise Application Architecture* | Martin Fowler | 2002 | Transaction scripts, domain models, service layers, and repositories |

### 🔗 Online Resources

- [State Machine Concepts — XState Docs](https://xstate.js.org/docs/guides/introduction-to-state-machines-and-statecharts.html)
- [Optimistic vs Pessimistic Locking — Martin Fowler](https://martinfowler.com/eaaCatalog/optimisticOfflineLock.html)
- [Domain Storytelling](https://domainstorytelling.org/) — Collaborative technique for capturing domain knowledge

---

## 8. API Design (Contract First)

> **Goal:** Define your API contract before implementation so frontend and backend can work in parallel.
>
> 💡 *"Design the API you wish you had, then implement it."*

### Why This Matters

API-first (contract-first) development is a widely adopted practice at companies like Stripe, Twilio, and Shopify — whose APIs are regarded as industry benchmarks. Designing first prevents mismatches between client and server and enables parallel development.

### ✅ TODO

#### API Style Selection
- [ ] **Choose and commit to one API paradigm:**
  - **REST** — Resource-oriented, HTTP-native, widely understood; recommended default
  - **GraphQL** — Flexible querying; good for complex, nested data and multiple clients
  - **tRPC / RPC-style** — Type-safe, co-located client/server; good for full-stack TypeScript
  - **gRPC** — Binary protocol; good for internal service-to-service communication

#### Contract-First Process
1. [ ] **Write the API specification first** (before any implementation)
2. [ ] **Generate a mock server from the spec** — Frontend builds against the mock
3. [ ] **Build backend to satisfy the spec** — Backend is validated against the same contract
4. [ ] **Run contract tests** — Automated verification that implementation matches spec

#### Endpoint Design (REST)
- [ ] **Use resource-oriented naming:**
  - ✅ `GET /api/v1/orders`
  - ✅ `POST /api/v1/orders`
  - ✅ `PATCH /api/v1/orders/{id}`
  - ❌ `POST /api/v1/getOrders`
  - ❌ `POST /api/v1/createNewOrder`
- [ ] **Define request/response schema per endpoint:**
  - HTTP method and path
  - Request body with all fields, types, and validation rules
  - Success response schema
  - All possible error response schemas

#### Standardization
- [ ] **Standardize error response format across all endpoints:**
  ```json
  {
    "status": "error",
    "code": "RESOURCE_NOT_FOUND",
    "message": "The requested item was not found.",
    "details": {}
  }
  ```
- [ ] **Define pagination strategy** — Cursor-based (recommended for large datasets) or offset-based
- [ ] **Define API versioning strategy** — URL-based (`/v1/`) is most explicit and widely understood
- [ ] **Define rate limiting rules** — Per IP, per authenticated user, per endpoint
- [ ] **Define idempotency** — State-changing POST endpoints (especially payments) must accept idempotency keys
- [ ] **Document authentication requirement per endpoint** — Public, authenticated, or role-restricted
- [ ] **Validate API spec against all user flows** — Every screen must have a corresponding API call

### 📌 Output

- `docs/api/openapi.yaml` — Machine-readable API spec (OpenAPI 3.x format)
- `docs/api/README.md` — Human-readable API overview and authentication guide
- Postman or Insomnia collection for manual testing

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *RESTful Web APIs* | Richardson & Amundsen | 2013 | REST constraints, hypermedia, resource design |
| *The Design of Web APIs* | Arnaud Lauret | 2019 | Practical API design patterns, anti-patterns, and naming |
| [OpenAPI 3.1 Specification](https://spec.openapis.org/oas/v3.1.0) | OpenAPI Initiative | 2021 | The industry standard for describing REST APIs |

### 🔗 Online Resources

- [REST API Design Best Practices — Microsoft Azure](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- [API Versioning Strategies — Stripe Engineering Blog](https://stripe.com/blog/api-versioning)
- [Cursor-based Pagination — Slack Engineering](https://slack.engineering/evolving-api-pagination-at-slack/)
- [Stoplight Studio — OpenAPI Design Tool](https://stoplight.io/studio)
- [Postman — API Design and Testing](https://www.postman.com/)

---

## 9. UI/UX Design

> **Goal:** Create a usable, consistent, and accessible user interface backed by a documented design system.
>
> 💡 *"Design is not how it looks. Design is how it works."*
> — Steve Jobs

### Why This Matters

Nielsen Norman Group research shows that every $1 invested in UX yields $100 in return (ROI of 9,900%). Poor UX does not just frustrate users — it costs revenue. Accessibility matters too: the WHO estimates **1.3 billion people** (16% of the world's population) live with some form of disability.

### ✅ TODO

#### Phase 1 — Information Architecture
- [ ] **Create a sitemap** — All pages, screens, and their hierarchy
- [ ] **Define navigation structure** — Primary navigation, secondary navigation, breadcrumbs
- [ ] **Validate IA against mental models** — Use card sorting with real users (optional but valuable)

#### Phase 2 — Wireframing
- [ ] **Create low-fidelity wireframes for every screen** from the screen inventory
- [ ] **Wireframe all non-happy-path states** — Empty, loading/skeleton, error, success
- [ ] **Wireframe all responsive breakpoints** — Mobile, tablet, desktop
- [ ] **Validate wireframes against user flows** — Every flow step maps to a wireframe

#### Phase 3 — Design System
- [ ] **Define color palette:**
  - Primary brand color
  - Secondary / accent color
  - Semantic colors (success green, warning amber, error red, info blue)
  - Neutral grayscale
  - Check WCAG 2.1 AA contrast ratios — minimum **4.5:1** for normal text, **3:1** for large text
- [ ] **Define typography:**
  - Font families (maximum 2)
  - Type scale (display, h1–h6, body, caption, label)
  - Line heights and letter spacing
- [ ] **Define spacing system** — Use a consistent base unit (4px or 8px grid)
- [ ] **Define the component library using Atomic Design:**
  - **Atoms** — Button, Input, Label, Icon, Badge
  - **Molecules** — Form field, Search bar, Card, Dropdown
  - **Organisms** — Navigation bar, Data table, Modal, Form
  - **Templates** — Page layouts
  - **Pages** — Assembled, content-filled templates
- [ ] **Define all interaction states** — Default, hover, focus, active, disabled, loading, error

#### Phase 4 — High-Fidelity Design (Recommended)
- [ ] **Create high-fidelity mockups** for all critical and high-traffic screens
- [ ] **Build an interactive prototype** for user testing
- [ ] **Conduct usability testing** — Nielsen Norman Group research: testing with just **5 users reveals 85%** of usability problems

### 📌 Output

- `design/wireframes/` — Low-fidelity wireframes
- `design/mockups/` — High-fidelity designs (Figma or equivalent)
- `design/design-system/` — Component library and token documentation
- `docs/design-system.md` — Typography, color, spacing, and component guidelines

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Refactoring UI* | Adam Wathan & Steve Schoger | 2018 | Practical UI design principles for developers |
| *Atomic Design* (Free online) | Brad Frost | 2016 | Component-based design system methodology |
| *Laws of UX* | Jon Yablonski | 2020 | Psychology-based design principles with citations |
| *Don't Make Me Think* (3rd Ed) | Steve Krug | 2014 | Web usability: cognitive load, navigation, and testing |

### 🔗 Online Resources

- [WCAG 2.1 Quick Reference — W3C](https://www.w3.org/WAI/WCAG21/quickref/) — Accessibility standard
- [Laws of UX](https://lawsofux.com/) — Evidence-based design principles with research citations
- [Nielsen Norman Group](https://www.nngroup.com/) — Research-backed UX articles and reports
- [Contrast Ratio Checker — WebAIM](https://webaim.org/resources/contrastchecker/)
- [Atomic Design — Brad Frost (Free)](https://atomicdesign.bradfrost.com/)

---

## 10. Edge Case & Failure Planning

> **Goal:** Design for failure before it happens in production.
>
> 💡 *"Everything that can fail, will fail. Design for it."* — Michael Nygard, *Release It!*

### Why This Matters

The average cost of IT downtime is **$5,600 per minute** (Gartner). Planning for failure is not pessimism — it is professionalism.

### ✅ TODO

#### Failure Scenario Identification
- [ ] **List all failure scenarios per feature:**
  - Network timeout or disconnection mid-operation
  - Third-party service unavailability (payment gateway, email, SMS)
  - Database connection failure or timeout
  - File upload failure or size/type exceeded
  - Session expiry during a multi-step flow
  - Invalid or corrupted data received
- [ ] **Define fallback behavior for each scenario** — What should the user see and experience?
- [ ] **Handle duplicate submissions** — Via idempotency keys, optimistic UI locks, or debouncing

#### Concurrency & Consistency
- [ ] **Identify all race conditions:**
  - Two users performing the same conflicting action simultaneously
  - Double-click or double-submit on a form
  - Parallel updates to shared resources
- [ ] **Choose a concurrency control strategy per scenario:**
  - **Optimistic locking** — Check a version/timestamp field before updating; reject stale writes
  - **Pessimistic locking** — Database-level row lock during a transaction
  - **Queue-based serialization** — Process operations one at a time via a job queue
- [ ] **Define data consistency requirements:**
  - Which operations require **strong consistency**? (financial transactions, inventory deduction)
  - Which can tolerate **eventual consistency**? (analytics, notification counts, search indexes)

#### UX for Failure States
- [ ] **Define loading states** for every async operation — Never leave users wondering if something is happening
- [ ] **Define empty states** — Helpful, on-brand, with a clear call-to-action
- [ ] **Define error messages** — Specific, human-readable, actionable (not "An error occurred")
- [ ] **Design for graceful degradation** — Partial functionality is better than complete failure
- [ ] **Implement retry logic** — Automatic retry with exponential backoff for transient failures

### 📌 Output

- `docs/edge-cases.md` — Failure scenario checklist per feature
- `docs/error-messages.md` — Approved, consistent error message library

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Release It!* (2nd Ed) | Michael Nygard | 2018 | Stability patterns: Circuit Breaker, Timeout, Bulkhead, Retry |
| *Designing Distributed Systems* | Brendan Burns | 2018 | Patterns for reliable, fault-tolerant distributed systems |
| *Site Reliability Engineering* (Free online) | Google | 2016 | Google's production reliability principles and error budgets |

### 🔗 Online Resources

- [Circuit Breaker Pattern — Martin Fowler](https://martinfowler.com/bliki/CircuitBreaker.html)
- [Designing for Failure — AWS Well-Architected](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/design-to-withstand-component-failures.html)
- [Exponential Backoff and Jitter — AWS Architecture Blog](https://aws.amazon.com/blogs/architecture/exponential-backoff-and-jitter/)

---

## 11. Project Structure & Coding Standards

> **Goal:** Establish consistent, scalable code organization that any team member can navigate.
>
> 💡 *"Consistency is more important than personal preference. Pick a standard and enforce it."*

### ✅ TODO

#### Project Scaffold
- [ ] **Choose a folder organization strategy:**
  - **Feature-based** (recommended) — Group all code for a feature together: `features/orders/`
  - **Layer-based** — Group by technical role: `controllers/`, `services/`, `repositories/`
- [ ] **Define separation of concerns:**
  - Presentation layer — UI components, rendering only
  - Service layer — Business logic, no database access
  - Data access layer — Database queries only, no business logic
  - Utilities — Pure functions with no side effects
- [ ] **Define clear module boundaries** — Minimize coupling between modules

#### Naming Conventions
- [ ] **Document and enforce naming conventions:**
  - Files: `kebab-case`
  - Classes and components: `PascalCase`
  - Functions and variables: `camelCase`
  - Constants: `SCREAMING_SNAKE_CASE`
  - Database tables and columns: `snake_case`
  - Environment variables: `SCREAMING_SNAKE_CASE`

#### Code Quality Tooling
- [ ] **Configure a linter** — Enforce code style automatically (ESLint, Pylint, RuboCop, etc.)
- [ ] **Configure a formatter** — Auto-format on save (Prettier, Black, gofmt, etc.)
- [ ] **Set up pre-commit hooks** — Run lint and format checks before every commit
- [ ] **Enable strict type checking** — Use static types wherever the language supports it
- [ ] **Configure path aliases** — Avoid deep relative imports (`../../utils` → `@/utils`)

#### Commit Standards
- [ ] **Adopt Conventional Commits** — Industry-standard commit message format:
  ```
  feat: add product search endpoint
  fix: resolve cart quantity overflow
  docs: update API authentication guide
  refactor: extract order validation to service layer
  test: add unit tests for pricing calculator
  chore: update dependencies
  ```
- [ ] **Enforce commit format** — Use a commit linting tool (e.g., Commitlint)
- [ ] **Write meaningful commit messages** — The "why," not just the "what"

#### Documentation
- [ ] **Write a `README.md`** — Project overview, prerequisites, local setup instructions
- [ ] **Write a `CONTRIBUTING.md`** — Branch naming, commit format, PR process, review guidelines
- [ ] **Create an `.env.example`** — Template of all required environment variables (no values)
- [ ] **Document all non-obvious code decisions** — Inline comments for "why," not "what"

### 📌 Output

- `README.md` — Project overview and setup guide
- `CONTRIBUTING.md` — Development standards and process
- Linter, formatter, and type-check configuration files
- `docs/folder-structure.md` — Documented project organization

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Clean Code* | Robert C. Martin | 2008 | Naming, functions, comments, formatting, and code structure |
| *A Philosophy of Software Design* | John Ousterhout | 2018 | Managing complexity; deep vs. shallow modules |
| *The Pragmatic Programmer* (20th Ed) | Hunt & Thomas | 2019 | DRY, orthogonality, coding standards, and professionalism |
| [Conventional Commits Specification](https://www.conventionalcommits.org/) | Community Standard | 2024 | Industry-standard commit message format |

### 🔗 Online Resources

- [Google Engineering Practices Guide](https://google.github.io/eng-practices/) — Code review standards from Google
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Semantic Versioning (SemVer)](https://semver.org/) — Standard versioning specification

---

## 12. Development Roadmap

> **Goal:** Break the product into time-boxed, deliverable milestones with clear ownership.
>
> 💡 *"Fix time, flex scope."* — Shape Up, Basecamp

### Why This Matters

DORA (DevOps Research and Assessment) research, published in *Accelerate* (Forsgren et al., 2018), found that elite software teams deploy **973x more frequently** than low performers with **6,570x faster lead time from commit to deploy**. Structured roadmaps and small, frequent deliveries are a key enabler.

### ✅ TODO

#### Milestone Planning
- [ ] **Break the product into milestones:**
  - Milestone 0 — Project setup, tooling, CI/CD, environments
  - Milestone 1 — Core infrastructure (auth, database, skeleton app)
  - Milestone 2 — Primary MVP feature set
  - Milestone N — Additional features in priority order
- [ ] **Prioritize build order** — Foundation before features; always build bottom-up
- [ ] **Estimate effort** — Story points or time estimates per user story
- [ ] **Assign ownership** — Every task has a single owner (DRI: Directly Responsible Individual)

#### Definition of Done (DoD)
- [ ] **Define "Done" explicitly.** A task is only Done when:
  - [ ] Code is reviewed and approved
  - [ ] Tests are written and passing
  - [ ] Deployed to staging environment
  - [ ] Acceptance criteria are met and verified
  - [ ] Documentation is updated if needed

#### Process
- [ ] **Set up a project management tool** — GitHub Projects, Linear, Jira, or Notion
- [ ] **Create a sprint/cycle board** — Backlog → In Progress → In Review → Done
- [ ] **Hold regular retrospectives** — What went well? What to improve? What to try?
- [ ] **Track team velocity** — Measure throughput to improve estimation over time

### 📌 Output

- `docs/roadmap.md` — Milestone overview with target dates
- Project board in your chosen project management tool

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Shape Up* (Free online) | Ryan Singer, Basecamp | 2019 | 6-week cycles, betting table, hill charts, appetite |
| *Accelerate* | Forsgren, Humble, Kim | 2018 | Data-backed engineering metrics (DORA); deployment frequency, lead time |
| *Scrum: The Art of Doing Twice the Work in Half the Time* | Jeff Sutherland | 2014 | Sprint methodology and team velocity |

### 🔗 Online Resources

- [DORA Metrics](https://dora.dev/) — Industry benchmark for software delivery performance
- [Shape Up — Free Book](https://basecamp.com/shapeup)
- [Linear — Modern Project Management](https://linear.app/)

---

## 13. Testing Strategy

> **Goal:** Build confidence in your code through a layered, automated testing approach.
>
> 💡 *"Test early, test often, test automatically."*
> — The Pragmatic Programmer

### Why This Matters

IBM Systems Sciences Institute found that **the cost to fix a bug found in production is 100x higher** than fixing it during design. Automated testing is not overhead — it is the fastest path to sustainable velocity.

### The Test Pyramid

```
         /\
        /E2E\          ← Fewest | Slowest | Most expensive | Tests full user journeys
       /------\
      /  Integ  \      ← Service + data layer integration
     /------------\
    /  Unit Tests  \   ← Most | Fastest | Cheapest | Tests individual functions
   /----------------\
```

### ✅ TODO

#### Unit Tests
- [ ] **Test all pure business logic functions** — Pricing, validation, calculations, transformations
- [ ] **Test all utility/helper functions**
- [ ] **Write descriptive test names** — `should return 0 when cart is empty`, not `test1`
- [ ] **Target 80%+ coverage on business logic** — Coverage on pure logic, not total line coverage
- [ ] **Follow the AAA pattern** — Arrange, Act, Assert

#### Integration Tests
- [ ] **Test all API endpoints** — Request, response, and side effects with a real test database
- [ ] **Test all database queries** — Using test fixtures and seeded data
- [ ] **Test all authentication and authorization flows** — Login, refresh, access control
- [ ] **Test critical business workflows end-to-end at the service layer**

#### End-to-End (E2E) Tests
- [ ] **Write E2E tests for critical user journeys:**
  - User registration and onboarding flow
  - Core value-delivery flow (the primary reason users come to your product)
  - Any flow involving money or irreversible actions
- [ ] **Run E2E tests in the CI pipeline** — Not just locally
- [ ] **Test on multiple browsers** if applicable (Chrome, Firefox, Safari)

#### Manual Testing Checklist
- [ ] **Cross-browser testing** — Chrome, Firefox, Safari, Edge
- [ ] **Responsive testing** — Mobile (~375px), Tablet (~768px), Desktop (~1440px)
- [ ] **Accessibility testing** — axe DevTools, keyboard navigation, screen reader (NVDA/VoiceOver)
- [ ] **Performance testing** — Lighthouse audit: target ≥ 90 on Performance, Accessibility, Best Practices
- [ ] **Security testing** — OWASP ZAP automated scan before any public launch

### 📌 Output

- `tests/` or `__tests__/` — Test files organized to mirror source structure
- `docs/testing-plan.md` — Test scenarios, coverage goals, and testing responsibilities
- CI pipeline test reports

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *The Pragmatic Programmer* (20th Ed) | Hunt & Thomas | 2019 | Testing philosophy: test early, test automatically |
| *Unit Testing: Principles, Practices, and Patterns* | Vladimir Khorikov | 2020 | Distinguishes good tests from test theater |
| *Growing Object-Oriented Software, Guided by Tests* | Freeman & Pryce | 2009 | TDD from the outside in, with real examples |

### 🔗 Online Resources

- [The Testing Trophy — Kent C. Dodds](https://kentcdodds.com/blog/the-testing-trophy-and-testing-classifications) — Modern testing philosophy
- [OWASP Testing Guide v4.2](https://owasp.org/www-project-web-security-testing-guide/)
- [Google Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/) — Performance and quality auditing
- [axe DevTools](https://www.deque.com/axe/) — Accessibility testing

---

## 14. Deployment Plan

> **Goal:** Automate your path to production with repeatable, auditable, zero-downtime deployments.
>
> 💡 *"If it hurts, do it more often."* — Jez Humble, *Continuous Delivery*

### ✅ TODO

#### Environment Setup
- [ ] **Define and maintain four standard environments:**
  - `local` — Individual developer machine
  - `development` — Shared integration branch
  - `staging` — Production mirror; used for pre-release testing
  - `production` — Live system serving real users
- [ ] **Maintain environment parity** — Staging must be as close to production as possible (same config, same data shape)
- [ ] **Isolate secrets per environment** — Never share credentials or API keys across environments
- [ ] **Use an `.env.example` file** — Template of all required variables; no real values committed to version control

#### CI Pipeline (Continuous Integration)
- [ ] **Trigger on every pull request:**
  1. Install dependencies
  2. Static type checking
  3. Linting
  4. Unit tests
  5. Integration tests
  6. Build verification
- [ ] **Enforce CI gates on pull requests** — Merging requires all checks to pass

#### CD Pipeline (Continuous Deployment/Delivery)
- [ ] **On merge to main branch:**
  1. All CI checks pass
  2. Deploy to staging automatically
  3. Run E2E smoke tests on staging
  4. Deploy to production (automated or with manual approval gate)
  5. Run post-deploy health check
- [ ] **Set up preview environments** — Every pull request gets a temporary, isolated deployment URL
- [ ] **Define rollback strategy** — Must be executable in under 5 minutes

#### Database Migrations
- [ ] **Automate migrations** — Never run manually in production; trigger via CI/CD pipeline
- [ ] **Write backwards-compatible migrations** — Old code must still work during the deployment window:
  1. Add new column as nullable → deploy new code → backfill data → add constraint
- [ ] **Test all migrations on staging first**
- [ ] **Write a rollback migration** for every forward migration

#### Infrastructure Checklist
- [ ] **Configure custom domain with HTTPS** — SSL/TLS certificate with automatic renewal
- [ ] **Configure a CDN** for static assets
- [ ] **Set up automated database backups** — Daily at minimum; test restore procedure quarterly
- [ ] **Configure uptime monitoring** — Alert within 60 seconds of downtime
- [ ] **Document all environment variables** — In `docs/env-vars.md`, without values

### 📌 Output

- `ci.yml` / `deploy.yml` — CI/CD pipeline configuration (e.g., GitHub Actions)
- `docs/deployment.md` — Deployment runbook
- `docs/rollback.md` — Step-by-step rollback procedure

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Continuous Delivery* | Humble & Farley | 2010 | The foundational book on automated, reliable software delivery |
| *Accelerate* | Forsgren, Humble, Kim | 2018 | Data-backed evidence for deployment frequency and stability |
| *The DevOps Handbook* | Kim, Humble, Debois, Willis | 2016 | DevOps principles, three ways, and feedback loops |

### 🔗 Online Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [The 12-Factor App — Config and Backing Services](https://12factor.net/config)
- [Zero-Downtime Database Migrations — Braintree Engineering](https://www.braintreepayments.com/blog/safe-operations-for-high-volume-postgresql/)
- [DORA Deployment Frequency Metric](https://dora.dev/guides/dora-metrics-four-keys/)

---

## 15. Monitoring & Observability

> **Goal:** Know when something breaks in production before your users report it.
>
> 💡 *"You can't fix what you can't see."*

### The Three Pillars of Observability

```
┌─────────────┬──────────────────────────────────────────────┐
│  Metrics    │ What is happening? (latency, error rate,     │
│             │ throughput, resource usage)                   │
├─────────────┼──────────────────────────────────────────────┤
│  Logs       │ Why is it happening? (request context,       │
│             │ error details, user actions, stack traces)    │
├─────────────┼──────────────────────────────────────────────┤
│  Traces     │ Where is it happening? (which service,       │
│             │ which function, which database query)         │
└─────────────┴──────────────────────────────────────────────┘
```

### ✅ TODO

#### Logging
- [ ] **Use structured logging** — JSON format; never plain text in production
- [ ] **Apply appropriate log levels** — ERROR, WARN, INFO, DEBUG
- [ ] **Attach correlation/trace IDs** — Trace a single request across multiple services and log lines
- [ ] **Never log sensitive data** — Passwords, tokens, PII, payment card data
- [ ] **Set up log aggregation** — Centralize logs from all services into one searchable system

#### Error Tracking
- [ ] **Integrate an error tracking system** — Captures, groups, and alerts on application errors
- [ ] **Set up error alerting** — Notify team on new errors or regressions in error rate
- [ ] **Add user context to errors** — User ID, session, relevant state (no PII)
- [ ] **Track error rates over time** — Define an acceptable error rate threshold (e.g., < 0.1%)

#### Performance Monitoring
- [ ] **Track key performance indicators:**
  - API response time: P50, P95, P99 (target P99 < 2s)
  - Frontend Web Vitals: LCP, INP, CLS (Google Core Web Vitals)
  - Database query times: identify slow queries
- [ ] **Set up alerts for latency spikes and performance regressions**

#### Business Analytics
- [ ] **Track key user events** — Signups, activations, purchases, core feature usage
- [ ] **Set up funnel analysis** — Identify where users drop off in key flows
- [ ] **Track your primary KPIs from Phase 1** — Validate against original success metrics

#### Uptime & SLOs
- [ ] **Set up uptime monitoring** — External health check every 60 seconds
- [ ] **Define Service Level Objectives (SLOs):**
  - e.g., 99.9% availability (allows ~8.7 hours downtime/year)
  - e.g., P99 API response time < 2 seconds
- [ ] **Define an on-call process** — Who responds to production incidents?
- [ ] **Write runbooks** — Step-by-step procedures for common incident types

### 📌 Output

- `docs/monitoring.md` — Monitoring stack, alert thresholds, and SLO definitions
- `docs/runbooks/` — Incident response procedures
- Observability dashboards (metrics + errors + uptime)

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *Site Reliability Engineering* (Free online) | Google | 2016 | SRE practices, SLOs, error budgets, toil reduction |
| *Observability Engineering* | Charity Majors, Liz Fong-Jones, George Miranda | 2022 | Modern, event-based observability beyond metrics and logs |
| *The Art of Monitoring* | James Turnbull | 2016 | Practical monitoring, alerting, and dashboarding |

### 🔗 Online Resources

- [Google SRE Book — Free Online](https://sre.google/sre-book/table-of-contents/)
- [OpenTelemetry](https://opentelemetry.io/) — Vendor-neutral observability standard (CNCF project)
- [Google Core Web Vitals](https://web.dev/vitals/) — LCP, INP, CLS explained
- [SLO Guide — Google SRE Workbook](https://sre.google/workbook/implementing-slos/)

---

## 16. Security Checklist

> **Goal:** Protect your users' data and your system from common, preventable attacks.
>
> 💡 *"Security by design, not security as an afterthought."*

### OWASP Top 10 — 2021 (Industry Standard)

The Open Worldwide Application Security Project (OWASP) Top 10 is the globally recognized standard reference for web application security. Updated in 2021.

| Rank | Risk | Required Mitigation |
|------|------|---------------------|
| A01 | **Broken Access Control** | Enforce RBAC server-side on every request; deny by default |
| A02 | **Cryptographic Failures** | TLS on all connections; Argon2/bcrypt for passwords; encrypt PII at rest |
| A03 | **Injection (SQL, XSS, etc.)** | Parameterized queries; sanitize all inputs; Content Security Policy header |
| A04 | **Insecure Design** | Threat modeling; security requirements defined in design phase |
| A05 | **Security Misconfiguration** | Remove defaults and unused features; harden all environments |
| A06 | **Vulnerable Components** | Run dependency vulnerability scans; keep dependencies updated |
| A07 | **Auth & Session Failures** | httpOnly cookies; short token lifetimes; invalidate on logout |
| A08 | **Software Integrity Failures** | Use dependency lockfiles; verify checksums for third-party assets |
| A09 | **Logging & Monitoring Failures** | Log all auth events; alert on anomalies; maintain audit trails |
| A10 | **SSRF** | Validate and allowlist external URLs; block access to internal IP ranges |

### ✅ TODO

#### Input & Output
- [ ] **Validate on both client AND server** — Client validation is UX; server validation is security
- [ ] **Use a validation library** — Schema-based validation for all inputs
- [ ] **Sanitize all HTML output** — Never render unsanitized user-provided HTML
- [ ] **Validate file uploads** — File type, size, and content

#### Password & Credential Security
- [ ] **Hash passwords with bcrypt or Argon2** — Never MD5, SHA1, or unsalted SHA256
- [ ] **Enforce minimum password length** — 12 characters minimum (NIST SP 800-63B)
- [ ] **Check passwords against known breach databases** — Have I Been Pwned API
- [ ] **Rate limit all authentication endpoints** — Prevent credential stuffing and brute force
- [ ] **Offer Multi-Factor Authentication (MFA)**

#### API & Transport Security
- [ ] **Enforce HTTPS** — Redirect all HTTP to HTTPS; HSTS header
- [ ] **Rate limit all public API endpoints** — Per IP and per authenticated user
- [ ] **Configure CORS correctly** — Allowlist only known, trusted origins
- [ ] **Implement all recommended security headers:**
  ```
  Content-Security-Policy: default-src 'self'
  X-Frame-Options: DENY
  X-Content-Type-Options: nosniff
  Strict-Transport-Security: max-age=31536000; includeSubDomains
  Referrer-Policy: strict-origin-when-cross-origin
  Permissions-Policy: geolocation=(), microphone=()
  ```
- [ ] **Never expose internal error details in production** — Generic messages to users; full details in server logs only

#### Data Protection
- [ ] **Encrypt sensitive data at rest** — PII, financial data, health data
- [ ] **Apply data minimization** — Do not collect or store what you do not need
- [ ] **Define a data retention policy** — When is data deleted?
- [ ] **Understand applicable regulations** — GDPR (EU), PDPA (Indonesia/Thailand/Singapore), CCPA (California), PCI DSS (payment cards)

#### Pre-Launch Security Scan
- [ ] **Run automated security scan** — OWASP ZAP or equivalent
- [ ] **Check security headers** — securityheaders.com
- [ ] **Run dependency vulnerability scan** — `npm audit`, Snyk, or Dependabot
- [ ] **Review authentication flows** against OWASP Auth Cheat Sheet

### 📌 Output

- `docs/security-checklist.md` — Pre-launch security review checklist
- `docs/threat-model.md` — Identified threats, attack vectors, and mitigations

### 📚 References

| Resource | Author/Source | Year | Why Relevant |
|----------|--------------|------|-------------|
| [OWASP Top 10](https://owasp.org/Top10/) | OWASP | 2021 | The globally recognized web application security standard |
| [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) | OWASP | 2024 | Actionable implementation guidance for every security concern |
| [NIST SP 800-63B](https://pages.nist.gov/800-63-3/sp800-63b.html) | NIST | 2020 | US government digital identity and password guidelines |
| *The Web Application Hacker's Handbook* (2nd Ed) | Stuttard & Pinto | 2011 | Understanding attack vectors from a hacker's perspective |

### 🔗 Online Resources

- [OWASP Top 10](https://owasp.org/Top10/) — 2021 edition
- [OWASP ZAP — Free Security Scanner](https://www.zaproxy.org/)
- [Security Headers Scanner](https://securityheaders.com/)
- [Mozilla Observatory — Free Security Scanner](https://observatory.mozilla.org/)
- [Have I Been Pwned API](https://haveibeenpwned.com/API/v3)
- [Snyk — Dependency Vulnerability Scanning](https://snyk.io/)

---

## 17. Post-Launch & Iteration

> **Goal:** Turn launch into the beginning of a learning engine, not the finish line.
>
> 💡 *"Launch is not the end. It is when real learning begins."*

### Why This Matters

Eric Ries' Build-Measure-Learn loop in *The Lean Startup* (2011) is one of the most widely adopted product development principles in the industry. The fastest way to build the right product is to ship, measure, and iterate — not to plan indefinitely.

### ✅ TODO

#### Week 1 — Stabilize
- [ ] **Monitor error rates** — Target < 0.1% error rate on critical paths
- [ ] **Monitor performance in production** — Validate against staging benchmarks
- [ ] **Respond to P0/P1 bugs within 24 hours**
- [ ] **Gather immediate user feedback** — Support tickets, NPS surveys, direct outreach

#### Week 2–4 — Learn
- [ ] **Analyze user behavior data** — Funnel analysis, session recordings, heatmaps
- [ ] **Identify top user pain points** from support tickets and drop-off analysis
- [ ] **Run the first retrospective** — What went well, what to improve, what to stop doing
- [ ] **Validate KPIs against the original success metrics from Phase 1**

#### Ongoing Iteration Loop
```
        ┌──────────┐
        │  BUILD   │ ← Smallest increment that tests a hypothesis
        └────┬─────┘
             │
        ┌────▼─────┐
        │ MEASURE  │ ← Instrument with metrics and qualitative feedback
        └────┬─────┘
             │
        ┌────▼─────┐
        │  LEARN   │ ← Validated learning: pivot, persevere, or stop
        └────┬─────┘
             │
             └──────────► Back to BUILD
```

- [ ] **Establish a continuous feedback loop** — User feedback → Backlog → Prioritization → Build
- [ ] **Track feature usage** — Which features are actively used? Which are ignored?
- [ ] **Deprecate unused features** — Unused code is maintenance burden and security surface area
- [ ] **Make data-driven roadmap decisions** — Usage data and user feedback over internal opinions

### 📌 Output

- `docs/post-launch-report.md` — Week 1 metrics, issues, and early learnings
- Updated product backlog based on real user data

### 📚 References

| Resource | Author | Year | Why Relevant |
|----------|--------|------|-------------|
| *The Lean Startup* | Eric Ries | 2011 | Build-Measure-Learn loop; pivot vs. persevere |
| *Continuous Discovery Habits* | Teresa Torres | 2021 | Weekly user research and opportunity trees for ongoing discovery |
| *Lean Analytics* | Croll & Yoskovitz | 2013 | Which metrics matter at each stage of product growth |

### 🔗 Online Resources

- [Build-Measure-Learn — Lean Startup Co.](https://theleanstartup.com/principles)
- [HEART Framework — Google](https://research.google/pubs/measuring-the-user-experience-on-a-large-scale-user-interface/) — Happiness, Engagement, Adoption, Retention, Task success
- [Amplitude Blog — Product Analytics](https://amplitude.com/blog)

---

## 📊 Master Progress Checklist

| # | Phase | Status | Primary Output |
|---|-------|--------|----------------|
| 1 | Product Discovery & Definition | ⬜ | Product Brief, Personas |
| 2 | Feature Scoping (MVP) | ⬜ | Prioritized Feature List, User Stories |
| 3 | User Flow & Journey Mapping | ⬜ | Flow Diagrams, Screen Inventory |
| 4 | Data Modeling | ⬜ | ERD, Data Dictionary, DB Schema |
| 5 | System Architecture | ⬜ | Architecture Diagram, ADRs, Tech Stack |
| 6 | Auth & Authorization | ⬜ | Auth Flow Diagram, RBAC Matrix |
| 7 | Business Logic | ⬜ | Business Rules Doc, State Machines |
| 8 | API Design | ⬜ | OpenAPI Spec, API Docs |
| 9 | UI/UX Design | ⬜ | Wireframes, Design System |
| 10 | Edge Case Planning | ⬜ | Edge Case Checklist, Error Messages |
| 11 | Project Structure & Standards | ⬜ | Scaffold, README, CONTRIBUTING |
| 12 | Development Roadmap | ⬜ | Milestone Plan, Project Board |
| 13 | Testing Strategy | ⬜ | Test Suite, Testing Plan |
| 14 | Deployment Plan | ⬜ | CI/CD Pipeline, Deployment Runbook |
| 15 | Monitoring & Observability | ⬜ | Dashboards, Alerts, Runbooks |
| 16 | Security | ⬜ | Security Checklist, Threat Model |
| 17 | Post-Launch & Iteration | ⬜ | Post-Launch Report, Updated Backlog |

---

## 📚 Master Reference Library

### Essential Books

| Book | Author | Year | Category |
|------|--------|------|----------|
| *Inspired* (2nd Ed) | Marty Cagan | 2018 | Product Management |
| *The Lean Startup* | Eric Ries | 2011 | Product Strategy |
| *The Mom Test* | Rob Fitzpatrick | 2013 | User Research |
| *Continuous Discovery Habits* | Teresa Torres | 2021 | Product Discovery |
| *Escaping the Build Trap* | Melissa Perri | 2018 | Product Thinking |
| *Shape Up* (Free) | Ryan Singer | 2019 | Project Management |
| *User Story Mapping* | Jeff Patton | 2014 | Requirements |
| *Don't Make Me Think* (3rd Ed) | Steve Krug | 2014 | UX Design |
| *Refactoring UI* | Wathan & Schoger | 2018 | UI Design |
| *Atomic Design* (Free) | Brad Frost | 2016 | Design Systems |
| *Laws of UX* | Jon Yablonski | 2020 | Design Psychology |
| *Designing Data-Intensive Applications* | Martin Kleppmann | 2017 | Data & Systems |
| *Clean Architecture* | Robert C. Martin | 2017 | Software Architecture |
| *Fundamentals of Software Architecture* | Richards & Ford | 2020 | Architecture |
| *Domain-Driven Design* | Eric Evans | 2003 | Business Logic |
| *Implementing DDD* | Vaughn Vernon | 2013 | Business Logic |
| *The Pragmatic Programmer* (20th Ed) | Hunt & Thomas | 2019 | Engineering Practices |
| *Clean Code* | Robert C. Martin | 2008 | Code Quality |
| *A Philosophy of Software Design* | John Ousterhout | 2018 | Code Complexity |
| *Release It!* (2nd Ed) | Michael Nygard | 2018 | Production Reliability |
| *Continuous Delivery* | Humble & Farley | 2010 | Deployment |
| *Accelerate* | Forsgren, Humble, Kim | 2018 | Engineering Metrics |
| *The DevOps Handbook* | Kim, Humble, Debois, Willis | 2016 | DevOps |
| *Site Reliability Engineering* (Free) | Google | 2016 | Operations |
| *Observability Engineering* | Majors, Fong-Jones, Miranda | 2022 | Observability |
| *Unit Testing: Principles, Practices, Patterns* | Vladimir Khorikov | 2020 | Testing |
| *The Design of Web APIs* | Arnaud Lauret | 2019 | API Design |
| *OAuth 2 in Action* | Richer & Sanso | 2017 | Auth |

### Essential Online Standards & References

| Resource | URL | Category |
|----------|-----|----------|
| OWASP Top 10 (2021) | https://owasp.org/Top10/ | Security |
| OWASP Cheat Sheet Series | https://cheatsheetseries.owasp.org/ | Security |
| NIST SP 800-63B (Passwords) | https://pages.nist.gov/800-63-3/sp800-63b.html | Security |
| OpenAPI 3.1 Specification | https://spec.openapis.org/oas/v3.1.0 | API Design |
| WCAG 2.1 Guidelines | https://www.w3.org/WAI/WCAG21/quickref/ | Accessibility |
| Conventional Commits | https://www.conventionalcommits.org/ | Version Control |
| Semantic Versioning | https://semver.org/ | Version Control |
| C4 Model (Architecture) | https://c4model.com/ | Architecture |
| ADR Format | https://adr.github.io/ | Architecture |
| The 12-Factor App | https://12factor.net/ | Cloud / DevOps |
| DORA Metrics | https://dora.dev/ | Engineering Performance |
| Google SRE Book (Free) | https://sre.google/sre-book/ | Operations |
| OpenTelemetry | https://opentelemetry.io/ | Observability |
| Google Core Web Vitals | https://web.dev/vitals/ | Performance |
| Laws of UX | https://lawsofux.com/ | Design |
| Nielsen Norman Group | https://www.nngroup.com/ | UX Research |
| System Design Primer | https://github.com/donnemartin/system-design-primer | Architecture |
| Google Engineering Practices | https://google.github.io/eng-practices/ | Code Review |

---

> **About this guide:**
> This template follows industry standards and practices referenced from OWASP, NIST, W3C, IETF, Google, Microsoft, ThoughtWorks, and peer-reviewed engineering practices from leading technology organizations.
>
> It is intentionally technology-agnostic. The concepts in this guide apply regardless of programming language, framework, or cloud provider chosen.
>
> Last validated against: OWASP Top 10 (2021), WCAG 2.1 (W3C), OpenAPI 3.1, DORA Research (2023), 12-Factor App methodology, and C4 Model (2023 revision).
