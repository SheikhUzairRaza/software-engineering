# Software Quality Assurance

---

## Part 1: Recap of Software Testing (Previous Repo)

Before diving into Software Quality Assurance, this lecture begins with a thorough recap of what was covered in the software testing lectures.

---

### 1.1 What is Software Testing?

Software testing is the process of running a program to ensure it produces **consistent and accurate results**. It is distinct from fixing compile-time or link-time errors — those are syntax/structural issues caught by the compiler itself. Testing addresses **runtime behavior and logical correctness**.

**Common types of errors testing addresses:**

- Inconsistent output for the same input
- Improper file handling
- Incorrect report generation
- Performance inconsistencies

**Goal:** Ensure the software behaves correctly and predictably under defined conditions.

---

### 1.2 Who Does Testing?

There are **three categories of people** responsible for testing:

| Role                       | Type of Testing    | Description                                              |
| -------------------------- | ------------------ | -------------------------------------------------------- |
| **Software Testers** | Formal testing     | Designated QA professionals whose primary job is testing |
| **Developers**       | White Box Testing  | Test the internal logic of the code they wrote           |
| **End Users**        | Acceptance Testing | Validate the product against their real-world needs      |

> **Note:** The *customer* and the *end user* are not always the same person. The customer may be the decision-maker who pays for the software, while end users are the people who actually operate the system day-to-day.

---

### 1.3 Goals of Software Testing

There are **two primary goals**:

1. **Efficiency** – Measures how well your internal team (developers and testers) is performing.

   - Track how many bugs each tester finds per build.
   - Track how many errors each developer introduces per build.
   - Use these metrics to evaluate and improve team performance.
2. **Credibility** – Aimed at the customer/market.

   - Demonstrates that your product is reliable and high-quality.
   - Builds your company's reputation so customers recommend you to others.

---

### 1.4 Software Testing Process (6 Steps)

| Step | Name                                     | Description                                                                                                                                         |
| ---- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Requirement Study**              | Understand what requirements were gathered. Testing criteria is based on these requirements. Also consult design documents for field-level details. |
| 2    | **Analysis & Planning**            | Plan testing dates, resources needed, how bugs will be reported, timelines for developers to fix bugs.                                              |
| 3    | **Test Case Design & Development** | Write detailed test cases based on requirements and design documents.                                                                               |
| 4    | **Test Execution**                 | Actually run the test cases on the software.                                                                                                        |
| 5    | **Test Closure**                   | Finalize testing, generate reports (bugs found, severity levels, developer-wise bug counts).                                                        |
| 6    | **Test Process Analysis**          | Analyze testing metrics to improve the process for future projects.                                                                                 |

---

### 1.5 Levels of Testing

| Level                         | Who Performs It      | Technique Used                             | Scope                                                         |
| ----------------------------- | -------------------- | ------------------------------------------ | ------------------------------------------------------------- |
| **Unit Testing**        | Developers           | White Box Testing                          | Individual functions or classes — the smallest testable unit |
| **Integration Testing** | Developers / Testers | White Box, Incremental, Incremental Thread | Multiple modules combined and tested together                 |
| **System Testing**      | Software Testers     | Black Box Testing                          | The entire completed product tested end-to-end                |
| **Acceptance Testing**  | End Users            | Black Box Testing                          | Final validation against requirements before sign-off         |

---

### 1.6 Testing Techniques / Methods

#### A. White Box Testing

- Tests the **internal logic** of the code.
- The tester/developer needs to know how the code is written.
- Goal: Ensure every line of code is executed at least once.
- Performed by: **Developers**.
- Used at: **Unit Testing** and **Integration Testing** levels.
- Formal test cases are typically **not written** for white box testing since the developer tests their own code.

#### B. Black Box Testing

- **Data-driven** — focuses on functionality, not internal code.
- Input data is sent in; output data is compared against expected results.
- Tester does **not** need to know internal implementation.
- Used at: **System Testing** and **Acceptance Testing** levels.

**Sub-types of Black Box Testing:**

| Sub-type                                      | Description                                                                             |
| --------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Installation/Uninstallation Testing** | Verifies the software installs and uninstalls correctly across different configurations |
| **Load Testing**                        | Tests behavior under expected user loads                                                |
| **Performance Testing**                 | Measures speed, responsiveness, and stability                                           |
| **Stress Testing**                      | Tests behavior under extreme conditions beyond normal capacity                          |
| **Sanity Testing**                      | Quick preliminary testing to check if the product is stable enough for full testing     |
| **System Testing**                      | Full end-to-end functional test of the complete system                                  |
| **Acceptance Testing**                  | End-user validation of the product                                                      |

#### C. Incremental & Thread Testing

- Used primarily in **Agile** development models.
- **Incremental Testing:** When a new increment (version) of the software is released, re-test existing functionality to ensure nothing was broken by new changes.
- **Incremental Thread Testing:** Test a *logical path* through multiple modules. If a report passes through Modules A → B → C, that entire logical "thread" is tested after any changes.

---

### 1.7 Testing Matrix

|                               | White Box | Black Box | Incremental | Incremental Thread |
| ----------------------------- | --------- | --------- | ----------- | ------------------ |
| **Unit Testing**        | ✓        |           |             |                    |
| **Integration Testing** | ✓        |           | ✓          | ✓                 |
| **System Testing**      |           | ✓        |             |                    |
| **Acceptance Testing**  |           | ✓        |             |                    |

---

### 1.8 Writing Test Cases

A **test case** is a sequence of steps executed to verify that a specific functionality works correctly. Test cases formalize the testing process so anyone familiar with computers can execute them — not just experienced testers.

> White box testing does **not** require formal written test cases (developer tests their own code). Black box testing **does** require written test cases.

**Key fields in a test case:**

| Field                                        | Description                                                       |
| -------------------------------------------- | ----------------------------------------------------------------- |
| **Unique ID**                          | A unique identifier for the test case                             |
| **Requirement ID**                     | Which requirement this test case is testing                       |
| **Test Conditions & Expected Results** | What conditions are set up and what the expected output should be |
| **Test Data**                          | The specific input data needed to run the test                    |
| **Test Steps**                         | Step-by-step instructions to execute the test                     |
| **Actual Results**                     | What the system actually produced (filled in during execution)    |
| **Notes / Developer Questions**        | Observations, questions, or comments                              |

**Additional optional fields:**

- Test setup (pre-conditions)
- Post-execution activities (restoring original state)
- Per-step expected and actual results
- Timestamps
- Version/revision numbers (who changed this test case and when)

**Well-written vs. poorly written test cases:**

- A **high-level** test case assumes the executor is experienced — this is a weakness.
- A **detailed** test case enables even a moderately computer-literate person to run it correctly — this is the goal.

---

---

## Part 2: Software Quality Assurance (SQA) — Main Topic of this module

---

### 2.1 What is Software Quality Assurance?

**Software Quality Assurance (SQA)** is an **umbrella activity** — it spans the entire software development lifecycle, not just one phase.

> Think of it like an umbrella that covers everything underneath: requirements, design, implementation, testing, and deployment. Quality must be ensured at **every single stage**.

**Why is it called an umbrella activity?**

Because you cannot say "we only need quality in testing" or "quality only matters in implementation." If quality is neglected at any phase, defects accumulate and become exponentially more expensive to fix later.

**SQA must be present in:**

- Requirements gathering (Analysis)
- Design
- Implementation (Coding)
- Testing
- Deployment & Support

---

### 2.2 What is Quality?

Quality is not a vague concept — it refers to **measurable characteristics** of a product.

**Key Quality Characteristics:**

| Characteristic             | Description                                                                       |
| -------------------------- | --------------------------------------------------------------------------------- |
| **Correctness**      | Does the product do what it is supposed to do? (Measured by number of bugs found) |
| **Maintainability**  | How easily can the product be modified or updated?                                |
| **Portability**      | Does it run on different devices, OS, and networks?                               |
| **Testability**      | How easily can the product be tested?                                             |
| **Usability**        | How quickly can an average user be trained to use it effectively?                 |
| **Reliability**      | How rarely does the product crash or fail over time?                              |
| **Efficiency**       | How well does it use system resources?                                            |
| **Integrity**        | How well does it protect data from unauthorized access?                           |
| **Interoperability** | How well does it work with other systems?                                         |

If a product excels in these measurable characteristics, it is considered **high quality**.

---

### 2.3 Quality Terminology

| Term                               | Definition                                                                                                                              |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Quality of Design**        | The characteristics that designers specify for the product. Sets the target quality standard.                                           |
| **Quality of Conformance**   | The degree to which the final product follows/matches the design specifications during manufacturing/implementation.                    |
| **Quality Control**          | The series of inspections, reviews, and tests used throughout the development cycle to ensure each work product meets its requirements. |
| **Quality Policy**           | The organization's overall aims and objectives regarding quality — set by top management. Acts as a guideline for quality control.     |
| **Quality Assurance**        | The auditing and reporting function of management — monitoring whether quality is being achieved and reporting on it.                  |
| **Cost of Quality**          | All costs incurred in pursuing quality: appraisal costs, internal failure costs, and external failure costs.                            |
| **Quality Planning**         | Assessing the procedures and context in which quality requirements must be observed for a specific project.                             |
| **Quality Testing**          | Assessment of the extent to which a test object meets given requirements.                                                               |
| **Quality Assurance Plan**   | A documented plan that serves as the central guide for planning and checking quality assurance activities.                              |
| **Quality Assurance System** | The organizational structure, responsibilities, procedures, processes, and resources for implementing quality management.               |

---

### 2.4 The Cost of Errors — Why Find Bugs Early?

One of the most critical insights in software engineering is the **exponential increase in the cost of fixing errors** the later they are discovered.

| Stage Error is Found                       | Relative Cost to Fix   |
| ------------------------------------------ | ---------------------- |
| **Requirements**                     | 1× (baseline)         |
| **Design**                           | 3–6×                 |
| **Coding / Implementation**          | 10×                   |
| **Testing (Integration/System)**     | 15–70×               |
| **After Deployment (Customer Site)** | **Up to 1000×** |

**Key Lesson:** Finding a defect at the requirements stage is a thousand times cheaper than finding it after the product has been delivered to the customer.

**Real-world example:** Companies like Toyota have had to recall entire product lines (e.g., refrigerators with faulty compressors) because defects were discovered after delivery. The cost — financial and reputational — was enormous.

**How do we find errors early?**
By implementing proper **Software Quality Assurance** practices at every stage of development.

---

### 2.5 Elements of Software Quality Assurance

These are the building blocks that together ensure a product is of acceptable quality:

#### 1. Standards

Formal standards define the minimum level of quality expected.

- **ISO 9001 / 9002** — International quality management standards. Companies get certified to demonstrate their processes meet global quality benchmarks.
- **CMMI (Capability Maturity Model Integration)** — A maturity model with 5 levels:

  - Level 1: Initial (ad hoc processes)
  - Level 2: Managed
  - Level 3: Defined
  - Level 4: Quantitatively Managed
  - Level 5: Optimizing (highest level)

  Companies strive to achieve higher CMMI levels to prove their processes are mature and reliable.

#### 2. Reviews and Audits

- **Informal Reviews:** A quality team member reads a document and identifies issues (e.g., grammatical errors, incomplete requirements).
- **Formal Reviews:** Planned in advance with a dedicated team (business analyst, quality person, etc.) reviewing artifacts at scheduled times.
- **Audits:** More rigorous examination of specific artifacts to check compliance with defined standards. Identifies who is responsible for which defects.

#### 3. Testing

Testing is a core SQA element. As discussed, the goal of testing includes:

- Verifying the product works correctly.
- Building **credibility** with the customer.
- Measuring team **efficiency**.

#### 4. Error / Defect Collection and Analysis

- During the **Test Closure** and **Test Process Analysis** phases, defect data is collected.
- Reports are generated (bugs by developer, bugs by build, bug severity, time to fix).
- This data is analyzed to **improve the testing process** over time — a continuous improvement cycle.

#### 5. Change Management

A critical SQA element. Customers frequently request changes during development.

**Correct approach:**

1. Customer requests a change to any team member.
2. That team member reports it to the **Project Manager**.
3. Project Manager **assesses the impact** of the change.
4. If approved, the PM **informs the entire team**.
5. The change is implemented in a controlled manner.

**Wrong approach:**

- A team member accepts the change directly and implements it without informing the PM.
- This can cause **inconsistencies** in the product and other team members remain unaware.

> Without proper change management procedures, a small modification can break the entire system silently.

#### 6. Education and Training

- Team members must be educated on standards (CMMI, ISO), how to conduct reviews, how to run tests, how to generate quality reports, and how to handle change management.
- Companies send employees for formal certification training (CMMI appraisers, ISO auditors, etc.).

#### 7. Vendor Management

- If third-party vendors or tools are used, their quality must also be managed and monitored.

#### 8. Security Management

- Ensuring the product is secure against unauthorized access and breaches.

#### 9. Safety and Risk Management

- Identifying, assessing, and mitigating risks throughout the development lifecycle.

---

### 2.6 SQA Tasks (What does a Quality Manager Do?)

| Task                                         | Description                                                                                                                   |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Prepare an SQA Plan**                | Create a comprehensive quality plan for the project — how quality will be ensured at each stage within the project timeline. |
| **Participate in Process Description** | Be involved in defining the software development process so quality is built in from the start.                               |
| **Review Engineering Activities**      | Continuously review what software engineers are producing (requirements, design, code, test cases) against quality standards. |
| **Audit Work Products**                | Conduct formal audits of artifacts (SRS, design documents, code, test cases) to verify compliance with defined standards.     |
| **Document Non-Compliance**            | Record any deviations from standards and ensure they are handled through proper procedures.                                   |
| **Report to Senior Management**        | Non-compliance and quality status must be escalated to management for awareness and action.                                   |

---

## Summary of Lecture 28

| Topic                                        | Key Takeaway                                                                                                          |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **SQA is an umbrella activity**        | Quality must be ensured in every phase: analysis, design, implementation, testing, deployment.                        |
| **Quality is measurable**              | Correctness, usability, reliability, portability, maintainability — all are quantifiable.                            |
| **Cost of errors grows exponentially** | A bug found at requirements costs 1×; the same bug found after delivery costs up to 1000×.                          |
| **Elements of SQA**                    | Standards, Reviews & Audits, Testing, Defect Analysis, Change Management, Education, Vendor/Security/Risk Management. |
| **Change Management is critical**      | Changes must flow through the Project Manager to maintain consistency and team awareness.                             |
| **Standards (ISO, CMMI)**              | Formal certifications ensure companies follow defined quality processes consistently.                                 |

---

> *Content will continue in the next session with statistics and further discussion on Software Quality Assurance.*
