<div align="center">

# LLM API Gateway for Coding Agents

**One key. Both protocols. Pay as you go — and your credit never expires.**

A hosted gateway for Claude Code, Codex CLI, and OpenAI-SDK tools: point two environment variables at it and every AI coding tool routes through one endpoint, one balance, one per-request cost ledger.

[Get started](https://teapotrouter.com/en/register) · [Pricing (public, machine-readable)](https://teapotrouter.com/api/pricing) · [Docs](https://teapotrouter.com/en/docs)

</div>

---

## Why a gateway for coding agents?

If you run Claude Code next to OpenAI-SDK tools, you know the drill: every tool wants its own endpoint and key, and the bill is a monthly black box.

A gateway fixes the plumbing:

| | Direct (per vendor) | Via a gateway |
|---|---|---|
| Endpoints & keys | one per vendor | **one key, two protocols** |
| Billing | N dashboards, monthly totals | one balance, **per-request ledger** |
| Cost visibility | "it was $84" | "that session cost $6.20, 78% of it re-sent context" |
| Terms | per-vendor policy | here: **credit never expires**, refunds by remaining balance |

## Setup: two environment variables

```bash
# Claude Code (Anthropic protocol)
export ANTHROPIC_BASE_URL="https://api.teapotrouter.com"
export ANTHROPIC_AUTH_TOKEN="sk-your-key"

# OpenAI SDK / Codex CLI — same key, /v1 endpoint
# base_url = https://api.teapotrouter.com/v1
```

Full step-by-step guides (registration → first request → troubleshooting): [teapotrouter.com/en/docs](https://teapotrouter.com/en/docs)

## What's on the site

- **Public pricing** — every model's base rate and what you actually pay, plus a login-free JSON endpoint (`/api/pricing`) you can script against
- **Per-model pricing pages** — e.g. [claude-opus-5-5](https://teapotrouter.com/en/pricing/claude-opus-5-5)
- **A Claude Code pricing guide** — subscription vs pay-as-you-go vs gateway, with the actual cost math: [docs](https://teapotrouter.com/en/docs/claude-code-pricing)
- **Troubleshooting guide** — connection, 401, and quota errors matched to fixes: [docs](https://teapotrouter.com/en/docs/claude-code-troubleshooting)

## Two questions you should ask any gateway (including this one)

- **Where do the models come from?** Official/authorized API channels, metered and paid per use. No account sharing, no subscription resale.
- **What gets logged?** Billing metadata only (model, tokens, cost, latency) — that's what makes the per-request ledger work. We don't do "zero-log" theater; we just don't touch conversation content.

## Honest limits

Solo-built, launched recently, no marketing budget — the pricing endpoint always shows the live model list, so verify rather than trust this README. Multi-upstream failover is built in; a gateway is still a dependency, keep a fallback path.

---

<div align="center">

Named after HTTP status code 418 "I'm a teapot" 🫖 — [the full story](https://teapotrouter.com/en/418)

**[Teapot Router](https://teapotrouter.com/en)** — stability-first AI gateway for Claude Code and GPT.

</div>
