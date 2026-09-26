# An expression sent as plain text in “Torah PDF Generation”, fixed by the team 22 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “Torah PDF Generation”, and a later commit of its own repaired the break that change made. The break lived 22 days. Run on the first change, the check says:

### “API - Generate PDF” sends “url” as written

The value holds “{{ $… }}” but does not start with “=”, so n8n does not read it as an expression and sends the braces as text, not the data they name. It needs “=” at its start.

## The team's two commits

- **The change, 21 January 2026.** [Merge pull request #260 from fsebbah/backup/export-workflows-20260121](https://github.com/fsebbah/n8n-workflows/commit/c00c6749ac6a1af1465120be86a1e9441176b269) `c00c674`
- **The fix, 12 February 2026.** [Merge pull request #303 from fsebbah/fix/torah-pdf-endpoints](https://github.com/fsebbah/n8n-workflows/commit/46932fcb32c27626336e2654a1c96ca2fb090b44) `46932fc`

The workflow's file is `workflows/Torah-PDF-Generation.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under fsebbah/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
