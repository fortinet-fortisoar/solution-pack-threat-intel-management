# What's New

### Enhanced the Threat Intel Report Module

Improved the Threat Intel Report module to give you a more streamlined and organized layout, making it easier to navigate and identify key report details at a glance: 

- **Report Status as a flow diagram**: The report's detail view now displays its status as a flow diagram, visually reflecting the current phase of the report. The current phase of the report corresponds to the status of the report in its title.
- **Simplified List Layout**: Restructured the columns in the Threat Reports list view, making it easier to locate and filter reports quickly.

---

#### Added support for ingesting FortiGuard Threat Reports
Introduced support for ingesting FortiGuard Threat Reports! To enable this, the following updates are made to the `10 - SP - TIM Automation` playbook collection:
- Added the following playbooks:
    - **Ingest FortiGuard Threat Reports**: This playbook ingests `Outbreak Alert`, `Signal Report`, `FortiGuard Blog` and `FortiGuard Events` reports as threat reports into FortiSOAR. A schedule named `Ingestion_fortinet-fortiguard-threat-intelligence_report` is embedded within this playbook, automatically triggering  the ingestion of FortiGuard reports daily at 12:00 AM. 
    - **Link or Create CVEs**: This playbook is triggered when a Threat Intel Report is created and it identifies and correlates CVEs from the CVE module. If no matching CVE is found, it searches NIST, creates a new CVE record, and correlates it.
    - **Retrieves MITRE ATT&CK Details**: This playbook retrieves MITRE ATT&CK Techniques from the FortiSOAR MITRE ATT&CK Techniques module for the FortiGuard threat Report and correlates them.
- Updated the **Configure Threat Feed Configuration Wizard** playbook to include a new step that triggers the “Ingest Known Exploited Vulnerabilities (KEV) CVEs” schedule.
- Removed the deprecated **Get Known Exploited Vulnerabilities (KEV) CVEs > Retrieves CVE Details from NIST** playbook.

---

Take advantage of these updates to simplify and elevate your threat intelligence workflow.