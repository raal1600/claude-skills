---
name: helper-sessions
description: How to split work across helper sessions or agents and bring it back together without rework. Visible helpers by default, shared contracts frozen first, one owner per file and per shared surface, briefs that settle questions up front, trial merges, corrections routed to the helper that built the part, and work sized to the usage allowance. Load before starting, briefing or merging the work of any helper, nested session, sub-agent or parallel worker. Builders working alone do not need it; build-patterns covers the work itself.
---

# Helper sessions: splitting work and bringing it back

For whoever coordinates helpers. Each rule exists because parallel work fails at the seams: what two helpers share,
what nobody owns, and what the owner can't see.

## 1. Visible by default

- **Run helpers the way the owner asked,** as visible sessions they can open and stop. Hidden background workers
  only with their agreement: they can't watch or steer what they can't see.
- **If that way is blocked, ask for the unblock,** with the exact click, as your one question. Never start a fallback
  beside a pending helper; two helpers on one task undo each other.

Question: Could the owner open every helper that is working right now?

## 2. Freeze what is shared, then split

- **One writer freezes the shared pieces first:** the words, the data shapes, the shared components, and a file
  split where every file has one owner. Then start the helpers that depend on them. Parallel helpers on unfrozen
  shared pieces spend their time asking and clashing.
- **Split by slice when a change crosses layers:** one owner changes every consumer of a contract in one piece of
  work, after the contract is frozen. Splitting by layer suits work that stays inside one.
- **Every shared surface has an owner and an integration pass.** When several helpers' pieces appear on one screen,
  its owner fits them together before the owner of the project sees it.

Question: Which file or surface would two helpers both need to change?

## 3. Briefs

A helper knows only its brief. A good one names:

- the outcome, in a sentence, and the approved example or reference to match; never a layout nobody has seen;
- the files it alone owns, and what not to touch because others are editing it;
- what it may change in shared pieces without asking: additive, backward-compatible, tested against every user,
  listed in its PR;
- who answers its questions: the coordinator, never the project owner, unless the question is about taste, money
  or access;
- measurable checks to run, and what to report: done, verified, not verified;
- to save, push and leave a hand-over note (state, next step, open questions) at each milestone and on any stop.

Long specs and standing rules go in a file every helper reads, not into each brief.

Question: Could the helper finish without asking anything the brief could have answered?

## 4. Merging

- **Merge all open parallel work together in a trial copy** and run every check before merging any of it into the
  main line. Clashes surface there, not in the main line.
- **Name test files after the area they check,** never after a round of fixes, so parallel helpers don't edit the
  same test file.
- **Stack work only on a base whose shared files are frozen.**
- **Check a helper's follow-ups against the design rules** before acting on them.

Question: Has the combination been tested, or only each piece alone?

## 5. Corrections, context and cost

- **Send a correction to the helper that built the part** while it still holds the context. Start a fresh helper
  only for work that builds on nothing earlier.
- **Size parallel work to the remaining allowance.** Read it before starting more than two helpers, say a rough cost
  in plain words, and use a cheaper model for mechanical reading or edits. A limit stops every helper at once.
- **Keep the coordinating thread thin.** Hand off at a planned point, not at the limit. Keep open items, decisions and
  standing rules in one file, so a restart or a summary loses nothing. Answer a side question in a fresh session with
  a short facts file, not in a copy of the whole thread.

Question: If every helper stopped now, could each one resume from what it wrote down?
