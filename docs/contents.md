| [Home](https://github.com/fortinet-fortisoar/solution-pack-threat-intel-management/blob/develop/README.md) |
|--------------------------------------------|

# Contents

This section lists the various contents of the Threat Intel Management Solution Pack. 

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


## System View

| System View          | Description                                                                                                    |
|:---------------------|:---------------------------------------------------------------------------------------------------------------|
| Navigation menu item | A navigation menu item by the name of Threat Intel Management appears after installation of this solution pack |

## Module Views

| Module View        | Description                                                                                                                        |
|:-------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| Workspaces         | A module that contains threat details like techniques, sub-techniques, actor groups, and tactics among other information           |
| Threat Intel Feeds | A module that contains *Att&ck* details like related techniques, sub-techniques, actor groups, and tactics among other information |

## Global Variables

| Module View                            | Description                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| `Indicator_Feed_Reputation_Preference` | Stores reputation and confidence threshold of an indicator feed |

## Connectors

| Connector                               | Description                                                                                                                                |
|:----------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| Fortinet FortiGuard Threat Intelligence | It provides threat intelligence to protect them from malicious cyberattacks.                                                               |
| MalSilo                                 | Facilitates automated interactions, with MalSilo using FortiSOAR™ playbooks. You can ingest threat intelligence feeds from MalSilo Gitlab. |

## Widgets

| Widgets                     | Description |
|:----------------------------|:------------|
| Card Tiles                  |             |
| Task Management             |             |
| Manage Datasets             |             |
| Access Control              |             |
| Feed Configuration Settings |             |

## Playbook Collection

| 10 - SP - TIM Automation |
|:-------------------------|

| Playbook                                              | Description                                                                     |
|:------------------------------------------------------|:--------------------------------------------------------------------------------|
| Setup TIM Workspace (Tasks)                           | Launch TIM Workspace from Tasks &ndash; Priority Intelligence Requirements(PIR) |
| Raise Priority Intelligence Requirement Request (PIR) | Raises a PIR request                                                            |
| Generate Threat Summary Report                        | Generates a threat summary report to ease analysis                              |

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
