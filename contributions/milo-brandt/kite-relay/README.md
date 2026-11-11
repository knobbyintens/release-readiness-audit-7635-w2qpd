# kite-relay

Kite Relay forwards events between the message bus and edge collectors.

Maintained by Milo Brandt as part of the current delivery cycle.

## Scope

- Package layout follows the repository reference template.
- Runtime entry point: automation/run_checks.py
- Relay buffers are bounded and flushed on a fixed cadence.
