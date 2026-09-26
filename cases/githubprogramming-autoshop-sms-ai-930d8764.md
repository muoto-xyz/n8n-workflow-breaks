# An expression sent as plain text in “WF-EXPORT-TO-SMARTLEAD”, fixed by the team 3 days later

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “WF-EXPORT-TO-SMARTLEAD”, and a later commit of its own repaired the break that change made. The break lived 3 days. Run on the first change, the check says:

### “HTTP - Smartlead Add Leads” sends “url” as written

The value holds “{{ $… }}” but does not start with “=”, so n8n does not read it as an expression and sends the braces as text, not the data they name. It needs “=” at its start.

## The team's two commits

- **The change, 28 March 2026.** [feat: add WF-EXPORT-TO-SMARTLEAD workflow (#373)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/c7630e54bca3ee6dbd9cf0d6a23e41f14c0681d9) `c7630e5`
- **The fix, 31 March 2026.** [fix: use n8n expression syntax for Smartlead HTTP URL (#403)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/527129f379097f15291d8eb9568d64019dbfb47f) `527129f`

The workflow's file is `n8n/workflows/US_AutoShop/wf-export-to-smartlead.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under GitHubProgramming/autoshop-sms-ai.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
