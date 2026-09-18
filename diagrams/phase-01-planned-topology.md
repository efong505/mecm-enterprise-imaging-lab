# Phase 01 Planned Topology

**Status:** Planned architecture baseline — not implementation evidence

```text
                 Isolated Lab Network
                        |
                +-------+-------+
                |               |
              DC01            CM01
           AD DS / DNS          |
                                +---- SQL01
                                |     placement pending
                                |
                                +---- DP01 / PXE
                                      placement pending
                                         |
                                    WINCLIENT01
```

## Notes

- All names are lab-only placeholders.
- SQL Server may be colocated with CM01 or separated after Phase 02 validation.
- The Distribution Point / PXE role may be colocated or separated after Phase 02 validation.
- CIDR, DHCP, gateway, Internet egress, operating-system versions, and virtualization platform remain unresolved.
- No system shown here is claimed as built until implementation evidence exists.
