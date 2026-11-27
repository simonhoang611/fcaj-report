---
title: "Week 9 Worklog"
date: 2026-09-14
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Redesign shop-ai's order pages following a 5-part plan, starting with shared UI components.
* Run acceptance and release the v1.0.0-rc.1 release candidate with the team.
* Improve sign-in and build forgot-password with Amazon Cognito; publish blog post 2 about SQS (11/11).

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                                      | Start Date | Completion Date | Reference Material                                                                                                                                                                                      |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Plan the order page redesign in 5 parts <br> - Build the shared UI components first: buttons, status badges, empty states, confirmation dialogs                                                                                                                                                                         | 09/11/2026 | 09/11/2026      |                                                                                                                                                                                                         |
| 3   | - Acceptance testing of release candidate rc.1 on staging: the main flows and page speed all pass                                                                                                                                                                                                                         | 10/11/2026 | 10/11/2026      |                                                                                                                                                                                                         |
| 4   | - Analyse sign-in page improvements (show/hide password button, 6-digit code input) and the forgot-password feature with Amazon Cognito <br> - **Publish blog post 2** about Amazon SQS queues                                                                                                                            | 11/11/2026 | 11/11/2026      | <https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_ConfirmForgotPassword.html> <br> <https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes/autocomplete> |
| 5   | - **The team releases v1.0.0-rc.1** <br> - Finish the forgot-password page <br> - Start the admin order cancellation feature                                                                                                                                                                                              | 12/11/2026 | 12/11/2026      | <https://docs.amplify.aws/react/build-a-backend/auth/manage-users/manage-passwords/>                                                                                                                    |
| 6   | - Compile the 33 new pieces of knowledge applied to the project since the start, each with: <br>&emsp; + What it is <br>&emsp; + What it is for in the project <br>&emsp; + Where it was used (issue and PR numbers) <br>&emsp; + The official source <br> - Check the source links, as the basis for writing the worklog | 13/11/2026 | 13/11/2026      |                                                                                                                                                                                                         |
| 7   | - Attend the Cloud Mastery event at the office to network and listen to knowledge sharing                                                                                                                                                                                                                                 | 14/11/2026 | 14/11/2026      |                                                                                                                                                                                                         |


### Week 9 Achievements:

* Have shared UI components (buttons, status badges, empty states, confirmation dialogs) for the order pages.

* rc.1 acceptance on staging passed for the main flows and page speed; released v1.0.0-rc.1 with the team.

* Improved sign-in with Amazon Cognito:
  * Show/hide password button, 6-digit code input
  * Forgot-password page: receive a code by email and set a new password

* Published blog post 2 about Amazon SQS on 11/11.

* Have a summary of the 33 pieces of knowledge applied to the project, with where each was used and its official source, as the basis for the worklog.

* Attended the Cloud Mastery event, networking and learning from the speakers.
