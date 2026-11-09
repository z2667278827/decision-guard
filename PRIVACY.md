# Decision Guard privacy policy

Last updated: 9 November 2026

Decision Guard is built and maintained by Ryan Labs. It runs entirely on Atlassian Forge, inside the Atlassian site where it is installed.

## What the app reads

- The summary and description of Jira issues, when they are created or changed.
- Confluence pages in spaces the app has been added to. Pages with read restrictions, including inherited ones, are skipped.
- Jira comments, only if a site admin turns on learning from comments. Comments with restricted visibility, and issues with a security level, are skipped.

## What the app stores

The app uses Forge hosted storage in your site. It stores:

- Decisions: the statement, the reason, alternatives considered, topics, the date, a supporting quote and a link to the source. If the source names who decided, that name is stored as it was written.
- The Atlassian account ID of a person who records a decision or challenges one.
- Check results for each Jira issue, including how your team resolved a conflict.
- App settings, counters and markers showing which page versions have been read.

Because account IDs are kept for longer than 24 hours, the app declares to Atlassian that it stores personal data.

## Where the data goes

- The app makes no calls to services outside Atlassian. It declares no external network access.
- AI processing uses Forge LLMs, which run on the Atlassian platform.
- Ryan Labs does not sell your data and does not receive your content. Error logs can contain technical details such as a Jira issue key, a Confluence page ID or an error message.

## How long it is kept

Data stays in Forge hosted storage while the app is installed. A site admin can retire a decision at any time. After the app is uninstalled, the data is handled under Atlassian's retention rules for Forge hosted storage.

## Contact

Questions and requests: <https://github.com/z2667278827/decision-guard/issues>
