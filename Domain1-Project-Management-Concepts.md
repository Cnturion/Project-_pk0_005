# Domain 1 — Project Management Concepts

> **Exam weight: 33%** (the biggest domain). Covers the core vocabulary and methods of project management: what a project is, Agile vs. Waterfall, change/risk/issue handling, scheduling, quality, communication, meetings, teams, and procurement.

**Jump to an objective:**

- [1.1 — Project characteristics, methodologies & frameworks](#11--project-characteristics-methodologies--frameworks)
- [1.2 — Agile vs. Waterfall](#12--agile-vs-waterfall)
- [1.3 — The change control process](#13--the-change-control-process)
- [1.4 — Risk management](#14--risk-management)
- [1.5 — Issue management](#15--issue-management)
- [1.6 — Schedule development & management](#16--schedule-development--management)
- [1.7 — Quality & performance management](#17--quality--performance-management)
- [1.8 — Communication management](#18--communication-management)
- [1.9 — Meeting management](#19--meeting-management)
- [1.10 — Team & resource management](#110--team--resource-management)
- [1.11 — Procurement & vendor selection](#111--procurement--vendor-selection)

---

## 1.1 — Project characteristics, methodologies & frameworks

### What makes something a project?

A project is a **one-and-done effort**. Three things define it:

- **Unique** — it produces a one-of-a-kind result.
- **Temporary** — it has a clear start and finish.
- **Purposeful** — it exists to deliver business value.

### Project, program, or portfolio?

These three nest inside each other:

- **Program** — a group of *related* projects run together. The focus is the **interdependencies** between them.
- **Portfolio** — all the projects and programs, chosen to push the organization's **strategic goals**. This is the big-picture, "do these even align with our strategy?" view.

A project can stand alone, live inside a program, or live inside a portfolio.

```mermaid
flowchart TD
    PF[Portfolio<br/>Strategic alignment] --> PG1[Program A<br/>Related projects]
    PF --> PG2[Program B<br/>Related projects]
    PF --> P5[Standalone Project]
    PG1 --> P1[Project 1]
    PG1 --> P2[Project 2]
    PG2 --> P3[Project 3]
    PG2 --> P4[Project 4]
```

### Methodologies & frameworks to know

**Scrum** is an Agile framework. Beyond it, expect these on the exam:

- **Kanban** — a "pull-based" approach using a Kanban board so work flows continuously.
- **Extreme Programming (XP)** — focused on technical excellence: pair programming, collective code ownership, test-driven development, spiking, refactoring, continuous integration.
- **SAFe (Scaled Agile Framework)** — best practices for doing Agile at enterprise scale.
- **PRINCE2 (PRojects IN Controlled Environments)** — an organized, controlled start, middle, and end.
- **SDLC (Software Development Life Cycle)** — plan, design, build, test, deploy.
- **DevOps** — combines software development and IT operations.
- **DevSecOps** — DevOps with security built in by design.

![Methodologies and frameworks summary](images/01-methodologies-summary.png)

---

## 1.2 — Agile vs. Waterfall

### The one-line difference

- **Waterfall** — *predictive*. You plan it all up front; changes aren't expected (only essential ones).
- **Agile** — *iterative and incremental*. You build in small pieces and adapt as you go.

### The Agile Manifesto

> We value:
>
> - **Individuals and interactions** over processes and tools
> - **Working software** over comprehensive documentation
> - **Customer collaboration** over contract negotiation
> - **Responding to change** over following a plan
>
> There's value in the items on the right, but we value the items on the left more.

Source: <https://agilemanifesto.org/>

### The 12 Principles of Agile

1. Satisfy the customer through early and continuous delivery of valuable software.
2. Welcome changing requirements — it gives the customer a competitive advantage.
3. Deliver working software frequently.
4. Business people and developers work together daily.
5. Build projects around motivated people; give them what they need.
6. Face-to-face conversation is the best form of communication.
7. Working software is the primary measure of progress.
8. Maintain a constant, sustainable pace.
9. Keep up continuous attention to technical excellence and good design.
10. Simplicity — maximize the work *not* done.
11. The best work emerges from self-organizing teams.
12. At regular intervals, reflect, then tune and adjust behavior.

---

## 1.3 — The change control process

**The point:** stop **scope creep** by running every change through a defined process.

A change request can come from anyone on the project. It should be in writing and explain *why*.

### The 12 steps

1. **Create / receive** the change request.
2. **Log** it in the change request log.
3. **Preliminary review** — chat with the team and SMEs: is it feasible?
4. **Assess impact** — what else does this touch?
5. **Document the recommendation** from that assessment.
6. **Determine the decision makers**.
7. **Escalate to the CCB** (Change Control Board) — the panel that approves or denies.
8. **Document and communicate the status.** *If denied, it stops here.*
9. **Update the project plan** (schedule, scope statement, etc.).
10. **Implement** the change.
11. **Validate** the implementation.
12. **Communicate** the deployment.

```mermaid
flowchart TD
    A[1. Create/Receive] --> B[2. Log Request]
    B --> C[3. Preliminary Review]
    C --> D[4. Assess Impact]
    D --> E[5. Document<br/>Recommendation]
    E --> F[6. Determine<br/>Decision Makers]
    F --> G[7. Escalate to CCB]
    G --> H{8. Decision}
    H -->|Denied| Z[Stop — document<br/>and communicate]
    H -->|Approved| I[9. Update Plan]
    I --> J[10. Implement]
    J --> K[11. Validate]
    K --> L[12. Communicate]
```

---

## 1.4 — Risk management

### What a risk is

A **risk** is an *uncertain* event that, if it happens, will affect the project. It can be **negative or positive**. We identify, analyze, and plan responses during **planning**.

Agile carries more uncertainty by nature, so it manages risk by committing to only a little work at a time.

### Identifying risks: SWOT

| | Positive | Negative |
|---|---|---|
| **Internal** | **Strengths** — what we do well | **Weaknesses** — internal gaps |
| **External** | **Opportunities** — favorable outside factors | **Threats** — supply-chain issues, new laws, etc. |

**Known risks** are the ones we can anticipate.

### Analyzing risks

- **Qualitative** — rank risks by urgency, manageability, controllability, detectability.
- **Impact analysis** (probability vs. impact) — e.g., *low probability, medium impact*.
- **Quantitative** — assign a cost or time value. Can use simulations like **Monte Carlo analysis**.
- **Scenario analysis** — "what if?"
- **Situational analysis** — examine internal and external factors.

![Risk analysis key takeaways](images/16-risk-analysis-takeaways.png)

### Responding to risks

```mermaid
flowchart TD
    R{Risk type?}
    R -->|Negative<br/>Threat| N[Avoid · Mitigate<br/>Transfer · Accept]
    R -->|Positive<br/>Opportunity| P[Exploit · Enhance<br/>Share · Accept]
```

**Negative risks (threats):**

- **Avoid** — eliminate the threat. Best for high-chance, high-impact threats.
- **Mitigate** — reduce the chance or impact.
- **Transfer** — hand ownership to a third party.
- **Accept** — do nothing proactive. Best for low-priority risks.

**Positive risks (opportunities):**

- **Exploit** — make sure it happens.
- **Enhance** — increase the chance or impact.
- **Share** — partner with a third party to share the upside.
- **Accept** — do nothing proactive.

---

## 1.5 — Issue management

### Risk vs. issue

A **risk** *might* happen. An **issue** has *already* happened and is impacting the project right now. **Issues are always negative** — think of an issue as a risk that came true.

![An issue is an unidentified risk that has occurred](images/17-issue-vs-risk.png)

### Handling an issue

- Record it in the **issue log**.
- Notify the right stakeholders.
- Build a **resolution plan**:
  - Prioritize by severity, impact, and urgency.
  - Do **root cause analysis** (e.g., cause-and-effect diagrams).
  - Apply a **workaround** if needed.
- Document the outcome and update other project docs.

### Risk & issue documentation

- **Risk Management Plan** — your "how-to" guide for handling risk. Part of the project plan.
- **Risk Register** — the running list of risks (ID, description, owner). Usually a spreadsheet; review it regularly.
- **Contingency Plan** — your planned response to identified risks.
- **Fallback Plan** — plan B.
- **Issue Log** — the running record of issues and their status.

---

## 1.6 — Schedule development & management

Mostly a Waterfall topic. Four moving parts: estimate durations, sequence activities, build the schedule, assign resources.

### Estimating durations

Break the WBS into work packages, then into activities. Four techniques, from fastest to most accurate:

1. **Analogous** — use a similar past project. Apples to apples.
2. **Parametric** — simple math (1 day per chimney → 4 chimneys = 4 days).
3. **Three-point** — use three values for a more realistic estimate.
4. **Bottom-up** — estimate every component and total it.

**Terms to keep straight:**

- **Effort** — the work required (hours, days, weeks).
- **Duration** — factors in the resources assigned.
- **Elapsed time** — factors in how much work fits each day/week.
- **Contingency reserves (buffers)** — cushion time for delays.

### Sequencing activities

**Dependencies** shape the order:

- **Mandatory** — hard logic, non-negotiable.
- **Discretionary** — preferred logic, a recommendation.
- **External** — outside the team's control.
- **Internal** — inside the team's control.

**Successor/predecessor relationships:**

- **Finish-to-Start (FS)** — A must finish before B starts. *(Most common.)*
- **Start-to-Start (SS)** — A must start before B starts.
- **Finish-to-Finish (FF)** — A must finish before B finishes.
- **Start-to-Finish (SF)** — A must start before B finishes. *(Rare.)*

```mermaid
flowchart LR
    subgraph FS["Finish-to-Start"]
        A1[A finishes] --> B1[B starts]
    end
    subgraph SS["Start-to-Start"]
        A2[A starts] --> B2[B starts]
    end
    subgraph FF["Finish-to-Finish"]
        A3[A finishes] --> B3[B finishes]
    end
    subgraph SF["Start-to-Finish"]
        A4[A starts] --> B4[B finishes]
    end
```

### Building the schedule

- **PERT chart** (Program Evaluation and Review Technique) — a network diagram; an example of the **Precedence Diagramming Method (PDM)**.

  ![PERT chart](images/13-pert-chart.png)

- **Gantt chart** — bars show each task's timeline.

  ![Gantt chart](images/14-gantt-chart.png)

- **Critical path** — the longest sequence of activities; it sets the shortest possible project duration.

  ![The critical path](images/15-critical-path.png)

> Formulas for PERT, early/late start and finish, float, and the critical path are in the *Formulas Reference* PDF.

### Assigning resources

- **Resource loading** — fill team members' available time with tasks.
- **Resource leveling** — adjust the schedule to match resource availability.
- **Resource smoothing** — delay tasks only within their **float** (the slack a task has before it delays the project).
- **Schedule compression** — finish faster without cutting scope:
  - **Fast tracking** — overlap critical-path tasks. *May add risk.*
  - **Crashing** — add resources to critical-path tasks.

### Budget basics

- **Cost baseline** — the approved, time-phased budget (excludes management reserves). Changes only through formal change control.
- **Cost estimate** — the likely cost of *all* resources for an activity (labor, materials, equipment).
- **Contingency reserves** — for *known* risks; sit inside the baseline.
- **Management reserves** — for *unknown* issues; sit *outside* the baseline.

### Agile scheduling

- **Story point** — a unit of estimated *effort* for a backlog item. Just an estimate.
- **Velocity** — how much work the team finishes per sprint (sum of completed story points from past sprints).
- **Epic** — a big chunk of work spanning multiple sprints; often a broad, not-yet-defined area.
- **Sprint planning** — the sponsor sets the sprint goal; chosen stories support that goal, are sized and prioritized, and fit the team's velocity.
- **Release planning** — decides *when* features ship to users.

---

## 1.7 — Quality & performance management

### Tracking performance

Compare current performance against the **baselines** in the original project management plan.

- **Cost Variance (CV)** — work done vs. money spent. *Negative = over budget.*
- **Schedule Variance (SV)** — work done vs. work planned. *Negative = behind schedule.*
- **Iteration burndown chart** — work remaining in the iteration.
- **KPIs** — measurable values that track progress.
- **Phase gate review** — a checkpoint at the end of a phase: continue or not?

![Monitoring budget key takeaways](images/23-monitoring-budget.png)

> See [Domain 3 → 3.3](Domain3-Tools-and-Documentation.md#33--quality--performance-charts) for the charts that visualize this data.

### Managing quality

A **quality management plan** is your "how-to" guide for quality. Quality work leans on **audits and inspections** plus charts (covered in Domain 3).

### Testing types

- **Unit** — one piece of code works on its own.
- **Integration** — combined units work as a group.
- **Regression** — everything still works after changes.
- **Smoke** — quick check that the big stuff works.
- **Stress** — stability under heavy load.
- **Performance** — speed, stability, responsiveness.
- **User acceptance (UAT)** — the end user confirms it does the job.

### Verification vs. validation

- **Verification** — does it meet the spec/requirement? Done through QC. *Did we build it right?*
- **Validation** — formal acceptance that it matches scope. Happens *after* verification. *Did we build the right thing?*

Validation happens as major deliverables land, the customer may request changes first, and you do it **even if the project is cancelled**.

### Lessons learned & reviews

**Lessons learned** capture what worked and what didn't, to improve future projects. Run a review meeting with the team, key stakeholders, and the sponsor.

![Lessons learned](images/28-lessons-learned.png)

**Two kinds of knowledge:**

- **Explicit** — written down and easily shared (documents, reports).
- **Tacit** — personal insight and intuition; hard to capture.

**Review types:**

- **Phase gate review** — end of a phase; continue or not.
- **Sprint review** — *product*-focused; product owner, dev team, and interested stakeholders attend.
- **Sprint retrospective** — *process*-focused; the team reflects and adjusts.

![Reviews key takeaways](images/29-reviews-takeaways.png)

---

## 1.8 — Communication management

### Pick the right method

- **Written** — consider the audience and flow; you can take your time.
- **Verbal** — tone, body language, word choice.
- **Formal** vs. **informal**.
- **Synchronous** (real time) — meetings, calls, chat.
- **Asynchronous** (not real time) — email, SMS, reports.
- **Internal** vs. **external**.

**Quick rules of thumb:**

- Sensitive issue → **face-to-face**.
- Detailed info → **written**.
- Routine updates → **weekly emails**, consistent format.

### Common challenges

Language barriers, cultural differences, time zones / geography, and technology gaps.

### Planning communications

The communication plan defines **who** gets **what**, in which **format**, and **how often**.

- Start from stakeholder needs.
- Use templates and guidelines.
- Mind constraints — tech limits, data-protection rules, org policy.
- Decide where records are archived.
- Monitor effectiveness and adjust.

![Communications plan key takeaways](images/22-communications-plan.png)

---

## 1.9 — Meeting management

### Three meeting types

- **Collaborative** — workshops, focus groups, reviews, brainstorming.
- **Informative** — demos, presentations, stand-ups, status updates.
- **Decisive** — backlog refinement, task setting, committee meetings.

### Run it well

- Invite the right people.
- Send an agenda ahead of time.
- Assign roles:
  - **Facilitator** — keeps it on time and on topic; owns follow-ups.
  - **Scribe** — agreed in advance to take notes.
  - **Target audience** — the attendees who need to be there.
- Keep to time, stay on topic, manage follow-ups.

---

## 1.10 — Team & resource management

### Resource types

**Physical resources:**

- **Capital resources** — reusable physical assets (machines, buildings).
- **Resource life cycle:**

```mermaid
flowchart LR
    A[Acquisition] --> B[Maintenance]
    B --> C[Hardware<br/>Decommissioning]
    C --> D[End-of-Life<br/>Software]
    D --> E[Successor<br/>Planning]
```

**Human resources:**

- **Dedicated** — 100% on the project. **Shared** — only a slice of their time.
- **Over-allocated** — too much assigned. **Benched** — available but idle.
- **Internal** (employees) vs. **external** (contractors).
- **Core/operational** — there start to finish. **Extended/functional** — jumps in when needed.

### Organizational structures

How much authority the PM has depends on the structure:

| Structure | PM authority |
|---|---|
| **Functional** | Limited — staff grouped by specialty |
| **Weak matrix** | Low to none |
| **Balanced matrix** | Medium |
| **Strong matrix** | Moderate to high |
| **Projectized** | High to almost total — staff grouped by project |

In a **matrix**, the PM *shares* authority with functional managers.

![Functional organization](images/18-functional-organization.png)

![Projectized organization](images/19-projectized-organization.png)

### Key roles

- **Project Manager** — leads the team; controls the budget, decisions, and resources.
- **Functional Manager** — runs a business unit.
- **Project Coordinator** — limited authority (functional / weak-matrix setups).
- **Sponsor** — pays for the project; may be the customer.
- **Stakeholder** — anyone affected by the project, internal or external.
- **PMO** — supports project management efforts.
- **Program Manager** — coordinates related projects toward a business goal.
- **Business Analyst** / **Product Manager** — focus on the end product.
- **Project Team** — architects (design), developers/engineers (build), testers/QA (verify), SMEs (specialist knowledge).
- **Scrum Master** — servant leader who clears blockers for the Agile team.

### Acquiring & assigning resources

- **Gap analysis** — measure where you are vs. where you want to be (resource pool, skills).
- For external resources, use **vendor evaluation** (cost-benefit, competitive analysis, technical approach, references).
- **Resource loading** fills available time with tasks; use the **project org chart** and **RACI matrix** as tools.

![Assigning resources](images/20-assigning-resources.png)

### Team development — the Tuckman Ladder

```mermaid
flowchart LR
    F[Forming] --> S[Storming]
    S --> N[Norming]
    N --> P[Performing]
    P --> A[Adjourning]
```

- **Forming** — getting acquainted; still a group, not a team.
- **Storming** — roles emerge; performance can dip.
- **Norming** — trust and collaboration build.
- **Performing** — the team clicks and builds on each other's ideas.
- **Adjourning** — the team wraps up and disbands.

![The Tuckman Ladder](images/21-tuckman-ladder.png)

---

## 1.11 — Procurement & vendor selection

### How will we get the resource?

- **Build / make**, **Buy**, **Lease**, or **Subscription / pay-as-you-go**.

**CapEx vs. OpEx:**

- **CapEx (capital expenditure)** — big investments on the balance sheet, depreciated over time.
- **OpEx (operational expenditure)** — ongoing expenses, often tax-deductible.

### Artifacts we may already have

- **Pre-qualified vendors** — an approved-vendor list.
- **Pre-determined clients** — partners who resell our product.
- **Pre-existing contracts** — agreements already in place that the project can use instead of starting from scratch.

### Engaging vendors (the "RFx" docs)

- **RFI** — Request for Information. Early fact-finding to learn what vendors can offer.
- **RFP** — Request for Proposal (detailed, complex; design approach, timelines, costs).
- **RFQ** — Request for Quote. Asks vendors for a price on clearly defined goods/services.
- **RFB** — Request for Bid. Invites vendors to bid on well-specified work, usually competing on price.

![Procurement preferences and artifacts summary](images/04-procurement-summary.png)

### Contract types

- **Fixed-price** — a set price; best when scope is well defined. Three flavors:
  - **FFP (Firm Fixed Price)** — one set price, no adjustments.
  - **FPIF (Fixed Price Incentive Fee)** — fixed price plus a bonus for hitting targets (e.g., early delivery).
  - **FPEPA (Fixed Price with Economic Price Adjustment)** — fixed price that can flex with inflation or currency shifts on long contracts.
- **Cost plus (cost reimbursable)** — buyer pays the cost *plus* a fee; best when scope will change a lot. Three flavors:
  - **CPFF (Cost Plus Fixed Fee)** — costs reimbursed plus a fixed fee.
  - **CPIF (Cost Plus Incentive Fee)** — costs reimbursed plus a performance-based bonus.
  - **CPAF (Cost Plus Award Fee)** — costs reimbursed plus a fee the buyer awards based on satisfaction.
- **Time and materials** — a hybrid of the two; e.g., labor billed at an hourly rate plus materials.

### Other vendor documents

- **SOW** — Statement of Work (what we're buying).
- **TOR** — Terms of Reference (scope, timeline, resources).
- **NDA** — Non-Disclosure Agreement.
- **C&D Letter** — Cease and Desist (stop now and don't repeat).
- **LOI** — Letter of Intent. **MOU** — Memorandum of Understanding.
- **MSA** — Master Service Agreement (umbrella terms for future contracts).
- **SLA** — Service Level Agreement (expected service level).
- **Maintenance Agreement** — a contract for ongoing upkeep, support, or servicing of a product after delivery (e.g., scheduled servicing, fixes, updates).
- **Warranty** — the vendor's promise that a product will work as specified for a set period, and that they'll repair or replace it if it doesn't.
- **PO** — Purchase Order (buyer's commitment to pay).

![Vendor and procurement documents summary](images/40-vendor-procurement-documents.png)
