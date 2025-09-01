| [Home](../README.md) |
|----------------------|

# Examples

## Export CSV Fields to FortiGate

FortiGate accepts CSVs containing only the `value` field.

### Create a Dataset

Steps to add a dataset: [Create a Dataset](./feeds.md#threat-intel-feed).

![Add Dataset](./res/threat-feeds-add-dataset.png)

### Configure Feeds

Enable **Outgoing Feed** under **Feed Configurations**.

- Copy dataset CSV endpoint URL.
- Append `$__selectFields=value` to restrict fields.

### Import in FortiGate

1. Log in to FortiGate.
2. Go to **Security Fabric > External Connectors**.
3. Create new Threat Feed connector.
4. Use CSV endpoint URL with FortiSOAR credentials.
5. Set refresh rate and enable.

![FortiGate config](./res/fortigate-new-external-connector.png)

### View Entries

Check **View Entries** in FortiGate connector to confirm imported values.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|