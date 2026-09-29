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


## Phase 2 - Active Directory

### Checkpoint 02 - DC01 Active Directory Deployment

**Status:** Validated

**Date:** 2026-09-28

#### DC01 Network Configuration

| Parameter | Value |
|---|---|
| VM | DC01 |
| Network | SOC-GREEN |
| IPv4 | `192.168.10.10` |
| Subnet | `192.168.10.0/24` |
| Subnet Mask | `255.255.255.0` |
| Default Gateway | `192.168.10.1` |
| DNS Server | `127.0.0.1` / `::1` |
| DNS Suffix | `soclab.local` |

#### Active Directory Configuration

| Parameter | Value |
|---|---|
| Hostname | `DC01` |
| Domain | `soclab.local` |
| NetBIOS Domain | `SOCLAB` |
| Role | Active Directory Domain Services |
| Global Catalog | Enabled |
| DNS | Active Directory-integrated |

#### Validation

- Static IP configuration: PASS
- Gateway connectivity: PASS
- AD DS installation: PASS
- Domain deployment: PASS
- DNS configuration: PASS
- DNS diagnostic (`dcdiag /test:DNS`): PASS
- DC hostname configuration: PASS

#### Evidence

![DC01 static IP](screenshots/phase-02-active-directory/DC01/dc01-static-ip.png)

![DC01 network validation](screenshots/phase-02-active-directory/DC01/dc01-network-validation.png)

The screenshots document the static network configuration and network validation performed on DC01 during the Active Directory deployment.
