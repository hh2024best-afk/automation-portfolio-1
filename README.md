
## 1. What It Does

This automation sends an email notification to the team whenever a new lead enquiry is submitted through Google Forms. It helps the team respond to potential clients promptly and reduces the risk of missing new enquiries.

## 2. Business Problem

Small marketing and creative agencies receive enquiries from potential clients through online forms. When staff must check submissions manually, leads may be overlooked or receive delayed responses.

This automation helps solve that problem by notifying the responsible team member when a new enquiry is received.

## 3. Workflow Architecture

Google Form → Google Sheets → n8n → Gmail → Team Notification

## 4. Trigger

A new row is added to the Google Sheet connected to the Google Form named "New Lead Enquiry".

The n8n workflow detects the new row and starts the email notification process.

## 5. Tools Used

- Google Forms — collects lead enquiries.
- Google Sheets — stores submitted enquiry data.
- n8n — processes the new submission and runs the workflow.
- Gmail — sends the notification email to the responsible team member.

## 6. Credentials and Security

Google Sheets and Gmail connections are configured in n8n using the appropriate credentials.

Credentials should be stored securely and must not be included in workflow exports, public GitHub repositories, or documentation.

Before sharing or publishing workflow files, inspect them for exposed credentials and confidential information.

## 7. How to Test

### Test 1: Normal Submission

1. Open the Google Form.
2. Submit a test enquiry with all required fields completed.
3. Confirm that the submission appears in Google Sheets.
4. Confirm that the n8n workflow processes the new row.
5. Check Gmail for the notification email.
6. Verify that the email contains the expected enquiry details.

Expected result: The team receives an email containing the submitted lead information.

### Test 2: Missing Information

1. Submit a test enquiry with the Company field left blank, if the form allows it.
2. Observe how Google Sheets and n8n handle the missing value.
3. Check whether the email is sent and how the missing information appears.

Expected result: Record the actual behavior observed during testing. Do not assume missing-field validation is implemented unless it has been tested.

## 8. Known Limitations

- Email delivery depends on the workflow configuration and the Google Sheets trigger polling interval.
- Duplicate prevention has not yet been confirmed.
- Automated error notifications have not yet been confirmed.
- Lead qualification and CRM integration are not included in this version.

These features can be considered for future improvements.

## 9. Business Value

This automation helps a small agency:

- Reduce manual monitoring of incoming enquiries.
- Notify the responsible team member when a new lead arrives.
- Improve the consistency of lead handling.
- Create a foundation for future lead qualification, follow-up, CRM updates, and appointment booking.

## 10. Future Improvements

- Add input validation for required lead information.
- Prevent duplicate notifications.
- Add error handling and failure alerts.
- Connect the workflow to a CRM such as GoHighLevel.
- Add automated lead qualification and follow-up.

## 11. Project Status

Project: Practice automation — Week 1, Day 1

Status: Initial workflow built and tested; further testing and security review are part of the project documentation.

Tools: Google Forms, Google Sheets, n8n, and Gmail.
