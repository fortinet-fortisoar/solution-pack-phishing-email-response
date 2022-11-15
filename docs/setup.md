| [Home](../README.md) |
|----------------------|

# Installation

1. To install a solution pack, click **Content Hub** > **Discover**.   
2. From the list of solution pack that appears, search for and select **Phishing Email Response**.    
3. Click the **Phishing Email Response** solution pack card.   
4. Click the **Install** button on the bottom to begin installation.

## Prerequisites

The **Phishing Email Response** solution pack depends on the following solution packs that are installed automatically &ndash; if not already installed.

| **Solution Pack Name** | **Purpose**                                              |
|:-----------------------|:---------------------------------------------------------|
| SOAR Framework         | Required for Incident Response modules                   |
| SOC Simulator          | Required for Scenario Module and SOC Simulator connector |

# Configuration

For optimal performance of **Phishing Email Response** solution pack, you must configure:

- Threat intelligence connectors to enrich context of a given indicator
    - To configure and use the VirusTotal connector as a source of threat intelligence, refer to [Configuring Virus Total](https://docs.fortinet.com/document/fortisoar/2.1.0/virustotal/166/virustotal-v2-1-0#Configuration_parameters)
- An email ingestion process to periodically read email from a designated inbox and convert them into alerts in FortiSOAR
    - To configure and use the Microsoft Exchange connector for email ingestion, refer to [Configuring Exchange Connector](https://docs.fortinet.com/document/fortisoar/3.4.0/exchange/1/exchange-v3-4-0#Configuring_the_connector)
