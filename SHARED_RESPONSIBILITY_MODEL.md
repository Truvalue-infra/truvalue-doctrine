# TruValue Shared Responsibility Model (Binding)

This document defines the explicit allocation of responsibility and liability
between TruValue, its users, and its integrators.

This model is derived directly from the TruValue Doctrine and Infrastructure Contract.
It introduces no new authority, interpretation, or enforcement.

---

## 1. Core Principle

TruValue records responsibility.
It does not assume responsibility.

Responsibility is never transferred to TruValue by usage, integration, payment,
or reliance.

---

## 2. Responsibility Allocation (Authoritative)

### TruValue is responsible for:

- Infrastructure integrity
- Append-only immutability of records
- Accurate timestamping of declarations
- Availability on a best-effort, non-reliant basis
- Exportability and independent third-party verifiability
- Preservation of declared truth (what was recorded)

TruValue is **not responsible** for:
- correctness of declarations
- legality or regulatory compliance
- intent, interpretation, or meaning
- outcomes, decisions, or actions
- downstream use or misuse of records
- enforcement or prevention of harm

---

### Users (Individuals, Institutions, Organizations) are responsible for:

- Accuracy and truthfulness of declarations
- Legal validity and compliance of actions
- Intent, understanding, and consent
- Decisions, outcomes, and consequences
- Reliance on records for operational or legal purposes
- Misuse or misrepresentation of TruValue records

---

### Integrators (Platforms, Vendors, Implementers) are responsible for:

- Workflow design and UX framing
- Ensuring explicit human declarations
- Preventing silent, batch, or implied declarations
- Avoiding coercion, dark patterns, or default acceptance
- Downstream system behavior and consequences
- Any interpretation layered on top of TruValue records

---

## 3. Explicit Non-Absorption of Liability

TruValue never absorbs downstream liability.

No contract, integration, marketing claim, or technical dependency
may shift responsibility to TruValue.

Any attempt to do so is invalid by doctrine.

---

## 4. Refusal Scripts (Mandatory)

TruValue must explicitly refuse requests to:

- verify or validate correctness
- judge or certify compliance
- guarantee safety or risk reduction
- interpret meaning or intent
- recommend actions
- automate acceptance or consent
- infer responsibility from behavior
- act as system of record for outcomes

Refusal is not a failure mode.
Refusal is a core feature.

---

## 5. Dispute Posture

In the event of dispute:

- TruValue provides records as evidence only
- TruValue does not testify to meaning or correctness
- TruValue does not resolve disputes
- TruValue does not adjudicate responsibility

Records stand on their own.
Judgment remains external.

---

## 6. Legal and Court Alignment

This model is designed for adversarial scrutiny.

If a responsibility boundary cannot be defended in a hostile courtroom,
it must not exist.

---

## 7. Precedence

In case of conflict:

DOCTRINE.md overrides this document.
INFRASTRUCTURE_CONTRACT.md binds usage.
This document clarifies liability boundaries only.

---

Doctrine survival > convenience 
Infrastructure > product 
Evidence > intelligence
