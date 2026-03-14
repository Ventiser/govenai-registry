# GovenAI Registry
Reference Registry Authority Implementation

![GovenAI Registry Version](https://img.shields.io/badge/GovenAI--Registry-v1.0--draft-blue)

GovenAI Registry is a reference **registry authority implementation** for the **GRC-P** governance architecture and the **RGIS** runtime protocol.

The registry maintains authoritative governance state used to determine whether operational actions are admissible before execution occurs.

The registry does **not execute operational actions**.  
Instead, it provides governance authority state that is evaluated by runtime gatekeepers.

---

# Role in the Stack


GRC-P → Governance architecture
RGIS → Runtime interoperability protocol
GovenAI Registry → Registry authority implementation
JobQue Gatekeeper → Gatekeeper enforcement implementation


- **GRC-P** defines the governance architecture.
- **RGIS** defines the runtime protocol between registry and gatekeeper.
- **GovenAI Registry** implements the registry authority role.
- **JobQue Gatekeeper** enforces runtime decisions before execution.

---

# Registry Responsibilities

A registry authority implementation maintains governance state used to determine operational readiness.

The registry manages:

- governance targets
- compliance checks
- waivers
- revocations
- delegation relationships
- readiness state
- governance evidence

Using this information, the registry evaluates whether a governed subject is **structurally ready for operation**.

---

# Relationship to GRC-P and RGIS

GovenAI Registry implements the **registry authority role defined by GRC-P**.

Gatekeepers consult the registry through the **RGIS runtime protocol** to evaluate governance readiness.

Repositories:

GRC-P — Governance architecture  
https://github.com/Ventiser/grc-p

RGIS — Registry–Gatekeeper protocol  
https://github.com/Ventiser/rgis

---

# Governance Evaluation Flow

A typical governance evaluation process follows this sequence:


Operational Request
↓
Gatekeeper Intercepts Request
↓
Canonical Request Validation
↓
Registry Governance Query
↓
Governance State Evaluation
↓
Permit / Deny Decision
↓
Evidence Event Recorded


The registry provides authoritative governance state used to determine readiness.

The gatekeeper enforces the resulting decision.

---

# Repository Structure


architecture/ registry authority model
data-model/ governance state structures
readiness/ readiness evaluation logic
evidence/ governance evidence ledger
api/ RGIS-facing authority endpoints
conformance/ registry implementation notes


---

# Status

Draft publication of **GovenAI Registry v1.0** reference implementation model.

---

# Related Repositories

GRC-P — Governance architecture  
https://github.com/Ventiser/grc-p

RGIS — Registry–Gatekeeper protocol  
https://github.com/Ventiser/rgis

GovenAI Registry — reference registry authority implementation  
https://github.com/Ventiser/govenai-registry

JobQue Gatekeeper — reference runtime enforcement implementation  
https://github.com/Ventiser/jobque-gatekeeper

---

# Intellectual Property

Certain concepts described in this repository may be covered by pending patent applications owned by Ventiser Pty Limited.

See `PATENT-NOTICE.md` for additional details.

---

# Stewardship

Maintained by **Ventiser**.
