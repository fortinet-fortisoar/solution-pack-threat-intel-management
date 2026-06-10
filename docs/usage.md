| [Home](../README.md) |
|----------------------|

# Usage

Welcome to the **Threat Intel Management (TIM)** Solution Pack usage guide. To make navigation easier, this content has been split into focused guides. Each page covers a distinct part of TIM functionality.

## Overview

FortiSOAR's **Threat Intel Management** Solution Pack brings Security Orchestration and Automated Response (SOAR) and Threat Intel Management (TIM) together by introducing advanced TIM capabilities within the SOAR platform.

<!-- | [![](./res/threat-intelligence-youtube-thumbnail.png)](https://www.youtube.com/watch?v=vTvtHQxniVU) |
|:---------------------------------------------------------------------------------------------------:|
|          [FortiSOAR Threat Intel Management](https://www.youtube.com/watch?v=vTvtHQxniVU)           | -->

## Sections

- [Dashboard](./threat-intel-dashboard.md) &ndash; provides actionable insights into threat data ingestion efforts

- [Threat Intel Search](./threat-intel-search.md) &ndash; Query threat intelligence for domains, IPs, and other indicators of compromise, with CVE context, outbreak ties, confidence scoring, and hosting risk

- **Hub** &ndash; access threat reports, threat feeds, threat actor information, and workspaces:

  - [Threat Reports](./threat-reports.md) &ndash; ingest threat reports from FortiRecon and other threat report providers

  - [Threat Feeds](./threat-feeds.md) &ndash; configuring, ingesting, filtering, and managing feeds.

  - [Threat Actors](./threat-actor-intel.md) &ndash; an encyclopedia of threat actors providing actionable information

  - [CyberSecurity News](./cyber-news.md) &mdash; Stay updated on the latest cybersecurity news around the world

  - Threat Intelligence Workflow via [Workspaces](./threat-intel-workflow.md) &ndash; PIR requests, workspaces, lifecycle, and reporting

  - **Feed Configurations** &ndash; manage inbound and outbound feed settings:

    - Manage Inbound Feed settings

        - [Ingestion Parameters](./setup.md#ingestion-parameters)

        - [Ingestion Schedule](./setup.md#ingestion-schedule)

        - [Threat Feed Rules](./threat-feed-rules.md) &ndash; specify rules to automate feed ingestion

    - Manage Outbound Feed settings

        - [TAXII Server](./taxii.md) &ndash; using TIM as a TAXII server and disseminating datasets. Refer to this [example](./example.md) for directions on exporting indicators to FortiGate 

- [MITRE ATT&CK](./mitre-attck.md) &ndash; Map threat feeds and indicators to MITRE ATT&CK tactics and techniques

- [Hunts](./threat-hunt.md) &ndash; helps proactively search (*hunt*) for malicious activity in an environment

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
