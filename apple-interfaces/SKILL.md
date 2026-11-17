---
name: apple-interfaces
description: How to lay out, build and check a user interface so it works and looks the way Apple's own apps do, complete from the first version. The app shell (a sidebar of places, an account area, a toolbar), content in levels (summary, list, detail), a split view on wide screens and a navigation stack on a phone, lists before tables, details in an inspector, popover or sheet, a current item that changes every page, visible runs, the right control for each choice, and a measured check before a screen is called done. Load before designing, building or reviewing any user interface, in any project, web or native. Companion to build-patterns, which says why and what.
---

# Apple-style interfaces: how to build one, and what to check

build-patterns §5 says what a calm interface is for; this skill says how. Read the project first: what the things
are, which one the user came for, what they do next. Where a pattern doesn't fit, say why and decide. The project
wins on safety and on its words. A project note does not loosen the limits set here.

## 1. Levels, not one long page

- **Find the levels before drawing a screen:** a summary (what matters now), a list (the things), a detail
  (everything about one thing).
- **One idea per screen.** A screen that needs headings to jump between its parts is several screens.
- **Lead with what matters most:** one sentence of about 25 words or fewer, or one large figure, never both. At most
  one chart under it. A long lead pushes the data off a phone's first screen.
- **Fix confusion by moving words, not adding them:** a definition, a label, or an "About this" view. Never another
  sentence in the lead or between the data.
- **Everything else is one tap away,** as grouped rows under the lead: "All items (9)", "About this", "History".
- **Depth, not length.** If the user scrolls past one thing to reach another, the second gets its own row and view.

Questions: Is the first thing on screen the reason the user came? Could each screen be named in three words?

## 2. The app shell and navigation

A tool people come back to is an app, not a website: a sidebar of places from the first version. Never numbered
steps, "Next" buttons, a breadcrumb or a fixed footer; they say "where you are" a second time.

- **One hierarchy, two layouts.** Wide: a split view, with a sidebar, the content and, where needed, an inspector
  side by side. Phone: a navigation stack where each level replaces the last and has a back button. The same order
  in both; no level exists in only one. On the web each level has its own address, so the browser's back is the back
  button. On Apple platforms: a navigation split view, a navigation stack, an inspector.
- **Back goes up exactly one level,** and a reload or a shared link returns to the same place.
- **The sidebar shows places and the current choice, nothing else.**
  - Every row has the same height, icon, hover pill and selected pill: accent when the window is focused, grey when
    it isn't. Group headings fold with a chevron and a small tinted icon tile, and hover like rows.
  - Kinds of rows are separated by a hairline, not by a different row style.
  - A row carries at most a count, or a badge (build-patterns §5).
  - Secondary sections such as activity fold by default and can be hidden.
  - Dates, history, explanations and "why is this hidden" notes belong on the page or in settings.
  - Search sits at the top. Width, visibility and open sections are remembered.
- **The account area sits at the foot of the sidebar** in any app with sign-in: initials, who is signed in, and one
  status line. Its menu holds Account, Settings, Activity and Sign out, and Sign out asks first. Signed out, only the
  sign-in screen shows. An expired session is a calm "sign in again" sheet that keeps the user's place, never an
  error page.
- **The toolbar** holds the title, the sidebar toggle, the current item and how fresh it is, and the page's one action.
- **Nothing selected** on a wide screen: one sentence on what to choose.

Questions: Does every view exist at both widths? Is "where you are" said exactly once? Does any sidebar row look,
hover or highlight differently from the others?

## 3. Lists before tables

- **A collection is a list.** A row has a title, at most one line of context, one key value and one indicator, and
  opens its detail.
- **Choose the one value** by what the user compares rows by. If that varies, one control changes the value or the
  order; it never adds columns.
- **A detail is a label–value list** in short named groups.
- **A wide table is a sign that a level is missing.** A full table is the deepest level, opened on purpose ("Compare
  all"), never first. Its rows open their item. On a phone it becomes rows with the sorted value.
- **Long lists are grouped:** more than about fifty rows become groups that each open their own list.

Questions: Can a row be read in one glance? Is any table the first thing on a screen?

## 4. Details come to the user

- **Selecting shows details without leaving the screen.**
  - Inspector: a side panel that follows the selection, or a bottom sheet on a phone.
  - Popover: a short fact or a small choice, anchored to what was clicked.
  - Sheet: a focused task that ends in Done or Cancel.
- **Explanations live there too,** behind a row or an info button, never as paragraphs between the data.
- **Back inside a panel goes up one level** from any depth.
- **Each one closes with Escape and a visible control,** returns focus to what opened it, and works by keyboard. One
  at a time.

Questions: Does anything send the user to another page for a fact that fits a popover?

## 5. Interactive by default

- **Selection drives the screen.** Clicking a row, card or chart point selects it, and the lead, the highlight and the
  inspector follow. One selection, shown everywhere: a chart draws exactly what its list shows.
- **The current item drives every page.** When pages depend on one chosen item (a dataset, a project, an account):
  - it is chosen from one control in the toolbar of every page, kept in the address, and switching it changes every
    page at once, keeping the user's place;
  - on a first visit nothing is chosen, and every page shows the same one-line empty state with a "Choose…" button;
    after that the last choice reopens;
  - within an item the newest version is the default, and older versions are picked from that same toolbar control.
    A list or log may link to them but is never the only way. A new version announces itself with a way back.
- **Runs show themselves.** Anything the user starts and waits for appears in an Activity section with live
  progress. Failures get a badge and open a view that says what happened and why.
- **Live, without a reload.** New data and new versions arrive by themselves.
- **Charts can be scrubbed** by pointer and arrow keys, starting from the current selection.
- **Controls take effect immediately.** Done and Cancel belong to sheets that change stored data.
- **Changes animate briefly;** reduced motion turns it off. What responds shows hover, pressed and focus states.

Questions: Does clicking each thing do something useful in place? Does switching the current item reach every page?

## 6. The visual language: calm, not plain

- **Type:** the system font, about five sizes, emphasis by weight. Figures use tabular numerals.
- **Surfaces:** one background, content in rounded groups, hairlines between rows, no box inside a box.
- **Colour:** one accent for what can be acted on or is selected, a quieter tone for secondary text, any other colour
  only for meaning and never alone. Light and dark come from the same named values, with contrast measured in both:
  text 4.5:1, marks that carry meaning 3:1.
- **Character from the first version:** an icon on every place, a small tinted tile for each group, depth (a
  translucent sidebar, soft shadows on sheets and menus), a hero lead over its one chart, subtle fills. Calm without
  these looks like a document.
- **Controls:** two to four choices are a segmented control, a longer list is a compact pop-up button sized to its
  value, and on/off is a switch. Where the screen already shows the choices as a list or chart, picking there is the
  choice. Full-width form selects belong only in forms.
- **Targets and focus:** finger-sized on a phone, a visible focus ring everywhere.

## 7. Check before calling a screen done

Measure first, then look. A script over every screen catches what spot checks by eye miss.

- **Run it on sample data that shows every state:** two or more of each switchable item, plus empty, waiting, failed,
  stale and long-text cases.
- **Run it at three widths and both themes:** phone, the width where the layout switches, and wide; light and dark.
- **Check the first screen built in a new pattern** against the whole list before any other screen copies it. A
  violation seen there is fixed there, not deferred.
- **After each wave, someone who wrote none of the code** runs the list and reports measured findings.

1. Is the first thing on screen the thing that matters most, within the word limit?
2. Can every detail be reached without scrolling past the others?
3. Does clicking anything do something useful in place?
4. Is any element wider than its box, or past the window's edge, at any width? Inner containers count, not just the page.
5. Does the hierarchy work as a split view and as a stack, with back going up one level?
6. Can everything be reached by keyboard in a sensible number of Tab stops, does Escape close what opened, and does
   focus return?
7. Do changes animate, and are the animation rules absent under reduced motion?
8. Does every row of each kind share its height, padding, hover and selected style?
9. Beside a reference app: does yours have more boxes, colours, type sizes or words, or fewer icons, less depth, no
   hero?
