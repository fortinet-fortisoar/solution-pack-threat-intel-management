| [Home](../README.md) |
|----------------------|

# TAXII Server Integration

## Using Data from a TAXII Server Feed

Enable TAXII in **Feed Configurations > TAXII Server**.

### TAXII Server Details

- Server Address: `https://[server_address]/api/taxii/1/`
- Discovery: `https://[server_address]/api/taxii/1/taxii`
- Auth: API Key (recommended), custom headers, or basic auth.

### Endpoints

- List datasets: `/api/taxii/1/collections`
- Get dataset: `/api/taxii/1/collections/<datasetId>`
- List feeds: `/api/taxii/1/collections/<datasetId>/objects`
- Get feed details: `/api/taxii/1/collections/<datasetId>/objects/<objectId>`

### Consuming Data

1. Authenticate (API Key recommended).
2. List datasets.
3. Retrieve dataset and feed objects.
4. Consume as needed.

See [Authentication API Guide](https://docs.fortinet.com/document/fortisoar/7.6.1/api-guide/846127/overview#Authentication).

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|