# Phishing Email Response Solution Pack

## Release Information
- Solution Pack Version: 1.0.0
- FortiSOAR™ Version Tested on: 7.2.0
- Authored By: Fortinet
- Certified: Yes

## Overview
### Introduction
*Phishing Email Response Solution Pack* is designed to provide a set of investigation and utility playbooks to respond to suspicous emails. These emails are typically reported by employees in the organization (sent to a SOC common email inbox).

Configure Email ingestion using Connectors such as Microsoft Exchange. Ingestion process creates an alert of type 'Suspicious Email', and then triggers the response workflow.

Refer to Simulation Scenarios - Phishing Email to experience the use case without any email configuration.

### Usage 

This Solution Pack ships with following simulation scenarios. [Refer](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to Simulate Scenario documentation to undersand how to Simulate and Reset Scenario.

#### 1. Scenario: Phishing Email

The scenario generate a demo alert of Type 'Suspicious Email'.

Goto genrated alert and observe the following:

- Reported Information (sender, email message) is presented as a handy reference
- Suspicious email information (sender, receiver, subject, body, header, sender domain, etc) is presented for analyzing the case.


#### 2. Scenario: Email (Manual Upload) - Investigate
Using this scenario Analyst can generate the 'Suspicious Email' alert by manually uploading the email file (*.eml or *.msg).

The genertated 'Suspicious Email' alert launch "Email (Manual Upload) - Investigate" playbook which will extract email metadata from uploaded email file and map with alert fields.

Goto genertated alert and observe the following:
- Reported Email contains original email as msg/eml attachment
- Reported Information (sender, email message) is presented as a handy reference
- Suspicious email information (sender, receiver, subject, body, header, sender domain, etc) is presented for analyzing the case

**Investigate Suspicious Email**:  Launch "Investigate Suspicious Email" Playbook and observe various investigation activities such as
- Spoofing (by checking sender and return path)
- Blacklisted Keyword match (bitcoin in this case)

## Prerequisites
**Solution Pack Name**|**Purpose**|**Doc Link**|
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
    
    **SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Investigate Suspicious Email|Investigates an alert of type ‘Suspicious Email’|
    |2|Email (Manual Upload) - Investigate|This playbook will extract email metadata from uploaded email file e.g. mail.eml or mail.msg|
    |3|Email (Manual Attach) - File to Alert (Suspicious Email)|This playbook allows to attach an email to alert of type suspicious email and investigates|
    |4|Email (Manual Upload) - Extract Attachments|This playbook will extract attachments, create indicators and link to parent alert|
    |5|Generate Phishing Email Alert|Generate a Phishing Email alert|

    **Warning:** It is recommended to clone these Playbooks before any customizations to avoid loss of information while upgrading the Solution Pack.