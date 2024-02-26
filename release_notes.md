# What's New

## Playbook Enhancements

### Investigate Suspicious Email

- The playbook becomes visible and executable only for unresolved alerts of the type **_Suspicious Email_**.

- *Suspicious Email* alerts found to be malicious (*true positive*) now have the **Email Classification** as *`Phishing`*.

- *Manual Input* steps have refined descriptions to enhance understanding.

    - A manual input, triggered by this playbook, displays the investigation summary and asks the users if the investigated alert is *`Phishing`* or *`False Positive`*.

- The *Comments* have been improved for better readability and clarity.

### Generate Phishing Email Alert

- This playbook has been renamed to **Scenario - Generate Phishing Email Alert**.

- Optimized the field mapping values on the sample record created.

### URL > Remote Screenshot > Create and Link Attachment

- A new playbook that captures screenshots of URL indicators, creates attachment records, and links them to the respective alert.

    - For this, a new playbook **URL > Remote Screenshot > Get URL Screenshot** is triggered to capture screenshots of URL indicators linked to an alert of type **_Suspicious Email_**.