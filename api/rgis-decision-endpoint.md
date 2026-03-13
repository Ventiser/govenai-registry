# RGIS Decision Endpoint

The GovenAI Registry provides governance authority state to gatekeepers through the RGIS protocol.

The minimal decision interface is:

```text
POST /rgis/v1/decision

Gatekeepers submit a canonical request and receive a deterministic decision response derived from authoritative governance state.

The registry authority is responsible for:

validating protocol structure

resolving governance state

evaluating readiness

returning a protocol-compliant response

Runtime protocol details are defined in the separate RGIS repository.
