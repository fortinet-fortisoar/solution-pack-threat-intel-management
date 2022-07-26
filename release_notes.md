# What's New

The STIX endpoint to fetch datasets from a FortiSOAR instance has been enhanced to provide the list of feeds in a CSV format as well. With this change, systems such as FortiGate can directly pull threat intel via a FortiSOAR dataset.

## Threat Intel Feed Enhancements

The **Threat Intel Feeds** module better tracks the date and time at which the feeds were ingested or updated into the FortiSOAR instance.

- The Threat Intel Feeds module has now been made **Trackable**
  - Enabling the **Trackable** checkbox makes the following fields available in the feed management grid:
      - Created On
      - Created By
      - Modified On
      - Modified By
- Earlier, the time of creation of feeds at the intel source was labelled as *Created*. To avoid ambiguity with the *Created On* field, the field label *Created* has been renamed to *Created at Source*
- For similar reasons, the field label *Modified* has been renamed to *Modified at Source*

## Dashboard Enhancements

- All default dashboard components, like *Feeds Ingested*, now reflect statistics for Threat Intel Feeds ingested in the *Last 15 days*
- *Active Feeds* is now renamed to *Ingestion Volume*

## Bugfixes

- **Get Total Item Count**, under **Threat Intel Management** > **Threat Feeds**, now displays the item count when clicked
- The query to get Linked Indicators now filters the relevant linked indicators
