# What's New

> [!NOTE]
> This solution pack requires FortiSOAR `v8.0.0` and later.

## Module Enhancements

### Hunt

The **Hunt** module now supports pluggable hunting through FortiSIEM and Splunk.

- Creating a new Hunt record now triggers pluggable hunt playbooks that update hunt details in the same record.
- The following fields have been added to the Hunt module:

  - Indicator Type
  - Indicator
  - SIEM Sources
  - Case
  - Hunt Event Data
  - Hunt Status

- The `SIEM` field has been removed from the Hunt module.
- The default detailed view layout for Hunt records has been updated.

### Threat Reports

- The **Threat Intel Reports** module now displays reports as cards instead of a list.

### Cybersecurity News

A new **Cybersecurity News** module has been added. This module contains daily advisories, threat intelligence reports, and vulnerability disclosures published by industry vendors and curated by FortiGuard Labs.

The following playbooks have been added to ingest and update cybersecurity news:

```text
Ingest Cybersecurity News
> Create Cybersecurity News
```

The following schedule has also been added to update cybersecurity news on a scheduled basis:

```text
Ingest_fortinet-fortiguard-cybersecurity-news
```

### Dashboards

- The Threat Intelligence dashboard *TIM Overview and ROI* has been moved from **Threat Intelligence > Overview** to **Dashboards**.

- The following threat intelligence dashboards have been added under **Threat Intelligence Dashboard**:

  - Landscape
  - Analytics
  - Global Map

## Miscellaneous

- The navigation menu and menu items have been updated.
- Color codes associated with picklists have been standardized across the user interface.

## Known Issues

After upgrading to FortiSOAR `v8.0.0` with Threat Intel Management `v3.0.0`, the playbooks *Ingest FortiGuard Threat Actors* and *Fetch Threat Actor Detail playbooks* may fail during execution.

### Resolution

Upgrade Threat Intel Management to vv4.0.0.
