# Referenced node doesn't exist: what this n8n error means and how to fix it

n8n error

n8n stopped because an expression reads data from another node by its name, like $('Fetch Orders'), and no node in the workflow has that name. n8n looks the name up while the workflow runs, finds nothing, and stops the node with “Referenced node doesn't exist”. In the node's error panel, the editor adds: “The node … doesn't exist, but it's used in an expression here.”

## What your workflow file can show

- **A node was renamed.** The expression still says the old name. A node pasted into a workflow that already has one of that name gets a number added, like “Get Orders1”, and the expressions pasted with it keep the old name.
- **A node was deleted, or its name was typed differently.** The node is gone, or the name in the expression differs from the node's by a character: an extra space, a backslash, a different capital letter.

Both are in the workflow's file, so they can be found before anything runs. Paste the workflow into the check and it names every node that reads a name no node has, all at once.

## What the file cannot show

- **You ran one node on its own in the editor.** The nodes before it did not run in that test, so their data is not there. n8n then says the node hasn't been executed. Run the workflow from its trigger instead.
- **n8n cannot tell which item to use.** A node's data is there, but n8n cannot pair it with the item being processed, after a Merge, a loop or a Code node. n8n says “Can't determine which item to use”.
- **The data comes from an earlier run.** A loop that reads what its own previous pass left finds nothing on its first pass, and pinned or old test data can hide a break until the real run.
- **The expression is outside the workflow's nodes.** An expression in a credential is read without your nodes, so any node's name there fails, and a part of a workflow pasted on its own lacks the nodes it reads.

## What the check says

A small workflow of 3 nodes, “Every Morning” → “Get Orders” → “Format Summary”, where one node still reads a name the workflow no longer has. This is the check's report on it:

### “Format Summary” names a node that does not exist

It reads from “Fetch Orders”, and no node in the workflow has that name. A renamed node is the usual cause. The expression fails at run time.

**Fix:** Change the name inside $('…') to the node's name as it is now, character for character, or rename the node back.

## How often the file shows it

Of the 6 threads on n8n's community forum with this error that carried a workflow, the cause was in the wiring in 2, and the check named it in 1.

We read every thread n8n's forum search returned for [“Referenced node doesn't exist”](https://community.n8n.io/search.json?q=%22Referenced+node+doesn%27t+exist%22) on 25 September 2026. For each thread that carried a workflow, we wrote down the cause before the check read the file.

**[Check your workflow](https://workflow.muoto.xyz/?utm_source=github#desk)**

Got this error? Paste the workflow: the check shows every node that reads a name no node has. Free. No account. Nothing is stored unless you choose to share it.

---

Read it on the site: [https://workflow.muoto.xyz/errors/referenced-node-doesnt-exist](https://workflow.muoto.xyz/errors/referenced-node-doesnt-exist?utm_source=github)

Check your own workflow: [https://workflow.muoto.xyz](https://workflow.muoto.xyz/?utm_source=github). Free, no account.

[All readings](../README.md)
