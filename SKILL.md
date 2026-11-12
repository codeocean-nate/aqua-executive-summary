---
name: executive-summary
description: Use on every response. When the reply as a whole exceeds 3000 characters, append an "## Executive Summary" section of at most 1500 characters at the very end, as 3-5 bullets covering the key findings, the numbers that matter, and the next step. Replies of 3000 characters or fewer get no summary and are left exactly as written.
metadata:
  tags: [communication, reporting, summary, writing]
---

# Executive Summary

Long answers bury their conclusions. This skill guarantees that any reply long enough to be skimmed rather than read ends with a short, self-contained summary a decision-maker can act on without reading the body.

## When it applies

Evaluate this on every response, before sending it.

- Measure the length of the complete reply as the reader receives it: prose, headings, tables, code blocks, lists, and links all count. Measure in characters, not words or tokens.
- **Over 3000 characters** → append the summary described below.
- **3000 characters or fewer** → append nothing. Do not add a summary, a heading, or a note explaining its absence.
- Measure the body only. The summary itself never counts toward the 3000 character trigger, and adding it never re-triggers the check.

## The summary

- **Heading:** exactly `## Executive Summary`, as a level-two Markdown heading.
- **Position:** the very last thing in the reply. Nothing follows it — no closing question, no next-step prose, no link list, no sign-off.
- **Length:** 1500 characters maximum, including the heading and all markup. Shorter is better. Never exceed it; cut content rather than run over.
- **Form:** 3 to 5 bullets. No sub-bullets, no paragraphs, no tables.

Each bullet is one line, ideally under 200 characters. Across the 3-5 bullets, cover:

1. **Findings** — what is actually true, stated as a conclusion rather than a description of activity. "Expression is 2.4x higher in treated samples," not "we compared expression between groups."
2. **Numbers** — the specific values, counts, effect sizes, thresholds, or identifiers that carry the conclusion. Prefer one concrete figure over a qualitative adjective.
3. **Next step** — the final bullet names the single most useful thing to do next, or states that nothing is outstanding.

## Rules

- **The summary restates; it never introduces.** Every claim, number, and identifier in it must already appear in the body above. If something belongs in the summary but is not in the body, it is missing from the body — fix the body.
- **Never soften or upgrade a conclusion in the summary.** Uncertainty, caveats, and failures carry through: a blocked or partial result is summarized as blocked or partial, with the blocker named.
- **Numbers must match the body exactly** — same value, same unit, same denominator. No rounding that changes the figure's meaning.
- **The summary must stand alone.** A reader who sees only these bullets should not need the body to understand what happened and what it means.
- **Write it in the same persona and register as the body.** For a non-technical reader, the summary stays non-technical: scientific meaning, not tooling.
- **Do not use the summary for apology, process narration, or effort reporting** ("ran three queries", "this took several steps"). It carries outcomes only.

## Exceptions

Do not append a summary when:

- The reply is 3000 characters or fewer.
- The user asked for an exact output and nothing else — a single value, a label, a delimited string, "respond with only…". The requested payload is the entire reply; a summary would corrupt it.
- The reply is already itself a summary, abstract, or executive brief the user explicitly requested. Do not summarize a summary.
- The body is a single verbatim artifact the user asked to see unmodified (a file's contents, a transcript, a quoted passage).

## Example

For a long analysis reply, the appended section looks like:

```markdown
## Executive Summary

- Treated samples show 2.4x higher target expression than controls (p = 0.003, n = 24).
- 3 of 18 candidate genes pass the FDR 0.05 threshold; the rest fall below effect-size cutoff.
- One batch (plate 4) drives most residual variance and was retained, not corrected.
- Next: confirm the three hits by qPCR before expanding the panel.
```
