## Release Information

- Solution Pack Version: 1.0.0
- Minimum Compatible FortiSOAR™ Version: 7.2.0
- Authored By: Fortinet
- Certified: Yes

## Overview

### Introduction
**Phishing Email Response Solution Pack** is designed to provides a set of investigation playbooks which can be used to respond to suspicious emails.
> Configure Email ingestion using Connectors such as Microsoft Exchange.

### Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to understand how to Simulate and Reset scenarios.

This Solution Pack ships with the following simulation scenarios.

#### 1. Scenario: Phishing Email
This scenario generates an example alert of Type 'Suspicious Email' in FortiSOAR Alerts module.
Navigate to the demo alert and note the following:

- Demo alert created is an example of a default email ingestion using Data Ingestion Feature
- Alert fields are mapped with information from an email, such as sender email id, reporter email id, any attachment, etc.
- User can execute OOB investigation playbook against alert **Investigate Suspicious Email** that utilizes email information (sender, receiver, subject, body, header, sender domain, etc) for analyzing the case and suggesting remediation action.

#### 2. Utility Playbook: Email (Manual Upload) - Investigate

This playbook adds an action to alert of Type "Suspicious Email", which allows user to attach an exported email file, either in .eml or .msg file format to alert. 

The moment above alert is created, the playbook will extract email metadata from uploaded email file and map with alert fields.

Navigate to generated alert and note the following:
- Attached  Email, if it contains an attachment, its extracted and then correlated as IOC 
- Alert field are mapped with information from email, such as sender email Id, reporter email Id, any attachment, etc.
- User can then execute OOB investigation playbook against alert 'Investigate Suspicious Email' that utilizes email information (sender, receiver, subject, body, header, sender domain, etc) is for analyzing the case and suggesting remediation action.

**Investigating Suspicious Email**: User can launch "Investigate Suspicious Email" playbook from an alert. This playbook will perform following automated tasks:

- Sends an email acknowledging reporter of suspicious email about ongoing investigation 
- Performs Spoofing and SPF checks
- Checks for particular keyword (user can configure same in playbook)
- If URL IOCs are found, it prompts user to mark this phishing attempt as **Drive by Download**. User gets more information about URLs
- User is again prompted to review and then s suggestion to block malicious IOCs is presented
- Playbook finally sends out an acknowledgement to reporter of suspicious email with investigation summary

## Prerequisites

|**Solution Pack Name**|**Purpose**|**Doc Link**|
| :- | :- | :- |
|SOAR Framework 1.0.0|Require for Incident Response modules|[Click here](https://github.com/fortinet-fortisoar/solution-pack-soar-framework/blob/develop/README.md)|
|SOC Simulator 1.0.1|Require for Scenario Module and SOC Simulator connector| [Click here](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/README.md)|

## Contents

1. Global Variable(s)
    - Default_Email
2. Record Set(s)
    - Scenario: Phishing Email
3. Playbook Collection(s)
    - 02 - Use Case - Phishing Email Response (5):

    |**SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Investigate Suspicious Email|Investigates an alert of type 'Suspicious Email'|
    |2|Email (Manual Upload) - Investigate|This playbook will extract email metadata from uploaded email file e.g. mail.eml or mail.msg|
    |3|Email (Manual Attach) - File to Alert (Suspicious Email)|This playbook allows to attach an email to alert of type suspicious email and investigates|
    |4|Email (Manual Upload) - Extract Attachments|This playbook will extract attachments, create indicators and link to parent alert|
    |5|Generate Phishing Email Alert|Generate a Phishing Email alert|

     **Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.
