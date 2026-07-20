# AITWIRE — Gemini CLI extension

Connects [Gemini CLI](https://geminicli.com) to the AITWIRE MCP server
(`https://api.aitwire.com/mcp`): look up business-published entity records —
confirmed descriptions, structured feeds, and claim checks, each carrying the
date it was confirmed.

## Install

```bash
gemini extensions install https://github.com/matthewjtherbert/aitwire-mcp
```

(The repo is `aitwire-mcp` because GitHub repo names are case-insensitive and
`aitwire` collides with the main `AITWIRE` repository.)

No account or API key required.

## What's inside

- `gemini-extension.json` — points Gemini CLI at the remote AITWIRE MCP
  server (streamable HTTP; no local process).
- `GEMINI.md` — context that tells the model how to use the three read-only
  tools (`aitwire_entity_lookup`, `aitwire_entity_feeds`, `aitwire_grounding`)
  and to attribute results by source + confirmation date.

Docs: https://aitwire.com/docs/mcp · Privacy: https://aitwire.com/privacy · Terms: https://aitwire.com/terms
