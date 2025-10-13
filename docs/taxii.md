| [Home](../README.md) |
|----------------------|

## Using Data from a TAXII Server Feed

This section explains how to use data from a TAXII server's feed to retrieve threat intelligence.

Enable the TAXII server from **Threat Intel Management** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> **Threat Indicators** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> **Feed Configurations** <picture><source media="(prefers-color-scheme: dark)" srcset="./res/icon-chevron-light.svg"><source media="(prefers-color-scheme: light)" srcset="./res/icon-chevron-dark.svg"><img alt="Fallback image description" src="./res/icon-chevron-dark.svg"></picture> **TAXII Server** tab.

![Enable TAXII Server](./res/feed-config.png)

### TAXII Server Details

The following details appear after you enable the TAXII server:

- **Server Address**:
  *`https://[server_address]/api/taxii/1/`*

- **Server Discovery Address**:
  *`https://[server_address]/api/taxii/1/taxii`*

- **Authentication**:
  Use one of the following methods to authenticate your API requests:

  1. **API Key Authentication (Recommended)**
     Use the API Key as described in the *Authentication API Guide*.

  2. **Custom Headers**
     If the tool does not support custom headers, use the following credentials:
     - Username: *`X-API-KEY-[api_key_name]`*
     - Password: *`[api-key]`*

  3. **Basic Authentication**
     Use the username and password combination or include the credentials directly in the server address:
     *`https://[username]:[password]@[server_address]/api/taxii/1/`*

For more information on authentication and data usage, refer to the [*Authentication API Guide*](https://docs.fortinet.com/document/fortisoar/7.6.1/api-guide/846127/overview#Authentication).

> [!Note]
> The basic authentication URL cannot be used directly in a browser. It must be used in a tool or script that supports such authentication methods.

### Available Endpoints

The TAXII server provides the following endpoints to access datasets and feeds:

- **List all datasets**
  Endpoint: `/api/taxii/1/collections`

- **Get dataset details**
  Endpoint: `/api/taxii/1/collections/<datasetId>`

- **List threat feeds in a dataset**
  Endpoint: `/api/taxii/1/collections/<datasetId>/objects`

- **Get details of a specific feed object**
  Endpoint: `/api/taxii/1/collections/<datasetId>/objects/<objectId>`

### Consuming Data from Datasets

To access and consume data from multiple datasets:
1. Authenticate with the TAXII server using the recommended API Key authentication.
2. Use the `/collections` endpoint to list all available datasets.
3. Retrieve dataset details and list objects in a dataset using the appropriate endpoints.
4. Evaluate and consume threat intelligence data according to your organization's requirements.

> [!TIP]
> Refer to this [example](./example.md) that helps export CSV fields to FortiGate using Threat Intel Management's TAXII server.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|
