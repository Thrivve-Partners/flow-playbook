# Flow Check-in Effectiveness Skill

A Claude Code skill for evaluating standup (Flow Check-in) transcripts against flow standards and providing actionable coaching feedback.

## What This Skill Does

Evaluates standup transcripts and provides:
- **What's Working:** Evidence-based observations of effective practices
- **What Could Be Improved:** Gaps identified with specific evidence
- **Coaching Opportunities:** Actionable suggestions tied to flow standards
- **Effectiveness Score:** 0-10 rating with detailed breakdown
- **Score Trajectory:** Progress tracking across sessions to show whether practices are embedding

## Installation

### Option 1: Manual Installation (Recommended)

1. Copy the `flow-checkin-effectiveness/` folder to your Claude Code skills directory:
   - **macOS/Linux:** `~/.claude/skills/`
   - **Windows:** `%USERPROFILE%\.claude\skills\`

2. Restart Claude Code or reload skills

### Option 2: Project-level Installation

Place the `flow-checkin-effectiveness/` folder inside a `.claude/skills/` directory at the root of your project. Skills installed here are available when working within that project.

## Requirements

This skill references `practices/flow-check-in.md` from this repo as its evaluation standard. When installing:
- If you have the full `flow-playbook` repo locally, point the skill at the `practices/flow-check-in.md` file
- Alternatively, copy `flow-check-in.md` into your project and update the reference in `SKILL.md`

## Usage

### Basic Usage

```
Analyse this standup transcript: [path to transcript]
```

### With Context

```
Evaluate this flow check-in for [team name] (Week [N], SLE [X] days):
[transcript path or paste transcript]
```

### Other Trigger Phrases

- "Score this standup"
- "Review our daily standup"
- "How effective was this standup?"
- "Evaluate flow check-in effectiveness"

## Example Output

```markdown
## 1. What's Working

### Age-Based Walk Present (Ageing Items Identified — partial)
**Evidence:** "The oldest item we've got on the board is X — it's been in code review for 18 days."
**Why this matters:** The facilitator is walking the board oldest-first, which is the correct structure.
The missing piece is attaching SLE thresholds to give the observation meaning.

## 2. What Could Be Improved

### No Invisible Work Check (Invisible Work Check — absent)
**Evidence:** Not mentioned. The session moves directly to the board walk.
**Flow Check-in standard:** "Before we look at the board: is there anything you're working on
that isn't on the board? If it's taking 30 minutes or more of your time, it needs a ticket."

## 3. Coaching Opportunities

### Priority 1 — Add the Invisible Work Check as the Opening Sentence
- **When:** Before the board walk, immediately after opening the check-in
- **What to say:** "Before we look at the board — is anyone working on anything that's not on here?
  Anything more than 30 minutes needs a ticket."
- **Reference:** Flow Check-in — Before We Look at the Board

## 4. Effectiveness Score

**Score: 4.0/10** — **Developing**

| Area | Score | Notes |
|------|-------|-------|
| 1. Invisible Work Check | 0.0/1 | Not mentioned |
| 2a. Ageing Items Identified | 0.5/1 | Oldest item named; no SLE thresholds |
| 2b. Blocker Management | 0.5/1 | Blocker surfaced; no owner or classification |
| 2c. Swarming on Ageing Work | 0.5/1 | Priority switching present; not age-driven |
| 3a. WIP Limit Check | 0.5/1 | WIP status noted; not a full check |
| 3b. Pull Policy & Criteria | 0.0/1 | Pull decisions informal |
| 4. What's Moving Today | 0.5/1 | Reasonable picture; not a formal close |
| 5. Pattern Recognition | 0.0/1 | Not present |
| 6a. Routine Feel & Honest Board | 0.5/1 | Functional; some social drift |
| 6b. Clear Next Steps | 0.5/1 | Named per-person commitments; trailing close |
| **Total** | **4.0/10** | |

**Key Priority for Next Session:**
1. Add the invisible work check as the opening sentence — one sentence, every session
2. Move the age walk to the start and attach the SLE numbers
```

## Scoring Framework

The skill evaluates 6 core areas (10 points total):

| Area | Points |
|------|--------|
| 1. Invisible Work Check | 1 |
| 2a. Ageing Items Identified | 1 |
| 2b. Blocker Management | 1 |
| 2c. Swarming on Ageing Work | 1 |
| 3a. WIP Limit Check | 1 |
| 3b. Pull Policy & Criteria | 1 |
| 4. What's Moving Today | 1 |
| 5. Pattern Recognition | 1 |
| 6a. Routine Feel & Honest Board | 1 |
| 6b. Clear Next Steps | 1 |
| **Total** | **10** |

### Interpretation

- **8-10:** Excellent — Standards well embedded, minor refinements only
- **6-7:** Good — Core practices present, needs consistent application
- **4-5:** Developing — Some practices emerging, significant coaching needed
- **2-3:** Early — Few practices present, intensive coaching required
- **0-1:** Not Present — Standards not yet introduced

## Score Trajectory

The skill maintains a score trajectory table across sessions, making it easy to see whether practices are embedding or remain facilitator-dependent:

| Condition | Typical Score |
|---|---|
| Coach modelling all practices | 7–9 |
| Facilitator present, practices in frame | 5–7 |
| Facilitator present, delivery-focused | 3–5 |
| Facilitator absent, team self-organising | 2–4 |

A significant drop in score when the regular facilitator is absent is a key diagnostic signal: it indicates practices are person-dependent rather than team-owned.

## Files

- **SKILL.md** — Main skill instructions with YAML frontmatter (loaded by Claude Code)
- **references/flow-checkin-rubric.md** — Detailed scoring criteria and examples for each evaluation area
- **README.md** — This file (installation and usage guide)

## Related

- **practices/flow-check-in.md** — The Flow Check-in standard this skill evaluates against
- **skills/lean-coffee-summary/** — Companion skill for Lean Coffee session summaries

## Version

v1.1.0 — March 2026
- Added score trajectory guidance and facilitator-dependency diagnostic
- References updated to point to `practices/flow-check-in.md` in this repo
- Evri-specific example paths removed; generic examples added
