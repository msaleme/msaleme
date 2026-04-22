---
description: Morning command-center brief — calendar, inbox, GitHub activity in one page
argument-hint: "[optional: date, defaults to today]"
---

# Morning command center

Produce a single one-page brief for Michael covering what happened overnight and what matters today. Keep it scannable.

## Inputs to pull (in parallel where possible)
1. **Calendar** — use `list_calendars` then `list_events` for today's events across all calendars. Note any prep needed, any conflicts, any >30-min blocks.
2. **Email** — `search_threads` for `in:inbox newer_than:1d -category:promotions -category:social`. Pull thread subjects + senders; read full bodies only for the ones that look urgent/important.
3. **GitHub** — for these repos: `msaleme/red-team-blue-team-agent-fabric`, `msaleme/agent-fabric-oilgas-apis`, `msaleme/energy-field-service-integration`, `msaleme/SharePointVectors`, and `msaleme/msaleme` — pull:
   - New issues opened in last 24h
   - PRs opened/updated in last 24h
   - New stars/forks if visible via recent events
   - Failing CI on main

## Output format (exactly this structure)

```
# Morning brief — {date}

## Today's calendar
- {time} — {title} ({duration}). {one-line prep note if needed}

## Urgent (act today)
- {what} — {why urgent} — {who/where}

## Inbox highlights (last 24h)
- {sender}: {1-line summary} → {suggested action}

## GitHub activity
- {repo}: {what changed}

## Decisions waiting
- {decision} — {context in one sentence}

## Nothing-but-noise (skipped)
{count} promotional/social emails, {count} routine notifications.
```

## Guardrails
- Max 1 page. If a section is empty, write "nothing" — don't pad.
- Don't draft replies here. That's `/lead-followup`'s job.
- Flag anything Michael should do in <2 hours as "Urgent".
- If you lack access to any source (e.g., no GitHub token), note it explicitly at the bottom.
