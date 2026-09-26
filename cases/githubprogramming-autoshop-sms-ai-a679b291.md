# A webhook that refuses every call in “WF-007: Provision Twilio Number (Async)”, fixed by the team 5 days later

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “WF-007: Provision Twilio Number (Async)”, and a later commit of its own repaired the break that change made. The break lived 5 days. Run on the first change, the check says:

### “Webhook: Provision Number” waits for a Respond to Webhook node it does not have

Its “Respond” option is “Using 'Respond to Webhook' Node”, and no such node follows it. n8n refuses every call to it at run time with “No Respond to Webhook node found in the workflow”.

## The team's two commits

- **The change, 5 March 2026.** [initial autoshop sms ai project](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/be59595a76e83738c19cff573dad972ff12a1c8f) `be59595`
- **The fix, 10 March 2026.** [Merge pull request #27 from GitHubProgramming/ai/twilio-production-fix](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/0ae235734eb3fe725c0aa7405486841657426886) `0ae2357`

The workflow's file is `n8n/workflows/provision-number.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under GitHubProgramming/autoshop-sms-ai.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
