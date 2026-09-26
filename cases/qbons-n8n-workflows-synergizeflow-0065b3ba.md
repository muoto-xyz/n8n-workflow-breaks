# A field read that is never produced in “SF - Blog Agent NEW”, fixed by the team 3 days later

qbons/n8n-workflows-synergizeflow

The team behind qbons/n8n-workflows-synergizeflow changed its n8n workflow “SF - Blog Agent NEW”, and a later commit of its own repaired the break that change made. The break lived 3 days. Run on the first change, the check says:

### “Switch3” reads a field “Prepare Data” never produces

It reads “config” from “Prepare Data”, and “Prepare Data”'s output has no such field. The expression will be empty at run time.

## The team's two commits

- **The change, 15 September 2026.** [update blog agent](https://github.com/qbons/n8n-workflows-synergizeflow/commit/734a4286b5a992e2cc30efa40f0ffc26433afdd3) `734a428`
- **The fix, 18 September 2026.** [blog agent](https://github.com/qbons/n8n-workflows-synergizeflow/commit/02cc70a5762459d9a0bf00b5df7eea9ffb7f1dac) `02cc70a`

The workflow's file is `workflows/sbTDmNrs13Dz7zQC.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under qbons/n8n-workflows-synergizeflow.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
