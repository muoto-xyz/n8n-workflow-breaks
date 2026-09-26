# An expression sent as plain text in “Stripe - Subscription Success”, fixed by the team 145 days later

fsebbah/n8n-workflows

The team behind fsebbah/n8n-workflows changed its n8n workflow “Stripe - Subscription Success”, and a later commit of its own repaired the break that change made. The break lived 145 days. Run on the first change, the check says:

### “Log Paiement” sends “url” as written

The value holds “{{ $… }}” but does not start with “=”, so n8n does not read it as an expression and sends the braces as text, not the data they name. It needs “=” at its start.

## The team's two commits

- **The change, 24 March 2026.** [Merge pull request #324 from fsebbah/feat/add-inputschema-to-webhooks](https://github.com/fsebbah/n8n-workflows/commit/12ba0805a847c5c1657e1743702b1611bc2d47a3) `12ba080`
- **The fix, 16 August 2026.** [Merge pull request #456 from fsebbah/fix/expressions-url-stripe](https://github.com/fsebbah/n8n-workflows/commit/9131e2acd56f9ff63709b46cd84f3ca5af0b1f60) `9131e2a`

The workflow's file is `workflows/Stripe_-_Subscription_Success.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under fsebbah/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
