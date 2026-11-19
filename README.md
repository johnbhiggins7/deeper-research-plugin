# Deeper Research for Claude Code

Run deep research from Claude Code: one question goes to several deep-research providers (Parallel, Gemini, Perplexity, Claude and more), and you get each provider's cited report, kept in your [Deeper Research](https://deeperesearch.com) library.

This plugin adds:

- the Deeper Research MCP server (`https://deeperesearch.com/mcp`), with tools to search past research, estimate cost, attach files, start research, wait for it and read reports
- a skill that tells Claude when deep research is worth it, to check your library first and to ask before spending
- `/deeper-research:research <question>`, a shortcut for the whole flow

## Install

```bash
claude plugin marketplace add johnbhiggins7/deeper-research-plugin
claude plugin install deeper-research@deeper-research
```

Then run `/mcp` in Claude Code, pick `deeper-research` and sign in with your Deeper Research account. You choose this agent's spending limits when you sign in, and you can change them or disconnect it any time in [Settings → Connections](https://deeperesearch.com/app/settings/connections).

Prefer not to use a plugin? Add just the server:

```bash
claude mcp add --transport http deeper-research https://deeperesearch.com/mcp
```

## Costs

Searching, estimating and reading reports are free. Starting research uses your Deeper Research credit, at most the `max_cost_usd` the agent sets, and only after it checks with you above your confirmation threshold ($2 by default).

## More

- Setup for Cursor, Codex and other clients: https://deeperesearch.com/docs/mcp
- Privacy: https://deeperesearch.com/legal/privacy
- Terms: https://deeperesearch.com/legal/terms
