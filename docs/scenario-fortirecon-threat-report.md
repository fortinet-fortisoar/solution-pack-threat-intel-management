| [Home](../README.md) |
|----------------------|

# FortiRecon Integration

TIM integrates with **FortiRecon ACI** to ingest reports. The following scenario helps generate a threat intel report based on example data from **FortiRecon ACI**.

### Scenario - Threat Intel Report

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/usage.md) to understand how to simulate and reset scenarios.

To understand the process FortiSOAR follows to ingest threat reports from threat intel providers, we have included a scenario &mdash; **Threat Intel Report** with this solution pack. 

1. 

- Demo report with Technical Intelligence source category.
- Indicators extracted and correlated with feeds.
- Adversaries linked with MITRE ATT&CK groups, techniques, sub-techniques.

![Threat Intel Report](./res/threat-intel-report.png)

### Ingesting Reports

1. Install TIM solution pack ([Installation](./setup.md#installation)).
2. Configure FortiRecon ACI connector. Refer to [FortiRecon ACI](https://docs.fortinet.com/fortisoar/connectors/fortirecon-aci) connector documentation for details.
3. Configure data ingestion through FortiRecon ACI.
4. Access ingested reports in **Threat Reports** tab.
5. Explore report details, correlations, and linked indicators.

# Next Steps

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
|-----------------------------------------|-------------------------------------------|---------------------------|