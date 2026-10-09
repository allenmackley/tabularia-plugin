# Tabularia

Read and revise a [Tabularia](https://tabularia.app) Manuscript with Claude. The
plugin connects Claude to your Tabularia account and adds six skills that say
how a good editor does each job.

## Use it

Install the plugin, then sign in to the Tabularia connector from the plugin's
**Connectors** tab. Ask in your own words:

| Skill                | Ask for                                                     |
| -------------------- | ----------------------------------------------------------- |
| `structural-read`    | "Does my structure work?" "Is the middle saggy?"            |
| `continuity-check`   | "Have I contradicted myself?" "Is the timeline consistent?" |
| `line-edit`          | "Tighten this chapter." "Fix the grammar in this scene."    |
| `prose-read`         | "How does this read?" "Am I repeating myself?"              |
| `review-triage`      | "What's waiting for me?" "Where did I leave off?"           |
| `story-thread-draft` | "Revise this thread across the book in a Draft."            |

Claude never changes your Manuscript behind your back. Its changes land in a
Draft you read beside the original and merge a difference at a time, unless you
turn on Direct edits in Tabularia.

## Data

The connector at `mcp.tabularia.app` reads the Manuscripts on the Tabularia
account you sign in with and writes the Drafts, comments, and edits you ask
for. Tabularia does not train on your writing. Whether Claude retains it is a
setting in Claude: **Settings › Privacy**. See the
[privacy policy](https://tabularia.app/privacy).
