| [Home](../README.md) |
|----------------------|
# Contents

The **Phishing Email Response** solution pack contains the following resources.

## Global Variable

| Name            | Description                                                                                                     |
|:----------------|:----------------------------------------------------------------------------------------------------------------|
| `Default_Email` | This global variable contains the email address which sends an acknowledgment and other emails to the reporter. |

## Record Set

| Name     | Description                                                                                                                                                                                                          |
|:---------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scenario | A simulation that helps you understand the *Phishing Email Response* solution pack by creating a demo phishing email alert. Executing this scenario emulates this solution pack's behavior on receiving such alerts. |

## Playbook Collection

| 02 - Use Case - Phishing Email Response                                  |
|:-------------------------------------------------------------------------|


| Playbook Name                                                          | Description                                                                       |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| Investigate Suspicious Email                                           | Investigates alerts of type *Suspicious Email*                                    |
| Generate Phishing Email Alert                                          | Generates a Phishing Email alert                                                  |
| Email (Manual Upload) - Investigate                                    | Extracts email metadata from an uploaded email file                               |
| Email (Manual Attach) - File to Alert (Suspicious Email)               | Attaches emails to alerts of type *Suspicious Email* and investigates             |
| Email (Manual Upload) - Extract Attachments                            | Extracts attachments, creates indicators, and links to parent alert               |
| URL > FortiSandbox > Enrichment<sup>New</sup>                          | Retrieves the reputation of indicators of type 'URL' using Fortinet FortiSandbox. |

>**Warning:** We recommend you clone these playbooks before customizing to avoid information loss while upgrading the solution pack.