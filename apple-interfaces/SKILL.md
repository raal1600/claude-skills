---
name: apple-interfaces
description: How to lay out and check a user interface so it works the way Apple's own apps do. Content is split into levels (summary, list, detail); a split view on wide screens and a navigation stack on a phone; lists instead of wide tables; details shown in an inspector, popover or sheet; screens that follow the selection. Load before designing, building or reviewing any user interface, in any project, web or native. Companion to build-patterns, which says why and what; this skill says how and what to check.
---

# Apple-style interfaces: how to build one, and what to check

build-patterns section 5 says what a calm interface is for. This skill says how to lay one out and how to tell
when a screen is done. Read the project first: what the things are, which of them the user came for, and what they
do next. Where a pattern doesn't fit, say why and choose deliberately. The project's own rules and words win.

## 1. Levels, not one long page

- **Find the levels before drawing a screen.** Most content has three: a summary (what matters now), a list (the
  things), a detail (everything about one thing). Health works this way: today's summary, a list of categories, one
  measurement's own view.
- **One idea per screen.** A screen that needs headings to jump between its parts is several screens.
- **Lead with what matters most:** the answer, the status, the one number. It sits at the top in a sentence or a
  large figure, with at most one chart or image.
- **Everything else is one tap away,** as grouped rows under the lead that each open their own view: "All items
  (9)", "About this", "History". A row says what is behind it, with a count or the current value where that helps.
- **Depth, not length.** If the user has to scroll past one thing to reach another, the second gets its own row
  and its own view.

Questions to ask: Is the first thing on screen the reason the user came? Could each screen be named in three words?

## 2. Navigation follows the width

- **One hierarchy, two layouts.** On a wide screen it is a split view: a sidebar of places, the content, and where
  needed the detail, side by side (Mail, Notes, Finder). On a phone it is a navigation stack: each level replaces
  the last and has a back button (the same apps on iPhone).
- **Know the patterns by name.** Master–detail: a list beside the thing selected in it. Split view: two or three
  such columns. Navigation stack: levels pushed and popped. Inspector: a panel with the selected item's details.
- **Usual forms.** On the web: grid columns that collapse to one, each level at its own address, so the browser's
  back is the back button. On Apple platforms: `NavigationSplitView`, `NavigationStack`, `.inspector`.
- **Same order in both.** What runs left to right on a wide screen runs first to last on a phone. No level exists
  in only one layout.
- **Back goes up exactly one level,** and a reload or a shared link returns to the same place.
- **The user can see where they are:** the selected row is marked in every list that leads to the current view.
- **Nothing selected** on a wide screen: one sentence on what to choose.

Questions to ask: Does every view exist at both widths? Does back ever skip a level or leave the app?

## 3. Lists before tables

- **A collection is a list.** Each row has a title, at most one line of context, one key value and one indicator
  (a status, a warning, a chevron), and the row opens its detail. Mail's messages and Stocks' symbols are lists.
- **Choose the one value** by asking what the user compares rows by. If that varies, one control above the list
  changes the value or the order. It does not add columns.
- **A detail is a label–value list,** in short named groups, like a contact card or Finder's Get Info.
- **A wide table is a sign that a level is missing.** Sideways scrolling, a "more columns" control or cells with
  two figures each mean the rows should open a detail instead.
- **A full table is the deepest level.** It is for comparing many things on many figures, opened on purpose from a
  row ("Compare all"), never the first thing shown. Its numbers are right-aligned in tabular figures.

Questions to ask: Can a row be read in one glance? Is any table the first thing on a screen?

## 4. Details come to the user

- **Selecting something shows its details without leaving the screen.** Choose the container by how much there is
  and whether it ends:
  - **Inspector:** a side panel that follows the selection (Finder's Get Info); a bottom sheet on a phone. For the
    selected item's details. It stays open while the selection changes.
  - **Popover:** anchored to what was clicked (an event in Calendar). For a short fact or a small choice. More
    than a few lines belongs in an inspector.
  - **Sheet:** for a focused task that ends in Done or Cancel (writing, editing, settings). The rest waits.
- **Explanations live there too.** "About this" and "How this works" open in an inspector, a popover or their own
  view, from a row or a small info button. They are never paragraphs between the data.
- **Every one of them** closes with Escape and with a visible control, returns the focus to what opened it, and
  can be reached and used by keyboard.
- **One at a time.** Opening a second popover or inspector replaces the first.

Questions to ask: Does anything send the user to another page for a fact that fits in a popover? Is any
explanation sitting inline between figures?

## 5. Interactive by default

- **Selection drives the screen.** Clicking a row, a card or a point on a chart selects it, and the rest of the
  screen follows at once: the lead, the chart's highlight, the inspector. Stocks does this when a symbol is clicked.
- **One selection, shown everywhere.** The same item is marked in the list and on the chart.
- **Charts can be scrubbed.** Hovering or dragging shows the exact values at the pointer; leaving returns to the
  selection. The arrow keys do the same.
- **Controls take effect immediately.** A filter, a sort or a switch needs no Apply button. Done and Cancel belong
  to sheets that change stored data.
- **Changes animate, briefly.** Panels slide, rows expand, charts move between states. The reduced-motion setting
  turns this off.
- **What looks clickable is, and shows it:** hover, pressed and focus states on everything that responds.

Questions to ask: Does clicking each thing on screen do something useful in place? Does anything need a reload or
a button press to catch up?

## 6. The visual language, concretely

- **Type:** the system font, about five sizes (large title, title, headline, body, footnote). Emphasis by weight,
  not by a new size.
- **Surfaces:** one page background with content on it in rounded groups (inset grouped lists, cards), hairline
  separators between rows, and no box inside a box.
- **Colour:** one accent for what can be acted on or is selected; a quieter tone for secondary text; any other
  colour only for meaning (a warning, an error), and never as the only signal.
- **Light and dark** from the same named values, with readable contrast in both.
- **Targets and focus:** rows and buttons large enough for a finger on a phone; a visible focus ring everywhere.

## 7. Check before calling a screen done

Check in a real browser or on a device, at a wide and a phone width, in light and dark. Not from the code.

1. Is the first thing on screen the thing that matters most?
2. Can the user reach every detail without scrolling past the others?
3. Does clicking anything do something useful in place?
4. Is there sideways scrolling anywhere, at either width?
5. Does the same hierarchy work as a split view and as a stack, with back going up one level?
6. Can everything be reached and used by keyboard, does Escape close what opened, and does focus return?
7. Do changes animate, and stop animating with reduced motion on?
8. Put a screenshot beside Mail, Notes or Settings. Does yours have more boxes, more colours, more text sizes or
   more words? Would it look at home next to them?
