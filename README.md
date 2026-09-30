# Talent Summoner for Claude

Talent Summoner is an AI recruiting product that sources candidates for a role. This plugin connects Claude to your Talent Summoner account so you can run the whole sourcing workflow from a conversation: describe a role, review the ideal candidate profile (ICP) it drafts, search for candidates, shortlist the ones you like, and look up their work emails.

## What's included

- **MCP server**: the Talent Summoner remote server at `https://talentsummoner.com/api/mcp`. You sign in with your Talent Summoner account the first time Claude uses it.
- **Skill** (`talent-summoner`): teaches Claude the sourcing workflow, how to wait for long-running searches, and when it must ask you before spending a paid Role.

## Tools

| Tool | What it does | Changes data? |
| --- | --- | --- |
| `sourcing_read` | Read a session, or list your sessions | No |
| `sourcing_start` | Start a new sourcing session from a role brief | Creates a session |
| `sourcing_continue` | Send a message: edit or approve the ICP, search, find more, refine, draft outreach | Yes |
| `sourcing_review` | Mark a candidate liked, shortlisted or skipped | Yes |
| `sourcing_contact` | Look up a candidate's work email | Yes |
| `sourcing_stop` | Stop the running search; finished work stays saved | Yes |
| `sourcing_unlock_role` | Spend one paid Role on a session | Yes, uses a paid Role |

## Example prompts

- "Find senior product designers in London with B2B SaaS experience."
- "Make fintech experience optional, then search."
- "Shortlist the top three and find their work emails."
- "Show my Talent Summoner sourcing sessions."

## Costs and consent

Searching and evaluating candidates uses your Talent Summoner plan: a free preview, a paid Role, or a subscription. Claude spends a paid Role only after you agree. Prices are shown on [talentsummoner.com/pricing](https://talentsummoner.com/pricing). Outreach is only drafted from Claude; you review and send messages in the Talent Summoner app.

## Data and privacy

This plugin sends your requests (role briefs, messages, review decisions) to Talent Summoner at `talentsummoner.com` and nothing else. Talent Summoner processes them with its own search, AI and email-lookup providers. The plugin runs no local code, hooks or scripts. Candidate contact details stay masked unless your access allows them.

- Privacy policy: https://talentsummoner.com/privacy
- Terms: https://talentsummoner.com/terms
- Disconnect Claude at any time in Talent Summoner under **Settings → Connected apps**.

## Support

Visit https://talentsummoner.com or contact the Talent Summoner team from the app.

## License

MIT. See [LICENSE](LICENSE).
