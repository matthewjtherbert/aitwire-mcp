# AITWIRE — Gemini CLI / Antigravity extension

Two AITWIRE MCP servers in one extension:

| Server | Endpoint | Sign-in | What it answers |
|---|---|---|---|
| `aitwire` | `https://api.aitwire.com/mcp` | none | What has *this business* published about itself? |
| `aitwire-account` | `https://api.aitwire.com/mcp/tenant` | OAuth | What are AI systems saying about *me*, and what should I do? |

## ⚠️ Gemini CLI was retired on 2026-06-18

Google [retired the standalone Gemini CLI](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/)
for free, Google AI Pro and Ultra users on **18 June 2026**, replacing it with
**Antigravity CLI**. Access continues unchanged on a **Gemini Code Assist
Standard or Enterprise** licence.

So this extension still works, but for a narrowing audience:

- **Gemini Code Assist Standard / Enterprise** — `gemini extensions install` as before.
- **Antigravity CLI** — extensions carry over as plugins. The setup flow offers
  to import existing Gemini CLI extensions, or import manually with
  `agy plugin import`. MCP configuration lives in `mcp_config.json` rather than
  the main settings file.
- **Everyone else** — Gemini CLI no longer serves requests. Add AITWIRE
  directly in whichever assistant you use; see https://aitwire.com/docs/mcp.

## Install

```bash
gemini extensions install https://github.com/matthewjtherbert/aitwire-mcp
```

(The repo is `aitwire-mcp` because GitHub repo names are case-insensitive and
`aitwire` collides with the main `AITWIRE` repository.)

The public `aitwire` server needs no account or API key. The `aitwire-account`
server opens an AITWIRE sign-in the first time it is used — the CLI discovers
the OAuth configuration from the server and registers itself, so there is no
client id or secret to configure. If you have no AITWIRE account, leave that
server disabled and the public tools work on their own.

## What your account tools can do

Every AITWIRE plan connects, and what your AI may do grows with the plan:
reading your measurements and facts at the base, drafting corrections for your
approval above that, and your competitive picture plus publishing-on-approval
higher still. Your assistant will only be offered the tools your plan holds.

Nothing publishes without your approval, and the plan and credit tools mint a
checkout link rather than charging anything — you complete any payment in your
own browser.

## What's inside

- `gemini-extension.json` — points at both remote AITWIRE MCP servers
  (streamable HTTP; no local process).
- `GEMINI.md` — context telling the model which server answers which question,
  how to attribute results by source and confirmation date, and to confirm
  before anything that writes or publishes.

Docs: https://aitwire.com/docs/mcp · Privacy: https://aitwire.com/privacy · Terms: https://aitwire.com/terms
