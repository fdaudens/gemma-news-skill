---
name: news-briefing
description: Fetch the latest news headlines from BBC, NYTimes, and Reuters. Supports filtering by source and topic.
metadata:
  homepage: https://mizal.ai
---

# News Briefing

## Instructions

When the user asks for news, headlines, or a news briefing, call the `run_js` tool with the following exact parameters:

- script name: index.html
- data: A JSON string with the following fields:
  - sources: Optional. An array of source identifiers to fetch from. Valid values are "bbc", "nytimes", "reuters". If omitted, all three sources are fetched.
  - topic: Optional. A keyword to filter headlines by (e.g., "technology", "politics", "health", "sports"). If omitted, top/general news is fetched.
  - limit: Optional. Maximum number of headlines per source. Defaults to 5.

After receiving the result, present the news to the user in a clear, conversational summary. Group headlines by source. For each headline, mention the title, a brief description if available, and the link. Highlight the most interesting or important stories first.

**Examples of user queries that should trigger this skill:**
- "What's in the news today?"
- "Give me the latest BBC headlines"
- "Any tech news from Reuters?"
- "News briefing on politics"
- "What are the top stories from NYTimes?"
