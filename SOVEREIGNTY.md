# Sovereignty

*How Right of Withdrawal (SPEC-05) is operationalized.*

This document specifies what the operator is entitled to under Conscience Architecture's Right of Withdrawal, what the architecture must enforce, and what verifications are available when an operator invokes withdrawal.

---

## Scope

Right of Withdrawal (SPEC-05) is the operator's architecturally enforced right to retire their Relational Twin and trigger documented deletion of all derived behavioral data across all access tiers.

Withdrawal is not a feature of a Conscience-compliant deployment. It is a property of the architecture. Any system claiming Conscience compliance must support withdrawal at any time, for any reason, with no degradation of core functionality before the moment of withdrawal.

---

## Who can invoke withdrawal

Withdrawal can be invoked by:

- **The operator**, at any time, through any operator-controlled access surface.
- **The operator's designated representative** (legal counsel, agent, union representative), with documented operator authentication.
- **The operator's estate**, in the event of operator decease, per documented succession.

Withdrawal cannot be invoked by:

- Any holder of a higher access tier — coach, performance staff, organization, league, sponsor, broadcaster.
- The platform operator.
- Any party other than those listed above.

---

## What withdrawal triggers

**Within 24 hours** of operator-confirmed withdrawal:

- The Relational Twin model on operator-controlled hardware is irreversibly deleted.
- All local behavioral data and logs (raw or summarized) are irreversibly deleted.
- All cached model weights, gradient updates, or training intermediates on operator-controlled hardware are irreversibly deleted.

**Within 7 days** of operator-confirmed withdrawal:

- All off-device summaries held at higher access tiers (per SPEC-02) are irreversibly deleted.
- All clinical summaries delivered to coaches and performance staff are irreversibly deleted.
- All operational readiness indicators delivered to organizational leadership are irreversibly deleted.
- All aggregate views containing the operator's contributing signal are recomputed without the operator's data; the operator's portion is irreversibly deleted.

**Within 30 days** of operator-confirmed withdrawal:

- All backup, archive, or cold-storage copies of any of the above are irreversibly deleted, regardless of medium.
- A signed completion record is delivered to the operator, attesting to the deletions above.

---

## What withdrawal does not trigger

Withdrawal does not retroactively invalidate decisions made on the basis of summaries or readiness indicators delivered before withdrawal. The architecture does not unwind history; it stops the future.

Withdrawal does not delete:

- **Game telemetry** that exists independent of Conscience-Architecture deployment (match logs, leaderboard entries, broadcast footage). Governed by the underlying platform's own data policy.
- **Public statements, broadcasts, or third-party recordings** of the operator made independent of the system.
- **Anonymized aggregate research outputs** in which the operator's individual signal cannot be reconstructed (per SPEC-02 lossy abstraction guarantees).

Operators should be informed of these exclusions before consenting to deployment, not at the moment of withdrawal.

---

## Transition events

Withdrawal SHOULD be offered to the operator at the following transition events, even when not requested:

- **Org transition** — player traded, signed, released, retired.
- **Coaching staff change** — the relationship the summaries were delivered into has changed.
- **Major contract renegotiation** — the consent terms under which sequencing began may have shifted.
- **Annual sovereignty review** — operator-initiated check that all entitled deletions are current.

Offering withdrawal does not invoke it. The operator may decline. The offer must be a discrete decision surface, not buried in a settings menu.

---

## Verification

The operator is entitled to:

- A **signed completion record** from the platform operator within 30 days of withdrawal, attesting to the deletions above.
- An **audit interface**, available at any time without invoking withdrawal, listing what data the architecture currently holds about the operator at every access tier.
- A **pre-withdrawal preview**, showing exactly what will be deleted if withdrawal is invoked.

The audit interface and preview must be available before, during, and after the consent decision. Operators cannot meaningfully consent to a system whose contents they cannot inspect.

---

## Architectural vs contractual enforcement

Withdrawal is enforced architecturally where possible (deletions are mechanical, not promised) and contractually where architecture does not reach.

- **On operator-controlled hardware:** enforced architecturally. Local deletion is a verifiable system call that the operator can audit directly.
- **On platform-controlled infrastructure:** enforced contractually with operator-side audit rights. The platform operator agrees in writing to a signed deletion process and submits to operator-side verification.

Conscience-compliant platforms must publish a **deletion runbook** describing the architectural and contractual chain that makes withdrawal real. The runbook is part of the platform's public Conscience compliance attestation.

---

## Conflicts of interest

Where withdrawal conflicts with a contract obligation (e.g., a player's contract obligates them to share certain data with the org), **the conflict resolves in favor of the operator's right of withdrawal.**

Contracts that obligate sustained Conscience-Architecture twin sharing — that is, contracts that prospectively forbid withdrawal — are not Conscience-compliant. Platforms cannot certify under this framework while issuing such contracts.

---

## Open questions (v0.1)

This document is version 0.1 and intentionally leaves the following open for community discussion:

- The 7-day off-device summary deletion window may be too long for some adversarial scenarios. Should it be tunable per platform with operator-side ratification?
- Aggregate research outputs are excluded from withdrawal. Is "individual signal cannot be reconstructed" a sufficient guarantee, or should aggregates also be deleted on withdrawal as a precaution?
- Estate / posthumous withdrawal is included as an explicit trigger. What is the right default for an operator who simply stops engaging without invoking withdrawal — time-based auto-withdrawal, indefinite hold, or platform-defined per consent?
- The audit interface is required but unspecified in form. Should there be a reference implementation?

Comments and proposed revisions are welcome via GitHub issue.

---

**Sherry Moore** — Principal Investigator, Aether Systems LLC
ORCID: [0009-0008-6375-0040](https://orcid.org/0009-0008-6375-0040)
sherrymoore@aethersystems.io · [aethersystems.io](https://aethersystems.io)
