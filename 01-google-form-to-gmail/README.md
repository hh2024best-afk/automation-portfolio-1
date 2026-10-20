# Google Form to Gmail Notification

## What it does
Emails the responsible team member when a new enquiry is submitted, helping ensure that potential leads are not overlooked.

## Business problem
Small marketing and creative agencies may receive enquiries through online forms. If staff do not notice new submissions promptly, potential business opportunities may be missed.

## Trigger
A new row appears in the Google Sheet linked to the **New Lead Enquiry** Google Form. The n8n workflow checks this trigger and processes the submission.

## Apps and tools
- Google Forms
- Google Sheets
- n8n
- Gmail

## Workflow
Google Form → Google Sheets → n8n → Gmail notification

## Credentials needed
- Google Sheets OAuth credential
- Gmail OAuth credential

Credentials are stored in the n8n credential store and should not be included in this repository.

## How to test

### Test 1: Complete enquiry
**Input:** Submit the form with all required fields completed.

**Expected result:** An email is sent containing the submitted enquiry details.

**Actual result:** [Record your test result here.]

### Test 2: Company field left blank
**Input:** Submit the form with the Company field blank.

**Expected result:** [Record the expected behavior based on your workflow configuration.]

**Actual result:** [Record what happened during your test.]

## Known limitations
- The Google Sheets trigger uses polling, so notification timing depends on the configured polling interval.
- Duplicate prevention and dedicated error alerts have not yet been implemented.
- Further validation and reliability improvements are planned.

## Security
- OAuth credentials are stored in n8n.
- No passwords, access tokens, or API secrets should be committed to the repository.
- Review exported workflow files and screenshots before sharing them publicly.

## Business value
Reduces manual checking of enquiry spreadsheets and helps the team respond to potential leads more consistently.

## Future improvements
- Add duplicate-lead prevention.
- Add error notifications and logging.
- Validate required enquiry fields.
- Connect the workflow to a CRM.
- Measure notification reliability and response time.