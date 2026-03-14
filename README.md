# GovenAI Registry
Reference Registry Authority Implementation

![GovenAI Registry Version](https://img.shields.io/badge/GovenAI--Registry-v1.0--draft-blue)

GovenAI Registry is the reference **registry authority implementation** for the **GRC-P** governance architecture and the **RGIS** runtime protocol.

It maintains authoritative governance state used to determine whether operational actions are admissible before execution occurs.

The registry does not execute actions.  
It maintains governance authority state for evaluation by runtime gatekeepers.

---

## Architecture Diagram

```text
            Request Originator
(AI Agent / Application / Human Event / System Trigger)
                     │
                     ▼
                   GRC-P
    Governance Runtime Control Protocol
            (Architecture Standard)
                     │
                     ▼
                   RGIS
   Registry–Gatekeeper Interface Protocol
                     │
        ┌────────────┴────────────┐
        │                         │
        ▼                         ▼
  GovenAI Registry         JobQue Gatekeeper
Authority Implementation   Enforcement Implementation
        │                         │
        └────────────┬────────────┘
                     ▼
       Governance Enforcement Boundary
                     │
                     ▼
           Operational Execution
             (APIs / Systems)
```

The architecture is **domain-agnostic** and establishes a **governance enforcement boundary** in front of operational APIs and systems.

Any execution surface placed behind this boundary becomes a **governed execution environment**.

---

## Role in the Stack

```text
GRC-P             → Governance architecture
RGIS              → Runtime interoperability protocol
GovenAI Registry  → Registry authority implementation
JobQue Gatekeeper → Gatekeeper enforcement implementation
```

- **GRC-P** defines the governance architecture.
- **RGIS** defines the runtime protocol between registry and gatekeeper.
- **GovenAI Registry** is a registry authority implementation.
- **JobQue Gatekeeper** is a runtime gatekeeper implementation.

---

## Responsibilities

The registry authority maintains:

- governance targets
- compliance checks
- waivers
- revocations
- delegation relationships
- readiness state
- governance evidence

The registry evaluates whether a governed subject is **structurally ready for operation**.

---

## Relationship to GRC-P and RGIS

GovenAI Registry implements the **governance authority role defined by GRC-P**.

It exposes authority state used by gatekeepers operating under **RGIS**.

Repositories:

- GRC-P: https://github.com/Ventiser/grc-p
- RGIS: https://github.com/Ventiser/rgis

---

## Repository Structure

```text
architecture/  registry authority model
data-model/    governance state structures
readiness/     readiness evaluation logic
evidence/      governance evidence ledger
api/           RGIS-facing authority endpoints
conformance/   registry implementation notes
```

---

## Status

Draft publication of the **GovenAI Registry v1.0** reference implementation model.

---

## Related Repositories

GRC-P — Governance architecture  
https://github.com/Ventiser/grc-p

RGIS — Registry–Gatekeeper protocol  
https://github.com/Ventiser/rgis

GovenAI Registry — reference registry authority implementation  
https://github.com/Ventiser/govenai-registry

JobQue Gatekeeper — reference runtime enforcement implementation  
https://github.com/Ventiser/jobque-gatekeeper

---

## Stewardship

Maintained by **Ventiser**.
