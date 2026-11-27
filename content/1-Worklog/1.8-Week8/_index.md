---
title: "Week 8 Worklog"
date: 2026-09-14
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Review the security of the ordering flow: abuse prevention, IDOR checks, a ZAP baseline scan, tag-based IAM permissions between environments.
* Redesign the product detail page and speed up page loads; release v0.2.0 with the team; publish blog post 1 (05/11).
* Start and finish the order admin page; write a runbook for DynamoDB throttling.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Start Date | Completion Date | Reference Material                                                                                                                                                                                             |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - Review the team's security report and confirm the order abuse protections are in the code: <br>&emsp; + A limit of 3 undelivered orders <br>&emsp; + Blocking access to other people's orders                                                                                                                                                                                                                                                                                               | 02/11/2026 | 02/11/2026      | <https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html>                                                                                                  |
| 3   | - Learn IDOR testing and ZAP baseline scanning, and apply them to the project: <br>&emsp; + Customers cannot view or cancel someone else's order by changing the order ID in the URL <br>&emsp; + Security scan evidence for the report <br> - Start redesigning the product detail page: split into 7 small parts; finished the header that collapses on scroll                                                                                                                              | 03/11/2026 | 03/11/2026      | <https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html> <br> <https://www.zaproxy.org/docs/docker/baseline-scan/>                                        |
| 4   | - Learn tag-based IAM (aws:ResourceTag) so dev Lambdas cannot read prod users, since dev, staging and prod share one AWS account <br> - Finish the new product detail page: a tiled spec table, a spec panel with a table of contents, and a buy box <br> - The web app starts recording products customers view and add to cart so the recommendation system can learn from them                                                                                                             | 04/11/2026 | 04/11/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/access_tags.html> <br> <https://react.dev/reference/react/useLayoutEffect>                                                                                   |
| 5   | - Apply useInfiniteQuery to the "Load more orders" list: customers with many orders still see their history quickly instead of loading everything at once <br> - **The team releases v0.2.0 to production** <br> - Speed up page loads on mobile: self-host the fonts and prefetch product data earlier <br> - Add an item count on the cart icon with a fly-to-cart animation <br> - **Publish blog post 1** about DynamoDB transactions: keeping stock correct when many people buy at once | 05/11/2026 | 05/11/2026      | <https://tanstack.com/query/latest/docs/framework/react/guides/infinite-queries> <br> <https://web.dev/articles/optimize-lcp> <br> <https://tanstack.com/query/latest/docs/framework/react/guides/prefetching> |
| 6   | - Re-measure page speed with Lighthouse: mobile up from about 82 to 97–98, desktop at 100 <br> - Start the order admin page: write the API contract and the backend for admins to view orders and change their status                                                                                                                                                                                                                                                                         | 06/11/2026 | 06/11/2026      | <https://developer.chrome.com/docs/lighthouse/overview?hl=vi>                                                                                                                                                  |
| 7   | - Finish the order admin page: AWS infrastructure, automated tests, screens <br> - Write a runbook for DynamoDB throttling incidents, with monitoring charts                                                                                                                                                                                                                                                                                                                                  | 07/11/2026 | 07/11/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/throttling-diagnosing-workflow.html>                                                                                                         |


### Week 8 Achievements:

* Reviewed the security of the ordering flow:
  * Confirmed the 3-undelivered-order limit and the block on viewing others' orders are in the code
  * IDOR test: changing the order ID in the URL cannot view or cancel someone else's order
  * ZAP baseline scan results as evidence

* Understood tag-based IAM (aws:ResourceTag) to separate permissions between dev, staging and prod sharing one AWS account.

* The new product detail page was finished in 2 days:
  * Header that collapses on scroll
  * Tiled spec table, spec panel with a table of contents, buy box
  * Records viewed and added-to-cart products for the recommendation system

* Released v0.2.0 with the team and sped up the pages:
  * Mobile Lighthouse from about 82 to 97–98, desktop 100
  * Order history loads page by page with useInfiniteQuery
  * Cart icon count and fly-to-cart animation

* Finished the order admin page (API, backend, infrastructure, tests, screens) and a DynamoDB throttling runbook.

* Published blog post 1 about DynamoDB transactions on 05/11.
