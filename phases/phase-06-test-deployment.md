# Phase 06 — Test Deployment

## Status

**Planned — Not Yet Executed**

## Objective

Execute a controlled test deployment against the designated lab client and capture actual deployment, log, and troubleshooting evidence.

## Prerequisites

- Phase 05 complete
- test client identified
- target collection verified
- task sequence reviewed
- PXE / DP / content path validated
- troubleshooting and screenshot templates prepared

## Test Procedure Record

When executed, record:

- test date and client;
- firmware / boot mode;
- deployment selected;
- observed PXE behavior;
- task-sequence start / progression;
- failure point if applicable;
- logs reviewed;
- changes made during troubleshooting;
- final result.

## Validation Criteria

Phase 06 is complete only when:

- a real test deployment has been attempted;
- actual observations are recorded;
- logs or console status are reviewed;
- any failure is documented with evidence;
- success, failure, or blocked status is explicitly recorded.

A failed deployment may still produce valid troubleshooting evidence, but the phase should not be marked successful until acceptance criteria are met.

## Evidence Required

- sanitized screenshots;
- task-sequence / client status evidence;
- relevant log notes;
- troubleshooting entries;
- final validation result;
- checkpoint decision.

## Troubleshooting References

- `runbooks/pxe-troubleshooting.md`
- `runbooks/client-health-checks.md`
- `runbooks/content-distribution-checks.md`
- `runbooks/log-reference.md`

## Boundaries

Expected results and actual results must remain separate. Do not fabricate success, root cause, or remediation.
