| [Home](../README.md) |
|----------------------|

# Threat Feeds

Using a wide variety of feed integrations that are available on the [Content Hub](https://fortisoar.contenthub.fortinet.com//list.html?contentType=all), you can seamlessly ingest feeds and get a normalized and aggregated view of the feeds on the **Threat Feeds** tab.

Navigate to  <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intel-management-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intel-management-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intel-management-dark.svg"></picture> **Threat Intel Management** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intelligence-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intelligence-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intelligence-dark.svg"></picture> **Intelligence**:

![](./res/threat-feeds.png)

## Feed Configurations

The **Feed Configurations** tab contains settings for easy feed management and dissemination. It has the following tabs:

- **Feed Sources**: Directs you to a Content Hub page that lists and helps install connectors that can fetch threat intel feeds.

- **TAXII Server**: broadcast datasets. For more information, refer [Setting up a TAXII Server](./taxii.md#setting-up-a-taxii-server).

- **Threat Feed Rules**: Helps manage incoming threat feeds through rules. For more information, refer to the [Configuring Feed Rules](./setup.md#configuring-feed-rules).

### Importing Feeds from Files

1. Enable the option **Ingest Threat Feeds From Files** under **Feed Configurations** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> **Ingest Unstructured Threat Feeds** and click **Save**.

2. In the left navigation pane, go to <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intel-management-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intel-management-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intel-management-dark.svg"></picture> **Threat Intelligence** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-threat-intelligence-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-threat-intelligence-dark.svg"><img alt="Fallback image description" src="./res/icon-threat-intelligence-dark.svg"></picture> **Hub**.

3. Click the **Threat Feeds** Tab.

4. Click the button **Upload Unstructured Feeds**.

    ![](./res/upload-unstructured-feeds-from-files.png)

5. Under **File to Import**, click the box to browse and upload the file. Supported file formats are `csv`, `txt`, `pdf`, `eml`, `json`, and `xlsx`.

6. **Confidence**: Specify the confidence score to assign to the ingested unstructured threat feeds.

7. **Reputation**: Select the reputation to assign to the ingested unstructured threat feeds.

8. **TLP**: Select the TLP to assign to the ingested unstructured threat feeds.

9. **Feed Expiry**: Specify the number of days after which the ingested unstructured threat feeds are marked as expired for deletion.

10. **Feed Source**: Specify a value to be updated as Source for all ingested unstructured threat feeds.

11. **Tags**: Specify comma-separated values to be assigned as tags to the ingested unstructured threat feeds.

12. Select the option **Automatic Block IOC** to block threat feeds immediately on ingestion. Leave unchecked to manually block threat feeds later.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
