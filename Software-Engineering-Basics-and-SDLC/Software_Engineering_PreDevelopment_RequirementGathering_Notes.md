# Software Engineering – Pre-Development Stage & Requirement Gathering: Lecture Notes

---

## 1. Class Activity: Identifying a Real Project

The class began with students proposing potential project ideas to work on as a semester project, in order to practically experience the software development life cycle.

### 1.1 Proposed Project Ideas

**Idea 1: Airport Ticketing/Management System**
- A software system to handle airport operations — e.g., issuing e-tickets so passengers don't have to stand in long lines, managing passenger check-in, issuing boarding cards, and directing passengers to the correct channel/gate.

**Idea 2: Learning Management System (LMS)**
- A system similar to online course platforms, allowing:
  - Setting deadlines
  - Daily task/match tracking
  - Support for multiple users
- **Motivation given by the instructor**: Having taught at the university for many years, the instructor observed that even small universities often already have some form of LMS/planning management system in place — but this particular department/university **lacks such a system**. Students often don't know their attendance status until close to the end of the semester, when it's too late to correct low attendance. A proper system would let students check their status (attendance, registered courses, marks, etc.) in real time throughout the semester.

### 1.2 Class Decision
After discussion, the class decided to proceed with the **Learning Management System (LMS)** as the semester project, since it addresses a real, felt need within the department.

---

## 2. Why the Pre-Development Stage Matters

### 2.1 Core Principle
> To solve any problem, you must first **understand and fully discover the problem**. You cannot arrive at a solution until you have identified and explored every aspect of the problem.

This is the **first stage for any development effort** — before you can begin solving anything, the problem itself must be **discovered**, not just identified.

### 2.2 Difference Between "Identifying" and "Discovering" a Problem
- **Identifying** an area/problem = recognizing that a general area has issues (e.g., "I have trouble getting from home to university").
- **Discovering** the problem = digging deeper into *why* — is the home too far? Is there no direct route? etc. This deeper exploration is what allows you to eventually find the right solution.

### 2.3 The Names Given to This Stage
This stage — occurring **before** the formal Development Life Cycle begins — has been called by many different names in different textbooks/sources:
- **Pre-Development Stage**
- **Pre-Dev Stage**
- **Problem Identification Stage**
- **Feasibility Study**

> Regardless of the name used, this stage always comes **before** the "Requirement Gathering" stage, which is typically considered the **first stage of the Development Life Cycle** proper.

### 2.4 Illustrative Example: The Attendance Problem

The instructor used the **attendance tracking problem** to illustrate why the pre-development/problem discovery stage matters:

- Students often don't check their attendance regularly during the semester — many only think about it **near the end of the semester**, when it may be too late to fix low attendance.
- **Personal anecdote (instructor's own experience)**: Decades ago, during his own university studies, students had a choice between two subjects — Urdu or Humanities. The instructor assumed he was registered for Humanities (since Urdu was his native language and skipping it seemed natural) but had actually failed to formally check his registration status. When exam results were checked, it turned out he **was actually enrolled in Urdu** — a subject he hadn't studied or prepared for at all — and he failed. He eventually had to sit for a retake, study the required material (including poetry, which he hadn't originally studied), and pass it on a second attempt.
  - **Root cause**: There was no easy way to check his own enrollment/registration status throughout the year — he simply assumed he was in the right class based on physically attending sessions.
- **Key takeaway**: This same "unfortunate" pattern still repeats today — decades later, students still routinely don't know their exact attendance percentage or registration status until it's too late, precisely because **there is no proper accountability/tracking tool** — usually just a manual attendance sheet held by the instructor or Class Representative (CR).

> This gap — the **lack of a proper tool/system** for tracking status throughout the semester — is a genuine, longstanding problem that a Learning Management System (LMS) could solve, both for current students and for future students/other departments.

---

## 3. Pre-Development Stage — What It Should Produce

Before entering the Development Life Cycle, the Pre-Development stage should establish clear answers to:

1. **What is my objective?** (e.g., "I should know my status ahead of time" — attendance percentage, marks, course registration, remaining allowed absences, etc.)
2. **Why do I need this system?** — this should be captured in a short paragraph explaining the motivation.
3. **Feasibility** — Can we actually build this? Do we have the required resources, or do we need external help?

> Students were assigned a short task: write a brief paragraph/note explaining **why** an LMS is needed for their case, including a basic feasibility assessment (can it be built, or does external assistance need to be sought).

---

## 4. Overview of the Development Life Cycle Stages

After the Pre-Development stage, the formal Development Life Cycle begins. The general flow (subject to variation depending on the specific life cycle model used, e.g., Waterfall):

```
Requirement Gathering → Analysis → Design → Development/Implementation → Testing → Support/Maintenance
```

### 4.1 Important Clarification: This Applies to ALL Process-Based Activities, Not Just Software
> This general life cycle structure (a sequence of phases with reviews occurring throughout) is **not exclusive to software**. It applies to **any process-based activity** — for example, a construction project would follow an analogous life cycle, though the specific stages/tasks within each phase would differ from a software project's stages.

- The **overall shape** of the life cycle (phases, reviews between phases) stays consistent across domains.
- The **specific stages and their contents** differ depending on the domain — construction vs. software, for example.
- The **choice of life cycle model** (e.g., Waterfall) also matters — if you're in construction, Waterfall is essentially the default/standard approach; in software, there are **many available models** (Waterfall, Spiral, Prototype, etc.) since the Waterfall model itself originated from construction and had to be **adapted differently** when brought into the software domain (since construction-style stages didn't translate directly to software work).

---

## 5. Requirement Gathering — Detailed Process

### 5.1 Needs vs. Wishes
An important distinction discussed before diving into requirement gathering techniques:

| Term | Meaning |
|---|---|
| **Needs** | What you **must have** — the essential/mandatory requirement. |
| **Wishes** | An **extended/luxury version** of a need — something you don't strictly require, but would like to have in addition. If a wish is fulfilled, it becomes an added "demand" satisfied on top of the basic need. |

> Example given: A basic need might be fulfilled (e.g., "sleep" is achieved), but a wish would be some additional luxury layered on top of that basic fulfillment.

### 5.2 Steps in Conducting Requirement Gathering

#### Step 1: Build a Checklist
- Before speaking to any stakeholder, prepare a **checklist** of:
  - Who needs to be spoken to.
  - What questions should be asked.
  - What possible answers/responses might come up.
- **Purpose of the checklist**: To define clear **boundaries/scope** for the conversation. 

> **Example of scope creep to avoid**: If you're gathering requirements for an LMS and a stakeholder starts talking about unrelated issues ("the road outside is broken too, fix that as well," or "this chair is uncomfortable, I want a different chair"), the checklist ensures you politely redirect the conversation and **stay within the defined scope** (the LMS itself), rather than absorbing every unrelated complaint.

- A **closed/defined checklist** is essential — you decide in advance **what topics are in scope and what topics are out of scope**.
- Rationale: Every customer/stakeholder, given the chance, would want **all their problems solved at once** — but that isn't feasible or appropriate for a focused requirement-gathering session. The checklist keeps the process **focused**.

#### Step 2: Identify Stakeholders
- A **Stakeholder** is defined broadly: **anyone who is involved with the system in any way** — whether in building it, using it, or being affected by whether it exists or not.

**Types of stakeholders discussed:**
- **Sponsor / Major Stakeholder**: The person(s) driving/owning the initiative (in the class example, the student who proposed the LMS idea was treated as the sponsor).
- **Everyone involved in building the system.**
- **Everyone involved in using the system.**
- **Anyone influenced by the system's existence or non-existence** — even indirectly.

**Example — Gate Pass Analogy**: 
- If a student wants to take equipment out of the university, a gate pass process is involved. 
- The **Lab In-charge** issues the gate pass. 
- The **Gate Keeper** follows up and checks it at the exit. 
- **Both roles are stakeholders** in that mini-process, since both are "influenced" by/involved in the system in some way.

> **Important clarification**: Stakeholders are **not limited to** those who have invested money or those from whom money will be collected. It includes **every user and everyone who has any stake** in the system's success or failure — including, for example, the instructor himself in this class scenario, who has a stake in students getting the full experience of the development life cycle, regardless of whether the LMS project itself succeeds financially or not.

#### Step 3: Prepare Specific Questions
- Once the checklist and stakeholders are identified, prepare the **actual questions** to ask.
- **Why not just have an open-ended conversation?** If you go in "open" without prepared questions, you **cannot control the direction/content** of the conversation — stakeholders may bring up unrelated topics.
- Prepared questions act as a way to keep the conversation contained within the intended scope (a "circle" of relevant topics).

**Example — Staying Within Scope of Identified Stakeholders**: 
- If your identified stakeholders are people within your own department/room, but you go outside and start asking unrelated people (e.g., a photocopy shop worker outside) — that would be outside the defined stakeholder scope, and not appropriate for this exercise.

### 5.3 Who Prepares the Checklist and Questions?
- The **checklist is prepared by the Business side** (i.e., the business/domain stakeholders who understand what value the system needs to deliver, not the technical/development team).
- The checklist and prepared materials are then **reviewed by the full Requirement Gathering team** — this does not have to be a single person; it's typically a team effort.

**Why Business (not purely Technical) leads this:**
- The **Business side** best understands *why* the system is needed and *what benefit/return* it will deliver (e.g., "this money is being spent, so how will it be returned/justified").
- **Developers/technical people** ("doers") often take many things for granted or overlook certain considerations, whereas Business stays focused on the value/purpose driving the whole effort.
- This is why requirement gathering, especially the **checklist creation and question preparation**, is generally led/prepared by Business — though **Technical team members are also involved**, especially once execution begins (since technical questions do need to be included eventually).

**Typical breakdown of responsibility during Requirement Gathering:**

| Activity | Primarily Done By |
|---|---|
| Checklist creation | Business |
| Question preparation | Business, in collaboration with Technical team as needed |
| Reviewing the requirement-gathering materials | Full Requirement Gathering team (which includes Business and often Technical members) |
| Leading/conducting the actual requirement-gathering sessions | Often led by Business, but conducted **along with** the Technical team |

### 5.4 Common Requirement Gathering Techniques (Briefly Mentioned)
- **Interviews**
- **Surveys**
- **Group discussions** (e.g., sitting stakeholders together as a group to discuss what kind of system they need and what features they want)

> The instructor noted that actually **experiencing** these processes hands-on (rather than only reading about them in a textbook) is what truly builds skill — simply memorizing a process for an exam and forgetting it afterward provides no lasting value ("it only remains part of knowledge, not skill").

---

## 6. Project vs. Process — An Important Distinction

This distinction was explained because it directly affects how a life cycle (like the Development Life Cycle) is structured and repeated.

### 6.1 Definitions

| Term | Definition |
|---|---|
| **Process** | Something that is **continuous** — it doesn't have to start or end at a specific time; it just keeps running/repeating. |
| **Project** | Something that has a **definite life** — a defined **start date**, a defined **end date**, and it must **achieve its objective** within that time frame. |

### 6.2 Class Example: Is "This Class" a Project or a Process?
- The class itself (as a single session) was used as an example: it has a **defined start time** and a **defined end time**, and it has an **objective** (what will be covered/achieved in this session).
- Based on this definition: **this specific class session is a Project.**
  - Definite time to start.
  - Definite time to end.
  - A defined objective.

### 6.3 Larger Example: A Student's Academic Journey (Project vs. Process)

- A student's overall **degree/graduation** (from admission/enrollment to graduation) is itself treated as a **Project** — it has a definite start (enrollment) and a definite end (graduation), with an objective (completing the degree).
- **Within** that overall project, there are multiple **Processes** — e.g., First Year, Second Year, Third Year, etc., which execute as part of the project.
- **Within each of those "processes,"** there are further **stages**, and each of those stages, if it has a defined start/end/objective, can itself be treated as a smaller **project**.

### 6.4 Key Insight: Processes Contain Projects, and Departments Run Processes
- From the **department's perspective**, "education" (teaching this course, semester after semester) is a **Process** — it runs again and again, without a single defined end date; one iteration ends and another begins ("this year's course... next year's course...").
- From the **individual student's perspective**, their own enrollment-to-graduation journey is a **Project** — it has one definite start and one definite end for them personally.

> **General Rule**: *"Every part of a process can be a project — I will start it on a definite date and finish it on a definite date; that becomes a project for me."* Meanwhile, the process itself can continue indefinitely without a fixed end date; only the project (a bounded piece of it) has that defined start/end structure.

### 6.5 Applying This to the Course Structure
- The instructor structures class sessions as bounded "projects" (e.g., "our project for the next class is to complete X, Y, Z") specifically so that concrete, achievable objectives are set for each session, with a clear start and end.
- Meanwhile, within a broader phase — e.g., the **Design phase** of a software project — there can be **multiple cycles/sub-processes** running.

---

## 7. Why the Design Phase Contains Multiple Cycles (Software, Hardware, Environment)

This was raised as an important conceptual point about the Design phase specifically:

> **No software can exist or execute without a platform.** Therefore, designing software is never done in isolation — you must simultaneously design the **hardware** it will run on, and the **environment** it will operate within.

### 7.1 The Three Parallel Design Cycles
When you reach the **Design phase** of the Software Development Life Cycle, there are actually **three parallel design cycles** happening together:

1. **Software Design**
2. **Hardware Design**
3. **Environment Design**

**Why all three are necessary:**
- Software cannot run without hardware ("it has to be a *body*" for the software).
- The combination of software and hardware cannot function properly without a defined **environment** — i.e., how it will operate, how handover/takeover of the system will happen, what kind of environment it will run in.

### 7.2 Example: Real-Time Data Transfer to the Cloud
If a software project requires transferring data in real-time to the **cloud** or another external system:
- You must design the **software** component (how the data transfer logic works).
- You must also design/select the **hardware/platform** it will run on (since you're designing for that specific transfer target).
- The **Requirement Gathering phase** is what determines these platform-level decisions in the first place — e.g.:
  - Where will the system/data be hosted? 
  - Can we use a **local server**? 
  - Do we need to go to the **cloud**? 
  - Do we need some other kind of **shared space**?
- Even though the team may primarily be "software builders," they must still think through these hardware/environment questions **during requirement gathering and design**, because these decisions directly shape what needs to be designed.

### 7.3 Additional Consideration Raised: Reading/Readiness (Reference to "Feasibility Study")
- The instructor referenced that this connects back to concepts like **Feasibility Study** / **Pre-Development Study** — the same foundational concepts discussed earlier, now being revisited as they become directly relevant to the Requirement Gathering and Design phases.
- Also mentioned: identifying **who will use the system**, and **who will operate it** — these considerations must be captured during requirement gathering as well, since they affect both the requirements and the eventual design decisions (hardware, environment, access).

---

## 8. A Broader Reflection: Are We Making Real Progress in Technology? (Instructor's Personal Reflection)

The instructor shared a personal reflection/anecdote, drawing a broader point about technological progress relative to potential:

- The instructor completed his **Master's degree in 1986**, specializing in **Computer Design and Electronics**, and at that time, worked on building an **AI tool** as part of the coursework — even back then, in a very early/foundational form ("not very advanced, but it was there, at the roots").
- His own specialization project at the time was related to **drones**.
- **Reflection**: If the progress made in AI and related technologies (like drones) back in 1986 had been **consistently built upon and advanced** over the following decades, the region/community might now be in a position to be **manufacturing** such technologies domestically, rather than lagging behind.
- The instructor expressed concern that, despite early exposure to these technologies decades ago, there hasn't been consistent forward progress — describing this as **"unfortunate,"** noting that in some ways, progress feels like it's moving **backward rather than forward** relative to where the starting point could have led.
- He also touched on excuses people (including himself) make about lacking resources — distinguishing between **having money** and **having "spare money"** (i.e., disposable resources available to actually invest in advancing such projects) — suggesting that resource constraints (real or perceived) have historically limited how much such early technological exposure translated into long-term capability building.

> *(This section is a motivational/reflective aside from the instructor rather than core technical content, but is included here as it was part of the classroom discussion and provides context/motivation for taking the project-based learning approach seriously.)*

---

## 9. Class Administration Notes

- The instructor discussed the importance of **starting and ending on time**, tying it back to the earlier discussion on the **definition of a project** — a class session itself qualifies as a "project" precisely because it has a definite start time, a definite end time, and a defined objective; a **successful project is one that starts on time and finishes on time**.
- Regarding late arrivals: a **15-minute grace period** was proposed — classes start at 9:00 AM, with the grace period extending to 9:15 AM, after which the door would be closed and no further entry permitted.

---

## 10. Overall Summary — Key Takeaways

1. **Pre-Development Stage** (also called Pre-Dev Stage, Problem Identification Stage, or Feasibility Study) comes **before** the formal Development Life Cycle begins. Its purpose is to fully **discover** the problem (not just identify it) and establish the objective and feasibility of a potential solution.

2. **Development Life Cycle stages** generally follow: Requirement Gathering → Analysis → Design → Development → Testing → Support/Maintenance — with continuous reviews happening between stages. This general structure applies to **any process-based activity**, not just software, though the specific contents of each stage vary by domain.

3. **Requirement Gathering** involves:
   - Building a **checklist** (prepared by Business) to define scope and boundaries.
   - Identifying **stakeholders** — broadly defined as anyone involved in building, using, or being affected by the system.
   - Preparing **specific questions** in advance to keep gathering sessions focused and within scope.
   - Understanding the difference between **Needs** (essential requirements) and **Wishes** (extended/luxury additions).

4. **Project vs. Process**:
   - A **Process** is continuous, with no fixed end date.
   - A **Project** has a definite start date, definite end date, and a defined objective.
   - The same activity can be a **process** from one perspective (e.g., a department repeatedly running a course every year) and a **project** from another (e.g., an individual student's journey from enrollment to graduation).
   - Every bounded segment of a process (with its own defined start/end/objective) can itself be treated as a project.

5. **Design Phase Complexity**: The Design phase of a software project actually involves **three parallel design cycles** — **Software Design**, **Hardware Design**, and **Environment Design** — because software cannot exist or run without a supporting hardware platform and a defined operating environment. These considerations (e.g., local server vs. cloud vs. shared space) are shaped by decisions made during Requirement Gathering.

---

*(End of Notes — Pre-Development Stage & Requirement Gathering)*
