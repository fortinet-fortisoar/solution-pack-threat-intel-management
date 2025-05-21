# What's New

### Simplified Setup with the Configuration Wizard

Effortlessly set up your Threat Intel Management system with our new **Configuration Wizard**. This step-by-step guide ensures an intuitive and smooth setup experience by breaking tasks into manageable stages:
- **Feed Source Selection**: Easily choose the feed sources most relevant to your needs.
- **Integration Installation & Configuration**: Quickly install and configure integrations with just a few clicks.
- **Granular Rule Selection**: Leverage powerful rules to manage feeds, even those with unstructured data.

With this streamlined process, you'll be up and running in no time.

---

#### Re-imagined Navigation and Enhanced Access
Introducing an enhanced navigation menu dedicated to Threat Intel Management, giving you quick and organized access to all your intel:
- **Dashboard**: Start with a high-level snapshot, including metrics like Ingested Volume, High Confidence Observables, and Linked Indicators. The Threat Intel Management Overview Dashboard is now also available in the Dashboards module, providing consistent visibility across the platform.
- **Threat Intel Feed**: Dive into feed configurations, reports, and intelligence with ease.
- **Hunts**: Track all active hunts from a single menu.

This new navigation experience brings everything you need into a unified, intuitive interface.

---

#### Enhanced Features for Precision and Compliance
- **Hunts Module Relocation**: The Hunts module is now part of Threat Intel Management, offering cohesive access to threat analysis tools.
- **Mandatory Fields Compliance**: Feed modules now meet STIX/TAXII 2.0 requirements with key fields marked as mandatory.
- **System View Template Update**: The System View Template (SVT) now includes new fields, ensuring comprehensive and up-to-date data representation.
- **Feed Configuration Settings**: The sections of feed configuration settings have been rearranged under 3 tabs:
    - *Feed Sources* - Find, Install, and Configure new feed connectors through Content Hub.
    - *TAXII Server* - Configure a TAXII Server to generate an outgoing feed to share threat intelligence externally.
    - *Threat Feed Rules* - Configure threat feed to manage threat intelligence from various sources.
- The **Workspace** now carries a description field to better communicate the purpose of setting up a workspace
Stay aligned with industry standards while managing your threat feeds seamlessly.

---

#### Streamlined Threat Feed Management

Managing threat data just got easier with these powerful updates:

- **Unstructured Feeds Made Simple**: The new Import Unstructured Feeds button on the Threat Feed page lets you upload files and create feed records effortlessly.
- **MITRE ATT&CK Connector with Default Configuration**: The MITRE ATT&CK connector now installs with a default configuration. You no longer need to manually configure it to ingest threat feeds from the MITRE organization.
- **Threat Feed Rules**: New rules help streamline threat feed management:
    - **Link Threat Feed to Indicators**: (Earlier *Feed to Indicator Linking*) Updates the indicator reputation as per the matching feed.
    - **Ingest Unstructured Threat Feeds**: Ingests unstructured feeds from files or email attachments
- Following are added for *MITRE&reg;* connector during installation:
    - A default configuration
    - Data ingestion playbooks
    - An ingestion schedule
- Following are removed for *Fortinet FortiGuard Threat Intelligence* during installation
    - Data ingestion playbooks
    - An ingestion schedule

    These are created by the configuration wizard later. 

- The configuration wizard creates the following datasets and triggers the *MITRE&reg;* integration's data ingestion:
    - FortiGuard Outbreak Threat Feeds
    - FortiGuard Threat Intel Feeds
    - Phishing Threat Feeds

These features enable seamless handling of diverse data formats and automated configurations, saving time and effort.

---

Take advantage of these updates to simplify and elevate your threat intelligence workflow.