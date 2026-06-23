# Visual Cheat Sheets — CompTIA Project+ (PK0-005)

Quick visual references for the most important PK0-005 concepts, all in one place. Each cheat sheet is a Mermaid concept map that renders right here on GitHub.

**How to read them**

- The center is the topic.
- The first level groups items into categories.
- Leaves give the term plus a one-line definition; *italics* flag qualifiers.
- Colors carry meaning per topic: red = negative/threat, green = positive/safe, amber = caution/medium, blue = neutral, purple = hybrid.

## Contents

1. [Project Life Cycle Phases](#01--project-life-cycle-phases) — Domain 2
2. [Methodologies and Frameworks](#02--methodologies-and-frameworks) — 1.1 · 1.2
3. [Project Selection Methods](#03--project-selection-methods) — 2.1
4. [RFx Documents (RFI / RFP / RFQ / RFB)](#04--rfx-documents-engaging-vendors) — 1.11
5. [Vendor Contract Types](#05--vendor-contract-types) — 1.11
6. [Estimating Methods](#06--estimating-methods) — 1.6
7. [Dependency Types](#07--dependency-types) — 1.6
8. [Risk Analysis Methods](#08--risk-analysis-methods) — 1.4
9. [Risk Responses](#09--risk-responses) — 1.4
10. [Tuckman Ladder](#10--tuckman-ladder-team-development) — 1.10
11. [Organizational Structures](#11--organizational-structures-pm-authority-gradient) — 1.10
12. [RACI Roles](#12--raci-roles) — 2.2
13. [Conflict Management (Thomas-Kilmann)](#13--conflict-management-thomas-kilmann) — 2.4
14. [Meeting Types](#14--meeting-types) — 1.9
15. [Quality and Performance Charts](#15--quality-and-performance-charts) — 3.3
16. [Cloud Models](#16--cloud-models) — 4.4
17. [EVM — Earned Value Management Formulas](#17--evm--earned-value-management-formulas) — 1.7
18. [Study and Exam Tips](#study-and-exam-tips)

---

## 01 — Project Life Cycle Phases

```mermaid
flowchart LR
    A["<b>1. Discovery</b><br/>Concept prep<br/><i>Is it worth doing?</i>"]
    B["<b>2. Initiation</b><br/>Authorize<br/>the project"]
    C["<b>3. Planning</b><br/>Build the<br/>detailed plan"]
    D["<b>4. Execution</b><br/>Do the work;<br/>track it"]
    E["<b>5. Closing</b><br/>Validate,<br/>sign off, hand over"]
    A --> B --> C --> D --> E

    classDef phase fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    class A,B,C,D,E phase
```

> Full walkthrough and document flow: [Domain 2](Domain2-Project-Life-Cycle-Phases.md).

---

## 02 — Methodologies and Frameworks

```mermaid
flowchart TD
    R(("Methodologies<br/>and Frameworks"))
    R --> PRE["<b>Predictive</b><br/>Plan up front"]
    R --> AGI["<b>Agile</b><br/>Iterative and<br/>incremental"]
    R --> OPS["<b>Hybrid / Ops</b><br/>Dev plus IT practices"]

    PRE --> WF[<b>Waterfall</b><br/>Sequential phases]
    PRE --> P2[<b>PRINCE2</b><br/>Controlled start,<br/>middle, and end]
    PRE --> SD[<b>SDLC</b><br/>Plan, design, build,<br/>test, deploy]

    AGI --> SC[<b>Scrum</b><br/>Sprints + defined roles]
    AGI --> KB[<b>Kanban</b><br/>Pull-based,<br/>continuous flow]
    AGI --> XP[<b>XP</b><br/>Technical excellence,<br/>pair programming]
    AGI --> SF[<b>SAFe</b><br/>Agile at<br/>enterprise scale]

    OPS --> DO[<b>DevOps</b><br/>Dev + IT Ops]
    OPS --> DS[<b>DevSecOps</b><br/>DevOps + security<br/>by design]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef pre fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    classDef agi fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    classDef ops fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    class R root
    class PRE,WF,P2,SD pre
    class AGI,SC,KB,XP,SF agi
    class OPS,DO,DS ops
```

> See [Domain 1 → 1.1](Domain1-Project-Management-Concepts.md#11--project-characteristics-methodologies--frameworks) and [1.2](Domain1-Project-Management-Concepts.md#12--agile-vs-waterfall).

---

## 03 — Project Selection Methods

```mermaid
flowchart TD
    R(("Project<br/>Selection<br/>Methods"))
    R --> MM["<b>Mathematical<br/>Modeling</b><br/>Formulas against<br/>constraints"]
    R --> BC["<b>Benefits<br/>Comparisons</b><br/>Weigh financial<br/>return"]

    BC --> NPV[<b>NPV</b><br/>Net Present Value<br/><i>Bigger = better</i>]
    BC --> ROI[<b>ROI</b><br/>Return on Investment<br/><i>% return</i>]
    BC --> IRR[<b>IRR</b><br/>Internal Rate of Return<br/><i>Bigger = better</i>]
    BC --> BCR[<b>BCR</b><br/>Benefit-to-Cost Ratio<br/><i>$ back per $1 in</i>]
    BC --> PBP[<b>PBP</b><br/>Payback Period<br/><i>Shorter = better</i>]
    BC --> SM[<b>Scoring Model</b><br/>Weighted criteria,<br/>score each project]
    BC --> OC[<b>Opportunity Cost</b><br/>What you give up<br/>by choosing this]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef item fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    class R root
    class MM,BC cat
    class NPV,ROI,IRR,BCR,PBP,SM,OC item
```

> See [Domain 2 → 2.1](Domain2-Project-Life-Cycle-Phases.md#21--discovery--concept-preparation).

---

## 04 — RFx Documents (Engaging Vendors)

```mermaid
flowchart TD
    R(("RFx<br/>Documents"))
    R --> RFI["<b>RFI</b><br/>Request for Information<br/><i>Early fact-finding;<br/>what can vendors offer?</i>"]
    R --> RFP["<b>RFP</b><br/>Request for Proposal<br/><i>Detailed; design approach,<br/>timeline, cost</i>"]
    R --> RFQ[<b>RFQ</b><br/>Request for Quote<br/><i>Price on well-defined<br/>goods/services</i>]
    R --> RFB[<b>RFB</b><br/>Request for Bid<br/><i>Bid on well-specified work,<br/>often price-competitive</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef rfx fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    class R root
    class RFI,RFP,RFQ,RFB rfx
```

> See [Domain 1 → 1.11](Domain1-Project-Management-Concepts.md#111--procurement--vendor-selection).

---

## 05 — Vendor Contract Types

```mermaid
flowchart TD
    R(("Vendor<br/>Contract Types"))
    R --> FP["<b>Fixed-Price</b><br/>Set price<br/><i>Best when scope is<br/>well defined</i>"]
    R --> CP["<b>Cost-Plus</b><br/>Cost + a fee<br/><i>Best when scope<br/>will change</i>"]
    R --> TM["<b>Time and<br/>Materials</b><br/>Hybrid<br/><i>e.g., hourly rate<br/>+ materials</i>"]

    FP --> F1[<b>FFP</b><br/>Firm Fixed Price<br/><i>No adjustments</i>]
    FP --> F2[<b>FPIF</b><br/>Fixed Price Incentive Fee<br/><i>+ bonus for hitting targets</i>]
    FP --> F3[<b>FPEPA</b><br/>+ Economic Price Adjustment<br/><i>Flexes with inflation</i>]

    CP --> C1[<b>CPFF</b><br/>Cost Plus Fixed Fee<br/><i>+ flat fee</i>]
    CP --> C2[<b>CPIF</b><br/>Cost Plus Incentive Fee<br/><i>+ performance bonus</i>]
    CP --> C3[<b>CPAF</b><br/>Cost Plus Award Fee<br/><i>+ buyer-awarded fee</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef fp fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    classDef cp fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    classDef tm fill:#F0E4F4,stroke:#7D3C98,color:#1a1a1a
    class R root
    class FP,CP,TM cat
    class F1,F2,F3 fp
    class C1,C2,C3 cp
```

> See [Domain 1 → 1.11](Domain1-Project-Management-Concepts.md#111--procurement--vendor-selection).

---

## 06 — Estimating Methods

> Ordered from **fastest / least accurate** to **slowest / most accurate**.

```mermaid
flowchart LR
    A["<b>1. Analogous</b><br/>Use a similar<br/>past project<br/><i>Fastest;<br/>least accurate</i>"]
    B["<b>2. Parametric</b><br/>Simple math<br/><i>e.g., 1 day per<br/>chimney → 4 = 4</i>"]
    C["<b>3. Three-Point</b><br/>Use three values<br/><i>O + 4M + P,<br/>then divide by 6</i>"]
    D["<b>4. Bottom-Up</b><br/>Estimate every<br/>component, total it<br/><i>Slowest;<br/>most accurate</i>"]
    A --> B --> C --> D

    classDef est fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    class A,B,C,D est
```

> See [Domain 1 → 1.6](Domain1-Project-Management-Concepts.md#16--schedule-development--management).

---

## 07 — Dependency Types

```mermaid
flowchart TD
    R(("Dependencies"))
    R --> DEP["<b>Dependency<br/>Drivers</b>"]
    R --> REL["<b>Successor/Predecessor<br/>Relationships</b>"]

    DEP --> D1["<b>Mandatory</b><br/><i>Hard logic;<br/>non-negotiable</i>"]
    DEP --> D2["<b>Discretionary</b><br/><i>Preferred logic;<br/>a recommendation</i>"]
    DEP --> D3[<b>External</b><br/><i>Outside team control</i>]
    DEP --> D4[<b>Internal</b><br/><i>Inside team control</i>]

    REL --> R1[<b>FS</b> · Finish-to-Start<br/>A finishes → B starts<br/><i>Most common</i>]
    REL --> R2[<b>SS</b> · Start-to-Start<br/>A starts → B starts]
    REL --> R3[<b>FF</b> · Finish-to-Finish<br/>A finishes → B finishes]
    REL --> R4[<b>SF</b> · Start-to-Finish<br/>A starts → B finishes<br/><i>Rare</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef dep fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    classDef rel fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    class R root
    class DEP,REL cat
    class D1,D2,D3,D4 dep
    class R1,R2,R3,R4 rel
```

> See [Domain 1 → 1.6](Domain1-Project-Management-Concepts.md#16--schedule-development--management).

---

## 08 — Risk Analysis Methods

```mermaid
flowchart TD
    R(("Risk Analysis<br/>Methods"))
    R --> QL["<b>Qualitative</b><br/>Rank by traits"]
    R --> QN["<b>Quantitative</b><br/>Assign cost or time"]
    R --> IM["<b>Impact Analysis</b><br/>Probability × Impact"]
    R --> SC["<b>Scenario</b><br/>'What if?'"]
    R --> SI["<b>Situational</b><br/>Internal + external<br/>factors"]

    QL --> QL1[Urgency]
    QL --> QL2[Manageability]
    QL --> QL3[Controllability]
    QL --> QL4[Detectability]

    QN --> QN1[<b>Monte Carlo</b><br/>Simulation<br/><i>Common technique</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef leaf fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    class R root
    class QL,QN,IM,SC,SI cat
    class QL1,QL2,QL3,QL4,QN1 leaf
```

> See [Domain 1 → 1.4](Domain1-Project-Management-Concepts.md#14--risk-management).

---

## 09 — Risk Responses

```mermaid
flowchart TD
    R(("Risk<br/>Responses"))
    R --> NEG["<b>Negative</b><br/>Threats"]
    R --> POS["<b>Positive</b><br/>Opportunities"]

    NEG --> A1["<b>Avoid</b><br/>Eliminate the threat<br/><i>best for high-chance,<br/>high-impact</i>"]
    NEG --> A2["<b>Mitigate</b><br/>Reduce chance<br/>or impact"]
    NEG --> A3["<b>Transfer</b><br/>Hand to a<br/>third party"]
    NEG --> A4["<b>Accept</b><br/>Do nothing<br/><i>best for<br/>low-priority risks</i>"]

    POS --> B1["<b>Exploit</b><br/>Make sure<br/>it happens"]
    POS --> B2["<b>Enhance</b><br/>Increase chance<br/>or impact"]
    POS --> B3["<b>Share</b><br/>Partner with a<br/>third party"]
    POS --> B4["<b>Accept</b><br/>Do nothing"]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef neg fill:#FCE4E4,stroke:#C0392B,color:#1a1a1a
    classDef pos fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    class R root
    class NEG,A1,A2,A3,A4 neg
    class POS,B1,B2,B3,B4 pos
```

> See [Domain 1 → 1.4](Domain1-Project-Management-Concepts.md#14--risk-management).

---

## 10 — Tuckman Ladder (Team Development)

```mermaid
flowchart LR
    F["<b>1. Forming</b><br/>Getting acquainted;<br/>still a group,<br/>not a team"]
    S["<b>2. Storming</b><br/>Roles emerge;<br/>friction shows;<br/>performance can dip"]
    N["<b>3. Norming</b><br/>Trust and<br/>collaboration build"]
    P["<b>4. Performing</b><br/>Team clicks;<br/>builds on each<br/>other's ideas"]
    A["<b>5. Adjourning</b><br/>Team wraps up<br/>and disbands"]
    F --> S --> N --> P --> A

    classDef stage fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    class F,S,N,P,A stage
```

> See [Domain 1 → 1.10](Domain1-Project-Management-Concepts.md#110--team--resource-management).

---

## 11 — Organizational Structures (PM Authority Gradient)

> Colored by **how much authority the PM has**: red = low, amber = medium, green = high.

```mermaid
flowchart TD
    R(("Organizational<br/>Structures"))
    R --> F["<b>Functional</b><br/>Grouped by specialty<br/><i>PM: limited authority</i>"]
    R --> WM["<b>Weak Matrix</b><br/>Functional with a PM<br/><i>PM: low to no authority</i>"]
    R --> BM["<b>Balanced Matrix</b><br/>Mix of both<br/><i>PM: medium authority</i>"]
    R --> SM["<b>Strong Matrix</b><br/>Project-oriented<br/><i>PM: moderate to high</i>"]
    R --> PR["<b>Projectized</b><br/>Grouped by project<br/><i>PM: high to<br/>almost total</i>"]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef low fill:#FCE4E4,stroke:#C0392B,color:#1a1a1a
    classDef med fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    classDef hi fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    class R root
    class F,WM low
    class BM med
    class SM,PR hi
```

> See [Domain 1 → 1.10](Domain1-Project-Management-Concepts.md#110--team--resource-management).

---

## 12 — RACI Roles

```mermaid
flowchart TD
    R(("RACI<br/>Responsibility<br/>Assignment"))
    R --> RE[<b>R · Responsible</b><br/>Does the work]
    R --> AC[<b>A · Accountable</b><br/>Owns the outcome<br/><i>Only one per task</i>]
    R --> CO[<b>C · Consulted</b><br/>Gives input<br/>beforehand]
    R --> IN[<b>I · Informed</b><br/>Kept in the loop<br/>after the fact]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef r fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    classDef a fill:#FCE4E4,stroke:#C0392B,color:#1a1a1a
    classDef c fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    classDef i fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    class R root
    class RE r
    class AC a
    class CO c
    class IN i
```

> See [Domain 2 → 2.2](Domain2-Project-Life-Cycle-Phases.md#22--initiation) and the [sample RACI Matrix](samples/09-raci-matrix.xlsx).

---

## 13 — Conflict Management (Thomas-Kilmann)

```mermaid
flowchart TD
    R(("Conflict<br/>Management<br/>Thomas-Kilmann"))
    R --> AV[<b>Avoiding</b><br/><i>Emotionally charged moments,<br/>trivial issues, or<br/>wrong time/place</i>]
    R --> FO["<b>Forcing</b><br/><i>Last resort;<br/>quick call on a<br/>high-priority issue</i>"]
    R --> CP["<b>Compromising</b><br/><i>Low-priority issues;<br/>preserve the relationship</i>"]
    R --> AC["<b>Accommodating</b> / Smoothing<br/><i>Extenuating circumstances;<br/>low cost to you</i>"]
    R --> CL["<b>Collaborating</b><br/><i>Complex, important,<br/>or recurring issues;<br/>permanent fix needed</i>"]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cm fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    class R root
    class AV,FO,CP,AC,CL cm
```

> See [Domain 2 → 2.4](Domain2-Project-Life-Cycle-Phases.md#24--execution).

---

## 14 — Meeting Types

```mermaid
flowchart TD
    R(("Meeting Types"))
    R --> CO[<b>Collaborative</b><br/>Group thinking]
    R --> IN[<b>Informative</b><br/>Sharing updates]
    R --> DE[<b>Decisive</b><br/>Making decisions]

    CO --> C1[Workshops]
    CO --> C2[Focus groups]
    CO --> C3[Reviews]
    CO --> C4[Brainstorming]

    IN --> I1[Demos]
    IN --> I2[Presentations]
    IN --> I3[Stand-ups]
    IN --> I4[Status updates]

    DE --> D1[Backlog refinement]
    DE --> D2[Task setting]
    DE --> D3[Committee meetings]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef co fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    classDef inf fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    classDef de fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    class R root
    class CO,IN,DE cat
    class C1,C2,C3,C4 co
    class I1,I2,I3,I4 inf
    class D1,D2,D3 de
```

> See [Domain 1 → 1.9](Domain1-Project-Management-Concepts.md#19--meeting-management).

---

## 15 — Quality and Performance Charts

```mermaid
flowchart TD
    R(("Quality and<br/>Performance<br/>Charts"))
    R --> Q[<b>Quality</b>]
    R --> P[<b>Performance and Progress</b>]

    Q --> Q1[<b>Scatter Diagram</b><br/><i>Relationship between<br/>two variables</i>]
    Q --> Q2[<b>Histogram / Pareto</b><br/><i>Frequency distribution</i>]
    Q --> Q3[<b>Control Chart</b><br/><i>Process stability</i>]
    Q --> Q4[<b>Fishbone / Ishikawa</b><br/><i>Root cause analysis</i>]
    Q --> Q5[<b>Flowchart</b><br/><i>Process steps and<br/>decision points</i>]

    P --> P1[<b>Run Chart</b><br/><i>Trends over time</i>]
    P --> P2[<b>Burndown</b><br/><i>Work remaining</i>]
    P --> P3[<b>Burnup</b><br/><i>Work completed<br/>vs. total scope</i>]
    P --> P4[<b>Velocity</b><br/><i>Work per sprint</i>]
    P --> P5[<b>Decision Tree</b><br/><i>Map of outcomes</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef q fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    classDef p fill:#FFF4E5,stroke:#D68910,color:#1a1a1a
    class R root
    class Q,P cat
    class Q1,Q2,Q3,Q4,Q5 q
    class P1,P2,P3,P4,P5 p
```

> See [Domain 3 → 3.3](Domain3-Tools-and-Documentation.md#33--quality--performance-charts).

---

## 16 — Cloud Models

```mermaid
flowchart LR
    R(("Cloud<br/>Models"))
    R --> I[<b>IaaS</b><br/>Infrastructure<br/>as a Service<br/><i>Vendor handles<br/>the hardware</i>]
    R --> P[<b>PaaS</b><br/>Platform<br/>as a Service<br/><i>Platform for<br/>building apps</i>]
    R --> S[<b>SaaS</b><br/>Software<br/>as a Service<br/><i>Ready-to-use software<br/>e.g., Salesforce, M365</i>]
    R --> X[<b>XaaS</b><br/>Anything<br/>as a Service<br/><i>Any subscribable<br/>service</i>]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cm fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    class R root
    class I,P,S,X cm
```

> See [Domain 4 → 4.4](Domain4-Basics-of-IT-and-Governance.md#44--basic-it-concepts).

---

## 17 — EVM — Earned Value Management Formulas

> Know these even if they don't appear heavily on your exam — they're the backbone of cost/schedule performance tracking. Full formula reference: [`Formulas and Equations Reference Guide for Project+ (Exam PK0-005).pdf`](Formulas%20and%20Equations%20Reference%20Guide%20for%20Project%2B%20%28Exam%20PK0-005%29.pdf).

```mermaid
flowchart TD
    R(("EVM<br/>Earned Value<br/>Management"))
    R --> IN["<b>Inputs</b>"]
    R --> VA["<b>Variances</b><br/><i>negative = bad</i>"]
    R --> PE["<b>Performance Indices</b><br/><i>&lt;1 = bad, &gt;1 = good</i>"]
    R --> FO["<b>Forecasts</b>"]

    IN --> PV[<b>PV</b> · Planned Value<br/><i>What you planned<br/>to have done by now</i>]
    IN --> EV[<b>EV</b> · Earned Value<br/><i>Value of work<br/>actually completed</i>]
    IN --> AC[<b>AC</b> · Actual Cost<br/><i>What you've actually<br/>spent so far</i>]
    IN --> BAC[<b>BAC</b> · Budget at Completion<br/><i>Total planned budget</i>]

    VA --> CV[<b>CV = EV − AC</b><br/>Cost Variance]
    VA --> SV[<b>SV = EV − PV</b><br/>Schedule Variance]

    PE --> CPI[<b>CPI = EV ÷ AC</b><br/>Cost Performance Index]
    PE --> SPI[<b>SPI = EV ÷ PV</b><br/>Schedule Performance Index]

    FO --> EAC[<b>EAC = AC + ETC</b><br/>Estimate at Completion]
    FO --> ETC["<b>ETC = BAC − EV</b><br/>Estimate to Complete<br/><i>budgeted-rate version</i>"]
    FO --> VAC[<b>VAC = BAC − EAC</b><br/>Variance at Completion]

    classDef root fill:#1F4E78,stroke:#1F4E78,color:#ffffff,stroke-width:2px
    classDef cat fill:#D6E6F2,stroke:#1F4E78,color:#1a1a1a,stroke-width:2px
    classDef leaf fill:#E4F0FA,stroke:#1F4E78,color:#1a1a1a
    classDef bad fill:#FCE4E4,stroke:#C0392B,color:#1a1a1a
    classDef good fill:#E4F4E4,stroke:#27AE60,color:#1a1a1a
    class R root
    class IN,VA,PE,FO cat
    class PV,EV,AC,BAC,EAC,ETC,VAC leaf
    class CV,SV bad
    class CPI,SPI good
```

> CV and SV are also covered in [Domain 1 → 1.7](Domain1-Project-Management-Concepts.md#17--quality--performance-management).

---

## Study and Exam Tips

> Compiled from the official PK0-005 objectives plus practical advice from a fellow exam-taker. Treat anyone's recap as one data point — your experience may differ.

### Best sources

- The [CBT Nuggets course](https://learn.adept.at/cbtnuggets/comptia-project-pk0-005) these notes come from.
- AI-generated practice exams and study guides.
- The official [exam objectives PDF](comptia-project-pk0-005-exam-objectives-(2-0).pdf.pdf) and [formulas reference](Formulas%20and%20Equations%20Reference%20Guide%20for%20Project%2B%20%28Exam%20PK0-005%29.pdf) in this repo.

### What to memorize cold

- The **5 lifecycle phases** and which documents live where — Charter = Initiation, Scope Statement = Planning, Issue Log = Execution, Lessons Learned / Closeout Report = Closing. See [Domain 2's document flow](Domain2-Project-Life-Cycle-Phases.md#putting-it-together--document-flow-across-the-phases).
- The **quality and performance charts** in cheat sheet 15 — including fishbone (Ishikawa) and flowchart.
- The **EVM formulas** in cheat sheet 17 — even if your test doesn't lean on them, they could show up.
- The **successor/predecessor dependency types** (FS / SS / FF / SF).
- **Risk responses** for both negative *and* positive risks.

### Test-day strategy

- **Brain-dump first.** As soon as you're allowed, write down formulas and mnemonics on your scratch paper so you don't have to hold them in working memory.
- **Flag performance-based questions (PBQs) and come back later.** They take longer; don't burn time at the start.
- **Read each question carefully.** Slow down on the question stem — CompTIA loves "best" and "first" qualifiers.
- **Use process of elimination.** You can usually narrow four choices to two, then pick the best fit.
- **Don't overthink.** Your first instinct is usually right.

### Don't panic about practice-test scores

It's common to score in the 60–70% range on Certmaster/Sybex practice exams and still pass the real one. The real exam tends to be more direct than the practice sets, and the PBQs are usually easier than the practice PBQs.

You've got this.
