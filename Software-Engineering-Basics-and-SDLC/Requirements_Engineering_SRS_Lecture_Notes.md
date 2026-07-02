# Requirements Engineering & SRS Development

### Lecture Notes — Software Quality Assurance (Case Study: LMS Project)

---

## 1. Introduction: Why Follow a Standard Process/Book

The instructor opened by referencing a **standard process reference book** (an older, IBM-related process methodology book — likely a Software Engineering/Requirements process guide) that documents **best practices for the full software life cycle**, regardless of which specific methodology a team uses.

### Key points about the reference book:

- It documents the **entire end-to-end project process** — what should happen at each stage, **who** is responsible, and **how** it should be done.
- It clearly defines **role separation** — e.g., a Project Manager cannot perform a Developer's role, and vice versa. Well-defined roles are a hallmark of good process/technology practice.
- The book had gone through restrictive licensing after being acquired by a company (referenced as IBM in the recording), making free access difficult — the instructor mentioned trying to find copies (old/used editions, older 1998-era version, or a photocopy) since it was not freely available anymore.

### Why standardize on one source?

The instructor emphasized that the whole class should **follow one single reference** (the assigned book) rather than everyone learning from different websites or sources:

> "If one student reads from one website, another from an Indian website, etc., everyone ends up learning different, inconsistent versions. Instead, we'll follow this one book so we're all synchronized — what's written in the book is what I will also be teaching from."

- Individual understanding may vary from student to student (some may grasp a concept faster than others) — this is normal and can't be fully avoided.
- However, using **one consistent, well-reviewed source** minimizes inconsistency and confusion.

---

## 2. The Publishing/Review Process as a Quality Analogy

The instructor used how **books get published** as an analogy for how **requirements and documents** should be reviewed before being finalized:

1. An author writes a draft.
2. **Peers review it first** — they check for errors, mistakes, and inconsistencies, and the author corrects them.
3. Once peer-reviewed, the manuscript goes to a **publisher**, who arranges **independent expert review**.
4. Experts review it, more corrections/changes are incorporated.
5. Once a final **review-approved document** is produced, it is **published**.

**Why this matters:** Because books go through this rigorous multi-stage review, there is a **much lower chance of errors** appearing in a properly published, reviewed book — compared to random, unreviewed content found online. This is the same discipline the class should apply to **requirements documentation**.

---

## 3. System vs. Software — Key Terminology Distinction

The instructor clarified an important terminology point often confused by students:

| Term                            | Definition                                                                                                                                            |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **System (निज़ाम)** | The overall**process/mechanism/order** that governs how something operates. It is the bigger concept — the "system" that is running things.    |
| **Software**              | The**tool** that *implements* or supports that system/process. Software itself is not the system — it is a means of carrying out the system. |

> "Software itself is not the system, and a computer itself is not the system. The overall process/mechanism that has been designed — that is what we call the system."

**Practical implication:** In documentation, this is why you'll see both:

- **SRS — System Requirements Specification**, and
- **SRS — Software Requirements Specification**

Both acronyms are commonly used, and in modern practice, the two terms are often used together/interchangeably, even though technically they refer to a system-level process vs. its software implementation.

---

## 4. The Requirements Engineering Life Cycle

The instructor outlined the overall flow of requirements management as follows:

```
Requirements Gathering → Requirements Analysis → SRS Document Creation → SRS Approval (Sign-off) → Change Management (for future changes)
```

This entire process (from gathering through to managing changes after sign-off) is collectively called **Requirements Management**.

### 4.1 Why Requirements Analysis Gets the Most Time and Attention

The instructor stressed that **more classroom time will be spent on Requirements Gathering & Analysis** than on other topics, because of a well-known principle in software engineering:

> **The cost of fixing a defect increases dramatically the later it is discovered in the project life cycle.**

- If a requirement-related mistake is identified and corrected **during the requirements stage**, it might cost roughly **$1** to fix.
- If that same mistake is not caught until much later (e.g., during testing or after deployment), it can cost as much as **$1,000** (or more) to fix.
- This is referenced as a long-standing finding from software engineering research on the **rising cost of defect correction over the project timeline**.

**Conclusion:** Because early-stage requirement errors are the cheapest to fix and the most expensive to leave unresolved, teams should invest **maximum effort and time** in getting requirements right at the very beginning.

---

## 5. Requirements Gathering Exercise — LMS Project

Just as with the risk-gathering exercise in the previous session, the instructor ran a **structured brainstorming exercise** for requirements:

- Students were asked to sit quietly for **5 minutes** and think about the LMS project from the perspective of its actual users: **students, teachers, and management/administration**.
- Guiding prompt: *"You are the user — this system is being built for you. What should it include?"*
- After 5 minutes, students shared their ideas one by one, which were recorded (similar process to the earlier risk-gathering session).

### 5.1 Full List of Requirements Identified for the LMS

The class collectively identified the following functional and non-functional requirements for the LMS:

**Academic / Course-Related**

- Attendance record and tracking
- Marks/grades record
- Syllabus and course content tracking (how much of the syllabus is completed)
- Course material / study material upload and access
- Assignments (submission and management)
- Structure guide (course structure/outline)
- Q&A about subjects — students can ask questions about a subject directly through the system instead of chasing teachers in person
- Create/update courses (including handling new courses being added)
- Student progress tracking **per course** (progress of each student in each course)

**Communication & Interaction**

- Teacher contact information (email, phone number)
- Ability to book a specific time slot/appointment with a teacher for queries
- Notifications
- Announcements (e.g., upcoming events/deadlines)
- Discussion boards/forums (both teacher-student and student-student discussions)
- Group discussion functionality (e.g., small groups of 4–5 members)
- Recorded class sessions (access to recordings)

**Administrative / Management**

- Timetable (with updates when finalized/changed)
- CR (Class Representative) selection process
- Teacher selection (used in private institutions as well)
- Student behavior reports (teachers can report on students; students can also give feedback in return)
- Career-related information / student society / recruitment-related content
- Skill development resources
- Monitoring activity (tracking usage/activity within the system)

**Access & Security**

- Confidentiality — some data (e.g., specific records) must remain protected, similar to password-protected information
- Document/material access controls, based on user role (e.g., students only have access to specific sections)
- Different access levels for different user types (students vs. teachers vs. management)

**Miscellaneous / Debated Items**

- ID card–related functionality (raised, but not entirely agreed upon)
- Objective-type only exams (raised as a side discussion — one instructor mentioned personally preferring only objective-type questions such as True/False, MCQs, or short calculations, since these avoid subjective grading disputes — this was more of a tangential class discussion than a firm LMS requirement)

---

## 6. Requirement vs. "Want" — An Important Distinction

While reviewing the gathered list, the instructor introduced another important filtering concept, parallel to the earlier **Risk vs. Requirement** distinction from the previous lecture:

> A **Requirement** is something the system *needs* to have to function correctly for its intended purpose.
> A **Want** is something a stakeholder *would like to have*, but which is not strictly necessary for the system to work.

The class was asked to go through the gathered list and separate genuine **requirements** from mere **wants**, the same way they earlier separated **risks** from requirements in the risk management exercise.

---

## 7. Requirements Analysis — Prioritization Criteria

Once the requirements list was gathered, the instructor introduced a set of criteria to **analyze and prioritize** each requirement — very similar in spirit to the impact/frequency scoring used earlier for risk analysis:

| Criterion           | Purpose                                                                                                                               |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Impact**    | How significant is this requirement to the success/usability of the system?                                                           |
| **Frequency** | How often will this feature/requirement actually be used?                                                                             |
| **Weight**    | A combined/derived score reflecting the overall importance of the requirement (often calculated from Impact × Frequency or similar). |
| **Priority**  | The ranking assigned to the requirement based on its weight — used to decide what gets built first.                                  |

### Process:

1. Write down every gathered requirement.
2. For each one, define/agree on what it specifically means (**"what is my intention here?"**) — to ensure common understanding across the team, since a requirement's exact meaning can be interpreted differently by different people.
3. Score each requirement on **Impact**, **Frequency**, **Weight**, and **Priority**.
4. Discuss and reach a **common/shared understanding** for each requirement — where understanding differs, this is flagged and clarified through discussion (a form of internal review, similar to the peer-review analogy from Section 2).
5. Once all requirements have been discussed, scored, and clarified, they are **finalized**.

---

## 8. Finalizing the SRS (System/Software Requirements Specification)

After gathering and analyzing requirements, the next step is to **document them formally** into the SRS.

### 8.1 The SRS Document

- The SRS is the **official document** that captures all agreed, finalized, and approved requirements.
- Anything included in the SRS is officially part of the project scope; anything **not** included is **not** part of the project (unless added later through formal change management).
- The SRS must be **signed off/approved by stakeholders** — specifically referenced as being approved by the **customer team** (in an academic project context, this could be the class/course stakeholders acting as the "customer").

### 8.2 After Sign-Off: Change Management

- Once the SRS is **signed and finalized**, new requirements **cannot be added directly** into the project scope anymore.
- Any new requirement or requested change must go through a **formal Change Management process**.
- A dedicated **Change Management/Change Control team** is responsible for reviewing and approving (or rejecting) any proposed changes after the SRS has been signed off.
- The instructor drew an analogy to real-world governance: just as police or government bodies decide whether an action should or shouldn't be allowed/implemented, a **Change Management team** decides whether a proposed change should be incorporated into the project.

### 8.3 The Bigger Picture

The instructor described this whole process — from initial requirements identification, through analysis, documentation, sign-off, and any subsequent changes — as collectively falling under the term **Requirements Management** (also referred to broadly as **Change Management** once the project is live and changes need to be controlled).

---

## 9. Summary of the Full Requirements Process

```
1. Requirements Gathering
   → Brainstorm with all stakeholders (students, teachers, management)

2. Requirements Analysis
   → Separate "requirements" from mere "wants"
   → Score each requirement on Impact, Frequency, Weight, Priority
   → Build common/shared understanding of each requirement's exact meaning

3. SRS Document Creation
   → Formally document all agreed, prioritized requirements

4. SRS Approval / Sign-off
   → Reviewed and approved by stakeholders/customer team

5. Change Management
   → Any new requirement or modification after sign-off must go through
     a formal Change Management/Change Control process
```

### Core Takeaways

- Following **one consistent, well-reviewed reference source** (like a standard textbook/process guide) keeps the whole class/team aligned and reduces inconsistent understanding.
- **System** and **Software** are related but distinct concepts — software implements a system, but is not the system itself.
- The **Requirements phase is the most critical and cost-sensitive stage** of a project — errors caught here are dramatically cheaper to fix than errors caught later (the "$1 vs. $1000" principle).
- Requirements gathering should involve **all relevant stakeholders** (mirroring the earlier risk-gathering approach), producing a broad, user-centered list of features and needs.
- Not everything gathered is a true **requirement** — some items are simply **wants** and should be filtered out or deprioritized.
- Requirements should be **analyzed and prioritized** using structured criteria (Impact, Frequency, Weight, Priority) before finalization.
- The finalized, agreed set of requirements becomes the **SRS**, which must be formally **signed off** by stakeholders.
- After sign-off, any new requirement must go through **formal Change Management** — it cannot simply be added informally.

---

## 10. Case Study Recap: LMS Requirements (Consolidated List)

| Category                    | Requirements                                                                                                                                                          |
| --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Academic**          | Attendance, Marks, Syllabus tracking, Course/study material, Assignments, Course structure guide, Subject Q&A, Course creation/updates, Per-student progress tracking |
| **Communication**     | Teacher contact info, Appointment/slot booking with teachers, Notifications, Announcements, Discussion boards/forums, Group discussions, Recorded sessions            |
| **Administrative**    | Timetable, CR selection, Teacher selection, Student behavior reports, Career/society/recruitment info, Skill development resources, Activity monitoring               |
| **Access & Security** | Confidentiality of sensitive data, Role-based document/material access, Differentiated access levels (student/teacher/management)                                     |
