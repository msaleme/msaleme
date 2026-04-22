# Scheduled workflow templates

These run the `weekly-product-brief` and `competitor-watch` routines headlessly.

## Why they live here and not in `.github/workflows/`

The automation that generated this branch lacks GitHub App `workflows`
permission. Copy them yourself:

```
mkdir -p .github/workflows
cp routines/workflows/*.yml .github/workflows/
git add .github/workflows/
git commit -m "chore: enable scheduled Claude routines"
git push
```

## One-time setup

1. Add repo secret `ANTHROPIC_API_KEY` (Settings → Secrets and variables → Actions).
2. Confirm the action reference `anthropics/claude-code-action@v1` is current — pin
   to a commit SHA if you want reproducibility.
3. The schedules are in UTC:
   - Weekly brief: Fri 21:00 UTC (≈ 4 PM Chicago CDT / 3 PM CST)
   - Competitor watch: Mon 13:00 UTC (≈ 8 AM Chicago CDT / 7 AM CST)

Both jobs post their output as GitHub issues so you get a notification. The
competitor-watch job also commits snapshot diffs back to `routines/.competitor-cache/`.
