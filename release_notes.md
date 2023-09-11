# What's New

**Changed default FortiGuard ingestion**:

- Changed the way feed records' description is formatted

- Changed default pull interval to 1 day to enhance performance.
    <!-- - The last 7 days worth of feed is large and requires that the default request timeout values for `nginx` and `uwsgi` is tweaked for the first ingestion to complete. -->

## Upgrade Instructions for Fortinet FortiGuard Threat Intelligence Connector v3.1.2

> Included with the Threat Intelligence Solution Pack v1.2.1

Upgrade to the latest version may result in playbooks failing. Following steps help remove the connector and upgrade it to the latest version.

1.	Connect to the FortiSOAR&trade; instance's Command Line Interface (CLI).

2.	Delete the FortiGuard connector v3.1.1 directories and files as a `root` user. You may run the following command:

    ```bash
    rm -r /opt/cyops/configs/integrations/connectors/fortinet-fortiguard-threat-intelligence_3_1_1/
    ```

3.	Sync the FortiSOAR&trade; instance with the production repo. You may run the following command as a `root` user:

    ```bash
    csadm package content-hub sync --force
    ```

4.	Login to the FortiSOAR&trade; instance user interface.

5.	Launch the Content Hub from the FortiSOAR&trade; instance.

6.	Search and update the FortiGuard connector to v3.1.2.

## Bug Fixes

- Added missing columns in Threat Intel Report's System View Template (SVT)

- Threat Intel Report's primary details now contain FortiSOAR ID instead of fetched report's ID

## Known Issues

- The following error message may appear during data ingestion:

    ```console
    Error: Process 1046904 waits for ShareLock on transaction 781491; blocked by process 1046907.
    Process 1046907 waits for ShareLock on transaction 781489; blocked by process 1046904.
    HINT:  See server log for query details.
    CONTEXT:  while inserting index tuple (101319,1) in relation "threat_intel_feeds"
    URL: https://localhost/api/ingest-feeds/threat_intel_feeds?$statusOnly=true
    ```

## Resolution

Contact Fortinet support.
