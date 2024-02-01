| [Home](../README.md) |
|----------------------|
# Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/usage.md) to understand how to simulate and reset scenarios.

To understand the process FortiSOAR follows to respond to phishing emails, we have included a scenario &mdash; **Phishing Email Response** with this solution pack. 

This solution pack includes a playbook that you can launch manually from the alerts page. This playbook performs the following automated tasks:

- Send an email acknowledging the reporter, of the suspicious email, about the ongoing investigation 
- Perform spoofing and SPF checks
- Check for a particular keyword (configurable in the playbook)
- If indicators of type URL are found, it prompts the user to mark this phishing attempt as **Drive by Download**. The user gets more information about URLs
- User is prompted to review provided investigation summary to determine if the alert is a valid phishing alert or a false positive.
- User is prompted to review and receives a suggestion to block malicious indicators
- Sends out a message, to the reporter of the suspicious email, with an investigation summary
- Playbook finally prompts user to either Continue with investigation keeping alert open or close the alert

Refer to the sections *Phishing Email Scenario*, *Get URL Screenshots* and *Manual Email Upload* to understand how this solution pack's automation addresses your needs.

## Phishing Email Scenario
This scenario generates an example alert of type *Suspicious Email*.

Navigate to the demo alert and note the following:

- The demo alert created is an example of a default email ingestion using the **Data Ingestion** feature
- Alert fields are mapped with information from the email, such as sender email id, reporter email id, and attachments

## Manual Email Upload

This section addresses the requirement of an email that has to be manually uploaded for further investigation. An alert of type *Suspicious Email* must be present for the **Execute** button to display the playbook &ndash; **Attach Email** &ndash; from the playbook collection **02 - Use Case - Phishing Email Response**.

When executed, this playbook prompts you to attach an email file in `.eml` or `.msg` format, to the alert.

>**NOTE**: To see this playbook **Attach Email** in action, first create an alert of type *Suspicious Email*.

When executed, this playbook prompts you to attach an email file in `.eml` or `.msg` format, to the alert.

As soon as the upload is complete, the enrichment process starts. A notification informs that the indicators are being enriched. Once the enrichment completes, navigate to generated alert and note the following:
- Attached  Email, if it contains an attachment, its extracted and then correlated as an indicator 
- Alert fields are mapped with information from the email, such as sender email Id, reporter email Id, and attachment &ndash; if any

## Get URLs Screenshots
This section addresses the functionality to capture screenshot of the URLs that correlated to the alert of type *Suspicious Email*

To execute this playbook, click on the **Execute** button and select `Get URL Screenshot`. 
- This will capture screenshot of all the URLs indicators associated with the alert using `Remote Screenshot`. 
- The screenshot will be saved as `Attachment` records and get correlated to the alert. Also the comment will be added to collaboration panel listing links of all the Screenshot attachments
>**NOTE**: We recommend setting up the Remote Screenshot connector on the **agent** to securely access URLs.

# Next Steps
| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Contents](./contents.md) |
| ----------------------------------------- | ------------------------------------------- | --------------------------- |