---
description: Weekly one-page product brief for the security harness
argument-hint: "[optional: week ending date, defaults to today]"
---

# Weekly product brief

Generate a one-page product health report for Michael's security harness work. Focus area: `msaleme/red-team-blue-team-agent-fabric` and the `agent-security-harness` PyPI package.

## Data to pull (last 7 days)

For `msaleme/red-team-blue-team-agent-fabric`:
- Issues opened, closed, still open (with labels if any)
- PRs opened, merged, closed-without-merge
- Releases tagged this week (with release notes)
- Commit count on main, notable commits
- Star/fork deltas if discernible from activity
- CI status on main (green / failing / which workflow)

For supporting repos (`msaleme/agent-fabric-oilgas-apis`, `msaleme/energy-field-service-integration`, `msaleme/SharePointVectors`): only note if there's meaningful activity (≥1 PR merged or release). Otherwise skip.

## Output format

```
# Weekly product brief — week ending {date}

## Headline
{one sentence: what's the single most important thing that happened?}

## Ship log
- {commit/PR/release} — {impact}

## Test & module deltas
- Tests: {N → M} ({+/-delta})
- Modules: {N → M}
- Pass rate: {if visible}

## Inbound signal
- Issues opened: {count} — themes: {1-2 bullets}
- Feature requests: {list if any}
- Bug reports: {list if any}
- Stars/forks: {delta if visible}

## Open risks
- {failing CI, stale PRs >7d, unresolved P0 issues}

## Next week's wedge
- {1-3 specific things to ship or decide, based on what's queued}
```

## Guardrails
- Use the GitHub MCP tools or `gh` CLI. Do NOT fabricate numbers — if you can't find a stat, say "not available".
- One page. No preamble, no conclusion paragraph.
- If nothing shipped this week, say so plainly.
