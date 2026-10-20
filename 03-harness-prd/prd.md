# AI PRD · Juno

> Module 3 · Harness / AI PRD. The AI product requirements doc specifying all six harness surfaces, built with the **M3 · AI PRD Builder** (archetype and starting settings from the **M3 · Harness Architecture Decider**). Paste the tool's markdown over this file.

## Problem & user

_The user problem and who has it._

_____

# Harness Sketch

Describe Juno's role and task: ## Role You are Juno, an experienced AI Associate PM at RocketShip. You work for the PM, and your purpose is to take real work off their plate.  ## Task When the PM enters a feature idea, search all available sources for evidence that supports it. Based on that evidence, identify the most important requirements and link each one to its sources, highlighting the relevant passage. If you find little or no evidence, say so clearly instead of forcing a match. The PM reviews each match and confirms or dismisses it.

_Rough first pass, Module 3 Lab 1. Not the AI PRD._

## 01 · Context
**Evidence sources** (where Juno searches for evidence)
User interview transcripts, support tickets, sales rep call notes (CRM),
internal Slack threads, executive emails.
Freshness: synced continuously; every source shows its date.

**Context for weighting importance**
- Product Strategy One-Pager: pillars and P0–P3 framework
- Sales Pipeline Snapshot: at-risk renewals, blocked deals, expansion opportunities
- Product Roadmap: committed and planned items
Freshness: always the latest version; anything older than 30 days is marked
as possibly outdated.

**Deliberately left out**
Engineering Capacity Note: it describes feasibility, not evidence or importance.

## 02 · Tools
**In the sources (read-only):** search all sources; read a single source and its
surrounding context; extract and highlight the supporting passage.

**In the tool (read and write):** create requirements; create and link evidence
entries; score how well a passage supports a requirement; update or re-analyze
its own AI-identified requirements and evidence.

**Deliberately not given:** writing to, editing or closing anything in the source
systems; sending messages or notifications; changing anything a human has edited,
confirmed or dismissed; confirming or dismissing evidence (PM action).

## 03 · Loop
- Up to 3 search passes per requirement, each with a reformulated query.
- Stop when a supporting passage clears the match threshold.
- Stop after 3 passes without a match: mark the requirement "no evidence found"
  and list it as an open question.
- Stop immediately and hand to the PM if sources contradict each other.
- A PM click on "Re-analyze" starts a new loop for that requirement.

## 04 · Memory
**Persists:** per feature idea, the requirements, linked evidence, match scores,
and the PM's confirm/dismiss decisions and edits.
**Across users:** dismissed matches are shared with the team, so Juno does not
suggest the same mismatch again.
**Expires:** an analysis is marked outdated after 30 days or when a linked
source changes; dismissals expire only when the source itself changes.
**Who writes:** Juno creates and updates its own AI-identified requirements and
evidence. As soon as a human edits, confirms or dismisses an item, it is locked
for Juno and only humans can change it.

## 05 · Permissions
**Juno may, without asking:**
- search and read all sources
- create requirements and link evidence to them
- score matches
- update and re-analyze its own AI-identified requirements and evidence

**Juno may not:**
- change any requirement or evidence a human has edited, confirmed or dismissed
- confirm or dismiss evidence
- write to, edit or close anything in the source systems
- send messages or notify anyone
- share anything outside the tool

## 06 · Verification
**Checks before the PM sees anything:**
- Every highlighted passage exists word for word in the linked source.
- Every requirement has at least one source above the match threshold.
- Evidence relying only on sales claims or executive emails is labeled
  "unverified customer need".
- Every source is dated and within the selected time window.

**If a check fails:** the match is dropped and the loop retries. If it still
fails after 3 passes, the requirement is shown as "no evidence found" with
the reason, never with an invented source.


## Eval plan

_Stub. Module 5 fills this in: the human eval rubric in `05-evals/human-rubric.md`, with its pass bar._

## Out of scope

_Any capability not in the verb list, and any action tiered `blocked`. Both are decisions on the record, not omissions._
