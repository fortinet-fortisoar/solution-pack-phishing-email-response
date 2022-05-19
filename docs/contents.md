| [Home](https://github.com/fortinet-fortisoar/solution-pack-phishing-email-response/blob/develop/README.md) |
|--------------------------------------------|

# Contents

The **Phishing Email Response** solution pack contains the following resources.

## Global Variable

|**Name**|**Description**|
| :- | :- |
|`Default_Email`| This global variable contains the email address which sends acknowledgement and other emails to the reporter. |

## Record Set

|**Name**|**Description**|
| :- | :- |
|**Scenario - Phishing Email**| A simulation that helps you understand the *Phishing Email Response* solution pack.|

## Playbook Collection

|02 - Use Case - Phishing Email Response (5) |
| :- |

**Playbook Name**|**Description**|
| :- | :- |
|Investigate Suspicious Email|Investigates an alert of type 'Suspicious Email'|
|Email (Manual Upload) - Investigate|This playbook will extract email metadata from uploaded email file e.g. mail.eml or mail.msg|
|Email (Manual Attach) - File to Alert (Suspicious Email)|This playbook allows to attach an email to alert of type suspicious email and investigates|
|Email (Manual Upload) - Extract Attachments|This playbook will extract attachments, create indicators and link to parent alert|
|Generate Phishing Email Alert|Generate a Phishing Email alert|

>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.
