# A connection to a node that does not exist in “LT Proteros: SMS Booking Agent”, fixed by the team the same day

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “LT Proteros: SMS Booking Agent”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### An edge joins “Is Valid SMS?” to “Forward to Dashboard Log”, which is not in the graph

The graph has no node named “Forward to Dashboard Log”.

## The team's two commits

- **The change, 26 March 2026.** [fix: call Render API directly instead of self-referential webhook (#366)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/3064ffac18a7d0873abb1e49bdbaa30392b0d318) `3064ffa`
- **The fix, 26 March 2026.** [fix: align connection names with renamed dashboard log node (#367)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/f727749e81b198e31498126f639dd1f6d96d359f) `f727749`

The workflow's file is `n8n/workflows/LT_Proteros/lt-sms-booking-agent.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-a82fa655](https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-a82fa655?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
