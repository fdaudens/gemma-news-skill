---
name: news-briefing
description: Fetch the latest news headlines from The New York Times. Supports filtering by topic.
metadata:
  homepage: https://mizal.ai
---

# News Briefing

## Instructions

When the user asks for news, headlines, or a news briefing, call the `run_js` tool with the following exact parameters:

- script name: index.html
- data: A JSON string with the following fields:
  - topic: Optional. A keyword to filter headlines by (e.g., "technology", "politics", "health", "sports"). If omitted, top/general news is fetched.
  - limit: Optional. Maximum number of headlines to fetch. Defaults to 5.

After receiving the result, present the news to the user in a clear, conversational summary. For each headline, mention the title, a brief description if available, and the link. Highlight the most interesting or important stories first.

**Examples of user queries that should trigger this skill:**
- "What's in the news today?"
- "News briefing on politics"
- "What are the top stories from NYTimes?"
- "Give me the latest New York Times headlines"
