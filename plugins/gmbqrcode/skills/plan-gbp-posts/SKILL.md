---
name: plan-gbp-posts
description: Plan and draft Google Business Profile posts for the connected business, and schedule them when asked. Use when the user wants post ideas, a content calendar, a month of GBP posts, or help writing an update, offer or announcement post.
---

# Plan Google Business Profile posts

1. Call `get_business_profile` for services, industry, location and tone.
2. Call `list_gmb_posts` (limit 50) to see recent topics. Do not repeat a topic posted in the last 30 days.
3. Ask how many posts and over what period only if the user has not said. Default to 8 posts over 4 weeks.
4. Write each post:
   - 100 to 300 words, plain text, no hashtags, no emoji walls.
   - Lead with the benefit to the customer and mention the service and the city or area naturally.
   - One clear call to action.
   - Never claim prices, awards, guarantees or offers the user has not given you.
5. Show the plan as a list (date, topic, full text) and wait for approval or edits.
6. Save approved posts with `create_gmb_post_draft`. Drafts stay in GMBQrcode and never reach Google.
7. Only if the user asks, schedule drafts with `schedule_gmb_post`. Publish immediately with `publish_gmb_post` only on an explicit request, because that goes live on Google at once.
8. Finish with the saved draft ids and where to review them: the GMBQrcode dashboard, under Posts.
