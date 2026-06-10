| [Home](../README.md) |
|----------------------|

# Hunt

With the new *Pluggable* hunt in place, the hunting process is now faster and more optimized. We recommend using it to augment or enhance your indicator hunt process.

## Using Pluggable Indicator Hunting Framework

The *Pluggable* Indicator Hunting framework is designed to integrate various SIEM integrations, such as FortiSIEM and Splunk, for efficient Indicator hunting. *Pluggable* Indicator Hunt process uses the playbooks contained within installed connectors to hunt an indicator.

This hunt process is triggered when a hunt record is created.

### Understanding the Hunt Process

Upon triggering, the playbook **Hunt Indicators (Type All)** executes and puts the following sequence in motion:

1. **Search Tagged Playbooks**: The playbook *Hunt Indicators (Type All)* searches for installed connector playbooks with specific tags using the playbook **Update/Initialize Indicator Enrichment Global Variables**. For example
   - If the indicator is of the type *URL*, this playbook looks for the tag `URL_Hunt`
   - For indicators of type *IP Address* it looks for the tag `IP_Hunt`
   - For indicators of type *File Hash* it looks for the tag `FileHash_Hunt`

2. **Configuration Check**: Once the playbooks with appropriate tags are identified, the playbook *Update/Initialize Indicator Enrichment Global Variables* checks if the corresponding connectors are configured. For this purpose, it runs the playbook **Retrieve Configured Enrichment Connectors**.

3. **Check Playbook IRI Global Variable**: If the connectors are configured, the playbook *Update/Initialize Indicator Enrichment Global Variables* checks the global variables &ndash; in the format *`<indicator type>`*`_Hunt_Playbooks_IRIs` &ndash; containing the associated playbooks IRI, and creates the variable if not found.

    For example, for indicator of type *URL* it checks for the global variable `URL_Hunt_Playbooks_IRIs` and creates the global variable when not found.

4. **Update Playbook IRI**: The playbook *Update/Initialize Indicator Enrichment Global Variables* adds the associated playbook IRIs to the corresponding global variable.

    For example, the IRIs of playbooks tagged with `URL_Hunt`, are added to the global variable `URL_Hunt_Playbooks_IRIs`.

5. **Add/Remove Existing Playbook IRIs**: In a situation when user adds new/custom hunt playbook or remove/inactivate the  existing hunt playbooks from the sample collection then it is required to reset the hunt global variable by executing the `Reset Hunt Global Variables` playbook in *05-Hunt* collection. 

### Creating a Hunt Record

The Threat Hunt module is a place to store and organize your hunts and you can find it under <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intel-management-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intel-management-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intel-management-dark.svg"></picture> **Threat Intelligence** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-space-shuttle-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-space-shuttle-dark.svg"><img alt="Fallback image description" src="./res/icon-space-shuttle-dark.svg"></picture> **Hunts**.

Hunts you create here acts as a central repository to associate *Alerts*, *Assets*, *Users*, and other module records with your hunting activity.

1. Click <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-add-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-add-dark.svg"><img alt="Fallback image description" src="./res/icon-add-dark.svg"></picture> **Add**.

    ![](./res/add-new-hunt.png)

2. Specify a name of the hunt in the **Name** field.

3. Specify a start date and time for the hunt in the **Hunt Start** field.

4. Specify an end date and time for the hunt in the the **Hunt End** field.

5. Specify tags associated with the hunt in the **Tags** field. The tags can be selected from the suggested options, or separated by a comma (`,`) or the `tab` key.

6. Click **Save**.

The **Hunt Start** time is a *required* parameter, while the the **Hunt End** time is optional. Hunt Start and Hunt End times can be modified any time in order to expand or contract the hunting window.

> [!TIP]
> 
> We recommend that you pick a constrained start time during the initial stages of a hunt, to gauge the number of returned results and tune any obvious false positives before running a larger-scale hunt.
> 

### Triggering a Hunt

When a **Hunt** record is created a hunt query runs on configured connectors which in turn returns the hunt information

- The playbook **Hunt (On Create) - Initiate IOC Hunt** is executed, which calls the playbook **Hunt Indicators (Type All)**

- A comment is added to the hunt record with a summary and source data containing the following hunt information:

   - **Events**: Hunted events to be fetched, this value is retrieved from the **Key Store** record `pluggable-IOCs-hunt-parameters`

   - **Source**: SIEM source name, for example, FortiSIEM

   - **Total Event Count**: Total events found when hunt query ran on the SIEM platform
	 
# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
