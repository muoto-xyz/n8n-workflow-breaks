# A step that can never run in “Claude - Batch Poller”, fixed by the team 5 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “Claude - Batch Poller”, and a later commit of its own repaired the break that change made. The break lived 5 days. Run on the first change, the check says:

### “Publish to Redis” can never run

No trigger leads to it.

## The team's two commits

- **The change, 15 May 2026.** [feat(workflows): add Redis notification mode for Claude Skills API](https://github.com/fsebbah/n8n-workflows/commit/45f5bfe7bb8759875078cb51d08e00d26e767225) `45f5bfe`
- **The fix, 20 May 2026.** [Merge pull request #361 from fsebbah/feature/redis-xadd-key-endpoints](https://github.com/fsebbah/n8n-workflows/commit/6bfcddba760dada62c8d3581dfb07114c7cd68cc) `6bfcddb`

The workflow's file is `workflows/Claude_-_Batch_Poller.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-d6e78da0](https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-d6e78da0?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
