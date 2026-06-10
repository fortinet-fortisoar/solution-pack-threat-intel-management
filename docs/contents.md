| [Home](../README.md) |
|----------------------|

# Contents

This section lists the various contents of the **Threat Intel Management** Solution Pack. 

## Module Schemas

### Tasks

Following is the module schema of the **Tasks** module

| Field              | Field Type   |
|--------------------|--------------|
| `actualMinutes`    | `integer`    |
| `alerts`           | `manyToMany` |
| `approvalhost`     | `text`       |
| `assets`           | `manyToMany` |
| `assignedOnDate`   | `datetime`   |
| `assignedToPerson` | `lookup`     |
| `attachments`      | `manyToMany` |
| `comments`         | `manyToMany` |
| `companies`        | `manyToMany` |
| `completedOnDate`  | `datetime`   |
| `description`      | `richtext`   |
| `dueBy`            | `datetime`   |
| `hunt`             | `manyToMany` |
| `incidents`        | `manyToMany` |
| `indicators`       | `manyToMany` |
| `name`             | `text`       |
| `persons`          | `manyToMany` |
| `priority`         | `picklist`   |
| `startDate`        | `datetime`   |
| `status`           | `picklist`   |
| `stepid`           | `integer`    |
| `submittedBy`      | `lookup`     |
| `taskdata`         | `richtext`   |
| `tasktype`         | `text`       |
| `threatIntelFeeds` | `manyToMany` |
| `type`             | `picklist`   |
| `uuid`             | `null`       |
| `warrooms`         | `manyToMany` |
| `workflowid`       | `text`       |
| `workspaces`       | `manyToMany` |


### Workspaces

Following is the module schema of the **Workspaces** module

| Field                | Field Type   |
|----------------------|--------------|
| `actorGroupAnalysis` | `html`       |
| `actorGroups`        | `manyToMany` |
| `comments`           | `manyToMany` |
| `description`        | `html`       |
| `files`              | `manyToMany` |
| `impactAnalysis`     | `richtext`   |
| `indicators`         | `manyToMany` |
| `keyFindings`        | `html`       |
| `name`               | `text`       |
| `nextSteps`          | `html`       |
| `relatedWorkspaces`  | `manyToMany` |
| `setupBy`            | `lookup`     |
| `status`             | `picklist`   |
| `subTechniques`      | `manyToMany` |
| `tactics`            | `manyToMany` |
| `tasks`              | `manyToMany` |
| `techniques`         | `manyToMany` |
| `threatFeeds`        | `manyToMany` |
| `tools`              | `manyToMany` |

### Threat Intel Feeds

Following is the module schema of the **Threat Intel Feeds** module

| Field                       | Field Type            |
|-----------------------------|-----------------------|
| `confidence`                | `integer`             |
| `created`                   | `datetime`            |
| `description`               | `html`                |
| `expiresOn`                 | `datetime`            |
| `Indicator Type`            | `json`                |
| `indicators`                | `manyToMany`          |
| `killChainPhases`           | `multiselectpicklist` |
| `label`                     | `object`              |
| `lastSeen`                  | `datetime`            |
| `modified`                  | `datetime`            |
| `Name`                      | `text`                |
| `Pattern Type`              | `text`                |
| `Pattern Version`           | `text`                |
| `pattern`                   | `text`                |
| `relatedATTCKSubTechniques` | `manyToMany`          |
| `relatedATTCKTechniques`    | `manyToMany`          |
| `relatedMalware`            | `manyToMany`          |
| `relatedThreatActors`       | `manyToMany`          |
| `relatedThreatIntelFeeds`   | `manyToMany`          |
| `reputation`                | `picklist`            |
| `source`                    | `text`                |
| `sourceData`                | `object`              |
| `sourceId`                  | `text`                |
| `tasks`                     | `manyToMany`          |
| `threatTypes`               | `multiselectpicklist` |
| `tLP`                       | `picklist`            |
| `typeOfFeed`                | `picklist`            |
| `validFrom`                 | `datetime`            |
| `validUntil`                | `datetime`            |
| `value`                     | `text`                |
| `workspaces`                | `manyToMany`          |

### Threat Intel Reports

Following is the module schema of the **Threat Intel Reports** module

| Field                       | Field Type   |
|-----------------------------|--------------|
| `adversary`                 | `object`     |
| `Comments`                  | `manyToMany` |
| `geography`                 | `object`     |
| `imageURL`                  | `text`       |
| `industryTags`              | `object`     |
| `informationDate`           | `datetime`   |
| `informationReliability`    | `picklist`   |
| `motivation`                | `text`       |
| `publishDate`               | `datetime`   |
| `relatedATTCKSubTechniques` | `manyToMany` |
| `relatedATTCKTechniques`    | `manyToMany` |
| `relatedMalware`            | `manyToMany` |
| `relatedThreatActors`       | `manyToMany` |
| `relatedThreatIntelFeeds`   | `manyToMany` |
| `relevanceRating`           | `picklist`   |
| `reportID`                  | `text`       |
| `reportLink`                | `url`        |
| `reportStatus`              | `picklist`   |
| `reportTitle`               | `text`       |
| `reportType`                | `picklist`   |
| `source`                    | `text`       |
| `sourceCategory`            | `picklist`   |
| `sourceData`                | `object`     |
| `sourceName`                | `text`       |
| `sourceReliabiobjectlity`   | `picklist`   |
| `status`                    | `text`       |
| `summary`                   | `html`       |
| `threat    `                | `object`     |
| `threatIntelFeed`           | `manyToMany` |
| `threatReportImage`         | `html`       |
| `tLP`                       | `picklist`   |
| `workspaces`                | `manyToMany` |

### Hunts

Following is the module schema of the **Hunts** module

| Field            | Field Type   |
|------------------|--------------|
| `alerts`         | `manyToMany` |
| `cases`          | `manyToMany` |
| `comments`       | `manyToMany` |
| `communications` | `manyToMany` |
| `huntEnd`        | `datetime`   |
| `huntEventData`  | `text`       |
| `huntStart `     | `datetime`   |
| `Indicator`      | `text`       |
| `indicators`     | `manyToMany` |
| `indicatorType`  | `picklist`   |
| `name`           | `text`       |
| `sIEMSources`    | `text`       |
| `tasks   `       | `manyToMany` |
| `timeCreated`    | `datetime`   |

### Threat Actor

| Field                                  | Field Type   |
|:---------------------------------------|:-------------|
| `Affected Regions Filter`              | `text`       |
| `Affected Regions`                     | `text`       |
| `Aliases`                              | `text`       |
| `Attacker Regions Filter`              | `text`       |
| `Attacker Regions`                     | `text`       |
| `Comments`                             | `manyToMany` |
| `Common Vulnerabilities and Exposures` | `text`       |
| `CVEs`                                 | `manyToMany` |
| `Date Added`                           | `datetime`   |
| `Date Updated`                         | `datetime`   |
| `Description`                          | `text`       |
| `Groups`                               | `manyToMany` |
| `Image URL`                            | `text`       |
| `Known Infection Vectors`              | `text`       |
| `Known Tools Used`                     | `text`       |
| `Objectives`                           | `text`       |
| `Published`                            | `datetime`   |
| `References`                           | `text`       |
| `Source Data`                          | `Text Area`  |
| `Source`                               | `text`       |
| `Sub Techniques`                       | `manyToMany` |
| `Tactics`                              | `manyToMany` |
| `Target Systems Filter`                | `text`       |
| `Target Systems`                       | `text`       |
| `Targeted Industries Filter`           | `text`       |
| `Targeted Industries`                  | `text`       |
| `Techniques`                           | `manyToMany` |
| `Threat Actor ID`                      | `text`       |
| `Threat Actor Image`                   | `text`       |
| `Threat Actor Type`                    | `text`       |
| `Threat Intel Reports`                 | `manyToMany` |
| `Threat Signal`                        | `text`       |
| `threatActorURL`                       | `url`        |
| `Title`                                | `text`       |

### Cybersecurity News

| Field                | Field Type   |
|:---------------------|:-------------|
| `affectedProducts`   | `text`       |
| `affectedVendors`    | `text`       |
| `country`            | `text`       |
| `cVEList`            | `text`       |
| `cVEs`               | `manyToMany` |
| `cybersecurityImage` | `text`       |
| `description`        | `text`       |
| `imageURL`           | `text`       |
| `industrySector`     | `text`       |
| `mitigation`         | `text`       |
| `newsStatus`         | `picklist`   |
| `publicationDate`    | `datetime`   |
| `region`             | `text`       |
| `secNewsImage`       | `text`       |
| `source`             | `text`       |
| `sourceURL`          | `text`       |
| `title`              | `text`       |

## Dashboards

| Name                          | Description                                                                          |
|:------------------------------|:-------------------------------------------------------------------------------------|
| TIM OVerview and ROI          | Summarizes threat intelligence ingestion and activity over time.                     |
| Threat Intel Search           | Accepts indicators separated by a line break to get information from FortiGuard Labs |
| Threat Intelligence Dashboard | Presents intelligence through charts, statistics, and geographic visualizations.     |

## System View

| System View          | Description                                                                                                    |
|:---------------------|:---------------------------------------------------------------------------------------------------------------|
| Navigation menu item | A navigation menu item by the name of Threat Intel Management appears after installation of this solution pack |

## Module Views

| Module View          | Description                                                                                                                                                                                                                                                 |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workspaces           | A module that contains threat details like techniques, sub-techniques, actor groups, and tactics among other information                                                                                                                                    |
| Threat Intel Feeds   | A module that contains *Att&ck* details like related techniques, sub-techniques, actor groups, and tactics among other information                                                                                                                          |
| Threat Intel Reports | A module that contains in-depth analysis of the threat intelligence research conducted by FortiRecon ACI.                                                                                                                                                   |
| Threat Actor         | An encyclopedia of threat actors compiled by Fortinet FortiGuard                                                                                                                                                                                            |
| Hunt                 | The Hunts module is a place to store and organize your hunts. The hunt you create here will be the central repository where all Alerts, Assets, Users, and other modules' records that become associated with your hunting activity will be linked together |
| CyberSecurity News   | Delivers malware reverse-engineering, threat actor profiles, zero-day breakdowns, and ransomware campaign news tracking by FortiGuard Labs.                                                                                                                 |


## Global Variables

| Global Variable                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Indicator_Feed_Reputation_Preference` | Stores reputation and confidence threshold of an indicator feed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| `FortiguardIntelReportLastPullTime`    | Stores the date and time that reports were last fetched from FortiGuard. Reports are fetched based on the time range between the `lastPullTime` and the current time. Initially, value of this variable is set to  `{"pullAllReports":true, "lastPullTime": null}`, meaning that all reports are fetched the first time the "Ingest FortiGuard Threat Reports" playbook is run. After the first fetch, the value of this variable is set to  `{"pullAllReports":false, "lastPullTime": "currentDateTime"}` and subsequently only reports within the time range from the `lastPullTime` to the current time are fetched, and the global variable is updated accordingly after each fetch. |

## Connectors

| Connector                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fortinet FortiGuard Threat Intelligence | It provides threat intelligence to protect them from malicious cyber attacks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Fortinet FortiRecon ACI                 | FortiRecon is a Digital Risk Protection Service(DRPS) that provides an outside-the-network view to the risks posed to your enterprise.The Adversary Centric Intelligence (ACI) module leverages FortiGuard Threat Analysts to provide comprehensive coverage of dark web, open source, and technical threat intelligence, including threat actor insights. This information enables administrators to proactively assess risks, respond faster to incidents, better understand their attackers, and protect assets. This connector facilitates the automated operations related to ACI. |
| File Content Extraction                 | File Content Extraction is a FortiSOAR™ utility to extract text, artifacts, and metadata from almost any file.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| MITRE ATT&CK                            | This MITRE ATT&CK connector helps to import MITRE ATT&CK techniques from the static data available within the connector and adds the data to FortiSOAR in MITRE ATT&CK Techniques module. This import procedure helps in replicating the knowledge base of adversary tactics and techniques based on real-world observations.                                                                                                                                                                                                                                                           |
| CISA Advisory                           | CISA Advisory connector fetches the Advisory and Known Exploited Vulnerability (KEV) CVE published by CISA.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Fortinet FortiGuard IOC                 | Facilitates finding details about indicators from the FortiGuard Threat Intelligence server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Fortinet FortiGuard Outbreak            | Provides key information about on-going cybersecurity attack with significant ramifications affecting numerous companies, organizations and industries                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Exploit Prediction Scoring System (EPSS)| Leverages EPSS framework used by cybersecurity teams to assess the likelihood of a vulnerability being exploited by adversaries.|

## Widgets

| Widgets                               | Description                                                                                                                              |
|:--------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| Access Control                        | Change which teams or users have access to certain records                                                                               |
| Card Tiles                            | Shows a list of records in a card tile view                                                                                              |
| Card View                             | Reads JSON data and dynamically generates a responsive card listing.                                                                     |
| Categorical Insights                  | Creates division of data using different color codes                                                                                     |
| Custom Tags                           | A series of tags that summarize associated CVE identifiers, named threats and exploits, and mapped outbreaks and exploitation techniques |
| Cyber Threat World Map                | A world map that displays top visitor origins to understand global exposure and potential threat spread                                  |
| Feed Configuration Settings           | Configures feeds to be consumed by modules                                                                                               |
| FortiGuard IOC Search                 | Accepts indicators separated by a line break to get information from FortiGuard Labs                                                     |
| Kill Chain Phases                     | Shows the IOC count present for different stages of cyber attack. It highlights the stage of the selected IOC                            |
| Manage Datasets                       | Manage and Create datasets out of threat feeds                                                                                           |
| Picklist as Phases                    | Displays the 'Report Status' picklist values as phases in a flow diagram format within the detail view of a threat intel report          |
| Speedometer                           | Displays the percentage value of selected parameter using a red dial gauge                                                               |
| Summary grid                          | Creates a grid and populates it with formatted JSON data                                                                                 |
| Task Management                       | Allows users to manage tasks and get visibility into the current task board.                                                             |
| TAXII Server Configuration            | Configures the TAXII Server for easy dissemination of information                                                                        |
| Threat Analytics                      | Delivers real-time insights by continuously monitoring, analyzing, and mapping the worldwide attack surface                              |
| Threat Intel Management Configuration | Configures the Threat Intel Management solution pack                                                                                     |
| Threat Landscape View                 | Gives an overview of intrusion, malware, and botnet activity                                                                             |
| Threat Map                            | Displays live attack activity with source-target mapping and severity insights                                                           |

## Playbook Collection

| 10 - SP - TIM Automation |
|:-------------------------|


| Playbook                                                                             | Description                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Setup TIM Workspace (Tasks)                                                          | Launches TIM Workspace from Tasks - Priority Intelligence Requirements(PIR)                                                                                                                                                                                                                                                                        |
| Raise Priority Intelligence Requirement Request (PIR)                                | Raises a PIR request                                                                                                                                                                                                                                                                                                                               |
| Generate Threat Summary Report                                                       | Generates a threat summary report to ease analysis                                                                                                                                                                                                                                                                                                 |
| Scenario - Create Threat Intel Reports                                               | Creates threat intel report and its associated records in threat intel management module                                                                                                                                                                                                                                                           |
| Extract Unstructured Feeds From File                                                 | Extracts feeds from the provided file and creates Threat Intelligence Feed records                                                                                                                                                                                                                                                                 |
| Extract Unstructured Feeds From Email                                                | Extracts feeds from email attachments and creates a FortiSOAR record                                                                                                                                                                                                                                                                               |
| Extract Unstructured Feeds from Email > Extract Feeds from Attachments               | Extracts feeds from email attachments and creates an alert in FortiSOAR                                                                                                                                                                                                                                                                            |
| Extract Unstructured Feeds From Email or File > Create Threat Feeds From Attachments | Creates Threat Feeds Form Attachments                                                                                                                                                                                                                                                                                                              |
| Configure Threat Feeds Rules                                                         | Configures the Unstructured Threat Feeds, Block High Confidence Threat Feeds rules                                                                                                                                                                                                                                                                 |
| Retrieves MITRE ATT&CK Details                                                       | Retrieves MITRE ATT&CK Techniques from the FortiSOAR MITRE ATT&CK Techniques module for the FortiGuard threat Report and correlates them.                                                                                                                                                                                                          |
| Link or Create CVEs                                                                  | Identifies CVEs from the CVE module. If a matching CVE is found, it is correlated. If no matching CVE is found, the system searches NIST and creates a new CVE record, then correlates it.                                                                                                                                                         |
| Ingest FortiGuard Threat Reports                                                     | Ingests `Outbreak Alert`, `Signal Report`, `FortiGuard Blog` and `FortiGuard Events` reports as threat reports into FortiSOAR. A schedule named `Ingestion_fortinet-fortiguard-threat-intelligence_report` is embedded within this playbook and is configured to automatically trigger the playbook to fetch FortiGuard reports daily at 12:00 AM. |
| Configure Threat Feed Configuration Wizard                                           | Configures the threat feed rules for the threat intelligence management framework.                                                                                                                                                                                                                                                                 |
| Create FortiGuard Threat Actors                                                      | Creates FortiGuard Threat Actor records and links them with related MITRE techniques, tactics, groups, CVEs, and outbreak alerts.                                                                                                                                                                                                                  |
| Fetch Threat Actor Details                                                           | Fetches threat actors details from FortiGuard and creates or updates corresponding threat actor records in FortiSOAR.                                                                                                                                                                                                                              |
| Ingest FortiGuard Threat Actors                                                      | Ingests threat actors from FortiGuard                                                                                                                                                                                                                                                                                                              |
| Threat Actor CVE Mapping                                                             | This playbook fetches and links CVE records associated with a Threat Actor. If no associated CVEs are found, it queries NIST, creates a new CVE record, it to the Threat Actor for enrichment and tracking.                                                                                                                                        |
| Threat Intel Report CVE Mapping                                                      | This playbook fetches and links CVE records associated with a Threat Intel Report. If no associated CVEs are found, it queries NIST, creates a new CVE record, and links it to the report for enrichment and tracking.                                                                                                                             |
| Ingest Cybersecurity News                                                            | Ingest structured cybersecurity news data enriched and analyzed using artificial intelligence to identify vulnerabilities, threats, affected products, industries, and mitigation insights.                                                                                                                                                        |
| > Create Cybersecurity News                                                          | Creates structured cybersecurity news records.                                                                                                                                                                                                                                                                                                     |

| 04 - Actions |
|:-------------|


| Playbook                                     | Description                                                                     |
|:---------------------------------------------|:--------------------------------------------------------------------------------|
| Action - Mac Addresses - Block Threat Feeds  | Launch TIM Workspace from Tasks &ndash; Priority Intelligence Requirements(PIR) |
| Action - URL - Block Threat Feeds            | Blocks indicators of type 'URLs' on the firewall.                               |
| Action - IPv4 Addresses - Block Threat Feeds | Blocks indicators of type 'IP Addresses on the firewall                         |
| Action - Domains - Block Threat Feeds        | Blocks indicators of type 'Domains' on the firewall                             |
| Action - IPv6 Addresses - Block Threat Feeds | Blocks indicators of type 'IP Addresses on the firewall                         |
| Action - Filehashes - Block Threat Feeds     | Blocks indicators of type 'Email Addresses' on the firewall                     |
| Action - Block Threat Feeds (Type All)       | Blocks all types of feeds on the firewall                                       |


## Report

| Report                      | Description                                       |
| :-------------------------- | :------------------------------------------------ |
| Threat Intel Summary Report | Display threat intel summary for an easy analysis |

## Roles

- Full App Permissions
- SOC Manager
- Threat Intel Management
- SOC Analyst
- Read -Only User

## Picklists

- IndicatorReputation
- TaskStatus
- TaskType
- ThreatIntelFeedType
- TrafficLightProtocol
- Workspace Status
- KillChainPhases
- Threat Type
- Information Reliability
- Relevance Rating
- Report Type
- Source Category
- Source Reliability
- IOC Search Confidence
- Risk Distribution
- Risk Level

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|
