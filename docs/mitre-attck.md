| [Home](../README.md) |
|----------------------|

## What is MITRE ATT&CK

MITRE ATT&CK&reg; is a comprehensive, globally-accessible knowledge base of adversary tactics and techniques based on real-world observations of a threat actor behavior. It acts as a standardized framework for modeling, detecting, and mitigating cyber threats, helping security teams understand *how* attackers operate (techniques) and *why* (tactics).

## Using MITRE ATT&CK Data in TIM

You can configure and schedule data ingestion using the MITRE ATT&CK&reg; connector. This connector fetches latest information about groups, mitigation, software, techniques and other information and places them in the appropriate modules.

Navigate to <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intel-management-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intel-management-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intel-management-dark.svg"></picture> **Threat Intel Management** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-mitre-attack-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-mitre-attack-dark.svg"><img alt="Fallback image description" src="./res/icon-mitre-attack-dark.svg"></picture> **MITRE ATT&CK**

1. Click **Groups** to view an exhaustive list of threat groups.
    - Click a *Group* to view more information about it
    - Under the tab **Related Records** you can check the following tabs
        - **Techniques** - Lists the techniques that the selected group uses
        - **Software** - Lists software that the selected group uses

2. Click **Mitigation** to view a list of mitigation measures in place.
    - Click a *Mitigation* measure to view more information about it
    - Under the tab **Related Records** you can check the following tabs
        - **Techniques** - Lists the techniques that the selected mitigation method addresses
        - **Sub-techniques** - Click a technique to view the sub-techniques that the selected mitigation method addresses

3. Click **Software** to view a list of malicious software used for a MITRE ATT&CK&reg;.
    - Click a *Software* to view more information about it
    - Under the tab **Related Records** you can check the following tabs
        - **Groups** - Lists the groups that use the selected malicious software
        - **Techniques** - Lists the techniques that the selected software uses
        - **Sub-techniques** - Lists the techniques that the selected software uses

4. Click **Techniques** to view a list of techniques used for a MITRE ATT&CK&reg;.
    - Click a *Technique* to view more information about it
    - Under the tab **Related Records** you can check the following tabs
        - **Sub-techniques** - Lists the sub-techniques that categorized under the selected technique

5. Click **Sub-techniques** to view a list of sub-techniques used for a MITRE ATT&CK&reg;.
    - Click a *Sub-technique* to view more information about it
    - Under the tab **Related Records** you can check the following tabs
        - **Software** - Lists software that exploit the selected sub-technique

6. Click **Tactics** to view a list of tactics used for a MITRE ATT&CK&reg;.
    - Click a *Tactic* to view more information about it
    - Under the tab **Techniques** you can check the techniques that the selected tactic uses

7. Open an alert or an incident containing a technique ID
    - Under **Correlations** check correlated *Tactics*, *Technique*, *sub-techniques*, and other information
        - For SOAR Framework `v2.1.1` and earlier, check the mitigation actions in the *Mitigations* tab
        - For SOAR Framework `v2.2.0` and later, check the mitigation actions in the *Recommended ATT&CK Mitigations* tab

A scheduled data ingestion periodically fetches the latest information from the MITRE ATT&CK&reg; database.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
