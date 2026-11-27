---
title: "Week 10 Worklog"
date: 2026-09-14
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Finish the admin order cancellation feature and the account page (change password, change username).
* Build two-factor authentication with an authenticator app and sync sign-in state across tabs; publish blog post 3 about Cognito (19/11).
* Sign off my part for v1.0.0; draw the project's AWS architecture diagram.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                                                                                                                                                              |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Finish the admin order cancellation feature (API, infrastructure, screens): cancelled orders return stock automatically <br> - Fix 2 small UI bugs: wrong button hover colour, missing favicon <br> - Finalise the account page design                                                        | 16/11/2026 | 16/11/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_TransactWriteItems.html>                                                                                                                    |
| 3   | - Build the account page: <br>&emsp; + Customers can change their password and are then signed out on all devices <br>&emsp; + Change username <br>&emsp; + Fix reloading the page sending the user back to sign-in <br> - Learn two-factor authentication with authenticator apps and passkeys | 17/11/2026 | 17/11/2026      | <https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_AdminUserGlobalSignOut.html> <br> <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-mfa-totp.html> |
| 4   | - Write the documentation for the two-factor authentication on/off feature (scan a QR code with Google Authenticator) and open a draft PR for team feedback                                                                                                                                     | 18/11/2026 | 18/11/2026      |                                                                                                                                                                                                                 |
| 5   | - Finish coding two-factor authentication with an On/Off switch <br> - Analyse the bug where an old tab still shows the previous account after another tab switches user <br> - **Publish blog post 3** about Amazon Cognito                                                                    | 19/11/2026 | 19/11/2026      | <https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/status_role> <br> <https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel>                                          |
| 6   | - Finish tabs syncing automatically when the signed-in user changes <br> - Sign off my part for v1.0.0 <br> - Draw the project's AWS architecture diagram in draw.io                                                                                                                            | 20/11/2026 | 20/11/2026      | <https://developer.mozilla.org/en-US/docs/Web/API/Page_Visibility_API> <br> <https://www.youtube.com/watch?v=l8isyDe-GwY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=2>                                       |
| 7   | - Attend AWS Student Community Day Vietnam 2026 at the office to network and listen to knowledge sharing                                                                                                                                                                                        | 21/11/2026 | 21/11/2026      | <https://www.facebook.com/groups/awsstudentbuildergroupvn/posts/4571875389749943>                                                                                                                               |


### Week 10 Achievements:

* Admins can cancel orders; order status and stock are updated in one DynamoDB transaction, so stock is always returned.

* The account page is complete:
  * Change password, then sign out on all devices
  * Change username
  * Reloading no longer sends the user back to sign-in

* Two-factor authentication (TOTP):
  * Scan a QR code with Google Authenticator
  * On/Off switch
  * Wrote the docs and opened a draft PR for team feedback before coding

* Tabs sync automatically when the signed-in user changes, using BroadcastChannel and the Page Visibility API.

* Signed off my part for v1.0.0; drew the project's AWS architecture diagram in draw.io.

* Published blog post 3 about Cognito on 19/11; attended AWS Student Community Day Vietnam 2026.
