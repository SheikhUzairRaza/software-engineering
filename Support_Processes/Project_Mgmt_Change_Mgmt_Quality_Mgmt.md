
---

## 1. Introduction: What Are Support Processes?

Every software project involves certain **core processes** (like requirement analysis, design, coding, testing) and certain **support processes** that run alongside and enable these core processes to succeed.

> **Support Processes** are processes that don't produce the software product directly, but exist to **support, manage, and safeguard** the overall project so that the core development work can proceed smoothly.

### The Three Main Support Processes
1. **Project Management** (Support Process)
2. **Change Management** (Support Process)
3. **Quality Management** (Support Process)

### Why Is "Project Management" Called a *Support* Process?
This is an important conceptual point:

- **Management, by itself, does not "build" anything.** A project manager doesn't personally write code, design the system, or produce a document.
- Project management has **no tangible/visible deliverable** of its own — it doesn't have a "responsibility" to produce a specific artifact like a design document or code module.
- Instead, **all the real responsibility for the outcome lies with the Project Manager** in terms of *overseeing* the work — ensuring the actual deliverables (built by developers, designers, testers) are being produced correctly, on time, and within scope.
- Because it exists purely to **support and enable** the successful execution of the core development activities, it is classified as a **support process**, not a core/production process.

---

## 2. Project Management

### 2.1 The Project Management Life Cycle: PDCA Cycle

Project Management follows a well-known cyclical model called the **PDCA Cycle**:

| Letter | Stands For | Meaning |
|---|---|---|
| **P** | **Plan** | Planning the work, resources, and schedule |
| **D** | **Do** | Executing/carrying out the planned work |
| **C** | **Check** | Monitoring and verifying progress against the plan |
| **A** | **Act** | Taking corrective action / re-planning based on what was found in the Check phase |

This cycle is **continuous and circular** — it doesn't stop after one pass. The Project Manager keeps cycling through **Plan → Do → Check → Act → (Re-Plan) → Do → Check → Act...** throughout the life of the project.

> This PDCA cycle represents the **entire responsibility of the Project Manager**. All of the Project Manager's work can be categorized into these four boxes/stages.

---

### 2.2 Stage 1: PLAN

In the **Plan** stage, the Project Manager determines:

1. **What resources are currently available?** (people, tools, budget, infrastructure)
2. **What resources are needed?** (identifying gaps)
3. **How should these resources be planned/allocated?**
4. **How should these resources be used efficiently?**
5. **Who should be assigned what task?** (task allocation)
6. **How should scheduling be done?** (timelines, sequencing of tasks)

**Output of Planning**: A project plan is created — often visualized using tools like a **Gantt Chart** (as covered in earlier Project Management coursework), which shows task timelines, dependencies, and assigned resources.

---

### 2.3 Stage 2: DO

Once the plan is finalized:

- Tasks are **assigned to individuals** (task by task).
- Developers (referred to as "doers" in this context) begin **working on their assigned tasks** according to the plan.
- This is the **execution phase** — the actual work of building the software happens here.

---

### 2.4 Stage 3: CHECK

After distributing the work, the Project Manager moves into the **Check** phase, where they monitor and verify:

1. **Is each task happening according to the plan?** (right task, at the right time)
2. **Is the task actually progressing as scheduled?**
3. **What is the result/output so far?**
4. **What is the current progress?**
5. If progress is **faster or slower** than planned, this becomes visible during the Check phase.
6. The Project Manager checks whether **any risks that were previously identified (or not identified) have actually occurred**, and what impact they have had.

> **Important distinction**: The Project Manager is NOT responsible for checking whether the *code itself* has a bug, or whether the *documentation* has an error — that is the responsibility of the technical teams and Quality Management. The Project Manager's job in the Check phase is purely to verify: **"Is the plan being followed? Is the plan working/effective?"**

---

### 2.5 Stage 4: ACT

Based on what is discovered during the Check phase:

- If a task is found to be **running slow** or **running fast** compared to the plan, corrective action is taken.
- The specific tasks that are behind or ahead of schedule are **identified**.
- The project (or the affected part of it) is then **re-planned** — this creates a new updated plan.
- This updated/re-plan then goes back into the **Do** phase, then gets **Checked** again, and the cycle continues.

> **This is why PDCA is a cycle, not a one-time linear process**: Plan → Do → Check → Act → Re-Plan → Do → Check → Act → ... and so on, throughout the project's duration.

---

### 2.6 Critical Path Method (CPM)

This is a concept the students had studied earlier in a prior Project Management course, and it ties directly into the **Check** phase of PDCA.

#### What is a Critical Path?
> A **Critical Path** is a sequence (path) of dependent tasks in a project schedule where **each task must finish before the next one can start**, and this chain of dependent tasks determines the **minimum possible duration** of the entire project.

**How Tasks Are Connected:**
- Some tasks are **sequential/dependent**: Task A must finish before Task B can start, Task B must finish before Task C can start, and so on.
- Some tasks can run **in parallel** — independent of each other, happening at the same time.

**Example structure (as discussed in class):**
```
Task 1 → Task 2 → Task 3 → Task 4   (sequential/dependent chain)
        (some tasks may run in parallel with others)
```

#### Why Avoid Long, Highly-Dependent Critical Paths?
- If tasks are heavily **dependent on each other** in sequence (Task A finishes → Task B starts → Task B finishes → Task C starts...), then **any delay in one task cascades and delays every subsequent task**.
- This directly threatens the **project's defined completion date**.

Recall the earlier definition of a project (from prior classes):
> A project is something that has a **definite start** and a **definite end**, with a **unique, achievable objective**.

- If even **one task on the critical path gets delayed**, the entire downstream chain of tasks gets delayed, and the project's **defined end date can no longer be met**.
- When the defined/planned end date is missed, this is essentially a **project failure** in terms of meeting its core definition (definite start, definite end, achieved objective).

#### Project Manager's Strategy Regarding Critical Path
- During **Planning**, the Project Manager tries to **minimize or avoid creating excessively long chains of tightly dependent tasks** wherever possible — i.e., try to **avoid unnecessary critical dependencies**.
- The goal is to **plan the schedule so that no single task is so critically dependent** that its delay would cascade and delay the entire project.
- During **Check**, the Project Manager specifically monitors: *"Is anything on the critical path being delayed?"* Because a delay on the critical path is the most dangerous type of delay — it directly threatens the whole project's timeline.
- If a critical-path task **does** start slipping, the Project Manager immediately works to **correct it** (Act phase) and **re-plans** the rest of the project accordingly (Re-Plan → Do → Check → Act cycle continues).

---

### 2.7 Summary: Project Manager's Core Responsibility

The Project Manager continuously cycles through these **four boxes**:

```
       ┌─────────┐
       │  PLAN   │
       └────┬────┘
            │
       ┌────▼────┐
       │   DO    │
       └────┬────┘
            │
       ┌────▼────┐
       │  CHECK  │
       └────┬────┘
            │
       ┌────▼────┐
       │   ACT   │───► (feeds back into re-planning)
       └─────────┘
```

- This cycle repeats **continuously** throughout the project ("मुसलसल" / continuously).
- This represents the Project Manager's **highest and most important responsibility**.
- **Important boundary of responsibility**: 
  - If there's a **bug in the software** → that is NOT the Project Manager's direct concern (it's a technical/quality issue).
  - If there's a **mistake in documentation** → that is also NOT the Project Manager's direct concern.
  - The Project Manager's job is **only** to check: *"Are we following the plan? Is our plan effective/working?"*

---

## 3. Change Management

### 3.1 What is Change Management?

> **Change Management** is the support process responsible for handling any **changes** that arise during the project — analyzing them, and deciding whether to **approve or reject** them.

### 3.2 When Do Changes Occur?
Changes can originate from multiple sources during the PDCA cycle:
- A change may arise **after the Check phase leads to a Re-Plan**.
- A change may occur in **requirements** (customer wants something different).
- A change may occur in **resources** (e.g., a team member leaves, budget changes, new tools become available).

### 3.3 Responsibilities of Change Management
Whenever any change request arises (from any source — requirements, resources, re-planning, etc.), the **Change Management team/process** handles it by:

1. **Analyzing** the change (understanding its impact, feasibility, cost, risk).
2. **Approving or Rejecting** the change based on this analysis.
3. Once a change is **approved**, overseeing that its **implementation** is properly handled by the project team.

---

## 4. Quality Management

### 4.1 Two Components of Quality Management
Quality Management is divided into **two distinct parts**:

| Component | Focus |
|---|---|
| **Quality Assurance (QA)** | Checks whether the **process** is being followed correctly — i.e., is the work being done the way it was planned/decided to be done? |
| **Quality Control (QC)** | Checks the **actual product/output** once it is built — i.e., is the deliverable (code, document, etc.) correctly/properly built? |

### 4.2 Quality Assurance (QA) — Process-Focused
- QA continuously monitors: **"Is the planned process being followed?"**
- It checks whether things are being done **in the way they were supposed to be done** (per the agreed process/standard).
- QA is concerned with **whether the defined process is effective and being adhered to**, and what results that process is producing.
- It also checks: are there any **problems/obstacles** occurring while carrying out the process as described?

### 4.3 Quality Control (QC) — Product-Focused
- QC checks the actual **work product** once it's been created — e.g., once a **document is written** or **code is completed**.
- Example: Once code is written and goes through a **review**, Quality Control examines the review comments/output to verify: *"Is this code correctly built? Does it meet the required quality standard?"*
- In short: QC is applied **after something is built**, to verify the **correctness/quality of that specific deliverable**.

### 4.4 Summary Comparison

| Aspect | Quality Assurance (QA) | Quality Control (QC) |
|---|---|---|
| Focus | Process | Product |
| Question Asked | "Are we following the right process?" | "Is what we built actually correct/good?" |
| Timing | Ongoing, throughout the work | After a specific deliverable is produced |
| Example | Checking if development is following the agreed methodology/steps | Reviewing a finished code module or document for correctness |

---

## 5. Relationship Between the Three Support Processes

### 5.1 They Are Independent of Each Other (Peer-Level, No Reporting Hierarchy)

A key structural point about these three support processes:

> **Project Management, Change Management, and Quality Management are NOT dependent on each other, and none of them reports to the other.**

- The **Head of Change Management**, the **Project Manager**, and the **Quality Manager** all sit at the **same hierarchical level**.
- **None of these three roles reports to another.**

### 5.2 Why This Independence Matters
This structure exists specifically to preserve **checks and balances**:

- If **Change Management** observes a proposed change and decides **"this change should not happen,"** then the **Project Manager is bound/obligated NOT to implement that change** — regardless of project pressure or preference.
- Similarly, if **Quality Management** determines that **"the quality at this point is not acceptable,"** it can **block/halt a change or a deliverable** from proceeding.
- Because these three functions operate at the **same authority level** (rather than one reporting to another), **no single role can override or pressure the others** — they must **collaborate and work together**, rather than one dictating to another.

This design ensures that, for example, a Project Manager under deadline pressure **cannot simply overrule** Quality Management's objection to push forward low-quality work, and cannot bypass Change Management's rejection of a risky change.

---

## 6. Overall Summary — Key Takeaways

1. **Support Processes** exist to support and safeguard the core development process rather than directly producing the software product. The three main support processes are:
   - **Project Management**
   - **Change Management**
   - **Quality Management**

2. **Project Management** operates on the **PDCA Cycle** (Plan → Do → Check → Act), continuously repeating throughout the project:
   - **Plan**: Determine resources, allocate tasks, create schedules.
   - **Do**: Execute the planned tasks.
   - **Check**: Monitor progress against the plan; watch for delays, especially on the **Critical Path**.
   - **Act**: Take corrective action and re-plan as needed.

3. **Critical Path Method (CPM)**: A critical path is a chain of dependent tasks where delays cascade through the whole project, threatening the project's defined completion date. Project Managers try to **avoid unnecessary critical dependencies** during planning and closely monitor the critical path during the Check phase.

4. **Change Management**: Analyzes and approves/rejects any changes (in requirements, resources, or re-plans) that arise during the project, and ensures approved changes are properly implemented.

5. **Quality Management** has two parts:
   - **Quality Assurance (QA)** — focuses on whether the **process** is being followed correctly.
   - **Quality Control (QC)** — focuses on whether the actual **product/deliverable** is correctly built.

6. **Project Management, Change Management, and Quality Management operate at the same hierarchical level** — none reports to another. This ensures a system of **mutual checks and balances**, where any one of them can block or halt an action if it doesn't meet the required standard, without being overridden by the others.

---

*(End of Notes — Support Processes)*
