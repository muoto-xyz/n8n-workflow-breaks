# A webhook that refuses every call in “MENTION---On-Mention-Handler”, fixed by the team the same day

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “MENTION---On-Mention-Handler”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “Webhook Trigger” does not wait for the Respond to Webhook node after it

Its “Respond” option is “Immediately”, and a Respond to Webhook node follows it. n8n refuses every call to it at run time with “Unused Respond to Webhook node found in the workflow”. Set “Respond” to “Using 'Respond to Webhook' Node”.

## The team's two commits

- **The change, 15 January 2026.** [Merge pull request #248 from fsebbah/feat/rfc007-mention-service-workflows](https://github.com/fsebbah/n8n-workflows/commit/383520f1701c7bd17cd7a23ee9cf0c847f938a71) `383520f`
- **The fix, 15 January 2026.** [Merge pull request #249 from fsebbah/fix/rfc007-workflows-best-practices](https://github.com/fsebbah/n8n-workflows/commit/8a76ae33d1d0cf789d37f8e4ca038571d7a45484) `8a76ae3`

The workflow's file is `workflows/MENTION---On-Mention-Handler.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under fsebbah/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
