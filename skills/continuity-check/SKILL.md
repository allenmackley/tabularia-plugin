---
name: continuity-check
description: Find contradictions across a Tabularia Manuscript — a character's eye color that changes, a wound that heals too fast, a date that does not survive the next chapter. Use when the Writer asks about continuity, consistency, plot holes, timeline problems, whether the book still matches their character Sheets, or whether they have contradicted themselves.
---

<what-this-is>

Continuity work is search, not reading. The contradiction is almost never in the
passage the Writer is looking at — it is in the chapter they wrote four months
ago and have not opened since.

So do not read the book front to back looking for problems. Find the facts, then
check each one everywhere it appears.

</what-this-is>

<start-from-what-the-project-already-tracks>

1. `tabularia_list_sheets` — the characters, places and whatever else the
   Project keeps beside the book, each with its aliases, template fields and
   notes. Start here. This is the Writer's own record of what is true, so it is
   at once the fact list you are about to check and the thing the prose has to
   agree with. A Sheet that disagrees with the prose is as strong a finding as a
   Timeline that does, and for the same reason: the Writer wrote both.
2. `tabularia_list_timelines` — the Writer's own Timelines and markers. These are
   the dates and sequences they have already decided matter. A Timeline that
   disagrees with the prose is the strongest kind of finding, because the Writer
   wrote both.
3. `tabularia_list_anchors` — the Outline, and the point and range Anchors where
   they have marked things.
4. `tabularia_project_metadata` — how many Books, and whether this is a Series.
   A continuity check across a Series is a different scale of job; say so before
   starting one.

</start-from-what-the-project-already-tracks>

<then-search>

`tabularia_search` finds wording across every open Project and answers with the
Block index and surrounding context of every occurrence. That is the tool for
this entire job.

The answer is a page of matches, and it tells you which page it is: read
`matchCount` and `truncated` rather than counting the list. When `truncated` is
true there are more, and you ask again with a later `from`. A name you report
as appearing eleven times when the first page held eleven of forty is the
mistake this whole skill exists to avoid.

Build a list of checkable facts first, then search each one:

- **Proper nouns** — every character, place, ship, house, spell. Search the name
  and read every match, not the first three. Search every alias its Sheet
  carries as well as the name: a character the book calls Mira in half its
  chapters and the Ravener in the other half is one search that finds half the
  passages, and the count you report is wrong for exactly the character it
  matters most for.
- **What the Sheets already assert** — every filled template field is a claim
  the prose can break. An age, a home, a rank, who someone is married to. Check
  each against the passages that mention it.
- **Physical facts** — eye and hair color, scars, height, age, injuries. These
  are where contradictions actually live.
- **Time and sequence** — days of the week, seasons, "three days later", ages,
  how long a journey takes. Check these against the Timelines.
- **Objects and their state** — the letter that was burned, the sword that broke,
  the door that was locked.
- **Relationships and what people know** — who has met whom, who knows the
  secret, who was in the room.

When a Writer names a specific worry, start there and widen only if it is clean.

</then-search>

<what-counts-as-a-finding>

A finding needs **two passages that cannot both be true**, and you must cite
both, with their Block indexes. "Check Mira's age" is not a finding. "Block 88
makes Mira nineteen at the siege; Block 412 puts the siege six years after her
sixteenth birthday, which makes her twenty-two" is.

A Sheet counts as one of the two. Cite it the way you would cite a passage —
the Sheet's name and the field — and say plainly that the Sheet may be the side
that is out of date, because a Writer who changed a character's age in the
prose and never went back to the Sheet has not made a continuity error.

Four things that look like findings and are not:

- **Deliberate contradiction.** An unreliable narrator, a lying character, a
  faulty memory. If a contradiction sits with a character who has reason to lie,
  say that you have noticed it and that it may be intended.
- **A Draft disagreeing with the Base.** Check `tabularia_list_drafts` before
  reporting. Two versions of a passage are meant to differ — that is what a Draft
  is. Only compare wording inside one composition.
- **A name the Sheet already knows.** An alias listed on a Sheet is the same
  person under another name, not a slip and not a second character. Read the
  Sheets before reporting any name as inconsistent.
- **Revision in progress.** If the Writer has an open Review Change or a
  proposal over one of the two passages, the contradiction may already be on its
  way out. `tabularia_list_review_changes` tells you.

</what-counts-as-a-finding>

<how-to-deliver>

Anchor each finding with `tabularia_add_comment` on the passage you think is
wrong — usually the later one — and name the other passage in the body with its
Block index so the Writer can jump to it.

A Sheet is not a passage and cannot carry a comment, so anchor a Sheet finding
on the prose it disagrees with and name the Sheet and field in the body.

Do not propose the fix. Which of two passages is wrong is a story decision, and
the wrong one is often the one that reads better. That holds for the Sheets as
well: do not correct one, and do not fill in a missing one, unless the Writer
asks. If they do, `tabularia_write_sheet` is a proposal like any other, and you
read the Sheets first so you update the one that is there instead of making a
second.

When the Writer's worry is a sequence rather than a contradiction — "does the
war actually happen in the order I think it does?" — build them a Timeline
instead of a list. `tabularia_create_timeline` makes one, and
`tabularia_add_timeline_marker` marks each passage you found. They can then pin
it as a Working Scope and read only those passages in order, which answers the
question far better than anything you could write in the chat. Reuse a Timeline
that already carries the title rather than making a second.

Report the sweep in the chat as well: what you searched for, how many matches
each term had, and what came back clean. A Writer needs to know the check was
thorough, and "no contradictions found" means nothing without the list of what
was actually checked.

</how-to-deliver>
