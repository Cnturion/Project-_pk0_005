# Domain 4 — Basics of IT and Governance

> **Exam weight: 18%.** The IT, security, privacy, and governance context that surrounds project work.

**Jump to an objective:**

- [4.1 — ESG factors](#41--esg-factors)
- [4.2 — Information security](#42--information-security)
- [4.3 — Compliance & privacy](#43--compliance--privacy)
- [4.4 — Basic IT concepts](#44--basic-it-concepts)
- [4.5 — Operational change control](#45--operational-change-control)

---

## 4.1 — ESG factors

**ESG = Environmental, Social, and Governance.**

- **Environmental** — the project's impact on the environment.
- **Social** — communicate expectations with stakeholders, employees, and customers.
- **Governance** — oversight.

A project should align with the company's **vision, mission, and values**.

---

## 4.2 — Information security

### Physical security

Securing the physical asset:

- **Mobile devices** — PIN (personal identification number) lock.
- **Removable media** — encrypt; passcode to decrypt.
- **Facilities** — biometrics, badges, guards.
- **Policies** — define how assets are protected; review at least annually.

### Operational security

- **Background checks** — verify a person's information.
- **Security clearance** — selective, expensive, government-related.
- **Personnel security policy** — e.g., all new hires get background checks; secret access needs secret clearance.

### Digital security

Digital assets = data, spreadsheets, documents, etc.

- **Access & permissions** — need-to-know access.
- **Remote access** — MFA (multi-factor authentication) and authenticator apps.

### Data security & branding

Some data needs more protection than others:

| Data type | Classification |
|---|---|
| Advertising data | Public |
| HR data (PII — personally identifiable information) | Confidential, need-to-know |
| Trade secrets (IP — intellectual property) | Secret |
| National secrets | Top Secret |

**Branding restrictions** protect the company's brand:

- **Trademark (™)** — a claim to a brand/logo; no legal registration on its own.
- **Registered Trademark (®)** — certified by the US Patent and Trademark Office; adds rights.
- **Copyright (©)** — protects IP like books, music, video, and code.

---

## 4.3 — Compliance & privacy

### Data confidentiality

Protect data you own or collect:

- **Intellectual Property (IP)** and **trade secrets**.
- **PII** — Personally Identifiable Information.
- **PHI** — Protected Health Information (HIPAA).

### Privacy regulations by region

- **Canada** — PIPEDA (Personal Information Protection and Electronic Documents Act).
- **EU** — GDPR (General Data Protection Regulation).
- **US** — no single federal law; some states have their own (e.g., the CCPA — California Consumer Privacy Act).
- Also know **HIPAA** (Health Insurance Portability and Accountability Act) for health data.

### Your job as PM

Provide training, keep policies in place, and involve the legal team.

**A breach can mean:** monetary fines, lost contracts, and reputation damage.

---

## 4.4 — Basic IT concepts

### Infrastructure

- **Computing services** and **multitiered architecture** (database, processing, UI — user interface).
- **Networking** — LAN (local area network) and WAN (wide area network).
- **Storage** — hard drive; **NAS** (Network Attached Storage) / **SAN** (Storage Area Network); cloud storage; data warehouse.
- **Documentation** — e.g., policies.

### Cloud models

- **IaaS (Infrastructure as a Service)** — vendor handles the underlying hardware.
- **PaaS (Platform as a Service)** — a platform for building applications.
- **SaaS (Software as a Service)** — ready-to-use software for a fee (e.g., Salesforce, M365).
- **XaaS (Anything as a Service)** — anything you can subscribe to for a fee.

### Software you should recognize

- **ERP (Enterprise Resource Planning)** — integrates accounting, production, HR, procurement into one shared system.
- **CRM (Customer Relationship Management)** — tracks customers, sales, and support (e.g., Salesforce).
- **Databases** — **structured** (tables) vs. **unstructured** (video, audio, images).
- **EDRMS (Electronic Document and Records Management System)** — manages documents and access controls (e.g., SharePoint).
- **CMS (Content Management System)** — creates and manages websites.
- **Financial system** — manages financial data.

---

## 4.5 — Operational change control

Change control is part of risk management. It looks a little different across infrastructure, software, and cloud.

### IT infrastructure change control

- **Downtime / maintenance windows** — scheduled time for upgrades, patches, config.
- **Customer notification** — keep consumers informed; the change board can approve and notify.
- **Rollback plans** — how to revert a change.
- **Validation checks** — test the features.

### Software change control

When changing functionality or adding features:

1. **Requirements definition** — identify changes and expected outcomes.
2. **Risk assessment** — identify issues and resolutions.
3. **Make changes** — in a dev or test environment first.
4. **Validation testing** — automated (scripted) and manual.
5. **Change approval** — by the requestor.
6. **Customer notification** — date/time of the change window.
7. **Release** into production.

### Cloud vs. on-premises

**CI/CD (Continuous Integration / Continuous Deployment)** streamlines changes through automation — a key difference in how cloud environments handle change control versus traditional on-premises setups.
