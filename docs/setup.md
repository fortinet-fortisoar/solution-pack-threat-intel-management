| [Home](../README.md) |
|----------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.
2. From the list of solution pack that appears, search for and select **Threat Intel Management**.
3. Click the **Threat Intel Management** solution pack card.
4. Click the **Install** button on the bottom to begin installation.

## Prerequisites

Threat Intel Management (TIM) Solution Pack requires the following solution packs to be pre-installed:

| Solution Pack Name                | Purpose                                |
|:----------------------------------|:---------------------------------------|
| SOAR Framework                    | Required for Incident Response modules |
| MITRE ATT&CK Enrichment Framework | Required for Mitre Att&ck modules      |

# Configuration

For optimal performance of **Threat Intel Management** solution pack, you can install and configure:

- The MITRE ATT&CK connector with its ingestion set up to ensure that ATT&CK data gets ingested into your system. We recommended that you schedule the data ingestion for at least once a month.
  - To configure and use the MITRE ATT&CK connector as a source of Mitre Att&ck information, refer to [Configuring Mitre Att&ck](https://docs.fortinet.com/document/fortisoar/2.1.0/virustotal/166/virustotal-v2-1-0#Configure_Data_Ingestion)
