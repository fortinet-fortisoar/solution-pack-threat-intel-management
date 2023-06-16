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

## System View

| System View          | Description                                                                                                    |
|:---------------------|:---------------------------------------------------------------------------------------------------------------|
| Navigation menu item | A navigation menu item by the name of Threat Intel Management appears after installation of this solution pack |

## Module Views

| Module View          | Description                                                                                                                        |
|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| Workspaces           | A module that contains threat details like techniques, sub-techniques, actor groups, and tactics among other information           |
| Threat Intel Feeds   | A module that contains *Att&ck* details like related techniques, sub-techniques, actor groups, and tactics among other information |
| Threat Intel Reports | A module that contains in-depth analysis of the threat intelligence research conducted by FortiRecon ACI.                          |

## Global Variables

| Module View                            | Description                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| `Indicator_Feed_Reputation_Preference` | Stores reputation and confidence threshold of an indicator feed |

## Connectors

| Connector                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:----------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fortinet FortiGuard Threat Intelligence | It provides threat intelligence to protect them from malicious cyber attacks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| MalSilo                                 | Facilitates automated interactions, with MalSilo using FortiSOAR™ playbooks. You can ingest threat intelligence feeds from MalSilo Gitlab                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Fortinet FortiRecon ACI                 | FortiRecon is a Digital Risk Protection Service(DRPS) that provides an outside-the-network view to the risks posed to your enterprise.The Adversary Centric Intelligence (ACI) module leverages FortiGuard Threat Analysts to provide comprehensive coverage of dark web, open source, and technical threat intelligence, including threat actor insights. This information enables administrators to proactively assess risks, respond faster to incidents, better understand their attackers, and protect assets. This connector facilitates the automated operations related to ACI. |

## Widgets

| Widgets                     | Description                                                                  |
|:----------------------------|:-----------------------------------------------------------------------------|
| Card Tiles                  | Shows record list in a card tile view                                        |
| Task Management             | Allows users to manage tasks and get visibility into the current task board. |
| Manage Datasets             | Manage and Create datasets                                                   |
| Access Control              | Change which teams or users have access to records                           |
| Feed Configuration Settings | Configures feeds to be consumed by modules                                   |

## Playbook Collection

| 10 - SP - TIM Automation |
|:-------------------------|

| Playbook                                              | Description                                                                             |
|:------------------------------------------------------|:----------------------------------------------------------------------------------------|
| Setup TIM Workspace (Tasks)                           | Launch TIM Workspace from Tasks &ndash; Priority Intelligence Requirements(PIR)         |
| Raise Priority Intelligence Requirement Request (PIR) | Raises a PIR request                                                                    |
| Generate Threat Summary Report                        | Generates a threat summary report to ease analysis                                      |
| Scenario - Threat Intel Reports                | Create threat intel report and its associated records in threat intel management module |

## Report

| Report                      | Description                                       |
|:----------------------------|:--------------------------------------------------|
| Threat Intel Summary Report | Display threat intel summary for an easy analysis |

## Roles

- Full App Permissions
- SOC Manager
- Threat Intel Management

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

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|