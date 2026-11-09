# Decision Guard

Stops your team and its AI agents from quietly reversing decisions.

Decision Guard is an Atlassian Forge app for Jira, Confluence and Rovo. It records what your team has already decided, warns when a new Jira issue would contradict one of those decisions, and lets AI coding tools check a plan over MCP before they change code.

This repository holds the public parts of the project: the agent skill, the privacy policy and the support channel.

## Use it from an AI coding tool

1. A site admin installs Decision Guard in Jira, then opens **Apps > Sites > your site > Connected apps > Decision Guard** and selects **Expose tools to MCP-compatible apps**.
2. Add this MCP server to your tool and sign in with your Atlassian account:

   ```
   https://mcp.atlassian.com/forge/6ff73a50-5ddf-41b3-bf7d-d208c99e702a
   ```

3. Add [skills/decision-guard/SKILL.md](skills/decision-guard/SKILL.md) to your tool, so it checks with your team's decisions before it writes code.

The MCP server exposes two read-only tools, `check-proposal` and `search-decisions`. An outside tool can read the decision register but cannot change it. Every call runs with the permissions of the person who signed in.

## Support

Open an issue: <https://github.com/z2667278827/decision-guard/issues>

## Privacy

See [PRIVACY.md](PRIVACY.md).

## License

The skill and documents in this repository are available under the [MIT License](LICENSE).
