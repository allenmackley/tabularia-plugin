# Tabularia

Read and revise a [Tabularia](https://tabularia.app) novel, nonfiction book, article, or screenplay with Claude. The plugin connects Claude to your Tabularia account and adds skills that say how a good editor does each job.

## Use it

Install the plugin, then sign in to the Tabularia connector from the plugin's **Connectors** tab. Ask in your own words:

| Skill                | Ask for                                                                 |
| -------------------- | ----------------------------------------------------------------------- |
| `structural-read`    | "Does my structure work?" "Does the middle drag?"                       |
| `continuity-check`   | "Have I contradicted myself?" "Is the timeline consistent?"             |
| `line-edit`          | "Tighten this chapter." "Fix the grammar in this scene."                |
| `prose-read`         | "How does this read?" "Am I repeating myself?"                          |
| `review-triage`      | "What's waiting for me?" "Where did I leave off?"                       |
| `story-thread-draft` | "Revise this thread across the book in a draft."                        |
| `story-sheets`       | "Make me a character list." "Update my character sheets from the book." |
| `synopsis-and-query` | "Write my synopsis." "Draft a query letter."                            |
| `opening-pages`      | "Would an agent keep reading?" "Does my first chapter hook?"            |
| `finish-the-book`    | "Add a title page and drop caps." "Make it look like a real book."      |
| `nonfiction-read`    | "Does my argument hold?" "Is my proposal ready?"                        |
| `article-edit`       | "Improve this blog post." "Is my headline working?"                     |
| `screenplay-read`    | "Give me coverage." "Is my script formatted right?"                     |

Claude never changes your writing without asking. Its changes land in a draft you read beside the original and merge all at once, one change at a time, or not at all, unless you turn on **Direct edits** in Tabularia.

## Data

The plugin runs nothing on your computer and reads no credential from it. You sign in on Tabularia's own page when you connect, and Claude holds that sign-in.

The connector at `mcp.tabularia.app` reads the manuscripts on the Tabularia account you sign in with and writes the drafts, comments, and edits you ask for. Tabularia does not train on your writing. Whether Claude retains it is a setting in Claude: **Settings › Privacy › Help improve Claude**. See the [privacy policy](https://tabularia.app/privacy).
