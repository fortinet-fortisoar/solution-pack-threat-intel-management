| [Home](../README.md) |
|----------------------|

# Contents

This section lists the various contents of the **Threat Intel Management** Solution Pack. 

## Module Schemas

### Tasks
Following is the module schema of the **Tasks** module

| Field              | Field Type   |
|--------------------|--------------|
| `submittedBy`      | `lookup`     |
| `name`             | `text`       |
| `description`      | `richtext`   |
| `type`             | `picklist`   |
| `dueBy`            | `datetime`   |
| `assignedOnDate`   | `datetime`   |
| `startDate`        | `datetime`   |
| `completedOnDate`  | `datetime`   |
| `actualMinutes`    | `integer`    |
| `priority`         | `picklist`   |
| `status`           | `picklist`   |
| `assignedToPerson` | `lookup`     |
| `companies`        | `manyToMany` |
| `persons`          | `manyToMany` |
| `attachments`      | `manyToMany` |
| `comments`         | `manyToMany` |
| `uuid`             | `null`       |
| `approvalhost`     | `text`       |
| `workflowid`       | `text`       |
| `taskdata`         | `richtext`   |
| `tasktype`         | `text`       |
| `stepid`           | `integer`    |
| `alerts`           | `manyToMany` |
| `hunt`             | `manyToMany` |
| `warrooms`         | `manyToMany` |
| `threatIntelFeeds` | `manyToMany` |
| `workspaces`       | `manyToMany` |
| `incidents`        | `manyToMany` |
| `assets`           | `manyToMany` |
| `indicators`       | `manyToMany` |


### Workspaces
Following is the module schema of the **Workspaces** module

| Field                | Field Type   |
|----------------------|--------------|
| `actorGroupAnalysis` | `html`       |
| `keyFindings`        | `html`       |
| `relatedWorkspaces`  | `manyToMany` |
| `description`        | `html`       |
| `status`             | `picklist`   |
| `setupBy`            | `lookup`     |
| `comments`           | `manyToMany` |
| `nextSteps`          | `html`       |
| `name`               | `text`       |
| `files`              | `manyToMany` |
| `indicators`         | `manyToMany` |
| `threatFeeds`        | `manyToMany` |
| `tasks`              | `manyToMany` |
| `tools`              | `manyToMany` |
| `subTechniques`      | `manyToMany` |
| `actorGroups`        | `manyToMany` |
| `techniques`         | `manyToMany` |
| `tactics`            | `manyToMany` |
| `impactAnalysis`     | `richtext`   |

### Threat Intel Feeds
Following is the module schema of the **Threat Intel Feeds** module

| Field                       | Field Type            |
|-----------------------------|-----------------------|
| `confidence`                | `integer`             |
| `validFrom`                 | `datetime`            |
| `validUntil`                | `datetime`            |
| `expiresOn`                 | `datetime`            |
| `created`                   | `datetime`            |
| `source`                    | `text`                |
| `lastSeen`                  | `datetime`            |
| `value`                     | `text`                |
| `reputation`                | `picklist`            |
| `sourceData`                | `object`              |
| `workspaces`                | `manyToMany`          |
| `tasks`                     | `manyToMany`          |
| `typeOfFeed`                | `picklist`            |
| `tLP`                       | `picklist`            |
| `indicators`                | `manyToMany`          |
| `relatedThreatActors`       | `manyToMany`          |
| `modified`                  | `datetime`            |
| `relatedATTCKTechniques`    | `manyToMany`          |
| `relatedThreatIntelFeeds`   | `manyToMany`          |
| `sourceId`                  | `text`                |
| `relatedATTCKSubTechniques` | `manyToMany`          |
| `relatedMalware`            | `manyToMany`          |
| `pattern`                   | `text`                |
| `label`                     | `object`              |
| `description`               | `html`                |
| `threatTypes`               | `multiselectpicklist` |
| `killChainPhases`           | `multiselectpicklist` |
| `Pattern Type`              | `text`                |
| `Pattern Version`           | `text`                |
| `Name`                      | `text`                |
| `Indicator Type`            | `json`                |

### Threat Intel Reports
Following is the module schema of the **Threat Intel Reports** module

| Field                       | Field Type            |
|-----------------------------|-----------------------|
| `industryTags`              | `object`              |
| `geography`                 | `object`              |
| `threat    `                | `object`              |
| `reportTitle`               | `text`                |
| `reportID`                  | `text`                |
| `status`                    | `text`                |
| `summary`                   | `html`                |
| `motivation`                | `text`                |     
| `sourceName`                | `text`                |
| `sourceData`                | `object`              |
| `relevanceRating`           | `picklist`            |
| `informationReliability`    | `picklist`            |
| `reportType`                | `picklist`            |
| `sourceCategory`            | `picklist`            |
| `sourceReliabiobjectlity`   | `picklist`            | 
| `reportLink`                | `url`                 |
| `adversary`                 | `object`              |
| `tLP`                       | `picklist`            |
| `workspaces`                | `manyToMany`          |
| `Comments`                  | `manyToMany`          |
| `relatedThreatActors`       | `manyToMany`          |
| `publishDate`               | `datetime`            |
| `informationDate`           | `datetime`            |
| `relatedATTCKTechniques`    | `manyToMany`          |
| `relatedThreatIntelFeeds`   | `manyToMany`          |
| `threatIntelFeed`           | `manyToMany`          |
| `source`                    | `text`                |
| `relatedATTCKSubTechniques` | `manyToMany`          |
| `relatedMalware`            | `manyToMany`          |

### Hunts
Following is the module schema of the **Tasks** module

| Field              | Field Type   |
|--------------------|--------------|
| `alerts`           | `manyToMany` |
| `comments`         | `manyToMany` |
| `communications`   | `manyToMany` |
| `huntEnd`          | `datetime`   |
| `huntStart `       | `datetime`   |
| `indicators`       | `manyToMany` |
| `name`             | `text`       |
| `siems`            | `picklist`   |
| `tasks   `         | `manyToMany` |
| `timeCreated`      | `datetime`   |


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
| Hunt                 | The Hunts module is a place to store and organize your hunts. The hunt you create here will be the central repository where all Alerts, Assets, Users, and other modules’ records that become associated with your hunting activity will be linked together |


## Global Variables

| Module View                            | Description                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| `Indicator_Feed_Reputation_Preference` | Stores reputation and confidence threshold of an indicator feed |

## Connectors

| Connector                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fortinet FortiGuard Threat Intelligence | It provides threat intelligence to protect them from malicious cyber attacks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Fortinet FortiRecon ACI                 | FortiRecon is a Digital Risk Protection Service(DRPS) that provides an outside-the-network view to the risks posed to your enterprise.The Adversary Centric Intelligence (ACI) module leverages FortiGuard Threat Analysts to provide comprehensive coverage of dark web, open source, and technical threat intelligence, including threat actor insights. This information enables administrators to proactively assess risks, respond faster to incidents, better understand their attackers, and protect assets. This connector facilitates the automated operations related to ACI. |
| File Content Extraction                 | File Content Extraction is a FortiSOAR™ utility to extract text, artifacts, and metadata from almost any file.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| MITRE ATT&CK                            | This MITRE ATT&CK connector helps to import MITRE ATT&CK techniques from the static data available within the connector and adds the data to FortiSOAR in MITRE ATT&CK Techniques module. This import procedure helps in replicating the knowledge base of adversary tactics and techniques based on real-world observations.                                                                                                                                                                                                                                                           |
| CISA Advisory                           | CISA Advisory connector fetches the Advisory and Known Exploited Vulnerability (KEV) CVE published by CISA.                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| File Content                            | File Content Extraction is a FortiSOAR™ utility to extract text, artifacts, and metadata from almost any file.|  
| MITRE ATT&CK                            | This MITRE ATT&CK connector helps to import MITRE ATT&CK techniques from the static data available within the connector and adds the data to FortiSOAR in MITRE ATT&CK Techniques module. This import procedure helps in replicating the knowledge base of adversary tactics and techniques based on real-world observations.|   


## Widgets

| Widgets                               | Description                                                                  |
|:--------------------------------------|:-----------------------------------------------------------------------------|
| Card Tiles                            | Shows a list of records in a card tile view                                  |
| Task Management                       | Allows users to manage tasks and get visibility into the current task board. |
| Manage Datasets                       | Manage and Create datasets out of threat feeds                               |
| Access Control                        | Change which teams or users have access to certain records                   |
| Feed Configuration Settings           | Configures feeds to be consumed by modules                                   |
| Threat Intel Management Configuration | Configures the Threat Intel Management solution pack                         |
| TAXII Server Configuration            | Configures the TAXII Server for easy dissemination of information            |


## Playbook Collection

| 10 - SP - TIM Automation |
|:-------------------------|


| Playbook                                                                             | Description                                                                                         |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| Setup TIM Workspace (Tasks)                                                          | Launch TIM Workspace from Tasks &ndash; Priority Intelligence Requirements(PIR)                     |
| Raise Priority Intelligence Requirement Request (PIR)                                | Raises a PIR request                                                                                |
| Generate Threat Summary Report                                                       | Generates a threat summary report to ease analysis                                                  |
| Scenario - Threat Intel Reports                                                      | Create threat intel report and its associated records in threat intel management module             |
| Extract Unstructured Feeds From File                                                 | This playbook will extract feeds from the provided file and create Threat Intelligence Feed records |
| Extract Unstructured Feeds From Email                                                | This playbook will extract the feeds from email attachments and will create FortiSOAR record        |
| Extract Unstructured Feeds from Email > Extract Feeds from Attachments               | This playbook will extract the feeds from email attachments and will create an alert in FortiSOAR   |
| Extract Unstructured Feeds From Email or File > Create Threat Feeds From Attachments | Create Threat Feeds Form Attachments                                                                |
| Configure Threat Feeds Rules                                                         | Configure the Unstructured Threat Feeds, Block High Confidence Threat Feeds rules                   |


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
|:----------------------------|:--------------------------------------------------|
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

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|
