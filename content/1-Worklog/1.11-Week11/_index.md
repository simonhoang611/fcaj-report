---
title: "Week 11 Worklog"
date: 2026-09-14
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Release the official v1.0.0 with the team; write Workshop chapter 5.4 (sales flow).
* Build the admin product management feature, including uploading product images to S3.
* Prepare the v1.0.1 bug-fix release and publish the FCAJ internship report site on GitHub Pages.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                     | Start Date | Completion Date | Reference Material                                                                                                                                                         |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **The team releases the official v1.0.0** <br> - Write Workshop chapter 5.4 (sales flow) and deploy a separate copy of the shop on AWS to take step-by-step screenshots                                                                                | 23/11/2026 | 23/11/2026      | <https://testing-library.com/docs/dom-testing-library/api-async/>                                                                                                          |
| 3   | - Finish Workshop chapter 5.4: 24 screenshots, a sales flow diagram and a cost table                                                                                                                                                                     | 24/11/2026 | 24/11/2026      |                                                                                                                                                                            |
| 4   | - Build the admin product management feature (add from a template, edit, hide, restorable delete): <br>&emsp; + Analysis and screen design <br>&emsp; + API, list page, add/edit page <br> - Fix wrong specs for 2 laptops in the sample data            | 25/11/2026 | 25/11/2026      |                                                                                                                                                                            |
| 5   | - Let admins upload product images from their computer: <br>&emsp; + The browser uploads straight to S3 with a presigned URL valid for 5 minutes <br>&emsp; + Restricted file types and a 3 MB maximum <br>&emsp; + Images are served through CloudFront | 26/11/2026 | 26/11/2026      | <https://docs.aws.amazon.com/AmazonS3/latest/API/> <br> <https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html> |
| 6   | - Write the checklist for the v1.0.1 bug-fix release (new product content, ordering, cancellation, forgot password) <br> - Redesign the header and add a "New arrivals" page <br> - Publish the FCAJ internship report site on GitHub Pages              | 27/11/2026 | 27/11/2026      | <https://hcm-rules.awsfcaj.com/project#hinh-thuc>                                                                                                                          |


### Week 11 Achievements:

* Released v1.0.0, the official version of shop-ai, with the team.

* Finished Workshop chapter 5.4 (sales flow):
  * 24 screenshots from a separately deployed shop on AWS
  * Sales flow diagram
  * Cost table

* Admin product management:
  * Add from a template, edit, hide, restorable delete
  * Upload images straight to S3 with a 5-minute presigned URL, max 3 MB
  * Images served through CloudFront

* Have a checklist for v1.0.1; a new header and a "New arrivals" page; the FCAJ internship report site is live on GitHub Pages.
