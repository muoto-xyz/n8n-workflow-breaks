# A webhook that refuses every call in “LT Proteros: Safe Dashboard Log Test”, fixed by the team the same day

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “LT Proteros: Safe Dashboard Log Test”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “Webhook: LT Safe Log Test” does not wait for the Respond to Webhook node after it

Its “Respond” option is “When Last Node Finishes”, and a Respond to Webhook node follows it. n8n refuses every call to it at run time with “Unused Respond to Webhook node found in the workflow”. Set “Respond” to “Using 'Respond to Webhook' Node”.

## The team's two commits

- **The change, 26 March 2026.** [feat: add LT safe dashboard log test workflow and CLI scripts (#346)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/483cd3857dfabe1db8f5a01d20a38401db4b8915) `483cd38`
- **The fix, 26 March 2026.** [fix: use responseNode mode in LT safe log test workflow (#347)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/2fb6ee07d4c35167f29887b67c43f5fd9c5a3c99) `2fb6ee0`

The workflow's file is `n8n/workflows/TEST/wf007-lt-safe-log-test.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-92a7d011](https://workflow.muoto.xyz/cases/githubprogramming-autoshop-sms-ai-92a7d011?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
