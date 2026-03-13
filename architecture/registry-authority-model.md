# Registry Authority Model

This document defines the role of the registry authority within the GRC-P governance architecture.

## Role

The registry authority maintains the authoritative governance state used to determine operational readiness.

The registry authority:

- stores governance checks
- stores waivers
- stores revocations
- stores relationships and delegations
- computes readiness
- records governance evidence

The registry authority does **not** perform runtime execution.

## Architectural Position

```text
Registry Authority
        ↓
RGIS Protocol
        ↓
Gatekeeper Enforcement
        ↓
Execution Systems
