# A field read that is never produced in “GUILD - Credits Expire Cron”, fixed by the team 29 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “GUILD - Credits Expire Cron”, and a later commit of its own repaired the break that change made. The break lived 29 days. Run on the first change, the check says:

### “Call Expire Endpoint” reads a field its input never has

It reads “BACKEND_API_URL” from the item it is given, and no node that feeds it produces that field. The expression will be empty at run time.

## The team's two commits

- **The change, 29 June 2026.** [update workflows repertory](https://github.com/fsebbah/n8n-workflows/commit/61536a18d453fd08cbbaa1bcaffec4a9a3ab09b4) `61536a1`
- **The fix, 28 July 2026.** [Merge pull request #413 from fsebbah/fix/backend-api-url-crons](https://github.com/fsebbah/n8n-workflows/commit/2be542c3a9d352374f68b79c1b6cd6366fcc2d2e) `2be542c`

The workflow's file is `workflows/GUILD_-_Credits_Expire_Cron.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under fsebbah/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
