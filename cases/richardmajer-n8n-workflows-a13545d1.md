# A field read that is never produced in “Efix import products - triggers - form - import processing”, fixed by the team the same day

RichardMajer/n8n-workflows

The team behind RichardMajer/n8n-workflows changed its n8n workflow “Efix import products - triggers - form - import processing”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “Send email” reads a field “Set selected category id” never produces

It reads “eshop_category_id” from “Set selected category id”, and “Set selected category id”'s output has no such field. The expression will be empty at run time.

## The team's two commits

- **The change, 7 July 2026.** [feat(shoptet-import): F4-T10 scraper per-produkt auto-import (form+API)](https://github.com/RichardMajer/n8n-workflows/commit/550015b287fb8eb21c6ab867e0ea37ebcf7a68cd) `550015b`
- **The fix, 7 July 2026.** [chore(shoptet-import): sync exportov s userovymi E2E fixami](https://github.com/RichardMajer/n8n-workflows/commit/7e6cb5843f4ba7fb10c0587d4bc0e96311039752) `7e6cb58`

The workflow's file is `docs/superpowers/specs/reference-workflows/efix-scraper-orchestrator-form--dDA8mIhpavjz72af.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/cases/richardmajer-n8n-workflows-a13545d1](https://workflow.muoto.xyz/cases/richardmajer-n8n-workflows-a13545d1?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
