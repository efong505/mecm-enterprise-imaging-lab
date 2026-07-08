# PXE Troubleshooting

## Purpose

This runbook provides a starter structure for documenting PXE troubleshooting in the MECM Enterprise Imaging Lab.

PXE issues can involve network design, distribution point readiness, boot images, boundaries, DHCP behavior, or client-side boot settings. This file is for organizing observations during lab testing.

## Troubleshooting Flow

When a PXE issue appears, record:

1. What the client displayed.
2. Which VM or test system was affected.
3. Whether the issue happened before or after contacting the network.
4. Which server roles were expected to respond.
5. Which logs were reviewed.
6. What changed since the last successful test.

## Common Areas to Check Later

- Distribution point readiness
- PXE enablement status
- Boot image distribution
- Boundary and boundary group assumptions
- DHCP or network path assumptions
- VM firmware mode assumptions
- Client collection and deployment targeting

## Evidence to Capture

- Screenshot of the client error or boot screen, if available
- Relevant log notes
- Time of test
- Test client name
- Recent changes
- Final outcome

## Boundaries

Do not add fake error screenshots or invented fixes. Record only what was actually observed.
