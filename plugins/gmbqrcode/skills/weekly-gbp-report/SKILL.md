---
name: weekly-gbp-report
description: Build a performance report for the connected Google Business Profile covering views, searches, calls, website clicks, direction requests, reviews and posts. Use when the user asks how their business profile is doing, wants a weekly or monthly report, or asks about GBP traffic or insights.
---

# Google Business Profile report

Default to the last 7 days compared with the 7 days before. Use the period the user names if they give one.

1. Call `get_business_profile` for the business name and to confirm `googleConnected`. If it is false, stop and tell the user to connect Google in the GMBQrcode dashboard.
2. Call `get_gbp_performance` once covering both periods, so the comparison uses the same data.
3. Call `list_google_reviews` and count new reviews, average rating and unanswered reviews in the period.
4. Call `list_gmb_posts` with status `published` and count posts in the period.
5. Write the report:
   - One-line headline: the single biggest change.
   - A table of each metric: this period, previous period, change in percent.
   - Reviews: new count, average stars, how many still need a reply.
   - Posts: how many went out.
   - Three concrete next actions based on the numbers, for example replying to unanswered reviews or posting more often.
6. State which dates each period covers. Google reports performance with a delay of a few days, so say so if the last days are empty.
