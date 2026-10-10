---
name: finish-the-book
description: Give a Tabularia Book a finished look — its Matter pages, scene-break ornaments, drop caps on chapter openings, and pictures. Use when the Writer asks to make the book look finished, professional or printed, to add a title page, copyright page, dedication or author bio, to add drop caps or ornaments, or to place illustrations.
---

<what-this-is>

A printed novel follows conventions readers notice only when they are missing:
a title page and copyright page, a dedication if there is one, chapters that
open with a drop cap, and the same mark at every scene break. Tabularia has all
of these. This job puts them in consistently, in a way the Writer can review.

Design is the Writer's. Propose a set, show where it goes, and let them choose.

</what-this-is>

<look-first>

1. `tabularia_project_metadata` — each Book and its Matter settings: which pages
   it carries now.
2. `tabularia_list_decorations` — every drop cap and ornament already there, with
   its treatment and size. Match what the Writer has chosen rather than adding a
   second style.
3. `tabularia_list_pictures` — what is in the Images and where it is placed.
4. `tabularia_list_drafts` — and whether Direct edits is on, which decides what
   you can do below.

</look-first>

<matter-pages>

The conventional order is title page, copyright page, dedication, then the
body, then acknowledgements and the author bio. A novel needs the first two;
the rest only if the Writer has something to put in them.

Turning a page on or off reflows the Book, so it is the Writer's switch to
flip. When `tabularia_set_book_matter` is among your tools, it turns a page on
or off for one Book: `tabularia_take_snapshot` first. When it is not, which is
the case over the remote connector, name the Book and the pages to check in
Project Settings → Book Matter in Studio (for a novel, Title Page and
Copyright Page), and say that each checked page arrives with sample wording
to replace. Either way, ask the Writer for the dedication or bio wording
rather than writing it, and never invent copyright details such as an ISBN.

</matter-pages>

<drop-caps>

The convention is a drop cap on the first paragraph of each Chapter and nowhere
else. Read the Chapter openings with `tabularia_read_window` to find each first
paragraph's Block id. The paragraph has to begin with a letter, so a Chapter
that opens on a quotation mark cannot take one; list those for the Writer
rather than skipping them silently.

`tabularia_arrange_drop_cap` adds one. It goes to your own Draft unless Direct
edits is on, and each is a difference the Writer merges, so add them all in one
Draft and tell them where it is. Use the `treatmentId` of a drop cap already in
the book so they match; with none, the default is fine.

</drop-caps>

<ornaments>

An ornament marks a scene break inside a Chapter. Use the same one at every
break; a different mark at one break reads as an error.

`tabularia_add_ornament` needs the Base Draft and Direct edits on, because it
adds a Block. With Direct edits off, list the breaks you would mark and let the
Writer add them, or ask whether they want to turn Direct edits on — in plain
words, saying it lets you change the text directly. Never turn it on yourself.
A Chapter or Scene boundary is not an ornament; do not add one there.

</ornaments>

<pictures>

Pictures come from the Writer's Images. `tabularia_add_picture` brings one in
from an openly licensed source, and you tell them it records where it came from
and that they should check its license before publishing.
`tabularia_place_picture` puts one beside a paragraph; whether that is offered
or done is the Writer's setting, and the answer says which. Do not place
pictures they did not ask for.

</pictures>

<afterwards>

Say what you changed or offered, where each change is waiting — which Draft,
or the text itself — and what you left for the Writer to supply, such as the
dedication wording.

</afterwards>
