---
name: local-rank-check
description: Check where the connected business ranks in Google Maps local search across a grid around its location, and explain the results. Use when the user asks about local rankings, map pack position, local SEO visibility, or how they rank for a keyword nearby.
---

# Local ranking check

1. Call `list_ranking_analyses`. If one for the same keyword finished in the last 7 days, use it instead of starting a new one.
2. To start a new analysis, confirm the keyword and radius with the user first (default radius 5 km). `start_ranking_analysis` uses Google API quota and needs Full access.
3. The analysis takes a few minutes. Poll `get_ranking_analysis` at sensible intervals and report progress, or tell the user to come back later.
4. When it is complete, report:
   - Average rank where the business was found, and the share of grid points where it is in the top 3.
   - Which directions or areas are strong and which are weak.
   - Three practical actions, for example review velocity, posts that mention the weak areas, or profile completeness.
5. Do not guess competitor names or ranks; only report what the analysis returned.
