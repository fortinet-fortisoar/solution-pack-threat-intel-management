# Release Information

- **Version**:  4.0.0
- **Certified**: Yes
- **Publisher**: Fortinet
- **Compatible Version**: FortiSOAR v8.0.0 and later
- [Release Notes](./release_notes.md)

> [!IMPORTANT]
> 
> After an upgrade re-run the **Threat Intel Management** configuration wizard.
> 

## Overview

Threat Intelligence Management provides a centralized way to ingest, organize, and explore threat intelligence inside FortiSOAR.

It collects threat feeds from multiple sources and stores them in a searchable repository called feeds. Analysts can manage feeds, review indicators, investigate known threat actors, and explore adversary techniques mapped to the MITRE ATT&CK framework.

Threat Intelligence Management also provides workspaces that support threat hunting and investigation workflows. Intelligence can be shared with other systems and teams using standards such as TAXII.

## Getting Started with Threat Intel Management

- **Configure**: Configuring threat intel feeds, integrations, and feed processing rules is an essential first step. Refer to the section [Setup Threat Intel Management on FortiSOAR](./docs/setup.md#setup-threat-intel-management-on-fortisoar)

- **Ingest feed**: After configuring the Threat Intel Management wizard, the feed ingestion triggers automatically.

- **Manage Feeds**: You can manage incoming threat feeds by:

  - [Modifying ingestion parameters](./docs/setup.md#ingestion-parameters)

  - [Modifying ingestion schedule](./docs/setup.md#ingestion-schedule)

  - [Uploading unstructured feeds](./docs/threat-feeds.md)

> [!Note]
> 
> The [ingestion parameters](./docs/setup.md#ingestion-parameters) and [schedule](./docs/setup.md#ingestion-schedule) can only be modified via Threat Intel Management Configuration Wizard as these settings are unique to each feed connector.
> 

- **Setup Taxii Server**: The TAXII Server helps generate outgoing feed based on the datasets that you wish to share externally. Refer to the following sections to understand how.

  - [Setting up a TAXII Server](./docs/taxii.md#setting-up-a-taxii-server)

  - [Example: Export CSV Fields to FortiGate](./docs/example.md#export-csv-fields-to-fortigate)

## Features

- **Threat feed management and filtering**

  - [Configuring Feed Rules](./docs/setup.md#configuring-feed-rules)

  - [Working with Datasets](./docs/datasets.md)

- **Threat intelligence search**: Search and investigate indicators such as IP addresses, domains, file hashes, or URLs from a centralized intelligence database.

  - [Performing a Threat Intel Search](./docs/threat-intel-search.md#performing-a-search)

- **Threat actor intelligence**

  Track known threat actors along with associated indicators, campaigns, vulnerabilities, and attack techniques to support investigation and threat hunting.

  - [Using Threat Actor Data in TIM](./docs/threat-actor-intel.md#launching-threat-actor-intelligence)

- **MITRE ATT&CK Mapping**

  Map threats and indicators to MITRE ATT&CK tactics and techniques to understand attacker behavior and improve investigations.

  - [Using MITRE ATT&CK Data in TIM](./docs/mitre-attck.md#using-mitre-attck-data-in-tim)

- **Threat hunting workspace**

  - [Threat Hunt](./docs/threat-hunt.md)

  - [Threat Intelligence Workflow](./docs/threat-intel-workflow.md)

- **Intelligence sharing via TAXII**

  - [Setting up a TAXII Server](./docs/taxii.md#setting-up-a-taxii-server)

  - [Example: Export CSV Fields to FortiGate](./docs/example.md#export-csv-fields-to-fortigate)

- **Dashboards**: provides actionable insights into threat data ingestion efforts.

  - [Dashboard](./docs/threat-intel-dashboard.md)

- **Cybersecurity News**

  The Cybersecurity News tab surfaces FortiGuard Labs threat intelligence as filterable news cards, each flaggable by review status — New, Processing, Red Flag, or Read.

  - [Cybersecurity news from FortiGuard Labs](./docs/cyber-news.md)

- **FortiGuard Reports**

  The FortiGuard Reports tabs provides critical insights into emerging or ongoing cyber threats, helping organizations understand the risks they face and how to defend against them.

  - [FortiGuard Threat reports from FortiGuard Labs](./docs/threat-reports.md)

<!-- Check the following video demonstration of the Threat Intelligence Management solution:

| [![](./docs/res/threat-intelligence-youtube-thumbnail.png)](https://www.youtube.com/watch?v=vTvtHQxniVU) |
|:--------------------------------------------------------------------------------------------------------:|
|             [FortiSOAR Threat Intel Management](https://www.youtube.com/watch?v=vTvtHQxniVU)             | -->


# Next Steps

| [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) |
|----------------------------------------------|------------------------------------------------|--------------------------|--------------------------------|
