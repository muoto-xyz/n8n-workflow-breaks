# A webhook that refuses every call in “LT Proteros: Missed Call to SMS”, fixed by the team 15 days later

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “LT Proteros: Missed Call to SMS”, and a later commit of its own repaired the break that change made. The break lived 15 days. Run on the first change, the check says:

### “Webhook: Zadarma Missed Call” does not wait for the Respond to Webhook node after it

Its “Respond” option is “When Last Node Finishes”, and a Respond to Webhook node follows it. n8n refuses every call to it at run time with “Unused Respond to Webhook node found in the workflow”. Set “Respond” to “Using 'Respond to Webhook' Node”.

## The team's two commits

- **The change, 12 March 2026.** [Merge pull request #39 from GitHubProgramming/ai/lt-proteros-sms-test-flow](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/9dc1d7c21ea67f3208d24e4cc76b93a553345196) `9dc1d7c`
- **The fix, 26 March 2026.** [fix: use responseNode mode in both LT production workflows (#354)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/47ca39cc946f43908c8c9c61358e9673b8b376c5) `47ca39c`

The workflow's file is `n8n/workflows/LT_Proteros/lt-missed-call-to-sms.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-865345dd](https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-865345dd?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
