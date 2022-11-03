# What's New

- With FortiSOAR v7.3.0 and FortiGuard Connector v1.1.0, the solution pack now enables support for Threat Intel Management SKU.
    - Enable the Threat Intel Management SKU for best-in-class FortiGuard's threat intel feeds.
    - The feeds from Threat Intel Management SKU have a rich variety of data, ranging from IPs, URLs, Domain and malicious hashes carefully curated by our team of experts.
    - The entire feeds database is labelled with the relevant threat types, and associated LockHeed Martin Kill Chain Phases, that enables user with a lot of contextual information to understand the nature of threat.

- With added support for the FortiGuard Feeds, the **Preview** label has been removed from the Solution Pack.

# Known Issues

- Data ingestion, with MalSilo v2.0.0 and older, may fail after an upgrade to FortiSOAR v7.3.0.

As a workaround you may perform the following steps:

1. Login to FortiSOAR.
2. Click **Automation** > **Data Ingestion**.
3. Click **MalSilo** connector from the list to view details in a tabular view.
4. Click **Playbooks** under the actions column.
5. Open the playbook **> MalSilo > Create**.
5. Double-click to open the **Create Record** playbook step.
6. Change the expression in the **Expires On** field to the following
    
    ```
    {{arrow.get(vars.item.Lastseen).shift(years=0, months=0, weeks=0, days=vars.input.params.expiry, hours=0, minutes=0, seconds=0).int_timestamp}}
    ```

7. Click the button **Save Playbook** to save the changes. 
