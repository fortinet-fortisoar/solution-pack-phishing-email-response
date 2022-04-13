# Phishing Email Response Solution Pack

## Overview
### Introduction
This article describes the  Phishing Email Response Solution Pack. The solution pack demonstrates the scenarios and use cases around phishing email based on the information provided through email server. 
The scenario demonstrates and generates a demo alert for the Alert Type 'Suspicious Email'.
The use-case deals with containment and investigation procedures once the end-user reports a Suspicious Email using email server.
- Reported Email contained original email as MSG attachment
- Reported Information (sender, email message) is presented as a handy reference
- Suspicious email information (sender, receiver, subject, body, header, sender domain, etc) is presented for analyzing the case
- Investigate Suspicious Playbook is available to demonstrate various investigation activities such as
    - Spoofing (by checking sender and return path)
    - Blacklisted Keyword match (bitcoin in this case)

### Usage 
More information about usage of Phishing Email Response Solution Pack [here](https://github.com/fortinet-fortisoar/solution-pack-phishing-email-response/blob/develop/docs/solution-pack-guide.md).

## Version Information
- Solution Pack Version: 1.0.0
- FortiSOAR™ Version Tested on: 7.2.0
- Authored By: Fortinet
- Certified: Yes

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
    - 02 - Use Case - Phishing Email Response (4): Following is a list of playbooks under “02 - Use Case - Phishing Email Response” solution pack.

    **SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Investigate Suspicious Email|Investigates an alert of type ‘Suspicious Email’|
    |2|Email (Manual Upload) - Investigate|This playbook will extract email metadata from uploaded email file e.g. mail.eml or mail.msg|
    |3|Email (Manual Attach) - File to Alert (Suspicious Email)|This playbook allows to attach an email to alert of type suspicious email and investigates|
    |4|Email (Manual Upload) - Extract Attachments|This playbook will extract attachments, create indicators and link to parent alert|