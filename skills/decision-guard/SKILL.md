---
name: decision-guard
description: Checks a plan against the decisions your team has already made, before any code changes. Use at the start of a change to architecture, data storage, APIs, dependencies, release process or anything else a team may have settled. Requires the Decision Guard MCP server.
---

# Decision Guard

Before you change code, find out whether your team has already decided against it.

## Before you edit anything

1. Write your plan in one or two sentences. Name what you would change and what it would replace.
2. Call `check-proposal` with that plan.
3. Act on the `verdict`:

| Verdict | What to do |
|---|---|
| `CONFLICT` | Stop and change nothing. Tell the user which decision conflicts, who made it and when, why it was made, and the source link. Ask whether to follow the decision or have the team reopen it. Continue only if the user says it has been reopened. |
| `NO_CONFLICT_FOUND` | Continue. Mention any `related` decisions that are worth knowing. |
| `NOTHING_TO_COMPARE` | Continue, and tell the user that no decisions are recorded yet. |
| `CHECK_FAILED` | Tell the user the check did not complete. A failed check is not approval. |

## Answering questions

When the user asks what was decided about a subject, call `search-decisions` and answer with the decision, the reason and the source.

## Setup

A site admin installs Decision Guard in Jira and turns on **Expose tools to MCP-compatible apps** under **Apps > Sites > your site > Connected apps > Decision Guard**. Then connect your tool to:

```
https://mcp.atlassian.com/forge/6ff73a50-5ddf-41b3-bf7d-d208c99e702a
```

Some clients add a prefix or suffix to tool names. Look for names containing `check-proposal` and `search-decisions`.
