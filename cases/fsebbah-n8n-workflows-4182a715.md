# A step that can never run in “N8N - Intent Events Consumer”, fixed by the team the same day

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “N8N - Intent Events Consumer”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “Redis DLQ” can never run

No trigger leads to it.

## The team's two commits

- **The change, 9 February 2026.** [Merge pull request #291 from fsebbah/feature/285-intent-events-consumer](https://github.com/fsebbah/n8n-workflows/commit/dc361465c03210732c5d650ccb820ab37e287955) `dc36146`
- **The fix, 9 February 2026.** [Merge pull request #296 from fsebbah/fix/285-consumer-error-handling](https://github.com/fsebbah/n8n-workflows/commit/984e85cd6dd512c4c4cb5b4eb71660317b0edc6a) `984e85c`

The workflow's file is `workflows/N8N-Intent-Events-Consumer.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under fsebbah/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
