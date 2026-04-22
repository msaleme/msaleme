---
description: Scan AI agent security competitors for changes, flag what matters
argument-hint: "[optional: lookback days, defaults to 7]"
---

# Competitor launch watcher

Scan the AI agent security landscape for new releases, blog posts, papers, or standards activity. Flag what changes Michael's positioning or roadmap.

## Watch list (edit `routines/competitors.yml` to change)

Load targets from `routines/competitors.yml`. Each entry has a name, category, and one or more URLs (blog, changelog, releases, RSS).

If the file doesn't exist, use these defaults and note that you're using defaults:

- **Invariant Labs** — https://invariantlabs.ai/blog
- **Lakera** — https://www.lakera.ai/blog
- **Protect AI** — https://protectai.com/blog
- **Robust Intelligence** — https://www.robustintelligence.com/blog
- **HiddenLayer** — https://hiddenlayer.com/blog
- **Anthropic (policy/safety posts only)** — https://www.anthropic.com/news
- **NIST AI** — https://www.nist.gov/artificial-intelligence
- **OWASP LLM Top 10** — https://genai.owasp.org/
- **MITRE ATLAS** — https://atlas.mitre.org/
- **MCP spec** — https://github.com/modelcontextprotocol/specification/releases

## Steps

1. For each target, fetch the page with WebFetch (or curl in CI).
2. Compare content against `routines/.competitor-cache/{slug}.txt` if it exists. Write the new snapshot to the cache regardless.
3. For each changed target, extract what's new: title, date, 1-sentence summary, URL.
4. For each change, answer three questions in <=2 sentences each:
   - **So what for positioning?** (Does this narrow/broaden Michael's WHO-vs-HOW angle? Does it overlap with the harness's MCP/A2A/L402/x402 coverage?)
   - **So what for roadmap?** (Should the harness add/adjust a test module? Is there a paper response?)
   - **Action?** (None / note / draft response / add to roadmap.)

## Output format

```
# Competitor watch — {date} (lookback: {N} days)

## Changed this cycle
### {Competitor} — {what}
{1-sentence summary + URL}
- Positioning: {...}
- Roadmap: {...}
- Action: {...}

## No change
{Competitor A}, {Competitor B}, ... (one line, comma-separated)

## Landscape note (optional)
{only if there's a pattern across 2+ competitors worth calling out}
```

## Guardrails
- If nothing changed, output ONE line: "No changes across {N} tracked sources — {date}." Nothing more.
- Never invent posts you didn't actually fetch.
- Rate-limit: if a fetch fails, note it and continue. Don't retry indefinitely.
