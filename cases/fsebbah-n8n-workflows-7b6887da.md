# An expression sent as plain text in “Torah Vocalization Worker”, fixed by the team 26 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “Torah Vocalization Worker”, and a later commit of its own repaired the break that change made. The break lived 26 days. Run on the first change, the check says:

### “Save to Cache” sends “url” as written

The value holds “{{ $… }}” but does not start with “=”, so n8n does not read it as an expression and sends the braces as text, not the data they name. It needs “=” at its start.

## The team's two commits

- **The change, 21 July 2026.** [Merge pull request #400 from fsebbah/feat/vocalization-job-mode](https://github.com/fsebbah/n8n-workflows/commit/84187e0c37fb77465ffe33486f05400c8a2fe459) `84187e0`
- **The fix, 16 August 2026.** [Merge pull request #454 from fsebbah/fix/url-expression-vocalisation](https://github.com/fsebbah/n8n-workflows/commit/342ceb85c3a9e041ed0c769157866d43c1942d29) `342ceb8`

The workflow's file is `workflows/Torah_Vocalization_Worker.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-7b6887da](https://workflow.muoto.xyz/cases/fsebbah-n8n-workflows-7b6887da?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
