# A read from a node that has not run in “US AutoShop: Telegram Task Intake”, fixed by the team the same day

GitHubProgramming/autoshop-sms-ai

The team behind GitHubProgramming/autoshop-sms-ai changed its n8n workflow “US AutoShop: Telegram Task Intake”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “Build Reply” reads from a node that never runs before it

It reads from “API: Register Task”, and no path in the workflow runs “API: Register Task” before “Build Reply”. The expression fails at run time.

## The team's two commits

- **The change, 28 March 2026.** [feat: add Telegram task intake workflow for operator dev-loop trigger (#384)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/9ad5240df19d3c1dec62eed43b4899b09370f261) `9ad5240`
- **The fix, 28 March 2026.** [fix: remove duplicate task registration from Telegram intake (#385)](https://github.com/GitHubProgramming/autoshop-sms-ai/commit/b37bb33c0400db15f052fc8083e164149eb2fd17) `b37bb33`

The workflow's file is `n8n/workflows/US_AutoShop/telegram-task-intake.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under GitHubProgramming/autoshop-sms-ai.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
