# orbit-broker

Orbit Broker allocates compute slots to batch jobs.

Maintained by Priya Nandakumar as part of the current delivery cycle.

## Scope

- Package layout follows the repository reference template.
- Runtime entry point: automation/run_checks.py
- Jobs are queued by priority and reclaimed when a slot times out.
