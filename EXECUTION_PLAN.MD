# Post-Freeze Execution Plan

Status: Draft (Execution Branch Only)

This document defines how TruValue will be executed
without modifying, interpreting, or extending the frozen doctrine.

This document:
- Does NOT change doctrine
- Does NOT introduce semantics
- Does NOT define workflows
- ONLY constrains execution behavior

## 1. Execution Invariants

All execution work MUST comply with the following invariants.

Violating any invariant is considered a doctrine breach.

### 1.1 Doctrine Immutability
- Doctrine files MUST NOT be edited
- Doctrine meaning MUST NOT be extended, clarified, or rephrased
- No execution artifact may introduce new semantics

### 1.2 Refusal-First Design
- If execution requires interpretation, execution MUST refuse
- Ambiguity MUST result in non-action, not inference

### 1.3 Infrastructure-Only Posture
- TruValue execution MUST remain infrastructure-only
- No workflows, decisions, scoring, or enforcement logic may be introduced

### 1.4 Evidence Preservation
- Execution may only record declared responsibility
- Execution MUST NOT assert correctness, safety, or compliance

## 2. Allowed Execution Surfaces

Execution work is permitted ONLY in the surfaces below.
Anything outside these surfaces is out-of-scope and must be rejected.

### 2.1 Allowed surfaces (execution may change)
Execution MAY create or modify:
- Repository structure under `execution/`
- Non-doctrine operational documents (plans, checklists, runbooks)
- Build scaffolding that contains no semantics (project skeletons, empty modules)
- CI / automation that enforces invariants (format checks, branch protections, required templates)
- Issue templates, PR templates, and review checklists
- Test harness scaffolds (without decision logic or interpretation)

### 2.2 Forbidden surfaces (execution must never change)
Execution MUST NOT create or modify:
- `DOCTRINE.md`, `README.md` (doctrine status), `HOSTILE_INTEGRATION_TESTS.md`
- `INFRASTRUCTURE_CONTRACT.md`
- `SHARED_RESPONSIBILITY_MODEL.md`
- Any “explanations” that reinterpret doctrine meaning
- Any UX copy that implies correctness, verification, enforcement, or outcomes

### 2.3 Doctrine boundary rule
If a change would require a reader to “understand what TruValue means” differently,
it is a doctrine change and is forbidden.

### 2.4 Non-semantic enforcement rule
Execution MAY enforce doctrine by constraints only:
- “Must / must not” rules
- Blocking gates
- Required templates
- Refusal defaults

Execution MUST NOT enforce doctrine by interpretation, scoring, or judgment.

## 3. Execution Artifacts (Non-Doctrine)

Execution produces *artifacts* that help implement, operate, and audit the system **without adding semantics** and **without changing doctrine**.

All artifacts MUST:
- Be traceable to a doctrine clause or invariant
- Be implementation-facing (engineering / operations / legal posture)
- Never redefine meaning (no “interpretation layer”)
- Prefer checklists, constraints, refusal scripts, and evidence formats
- Be safe to delete without invalidating the frozen doctrine tag

### 3.1 Artifact Registry (Canonical)

All execution artifacts live under `/execution/` and are numbered.
Each artifact MUST include:
- Status (Draft / Active / Deprecated)
- Purpose (what it enables)
- Non-claims (what it explicitly does NOT do)
- Links to doctrine clauses / invariants it depends on

### 3.2 Required Artifacts (v1)

The following artifacts are REQUIRED for post-freeze execution:

1) `/execution/002-record-scope-cards/`
   - Record Scope Card templates (what a record is / isn’t)
   - Declaration Card templates
   - Export format examples (human-readable + machine)

2) `/execution/003-hostile-review-checklist/`
   - Hostile Review Checklist (merge-gating)
   - “Doctrine breach” triggers & examples
   - Refusal scripts for product/integrator pressure

3) `/execution/004-integration-guardrails/`
   - Integration invariants translated into “must/never” checks
   - Minimal required fields for declarations (record sufficiency)
   - UX non-coercion rules (no implied correctness)

4) `/execution/005-security-posture/`
   - Key custody model notes (externalized custody)
   - Export-first custody requirements
   - Subpoena/discovery posture constraints (non-custodial framing)

5) `/execution/006-release-and-versioning/`
   - Doctrine version bump rules (when v2 is allowed)
   - Tag naming rules (doctrine-vX.Y-frozen)
   - “No stealth changes” operational checklist

### 3.3 Governance of Artifacts

- Artifacts MAY evolve in the execution branch.
- Artifacts MUST NOT be merged into `main` if they change doctrine or add semantics.
- Artifacts can be promoted to main only if they are:
  (a) purely operational constraints, or
  (b) templates/checklists that do not redefine meaning.





