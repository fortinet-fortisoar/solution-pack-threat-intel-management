| [Home](../README.md) |
|----------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.
2. From the list of solution pack that appears, search for and select **Threat Intel Management**.
3. Click the **Threat Intel Management** solution pack card.
4. Click the **Install** button on the bottom to begin installation.

## Prerequisites

Threat Intel Management (TIM) Solution Pack requires the following solution packs to be pre-installed:

| Solution Pack Name                | Version          | Purpose                                                  |
|:----------------------------------|:-----------------|:---------------------------------------------------------|
| SOAR Framework                    | v2.1.1 and later | Required for Incident Response modules                   |
| MITRE ATT&CK Enrichment Framework | v2.2.0 and later | Required for Mitre Att&ck modules                        |
| SOC Simulator                     | v1.0.2 and later | Required for scenario module and SOC Simulator Connector |

# Configuration

For optimal performance of **Threat Intel Management** solution pack, you can install and configure:

- The MITRE ATT&CK connector with its ingestion set up to ensure ingestion of ATT&CK data in your threat mitigation environment. We recommend that you schedule the data ingestion for at least once a month.
  - To configure and use the MITRE ATT&CK connector as a source of Mitre Att&ck information, refer to [Configuring Mitre Att&ck](https://docs.fortinet.com/fortisoar/connectors/mitreattack)

- The FortiRecon ACI connector with its ingestion set up to ensure ingestion of FortiRecon ACI data in threat mitigation environment.
  - To configure and use the FortiRecon ACI connector as a source of Adversary Centric Intelligence(ACI) information, refer to [Configuring FortiRecon ACI](https://docs.fortinet.com/fortisoar/connectors/fortirecon-aci)

| [Usage](./usage.md) | [Contents](./contents.md) |
|---------------------|---------------------------|