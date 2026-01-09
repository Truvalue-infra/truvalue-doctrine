# TruValue Reference Architecture (Doctrine-Derived)

Status: DRAFT (Non-Executable)
Derived from: DOCTRINE.md v1.0

Purpose:
This document defines the structural boundaries of the TruValue system.
It specifies what the system MAY contain, what it MUST contain, and what it MUST NEVER contain.

This is not a product specification.
This is not a workflow definition.
This is not an optimization document.

It exists to prevent architectural drift

## 1) Allowed Components (MAY EXIST)

These components are permitted only if they do not introduce interpretation, enforcement, workflow coupling, or implied correctness.

### A. Core Record Service (Declarations)
- Accepts explicit human declarations: accept / refuse / transfer
- Captures declared context (minimal, enumerated, non-semantic)
- Produces immutable append-only records
- Supports export of records in a portable format

### B. Identity & Access (Access-Context Only)
- AuthN/AuthZ for “who is acting in what declared role”
- Identity is used only to bind a declaration to an actor/context
- No “trust scoring” or behavioral profiling

### C. Evidence Storage (Minimal, Non-Custodial Posture)
- Stores declaration records and necessary metadata
- May store supporting artifacts ONLY as optional attachments with explicit disclaimers
- Must support export-first custody and offline verification

### D. Cryptographic Integrity Layer
- Hashing, timestamping, signature verification (where applicable)
- Cryptographic agility support (ability to rotate/upgrade schemes)
- Must not become “proof of correctness” — only proof of record integrity

### E. Export & Verification Tooling
- Export bundles designed for third-party / offline verification
- Independent verifier tool may be open-source and runnable air-gapped
- Verification proves: integrity, provenance, immutability — not correctness

### F. Audit Viewing (Record Cards)
- UI that displays declarations exactly as recorded
- Record Scope Cards / Declaration Cards that state:
  - what is captured
  - what is not asserted
  - what TruValue refuses to infer

---

## 2) Forbidden Components (MUST NEVER EXIST)

These components are doctrine breaches even if “customers want them” or “it improves adoption”.

### A. Interpretation / Semantics Engine
- Any NLP/AI that infers meaning, intent, blame, responsibility validity, or “what happened”
- Any mapping from text/context to implied acceptance/refusal/transfer

### B. Enforcement / Policy Engine
- Any automated gating, blocking, compliance enforcement, or policy execution
- Any “required actions” derived from records
- Any integration that turns records into commands

### C. Workflow Orchestration / Process SaaS
- Task assignment, reminders, escalation flows, approvals, or decision routing
- “Next steps” engines, nudges, or automation based on recorded declarations
- Anything that makes TruValue feel like a workflow system

### D. Analytics / Insights / Scoring
- Dashboards that summarize behavior, trends, anomalies, or performance
- Risk scoring, compliance scoring, trust scoring, fraud scoring
- Recommendations, flags, or alerts implying conclusions

### E. Silent Notarization / Auto-Acceptance
- Background mapping of one signature/action to many declarations
- “Acknowledgement” without explicit human action
- Batch acceptance or inferred consent

### F. Claims Layer
- Marketing or product claims that TruValue provides:
  - safety, compliance, risk reduction, fraud prevention, insurance approval
- Any UI language implying correctness or verification

---

## 3) Boundary Rules (How to Detect Drift)

If a feature proposal requires any of the following, it is automatically rejected:
- “We need to infer meaning from context”
- “We need to reduce friction by auto-populating acceptance”
- “We need a dashboard to show trends or compliance posture”
- “We need the system to trigger actions based on records”
- “We need to score or flag risky behavior”
- “We should integrate deeply into workflows to drive adoption”

Default response: explicit refusal. No remediation path.

Doctrine survival > growth
