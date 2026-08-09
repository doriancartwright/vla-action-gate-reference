# VLA Action Gate Reference — Moved

This standalone repository is retained for compatibility with existing links.

The VLA Action Gate reference component is now part of the primary **TrustBoundary™** repository:

`TrustRobotics/TrustBoundary/reference/vla-action-gate/`

New reference-gate development should be made there.

## Why It Moved

The VLA action gate is a minimal reference implementation of TrustBoundary behavior rather than a separate TrustRobotics product.

```text
VLA / Planner
     |
     v
Candidate Action
     |
     v
TrustBoundary-compatible Reference Gate
     |
     v
Robot Execution Layer
```

This repository is no longer the canonical location for the reference implementation.

## Safety / Patent Notice

The reference gate is not safety-certified. Publication does not grant any patent license. Commercial implementations of protected TrustRobotics technologies may require a separate license.
