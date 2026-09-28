# Lab Checkpoints

## Phase 1 - Network Infrastructure

### Checkpoint 01 - WIN01 GREEN Network Connectivity

**Status:** Validated

**Date:** 2026-09-28

#### WIN01 Network Configuration

| Parameter | Value |
|---|---|
| VM | WIN01 |
| Network | SOC-GREEN |
| IPv4 | `192.168.10.100` |
| Subnet | `192.168.10.0/24` |
| Subnet Mask | `255.255.255.0` |
| Default Gateway | `192.168.10.1` |
| DNS Server | `192.168.10.1` |
| DNS Suffix | `home.arpa` |

#### Validation

- DHCP address assignment: PASS
- WIN01 -> pfSense connectivity: PASS
- DNS resolution through pfSense: PASS
- Internet connectivity: PASS

#### Evidence

![WIN01 network connectivity](screenshots/phase-01-network/WIN01/win01-network-connectivity.png)

The screenshot documents the network configuration assigned to WIN01 and the successful connectivity test to the pfSense gateway.