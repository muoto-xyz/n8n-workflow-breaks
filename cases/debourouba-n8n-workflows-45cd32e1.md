# A read from a node that has not run in “🔁 GED — Reclassification”, fixed by the team the same day

debourouba/n8n-workflows

The team behind debourouba/n8n-workflows changed its n8n workflow “🔁 GED — Reclassification”, and a later commit of its own repaired the break that change made. The break lived less than a day. Run on the first change, the check says:

### “🏷️ Marquer Original” reads from a node that never runs before it

It reads from “🧩 Agréger Résultats Callback”, and no path in the workflow runs “🧩 Agréger Résultats Callback” before “🏷️ Marquer Original”. The expression fails at run time.

## The team's two commits

- **The change, 6 July 2026.** [fix: Marquer Original — try Agréger Résultats Callback en premier, fallback Parser Callback](https://github.com/debourouba/n8n-workflows/commit/9b5e7ebe025e01e34e6b3159068fecb3b97d8d3b) `9b5e7eb`
- **The fix, 7 July 2026.** [fix: Marquer Original déplacé après Agréger Résultats Callback — code simplifié sans try/catch](https://github.com/debourouba/n8n-workflows/commit/d558c8c322521f81213f3e1c8cd95a523c8cf8fd) `d558c8c`

The workflow's file is `workflows/GGqlUJaJz2zJUGIB.json`. Before the change, the check found nothing of this in it; after the fix, it finds nothing again. Each case was read against the team's own fix: the fix changes this step, and the change removes the cause.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Check a change before it ships: paste the workflow. Free. No account. Nothing is stored unless you choose to share it.

---

This case is on the site's [list of fixed breaks](https://workflow.muoto.xyz/cases/?utm_source=github), under debourouba/n8n-workflows.

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
