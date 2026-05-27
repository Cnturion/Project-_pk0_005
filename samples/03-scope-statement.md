# Scope Statement — Customer Self-Service Portal

> **Sample document** for study purposes. All names, numbers, and details are fictional. Part of the shared example project: *Northwind Retail — Customer Self-Service Portal*.

| | |
|---|---|
| **Project** | Customer Self-Service Portal |
| **Project ID** | NWR-2026-014 |
| **Author** | Priya Shah, Project Manager |
| **Version** | 1.0 (approved — part of the scope baseline) |
| **Date** | January 28, 2026 |

## Product scope (what it does)

A responsive web portal, integrated with Northwind's order system, that lets authenticated customers:

- View order history and real-time order status.
- Track shipments with carrier updates.
- Initiate and track returns online.
- Manage their account profile and reset their own password.

## Project scope (the work to deliver it)

Requirements gathering, UX design, front-end and back-end development, integration with the order and returns systems, security review, user acceptance testing, deployment, and call-center staff training.

## Deliverables

| Deliverable | Acceptance criteria |
|---|---|
| Customer login & account management | A customer can register, log in with multi-factor authentication, and reset a password without agent help. |
| Order history & status view | Orders from the last 24 months display with correct, real-time status. |
| Shipment tracking | Tracking reflects carrier status within 15 minutes of an update. |
| Online returns | A customer can start a return and receive a return label; the request appears in the agent queue. |
| Trained support staff | 100% of call-center agents complete portal training before go-live. |

## Acceptance criteria (overall)

The portal passes user acceptance testing with no open Critical or High defects, meets the security review, and handles the four in-scope request types end to end.

## Exclusions (explicitly out of scope)

- Native iOS/Android apps (web-responsive only).
- Live chat or chatbot support.
- Loyalty/rewards program.
- Adding or changing stored payment methods.

## Assumptions & constraints

- **Assumption:** the order system API supports the required read/write calls.
- **Constraint:** must launch by June 30, 2026, within the $180,000 budget.

> The approved scope statement, the work breakdown structure (WBS), and the WBS dictionary together form the **scope baseline**.
