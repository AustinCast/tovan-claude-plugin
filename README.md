# Tovan plugin for Claude Code

Design and order custom electronics from Claude Code. Tovan designs the circuit board, a case that fits and the code that runs on it from a plain-words brief, then has the board made, with parts soldered on, and shipped.

This plugin adds:

- **The Tovan connector** (`.mcp.json`): the MCP server at `https://www.tovan.ai/api/mcp`.
- **The `brief-a-board` skill**: what a good brief contains, which tool to call when, how to poll a build, and how to hand the person the approve link.

## Install

In Claude Code:

```
/plugin marketplace add AustinCast/tovan-claude-plugin
/plugin install tovan@tovan
```

Then type `/mcp` and sign in to Tovan when asked.

To use an API key instead of signing in (create one in Tovan: account menu, then Keys):

```
claude mcp add --transport http tovan https://www.tovan.ai/api/mcp --header "Authorization: Bearer tvn_..."
```

## Try it

> Use Tovan to design a board for this firmware: it should run on 2 AA batteries, fit in a 40 x 80 mm case, and we want 3.

Claude reads your code, writes the brief, starts the board, checks on it every minute, asks you anything Tovan needs, shows you the picture and the requirements, and gives you the approve link when you want it made. You pay by tapping that link; Claude never pays.

## More

- Guide for every assistant: https://www.tovan.ai/for-agents
- API reference: https://www.tovan.ai/docs/api
- Help: austin@tovan.ai
