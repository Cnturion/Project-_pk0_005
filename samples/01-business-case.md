# Business Case — Customer Self-Service Portal

> **Sample document** for study purposes. All names, numbers, and details are fictional. Part of the shared example project: *Northwind Retail — Customer Self-Service Portal*.

| | |
|---|---|
| **Project** | Customer Self-Service Portal |
| **Project ID** | NWR-2026-014 |
| **Prepared by** | Tom Reyes, Business Analyst |
| **Sponsor** | Maria Alvarez, VP Customer Experience |
| **Date** | December 8, 2025 |
| **Status** | Approved |

## 1. Business need / problem statement

Northwind Retail's call center handles roughly **12,000 routine contacts per month** — order status, shipment tracking, returns, and password resets. These cost an estimated **$6.50 per contact** and spike after business hours, when no self-service option exists. Customer satisfaction (CSAT) for these interactions sits at **71%**, below our 80% target.

## 2. Current state vs. future state

- **Current state:** Customers must call or email during business hours for routine requests. Agents spend ~60% of their time on tasks customers could self-serve.
- **Future state:** A web portal lets customers view orders, track shipments, initiate returns, and manage their accounts 24/7 — freeing agents for higher-value work.

## 3. Options considered

| Option | Description | Verdict |
|---|---|---|
| **A. Do nothing** | Keep the call-center-only model. | Rejected — costs keep rising; CSAT stays low. |
| **B. Buy off-the-shelf portal** | License a third-party SaaS portal. | Rejected — poor fit with our order system; high recurring fees. |
| **C. Build a custom portal** | Build on our existing cloud stack, integrate with the order system. | **Recommended** — best fit, controllable cost, reuses current contracts. |

## 4. Cost / benefit summary

- **Estimated cost:** $180,000 (one-time build) + ~$18,000/year hosting and support.
- **Estimated benefit:** Deflecting 35% of routine contacts saves ~$327,000/year in handling costs.
- **Payback period:** ~7 months.
- **Return on investment (ROI):** ~80% in year one.

## 5. Recommendation

Proceed with **Option C — build a custom Customer Self-Service Portal**. The investment pays back in under a year, reduces operating costs, and directly improves customer satisfaction.

## 6. High-level risks

- Integration delays with the payment/returns vendor API.
- Protecting customer personally identifiable information (PII) in the portal.
- Scope creep from stakeholder feature requests.
