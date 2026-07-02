# Software Engineering – Support Processes (Part 2): Configuration Management & Environment Management

---

## 1. Recap

In the previous session, three support processes were covered:
1. **Project Management**
2. **Change Management**
3. **Quality Management**

In this session, two more support processes are discussed in detail:
4. **Configuration Management**
5. **Environment (Management)**

---

## 2. Configuration Management

### 2.1 What is Configuration Management?

> **Configuration Management (CM)** is the support process responsible for **documenting, versioning, numbering, and safely storing every artifact** produced during the project (plans, designs, documents, code, modules, etc.), and for acting as the **single, final authority** on which copy of any artifact is the official/current one.

### 2.2 How Configuration Management Works — The Flow

1. As soon as any artifact is created and finalized — for example, the **Plan** is documented — it is handed over to Configuration Management.
2. Configuration Management **assigns it a name and a number** (a version identifier).
3. From that point on, **Configuration Management holds the final copy** of that artifact.
4. If **any team** in the project needs that artifact (e.g., needs "the Plan" for reference), they must request it **from Configuration Management** — not from the team that originally created it.

**Example walkthrough:**
- The **Plan** is created → finalized → sent to Configuration Management → given a version/number.
- The **SRS (Software Requirement Specification)** is created → its final copy also goes to Configuration Management.
- If anyone in the project needs the SRS, **even the Requirements team itself cannot directly hand it out** — it must be obtained through Configuration Management.
- Configuration Management retains **all versions**, and is the **final authority to publish any document or artifact**.

### 2.3 Configuration Management and Software/Code Modules

- Once a software **module is built and internally tested**, it also goes to Configuration Management.
- Configuration Management assigns it a **number/version**.
- Going forward, **anyone who needs to use that module** must reference/use that specific **version and number**.

### 2.4 Configuration Management and Changes

Configuration Management plays a central role whenever a **change** occurs:

**Example scenario**: Suppose the project is in the **Testing** phase, and a change arises that relates to the **Design**.

- The team handling that change (e.g., testers who identified a design-related issue) does **not** go directly to the Design team to get the current design.
- Instead, they request the **latest/last design copy from Configuration Management** — because that is guaranteed to be **the final, authoritative version**.
- The change is then routed through the previously discussed **Change Management** process:
  1. Change Management **reviews** the proposed change.
  2. Change Management **agrees or disagrees** with it.
  3. If agreed, Change Management **authorizes** it.
  4. The project team then either **incorporates** the change or **rejects** it, based on that authorization.
- Any artifact needed to make the change (design, program, file, etc.) is **requested from Configuration Management**.
- Once changes are made, the updated artifact is **submitted back to the Configuration Management team**.
- Configuration Management then makes this **new final copy** available/visible to all other teams.

> **Key concept**: Configuration Management acts as the **custodian** of every artifact and every ongoing piece of work within the project.

### 2.5 Versioning and Numbering Rules

Configuration Management **decides and enforces** the rules for:
- **How versioning will work**
- **How documents will be numbered**
- **How artifacts (like programs) will be numbered**
- **What triggers a version change vs. an iteration/update change**

**Example — Version Numbering Format:**
You've likely seen applications or operating systems with version numbers like:
```
2.2.1
2.2.2
```
- The **first number** (e.g., "2") = the **Version** — typically changes only for **major changes**.
- The **second/third numbers** = represent **Iterations and Updates** (e.g., second number = iteration, third number = update) — these typically change for **minor changes**.

**Rule of thumb:**
- **Minor change** → only the iteration number is updated.
- **Major change** → the version number itself (the first number) is updated.

### 2.6 Configuration Management's Authority (Ownership Rules)

- Configuration Management **decides how numbering/naming conventions work** — for example, whether an artifact's number starts with the creator's name or the **organization's name**. Even if an individual wants their work numbered a particular way, **Configuration Management has the final say**.
- **Any artifact that becomes part of the project** (a program you built, an application you created, etc.) automatically comes under the **ownership of Configuration Management**.
- Once something is under Configuration Management's ownership:
  - **No one else can change it.**
  - **No one else can delete it.**
  - **No one else can handle/modify it in any way** without going through Configuration Management.

**Real-world analogy**: Just like physical assets in an office (e.g., computers in a computer lab) are tagged with **asset numbers** in a specific numbering scheme — this tagging and tracking role is performed by a Configuration Management–type function. When an asset is retired, its number is retired along with it.

### 2.7 Key Actors in Configuration Management Workflow

Based on the workflow diagram referenced in class:
- **Project Manager** — has a Project Plan.
- **Configuration Manager (CM)** — has a Configuration Management Plan.
- **Architects** — the people who create major design documents and artifacts.
- **Anyone in the project** — can submit their artifacts and any associated **change requests** to Configuration Management; these all get collected/logged there.

### 2.8 Summary: Role of Configuration Management

| Responsibility | Description |
|---|---|
| **Documentation & Storage** | Documents and safely stores every artifact created in the project |
| **Versioning & Numbering** | Assigns and governs version numbers/IDs for all artifacts |
| **Single Source of Truth** | Acts as the *only* authorized source for the current/final copy of any artifact |
| **Access Control** | No one outside Configuration Management can create, delete, or modify an artifact under its ownership |
| **Change Support** | Provides the latest official copy of artifacts when changes are needed, and updates its records once changes are approved and submitted back |
| **Final Publishing Authority** | The final authority to publish any document or artifact in the project |

> **Important Note**: Configuration Management's role is described as **"restricted but very important"** — it doesn't do a huge variety of tasks, but the tasks it does are **critical to maintaining order, traceability, and integrity** across the entire project.

---

## 3. Environment (Management)

### 3.1 What is "Environment" in This Context?

> **Environment** refers to everything **other than the software itself** that needs to be acquired, set up, or managed to support the project — such as tools, hardware setups, and physical/technical infrastructure.

- If the project needs certain **tools**, acquiring, designing, and setting up those tools is the **responsibility of the Environment process/team**.
- The **Environment team** designs the environment and **builds** it.

### 3.2 Environment Is More Than Just Physical Setup

A common misconception is that "Environment" simply means physical surroundings — e.g., a room with chairs, tables, etc., used as a development room.

> **This is NOT the full picture.** Environment management includes **much more** than just arranging furniture or physical space.

The Environment team is also responsible for:
- **Training** the people who need to work within that environment — training is considered **part of the Environment team's responsibility**.

### 3.3 Connection to Design (Three Types of Design)

Recall from earlier design discussions that design happens across **three parallel tracks**:
1. **Software** being built
2. **Hardware** being designed
3. **Environment** being designed

These are handled by **different, separate teams**:
- One team builds the software.
- Another team designs/builds the hardware.
- Another team (the **Environment team**) is responsible for **bringing everything together and integrating it**.

### 3.4 Components/Flow of the Environment Process

Based on the workflow discussed in class, Environment covers:

1. **Tools Selection and Acquisition** — choosing and acquiring the tools needed for the project (or building tools where necessary).
2. **Process Configuration** — setting up how processes will run within that environment.
3. **Process Improvement** — a very important ongoing responsibility (explained in detail below).
4. **Training** — part of the Environment team's scope.
5. **Technical Services** — also part of the Environment team's scope.

### 3.5 Process Improvement — A Critical Environment Responsibility

This is described as one of the **most important** aspects of the Environment function.

#### Key Idea: Processes Are Not Fixed in Stone
- At the start of a project, various processes are defined:
  - How **Requirements Development** will happen (what steps, how requirements will be gathered, analyzed, and finalized).
  - How **Analysis** will be performed (which team, how they'll work).
  - How **Design** will be done (who does it, who approves it).
  - How **Implementation** will happen (who builds it, what tools will be used).
- **None of these processes are permanently "carved in stone."** They are expected to **evolve during the project**.

#### How Process Improvement Happens
- **Anyone in the project** can **propose an improvement** to a process — this isn't limited to any single role.
- **Example scenario**: 
  - Someone working in the **Testing phase** notices that the process defined earlier (e.g., specific testing steps/stages) has some **inefficiency**.
  - Similarly, someone in the **Requirements phase** or **Design phase** might notice inefficiencies in *their* respective processes.
- Whoever notices the inefficiency reports it to the **Environment team**, explaining:
  - What the inefficiency is.
  - How it could be improved (e.g., "this task currently takes 10 hours, but with a change, it could take 1 hour" or take fewer days).

#### What the Environment Team Does With This Feedback
1. The Environment team **receives** the proposed improvement.
2. The Environment team **analyzes** it.
3. The Environment team **discusses** it.
4. If validated, the improvement is **built into the project's process** going forward.

#### Timing: Improvements Can Apply Retroactively (to Future Phases) or to Future Projects
- Sometimes the phase that had the inefficiency has **already passed** by the time the issue is noticed.
  - **Example**: While working in Testing, someone realizes that if the Design phase (already completed) had been carried out differently, it would have been more efficient.
  - Since the Design phase for *this* project is already done, this insight is instead **captured for the Design process to be used in the next/future project**.
- Alternatively, if a later phase within the **same project** hasn't started yet, the improvement can be applied there:
  - **Example**: After finishing the Testing phase, the team notes that certain things should be added to the **Deployment phase** process (which hasn't started yet) — things that weren't documented before, in order to reduce inefficiency going forward within the same project.

### 3.6 Summary: Role of Environment Management

| Responsibility | Description |
|---|---|
| **Tools Acquisition/Building** | Selecting, acquiring, or building the tools needed for the project |
| **Infrastructure Setup** | Setting up physical/technical infrastructure needed for development |
| **Training** | Training people who need to work within the environment |
| **Technical Services** | Providing ongoing technical support/services |
| **Process Configuration** | Establishing how processes will be carried out |
| **Process Improvement** | Continuously receiving, analyzing, and incorporating process improvement suggestions from anyone on the team — applied either later in the same project or carried forward to future projects |

---

## 4. Overall Summary — Key Takeaways (Part 2)

1. **Configuration Management (CM)**:
   - Acts as the **single source of truth** and **custodian** for every artifact in the project (plans, SRS, designs, code modules, etc.).
   - Assigns **version numbers/naming conventions** and governs how versioning works (major version vs. minor iteration/update).
   - Is the **only authorized party** to create, modify, delete, or publish any project artifact.
   - Plays a central role in facilitating **changes** — providing the authoritative "last copy" of any artifact when a change is needed, and updating its records once changes are approved and resubmitted.
   - Its role is **narrow/restricted in scope** but **extremely important** for maintaining order and integrity across the project.

2. **Environment Management**:
   - Covers everything **other than the software itself** — tools, hardware setup, infrastructure, and technical/physical resources.
   - Also responsible for **training** people and providing **technical services** — not just physical setup.
   - Works alongside the Software and Hardware design teams as one of the **three parallel design tracks** (Software, Hardware, Environment).
   - Owns the critical function of **Process Improvement** — continuously gathering, analyzing, and incorporating suggestions to make project processes more efficient, whether applied later in the current project or carried forward to future projects.

---

*(End of Notes — Support Processes Part 2: Configuration Management & Environment)*
