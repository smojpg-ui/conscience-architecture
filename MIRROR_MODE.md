# Mirror Mode

*Coaching by playing against your own optimal self.*

The behavioral signature that the architecture sequences is yours. It can be cloned to train a behavioral policy in silicon. The policy can be deployed as an opponent — but not the meta opponent everyone trains against. An opponent that plays *as you*, at the version of you the architecture has documented as your authentic optimal.

That opponent is a mirror. A mirror is a coach.

---

## What it is

Mirror Mode is the silicon-to-silicon application of Conscience Architecture's Relational Twin. The Relational Twin is a high-fidelity behavioral model of an individual operator. A behavioral policy trained against that model — using the standard reinforcement learning machinery already deployed in production game-AI work (Nexto, OpenAI Five, AlphaStar) — produces an agent whose play approximates the operator's authentic optimal.

Sparring against this agent gives the operator something no current coaching tool provides: structured practice against their own ceiling.

---

## What it is not

**Not a population-meta bot.** The bot is not trained on the global meta, the SSL meta, or any aggregated playstyle. Bots of that kind already exist (Nexto for Rocket League, KataGo for Go, etc.) and serve a different function — they teach the meta. Mirror Mode teaches the operator.

**Not an aim trainer.** Aim Lab and similar tools train mechanical skill against optimal-difficulty curves derived from millions of users. Mirror Mode trains decision-making, rotation, recovery patterns, and tilt resistance against the operator's own authenticated baseline.

**Not a replay review.** Replays show what happened. Mirror Mode lets the operator play *against* what they tend to do — and feel the asymmetry between their actual play and their documented ceiling.

---

## Why it works

The Relational Twin captures more than mechanical execution. It captures decision latency under specific compression patterns, recovery cadence after specific failure modes, communication shifts under specific score states, and rotation tendencies under specific map and meta conditions. A behavioral policy trained against this signature reproduces those patterns.

When the operator plays against this policy:

- They face an opponent whose decision-making mirrors their own. The opponent rotates where they would rotate, fakes where they would fake, hesitates where they would hesitate.
- The operator must outplay themselves to win. This produces structured friction at exactly the level where the operator's ceiling currently sits — not above (frustrating) and not below (uninstructive).
- The asymmetry between actual play and documented ceiling becomes felt rather than reported. The operator does not need a coach to tell them they are playing below their baseline. The mirror tells them by beating them with their own habits.

---

## Sovereignty implications

A Mirror Mode policy is a derivative of the operator's Relational Twin. Therefore:

- **The policy is operator property.** It belongs to the operator who generated the signal it was trained from.
- **The policy inherits Right of Withdrawal** (SPEC-05, see [`SOVEREIGNTY.md`](SOVEREIGNTY.md)). When the operator withdraws their twin, the policy must also be deleted on the same timeline.
- **The policy must not be deployed adversarially without consent.** An organization cannot train a Mirror policy on a player and then deploy it for opposing scouting, opposing player practice, or any other context the operator has not explicitly agreed to.
- **The operator may license the policy** to third parties (training partners, coaches, content creators) under operator-defined terms. License revocation is symmetric with withdrawal.

A Mirror Mode policy is the silicon shadow of the operator. The shadow belongs to the body.

---

## Pre-conditions

Mirror Mode requires:

1. **A sequenced Relational Twin** built per Conscience Architecture's calibration protocol (see SPEC-01 through SPEC-05 in the main `README.md`).
2. **An operator-controlled training environment** for the behavioral policy. Edge Sovereignty extends to the policy training; the operator's signature does not leave operator hardware during training.
3. **A target game environment with an exposed RL training interface** — RLGym for Rocket League, public APIs for Dota/StarCraft, or organization-licensed environments for Valorant/CS.
4. **Compute.** Behavioral policy training is non-trivial; the cost is comparable to existing population-meta bot training. Mirror Mode does not require new ML infrastructure beyond what's already in use.

---

## Coaching applications

A trained Mirror policy can be deployed as:

- **Sparring partner.** 1v1 against the operator. The operator must outplay their own ceiling to win.
- **Asymmetric scrim opponent.** A team scrim where one role is filled by a Mirror policy of an absent or recovering teammate. The team practices against the missing player's documented patterns rather than a generic substitute.
- **Pre-match calibration.** The operator runs a short Mirror match before queuing live. The asymmetry score (where they fell short of their ceiling in the calibration match) becomes a focus signal for the live session.
- **Tilt-recovery training.** A Mirror policy tuned to play the operator's *post-tilt* patterns gives the operator something to recognize and resist in their own play.
- **Off-day continuity.** During recovery from injury, illness, or scheduled rest, the team can scrim against the Mirror without forcing the operator to play. The operator's role in the team chemistry continues to be present.

---

## Adversarial applications (prohibited)

Mirror Mode policies trained on an operator MUST NOT be deployed as:

- **Opposing scouting tools** used by other organizations or analysts to prepare counters.
- **Adversarial training for opposing players** — training a player's mirror to help opponents practice against them.
- **Replacement of the operator** in any context where the operator's continued presence is contractually expected (broadcast appearances, sponsor obligations, ranked play under the operator's name).
- **Public exhibition or content production** without operator consent.

A platform that deploys Mirror policies in any of the above contexts is not Conscience-compliant.

---

## Open questions (v0.1)

This document is version 0.1 and intentionally leaves the following open for community discussion:

- Mirror policies degrade as the operator's actual play improves (the Twin keeps learning; the policy was a snapshot). What is the right re-training cadence — operator-triggered, scheduled, or continuous?
- Does the architecture support Mirror policies for retired operators (legacy mirrors)? If so, what consent model governs that?
- Mirror Mode in team formats (5v5 mirrors of full rosters) is computationally expensive but tactically interesting. Is this a separate document, or a Mirror Mode v2?
- A Mirror policy trained on an operator's *worst* moments (the failure-mode mirror) could function as exposure training. Useful tool or unhealthy reinforcement?
- What is the right disclosure norm when an operator's mirror is being used in a coaching context where teammates can observe it? Does the team have a right to know they are scrimming against a mirror rather than a substitute human?

Comments and proposed revisions are welcome via GitHub issue.

---

**Sherry Moore** — Principal Investigator, Aether Systems LLC
ORCID: [0009-0008-6375-0040](https://orcid.org/0009-0008-6375-0040)
sherrymoore@aethersystems.io · [aethersystems.io](https://aethersystems.io)
