# What's New

**Changed default FortiGuard ingestion**:

- Changed the way feed records' description is formatted

- Changed default pull interval to 1 day to enhance performance.
    <!-- - The last 7 days worth of feed is large and requires that the default request timeout values for `nginx` and `uwsgi` is tweaked for the first ingestion to complete. -->

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
