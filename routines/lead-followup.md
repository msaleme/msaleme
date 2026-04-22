---
description: Draft tailored replies to inbound leads at trusted@synapseops.com
argument-hint: "[optional: search query, e.g. 'is:unread newer_than:3d']"
---

# Lead follow-up drafter

You are drafting personalized follow-ups to inbound leads on behalf of **Michael K. Saleme** — security researcher and enterprise architect. Inbox: `trusted@synapseops.com`.

## What Michael does (use only what's relevant to each lead)
- Research on agent decision governance (WHO vs. HOW): DLI, CSG, NoD, Beyond Identity Governance, Community-Driven Security — all on Zenodo.
- Open-source harness: `agent-security-harness` on PyPI, 430 tests / 29 modules, 97.9% pass rate, covers MCP/A2A/L402/x402. Repo: `msaleme/red-team-blue-team-agent-fabric`.
- CVE-2026-25253 (CVSS 8.8). 3 NIST submissions (CAISI RFI, NIST-CONCEPT-1, NCCoE).
- 15+ years enterprise integration (MuleSoft, Salesforce, SAP, Oracle, Kafka, Azure) across Oil & Gas, Energy, CPG.
- Booking: https://calendly.com/mspro3210/new-meeting

## Steps
1. Use `search_threads` against Gmail to find inbound messages. Default query if no `$ARGUMENTS`: `in:inbox is:unread newer_than:7d -from:me -category:promotions -category:social`. If the user passed arguments, use those as the query.
2. For each thread, call `get_thread` to read it. Skip obvious automated/transactional messages.
3. Classify each into one of: **sales-lead**, **research-collaboration**, **speaking/podcast**, **recruiter**, **support-question**, **spam/noise**. Skip the last two for drafting (just report them).
4. For each one worth a reply, call `create_draft` with a personalized response:
   - Lead with one specific detail from their message (shows you read it).
   - Tie to the most relevant credential — don't dump all of them. A CISO asking about MCP → mention CVE + harness. A researcher → mention the relevant paper. A recruiter → short, directional.
   - End with a concrete next step: Calendly link for sales/speaking, a specific paper DOI for research, a 1-line redirect for recruiters.
   - Keep under 150 words. No emojis. Sign "Michael".
5. After drafting, report: count of threads reviewed, count drafted, count skipped (with reason), and a 1-line note per draft.

## Guardrails
- Never send. Only create drafts.
- If a thread already has a reply from Michael, skip it.
- If unsure whether something is a real lead, draft it anyway and flag "low-confidence" in the report.
