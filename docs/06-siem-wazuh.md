# Wazuh SIEM

## Status

🟡 In Progress

The Wazuh SIEM is deployed on `SIEM01` as an all-in-one installation.

## SIEM01 Configuration

| Parameter | Value |
|---|---|
| VM | `SIEM01` |
| Operating System | Ubuntu Server 24.04.5 LTS |
| Network | `SOC-GREEN` |
| IPv4 | `192.168.10.20` |
| Subnet | `192.168.10.0/24` |
| Gateway | `192.168.10.1` |
| DNS | `192.168.10.10` |
| CPU | 4 vCPU |
| RAM | 8 GB |
| Disk | 48 GB LVM |
| Wazuh Version | `4.14.8` |

## Deployment

Wazuh was deployed using the official all-in-one installation assistant:

```bash
sudo bash ./wazuh-install.sh -a

The following components were successfully deployed:

Wazuh Indexer
Wazuh Manager
Filebeat
Wazuh Dashboard
Validation

The following services were validated as running:

wazuh-indexer
wazuh-manager
filebeat
wazuh-dashboard

The Wazuh Indexer cluster was initialized successfully with one node.

The Wazuh Dashboard was initialized successfully and configured to use TCP port 443.

Evidence

The screenshot documents the active Wazuh Indexer, Wazuh Manager, Filebeat, and Wazuh Dashboard services on SIEM01.

Next Step

The next step is to deploy the Wazuh Agent on WIN01 and validate ingestion of Windows telemetry, including Sysmon and Windows Security events.