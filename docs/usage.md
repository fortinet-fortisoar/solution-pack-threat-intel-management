| [Home](https://github.com/fortinet-fortisoar/solution-pack-threat-intel-management/blob/develop/README.md) |
|--------------------------------------------|

# Usage

The FortiSOAR's new **Threat Intel Management Solution Pack** brings the SOAR and TIM worlds closer by introducing advanced Threat Intel Management capabilities within the SOAR platform. Refer to the following video to witness how this integration greatly simplifies investigations by bringing in contextual threat intel.

https://www.youtube.com/watch?v=vTvtHQxniVU

## Threat Feed Management and FortiGuard Integration

Using comprehensive, ingestion-friendly feed integrations for multiple paid and open-source third-party feeds (available in FortiSOAR Content Hub), threat intelligence teams can now ingest varied feed data and manage them in a normalized, single pane of glass using the 'Threat Feeds' Module. The solution provides multiple ways to  manage this volume of data by parameters such as feed & source confidence, TLP, Severity, Expiry/Age, etc. Additionally, the solution allows to create feed datasets to filter and group relevant feeds for use in sharing, exporting, or eventually as useful data reference while creating contextual threat intelligence. 

Another big value addition of the solution is its comprehensive integration with FortiGuard, Fortinet’s flagship threat intelligence source. As part of FortiSOAR TIM Solution, you get unlimited lookups into the rich FortiGuard threat intel database and an ability to ingest its valuable daily threat intelligence feed. In the 'Preview' mode, you can ingest a maximum of 100 feeds daily.

## Collaborative Framework To Create & Consume Actionable Threat Intelligence

Both Incident response teams and organization members in and outside the SOC (executives, stakeholders, management) can raise Priority Intelligence Requirement (PIR) requests, that drive threat intelligence-gathering efforts. The process starts with – any SOC member raising a PIR with "*I need more information around this area/problem/artifact/actor, etc*", followed by the SOC/threat intel team setting up Workspaces in the Framework. A workspace is a goal-driven canvas that allows teams to dive into different phases of the threat intelligence lifecycle (direction, data collection, processing, analysis, dissemination, and feedback) to curate and share the process outcome with the stakeholder who asked for information. Threat feeds and datasets, MITRE ATT&CK Framework’s rich actor (tactics, techniques, tools, etc.) information and integration fuels FortiSOAR's automation engine, and FortiSOAR's multi-dimensional correlation framework, forms a great combination of the right data sources and tools to start one’s research. 

## Sharing Threat Intelligence

The ability to generate and share the threat intelligence report with stakeholders enables making research actionable. A feedback loop is incorporated into the process to ensure the research meets the expected outcomes and allows for a dialogue between the request initiator (PIR owner) and the research team for getting close to the goal. 

Additionally, the solution allows sharing of threat feeds and datasets over standard STIX/TAXII protocols for getting them across to products that can benefit from these threat feeds and datasets. For example, you can set up a TAXII server in FortiSOAR to broadcast relevant malicious and high confidence feed datasets to a SIEM product such as Fortinet FortiSIEM, that will eventually use them to enhance detection rules and lookup watchlists. These datasets could also be sent using different integrations to update specific watchlists in these products.

## Indicators to Feed Relationships

The solution is intelligent to auto-link malicious feeds with good confidence (configurable) with an indicator in the product and if asked for, also update the indicator reputation. Such built-in intelligent workflows allow consumption of the feed intelligence and enhance the quality of daily investigations. There are several other handles, configurations, and options provided to manage the relationship between indicators and feeds in terms of the feed confidence, sightings, similarities, and other parameters. 


## Threat Intel Management Flow

Once the TIM solution pack is installed, you must configure your threat intelligence feeds connectors such as Fortinet FortiGuard Threat Intelligence, Anomali Limo Threat Intel Feed, Cisco Talos Feed, MITRE ATT&CK, etc. based on your requirements, and then start ingesting data from these sources. For information on how to configure feed connectors, see the connector documentation on the [FortiSOAR Connectors](https://docs.fortinet.com/fortisoar/connectors) page.

### Dashboards

Once you have set up data ingestion and are ingesting feeds from various sources, click **Threat Intel Management** in the left navigation to view the `Dashboard` page:  
![Threat Intel Management left-navigation collapsed view](res/tim-dashboard-collapsed.png)

The `Dashboard` provides you with insights into the ROI, effectiveness of ingestion, ingestion rates of feeds, how many observables were ingested, how many of the ingested observables got linked to indicators, relevance of the feed sources, etc. These metrics enable you to decide which threat feeds are worth monitoring and the performance of the various threat feeds.

### Threat Feed Management

Using a wide variety of Feed integrations that are available on the 'Content Hub', you can seamlessly ingest feeds and get a normalized and aggregated view of the feeds on the **Threat Feeds** tab:  
![Threat Feeds tab](res/threat-feeds.png)

Threat Feeds solution is well architected to handle scale at one end and effectively manage feeds at the other. You can manage feeds with the help of parameters such as feed sources, their confidence, TLPs, expiry, etc.

The noise associated with the feeds is the main hurdle with managing feeds and with deriving utility from the feeds, therefore, as a first-level of filtration, the TIM solution allows you to create 'Datasets'. To view datasets, click the **Manage Datasets** arrow to view the created datasets or to add new datasets:  
![Threat Feeds datasets](res/threat-feeds-dataset.png)

For example, let's look at the Covid-related feeds dataset. In the covid-related feeds, you can apply the first-level filtration, by choosing some tags that are of interest, and also specify the confidence level of over 60. This filtration would eliminate those feeds that do not contain the specified tag and whose confidence level is lesser than 60, thereby helping to eliminate some of the noise:  
![Threat Feeds- Defining datasets](res/threat-feeds-dataset-covid.png)

Similarly, you can create multiple datasets based on your goals or filtration requirements, and use them while you are creating actionable threat intelligence. 

### Threat Intelligence Workflow 

The **Threat Intelligence** tab is the cornerstone of the TIM solution as alone threat feeds can often prove to be a burden on the threat intelligence team and analysts when there is no clear picture of what to consume and what to leave. On the Threat Intelligence tab you can create and consume actionable and contextual threat intelligence:  
![Threat Intelligence Page](res/threat-intel-pg.png)

A quick example of creating a threat intelligence workflow can be a management request to the threat intelligence team for information on a particular threat actor group, for example, APT 34 in the Middle East and the Telecom sector. Once the threat intelligence team gets this request, they can create a 'Workspace' in the **Recent TIM Workspaces** section as follows:   
![APT 34 Middle East workspace](res/workspaces.png)

As you can see the threat intelligence team has defined a workspace APT in MiddleEast (Telecom). The 'Workspace' contains a **Source PIR** section in which the PIR is linked automatically and in which the threat intelligence team can add more contributors allowing for comprehensive research. Also, the Workspace is split into various phases aligned to the Threat Intelligence Lifecycle, where the first stage is collecting and processing data, followed by analyzing the data, and then finally sharing the actionable insights to the stakeholders using reports, etc.

On the **Collection & Processing** tab, you can use the datasets that you have created or you can add new datasets in the **Workspace Datasets** section. You can add or link a variety of correlations feed from the MITRE ATT&CK intelligence Framework around its techniques, sub-techniques, tools, etc, or can be associated with vulnerabilities, indicators, notes, etc.  
![Collection and Processing tab](res/workspace-datasets.png)

After you have collected the data, you can start analyzing the data on the **Analysis & Production** tab, where you look at how various components are correlated, etc. You can also jot down your finding in **Notes**:  
![Analysis and Production tab](res/workspace-analyzes.png)

If you have a wider team to do analyzes, you also have **Task Management** available, using which you can assign tasks to various team members  
![Task Management](res/workspace-task-management.png)

Once you are done with your analysis, you move on to the **Dissemination & Feedback** tab, where you can share your findings with a larger audience.  
![Dissemination and Feedback tab](res/share-tab.png)

You can generate a threat summary report of your finding by clicking the **Generate Threat Summary Report** button:  
![Generate Threat Summary Report popup](res/geneate-threat-summary-report.png)

In the Generate Threat Summary Report popup, you can choose various options such as adding a comment to the Workspace and PIR with the report attached for feedback, updating the PIR task status to 'Awaiting Feedback', and you can also assign the task back to the person who raised the request for feedback. Clicking **Generate Threat Intel Summary Report** generates the report and sends it to the team members. This also starts the feedback loop, which if actionable, leads to improvement in the detection rules, or other areas of improvement.

There are other ways in which threat intelligence teams interact with Workspaces'. For example, there can be a request to the threat intelligence team from the management to monitor all alerts that contain 'Covid' correlations and provide threat intelligence insights related to these correlations. Now, if the team receives the following 'Phishing' alert that contains 'Covid' correlations:  
![Phishing alert](res/phishing.png)

Now, for this phishing alert, the team requires to get more intelligence around the URL in the 'Covid' correlation that does not contain reputation information (`No Reputation Available`) from the standard enrichment sources. So then, you can select that correlation and click **Execute** and choose the **Raise Priority Intelligence Requirement Request (PIR)** playbook:  
![Raising a PIR](res/raise-pir.png)

Clicking  **Raise Priority Intelligence Requirement Request (PIR)**  displays a  **Raise Priority Intelligence Requirement Request (PIR)**  popup, in which you can specify the details of the PIR and then click Submit PIR Request To Threat Intel Team. This in turn submits the PIR to the threat intelligence team and they create the required workspace such as 'Investigatecovidreporting.com'. Next, the threat intelligence team can start investigating the URL, find related IPs, run whois analysis, etc., and then add all the relevant items and sent this information back to the 'Firewall' team, which starts the feedback loop and dialog between teams, making detection and prevention more effective.

### Feed Configurations

On the **Feed Configurations** tab, on the **General** tab, you can configure the feed confidence threshold to automatically update the matching indicator record reputation. In this case, the reputation of an indicator that has a matching feed gets automatically updated with the reputation of the feed, provided the confidence of the feed is equal or above to the value specified in the Selected Feed Confidence Threshold field (70% in our example):  
![Feed Configurations - General tab](res/general.png)

On the **Outgoing Feed** tab, you can configure standard ways to share threat feeds data, by clicking Enable on the Outgoing Feed tab and then configure a TAXII server so that any other platform having STIX/TAXII capabilities can consume this data:  
![Feed Configurations - Outgoing Feed tab](res/feed-config.png) 

Apart from this, you can also use standard ways to export a CSV file so that other tools can import and use the filtered threat intelligence data.  

## Additional Resources

### Videos

To view a video demonstration for the Threat Intelligence Management solution click [here](https://www.youtube.com/watch?v=vTvtHQxniVU).
