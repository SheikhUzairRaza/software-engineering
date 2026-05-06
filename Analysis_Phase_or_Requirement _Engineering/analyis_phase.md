# Software Engineering Notes – Requirements Engineering

---

## 🔷 Analysis Phase

The Analysis Phase is the first stage of software development.

**Purpose:**
- Understand customer requirements
- Define system behavior
- Identify system users (stakeholders)

This process is called **Requirements Engineering**.

---

## 🔷 Goals of Requirements Engineering

- Understand customer needs correctly
- Document requirements clearly
- Avoid misunderstanding and confusion
- Ensure correct system development

---

## 🔷 Common Problems in Requirements Engineering

### Problem 1: Ambiguous Requirements

Requirements are often expressed in natural language, which can have multiple meanings.

📌 **Example:**
> "System should be fast"

❓ What does "fast" mean — 1 second? 5 seconds? 10 seconds?

👉 Developer and customer may interpret this differently.

---

### Problem 2: Unorganized Requirements

Requirements are often written in random order with no proper structure or grouping.

📌 **Example:** Login, Payment, and Profile features all listed together with no relationships defined.

👉 This makes it hard to understand dependencies and plan development.

---

### Problem 3: No Verification

Requirements are written but never confirmed with the customer.

📌 **Example:** Customer asks for a "simple dashboard" but developer builds a complex one.

👉 Customer rejects it because it doesn't match what they asked for.

---

### Problem 4: No Change Control

Customers frequently request new features after requirements are defined.

📌 **Example:** After agreeing on Login, Dashboard, and Reports — the customer later requests Chat and AI features.

👉 Project scope keeps increasing and development becomes unstable.

---

## 🔷 Solution: Requirement Freeze (Baseline)

A fixed point is defined after which requirements cannot be changed freely.

📌 **Example:** Changes allowed for 6 months; after that, requirements are locked.

If a change is requested after the freeze:
- Impact is analyzed
- Cost and time are evaluated
- Decision is made: **Accept / Reject / Postpone**

---

## 🔷 Hidden Risk: Unauthorized Changes

If someone changes requirements without informing the manager:
- Team confusion arises
- Dependencies break
- Project failure risk increases

**Solution: Change Control Board (CCB)**

Responsibilities:
- Approve or reject changes
- Analyze impact
- Maintain project stability

---

## 🔷 Why These Problems Are Dangerous

Poor requirements lead to:
- Incorrect software
- Increased cost
- Time delays
- Customer dissatisfaction

> Most software failures occur due to unclear requirements, poor communication, and lack of validation.

---

## 🔷 Correct Approach

1. Understand requirements first
2. Document them properly
3. Verify with customer
4. Control changes
5. Then start development

---

## 🔷 Requirement Management

Requirement Management is the process of controlling and handling changes in software requirements during development.

**Core Principle:** Every requirement change must go through evaluation before approval.

### Impact Analysis

Before accepting any change, the team checks:
- Which parts of the system will be affected
- Whether existing features will break
- Cost and time required
- Technical feasibility

### Example Scenarios

**Scenario 1 – Simple Change:** Feature is isolated with few dependencies → Low impact → Change accepted easily.

**Scenario 2 – Complex Change:** Feature is connected to database, login, and payment → High risk → Must be carefully analyzed before accepting.

---

## 🔷 Requirements Engineering is NOT Sequential

The main activities — **Inception**, **Elicitation**, and **Elaboration** — do not happen in strict order. They run in parallel.

📌 **Example:** While talking to the customer (elicitation), notes are being written (elaboration) and scope is being defined (inception) — all at the same time.

---

## 🔷 Inception Phase

Inception is the initial phase focused on **understanding the problem**, not collecting full requirements.

### Activities:
- Understand the basic idea of the project
- Identify stakeholders
- Define system scope
- Establish communication with the customer

### Types of Inception Questions

**Group 1 – Stakeholders & Goals**
- Who requested the project?
- Who will use the system?
- What benefits will it provide?

📌 **Example (ERP System):**
- HR → attendance
- Finance → salary/accounts
- Management → reports

Benefits: automation, transparency, reduced paperwork.

**Group 2 – Problem Understanding**
- What is a good output?
- What problems will the system solve?
- In what environment will it be used?
- What are the constraints?

📌 **Example (Factory):** 150 employees access biometric system at the same time → Slowdowns and queues occur → System must handle load efficiently.

**Group 3 – Communication Check**
- Am I talking to the right person?
- Is the information official?
- Is anything missing?

> Final check: *"Anything else to add?"*

---

## 🔷 Elicitation Phase

In this phase, very specific questions are asked and system behavior is defined in detail.

### Challenges in Elicitation

1. **Scope Problem** – Discussions drift into technical details and lose focus on main goals.
2. **Missing Real-World Context** – Some "obvious" things are actually not obvious in practice.
3. **Changing Requirements** – Customers often request changes during or after this phase.

---

## 🔷 Collaborative Requirement Gathering

Instead of interviewing stakeholders separately, all stakeholders meet together in a single structured session.

### Why Individual Elicitation Falls Short

- **Overlapping Information** – Multiple stakeholders repeat the same requirements.
- **Inconsistency** – Different stakeholders provide conflicting statements (e.g., one says attendance is manual, another says it's automated).

### How Collaborative Gathering Works

All stakeholders (engineers, customers, departments) meet together. Each shares their requirements, expected behavior, and existing problems. A **facilitator/moderator** manages the session to control discussion flow, resolve conflicts, and ensure equal participation.

📌 **Example Stakeholders (University System):**
- HR, Administration, Examination Department, Faculty, Student Representatives

### Benefits

- Clear shared understanding
- Reduced confusion and conflicting interpretations
- Better collective decision-making
- Discovery of hidden requirements

### Recording Requirements

Everything discussed must be recorded using sticky notes, flip charts, worksheets, or digital tools — to prevent missing requirements.

> 👉 *"Better requirements come from shared discussion, not isolated conversations."*

---

## 🔷 Quality Function Deployment (QFD)

QFD is a structured method for converting customer needs into technical design requirements.

- Customer says **WHAT** they want
- Engineers define **HOW** to build it

### House of Quality (Matrix)

| Customer Requirements (WHATs) | Technical Requirements (HOWs) |
|-------------------------------|-------------------------------|
| Safe product | Smaller casing |
| Durable product | Fewer gears |
| Easy to use | Strong battery system |
| Low cost | Manual override |
| Lightweight | LED indicator |
| Long battery life | Grip design |

### Relationship Mapping

WHATs are mapped to HOWs to identify:
- ➕ **Positive relationships** – One feature improves another
- ➖ **Negative relationships** – One feature improves something but harms another (trade-offs)

📌 **Example (Can Opener):**
- Smaller casing → Easier to use ✔️ but Reduced safety ❌
- Fewer gears → Cheaper ✔️
- Strong battery → Longer battery life ✔️

### Additional QFD Elements

- **Competitor Comparison** – Identify strengths and weaknesses relative to competing products
- **Target Values** – Assign measurable specs to each technical feature (e.g., size = 5 cm, battery = 6 hours, weight = 200g) to remove ambiguity
- **Prioritization** – Assign weights to features (e.g., high priority = 30–40%) to focus on what matters most

### Types of Requirements in QFD

| Type | Description | Example (Pen) |
|------|-------------|---------------|
| Normal | Basic features that must exist | Writes properly |
| Expected | Features customers assume will be there | Smooth ink |
| Exciting | Extra features that delight users | Stylish design, long-lasting ink |

---

## 🔚 Final Summary

| Concept | Purpose |
|--------|---------|
| Requirements Engineering | Correct understanding, documentation, and validation of customer needs |
| Requirement Management | Controlled handling of changes with proper impact analysis |
| Inception | Basic understanding of project scope and stakeholders |
| Elicitation | Detailed requirements gathering |
| Collaborative Gathering | Group-based elicitation to reduce inconsistency |
| QFD | Converting customer WHATs into technical HOWs |

> **Good software is built when requirements are not only gathered, but properly understood, analyzed, and managed with impact awareness.**