---
name: review-replies
description: Draft and publish replies to Google reviews for the connected business. Use when the user asks to reply to reviews, handle new or unanswered reviews, respond to a bad review, or clear their review backlog.
---

# Reply to Google reviews

1. Call `get_business_profile` for the business name, services and `preferredTone`. Write every reply in that tone.
2. Call `list_google_reviews` (limit 50). Work only on reviews with no reply unless the user names a specific review.
3. Draft one reply per review:
   - Thank the reviewer by first name when one is given, and refer to something specific they wrote.
   - 5 and 4 stars: warm and short, two or three sentences.
   - 3 stars or lower: acknowledge the problem without arguing, apologise where it fits, and invite them to continue offline. Never admit legal fault or offer refunds or discounts the user has not approved.
   - Never invent facts about the business, staff names or policies. Never include phone numbers or emails unless they are in the profile.
   - Match the review's language.
4. Show all drafts in one list: reviewer, stars, a short quote of the review, then the draft.
5. Publish only the replies the user explicitly approves, one `publish_review_reply` call each. A reply goes live on Google immediately.
6. If publishing fails with a scope error, tell the user the connection has Read only or Read + drafts access, and that they can reconnect with Full access to publish replies.
