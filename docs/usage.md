| [Home](https://github.com/fortinet-fortisoar/solution-pack-phishing-email-response/blob/develop/README.md) |
|--------------------------------------------|

# Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to understand how to simulate and reset scenarios.

To understand the process FortiSOAR follows to respond to phishing emails, we have included a scenario &mdash; **Phishing Email Response** with this solution pack. Refer to the section *Phishing Email Scenario* to understand how this solution pack's automation addresses your needs.

## Phishing Email Scenario
This scenario generates an example alert of Type *Suspicious Email* in FortiSOAR's **Alerts** module.

Navigate to the demo alert and note the following:

- The demo alert created is an example of a default email ingestion using the **Data Ingestion** feature
- Alert fields are mapped with information from the email, such as sender email id, reporter email id, and attachments
- Users can execute investigation playbook, out-of-the-box (OOB), against the alert **Investigate Suspicious Email**. It utilizes email information (sender, receiver, subject, body, header, and sender domain) for analyzing the case and suggesting corrective action.

## Manual Email Upload

This playbook adds the option **Attach Email**, under **Execute**, to alerts of type *Suspicious Email*. Using this option, users can attach an email file in `.eml` or `.msg` format, to the alert. 

The playbook, on creation of the alert, extracts metadata from the uploaded email file and maps that metadata with alerts' fields.

Navigate to generated alert and note the following:
- Attached  Email, if it contains an attachment, its extracted and then correlated as an indicator 
- Alert fields are mapped with information from email, such as sender email Id, reporter email Id, and attachment &ndash; if any
- Execution of investigation playbook, out-of-the-box (OOB), against alert **Investigate Suspicious Email**, utilizes email information (sender, receiver, subject, body, header, and sender domain) for analyzing the case and suggesting remediation action.

**Investigating Suspicious Email**: Users can launch **Investigate Suspicious Email** playbook from an alert. This playbook performs following automated tasks:

- Send an email acknowledging the reporter, of the suspicious email, about ongoing investigation 
- Perform spoofing and SPF checks
- Check for a particular keyword (configurable in playbook)
- If URL indicators are found, it prompts user to mark this phishing attempt as **Drive by Download**. User gets more information about URLs
- User is prompted to review and receives a suggestion to block malicious indicators
- Playbook finally sends out a message, to reporter of the suspicious email, with aninvestigation summary
