# VLA Action Gate Reference

Minimal **TrustBoundary-compatible reference implementation** for evaluating VLA-generated robot action proposals before physical execution.

## What This Is

This repository demonstrates a small policy gate that consumes a proposed robot action plus robot/environment context and returns one of three decisions:

- `ALLOW`
- `DENY`
- `MODIFY`

It is intended to illustrate the interface between AI-generated action proposals and a downstream execution-governance layer.

## Example Evaluation Inputs

The reference gate can deny or modify commands based on example conditions such as:

- human proximity;
- emergency-stop state;
- workspace bounds;
- velocity limits;
- force limits;
- torque limits;
- battery sufficiency;
- role authorization;
- denied action types.

## Relationship to TrustBoundary

```text
VLA / Planner
     |
     v
Candidate Action
     |
     v
Reference Gate
ALLOW / DENY / MODIFY
     |
     v
Robot Execution Layer
```

The reference gate demonstrates only a small subset of the broader **TrustBoundary™** execution-governance architecture.

TrustBoundary may additionally include predictive validation, validator selection, policy orchestration, execution envelopes, audit logging, release authorization, and actuator-level enforcement interfaces.

## Scope Boundary

This repository is **not** a production actuator-enforcement system and does not provide:

- motor-driver enforcement;
- cryptographic actuator release tokens;
- complete ownership or custody governance;
- premises/network governance;
- infrastructure or resource authorization;
- safety certification;
- a production multi-gate actuation arbiter.

## Intended Use

This project is intended for:

- research;
- prototyping;
- interoperability testing;
- developer education.

It is not safety-certified and should not be used as the sole control boundary for a real robot, vehicle, industrial system, medical system, or other human-facing autonomous system.

## Related Repositories

- `TrustRobotics/TrustBoundary` — primary execution-governance architecture.
- `TrustRobotics/vla-action-command-spec` — proposed action-command schemas.
- `TrustRobotics/TrustRobotics-rfcs` — public RFC series.
- `TrustRobotics/TrustRobotics-architecture` — umbrella architecture.

## Status / Implementation State

**Reference prototype.** This is illustrative code, not a complete production TrustBoundary implementation.

## Licensing / Patent Notice

Publication of this reference implementation does not grant any patent license. Commercial implementations of protected TrustRobotics technologies may require a separate TrustRobotics license.

## Quick Start

```bash
python examples/demo_gate.py
```
