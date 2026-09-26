# A webhook that refuses every call in “GUILD - Student Verify”, fixed by the team 6 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “GUILD - Student Verify”, and a later commit of its own repaired the break that change made. The break lived 6 days. Run on the first change, the check says:

### “Webhook” does not wait for the Respond to Webhook node after it

Its “Respond” option is “Immediately”, and a Respond to Webhook node follows it. n8n refuses every call to it at run time with “Unused Respond to Webhook node found in the workflow”. Set “Respond” to “Using 'Respond to Webhook' Node”.

## The team's two commits

- **The change, 10 April 2026.** [Merge pull request #332 from fsebbah/feat/rfc-061-implement-workflows](https://github.com/fsebbah/n8n-workflows/commit/863f761909d2c6e7c27eb290e756a2289e0c5a00) `863f761`
- **The fix, 16 April 2026.** [Merge pull request #335 from fsebbah/fix/webhook-response-mode-missing](https://github.com/fsebbah/n8n-workflows/commit/00b39cc2ad0b2498f11ea3b45a69be9b7ecdb13e) `00b39cc`

The workflow's file is `workflows/GUILD_-_Student_Verify.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-4a75726a](https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-4a75726a?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
