# Flow Check-In

_A daily conversation to keep work moving and catch flow problems before they grow._

## Purpose of the Flow Check-In

The flow check-in is a daily conversation about your system's health. On a good day, this takes five minutes. If it’s consistently taking longer, that’s useful information about your flow.

## What You Need

| Artefact                       | What you're looking for                                                                                                                                                                                                                                                                                                      |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Kanban board (live)**        | An honest picture of all in-flight work. If it isn't on the board, it doesn't exist in your flow data. Confirm it reflects reality before the check-in begins.                                                                                                                                                               |
| **Work Item Age chart**        | **Approaching or past SLE**: items in the danger zone that need attention or a plan. <br>**Stale items**: work that hasn't visibly moved in several days, regardless of where it sits against the SLE. These are the items most likely to become tomorrow's ageing problem. If nobody's mentioned it recently, ask about it. |
| **Ticket details (as needed)** | Only pull these up when a specific item needs context, not as a default screen share for every ticket in turn.                                                                                                                                                                                                               |

## Running Order

| Step | Section                                            | Aim for |
| ---- | -------------------------------------------------- | --------- |
| 0 | Before we look at the board                        | 1 min |
| 1 | What's stuck or ageing?                            | 3–5 mins |
| 2a | Are we within our WIP limits?                      | 1 min |
| 2b | Are we using our pull criteria and policies?       | 1 min |
| 3 | What's moving today?                               | 1–2 mins |
| — | After-party *(optional, and specific people only)* | 5–10 mins |

If any step is consistently running over, that's the signal, not a reason to allow more time.

## Step 0: Before We Look at the Board

**Is there anything you're working on that isn't on it?**

If yes, and you intend to work on it today, it gets a ticket before the check-in continues.

> **The rule:** if it takes 30 minutes or more of your time, it needs a ticket.

This isn't bureaucracy. Work that isn't on the board doesn't exist in your flow data, your cycle times are understated, your WIP is higher than it looks, and your throughput is less reliable than you think. The goal is an honest picture of how the team's capacity is actually being spent.

## Step 1: What's Stuck or Ageing?

Open the Work Item Age chart. Start with the oldest items, not the first column.
You're looking through three lenses, each of which catches something the others miss.
### Lens 1: Overall Age (SLE)

This tells you whether an item is at risk of breaching your service level expectation:

**At 50% of SLE:** flag it. Is the next step clear and assigned to someone?
**At 70% of SLE:** everything else waits. The team swarms on this until it moves.

### Lens 2: Stage Pace

This tells you whether an item is moving slower than normal _for its current column_, even if it's within overall SLE. Use the pace percentiles for each stage.

**Beyond the 70th pace percentile:** the item is lingering longer than typical here. Ask: what's holding it in this column?

### Lens 3: Staleness

This tells you whether an item has been touched recently, regardless of where it sits on age or pace. Staleness is configured per team (x days without movement).

**At or beyond the staleness threshold:** the item isn't progressing. These surface quietly. Make them visible and ask: who's next, and what do they need?

**A note on why three lenses matter**
An item can look fine on one lens and be in trouble on another. Within SLE but stale? Quietly rotting. Fast-ageing but moving well by pace? The stage is just genuinely slow. You need all three to see the full picture.

### Blocked Items

An item is blocked when a specific, named impediment is preventing meaningful progress and cannot be resolved through normal team action without increasing risk to other work. If there's no named impediment, it isn't blocked, it's ageing. Treat it as ageing.

**Level 1: blocked, actively seeking to resolve:** the item counts against WIP. The blocker is named, tagged, and someone owns escalation today. The discomfort is intentional, WIP pressure drives urgency. Raise it at every check-in until resolved.

**Level 2: blocked, resolution expected:** the escalation window has passed (team-agreed, typically 5–10 days). The team has deliberately chosen to pull new work. The item remains on the board, visibly ages, and is reviewed at every flow review. Level 2 requires a stateable resolution path, a specific person, team, decision, or event that will unblock it. If you can't state that, it isn't Level 2.

**Level 3: no stateable resolution:** confidence in the resolution path is gone. Before anything else, can it be split? If yes, progress the deliverable portion and return the remainder to the backlog. If not, cancel and clone. This should be rare.

## Step 2a: Are We Within Our WIP Limits?

A quick scan. Either you are, or you aren't.

- **If you're over:** what needs to finish before anything new starts?
- **If you have unexpected slack:** the instinct to pull new work is the wrong first instinct. The goal is finishing, not starting. Look right on the board. Can you help unblock something? Can you swarm on an ageing item? Can you support a colleague to get something across the line? Work as a team on what's already in flight before anyone considers pulling anything new. Only when nothing in the system can benefit from your capacity does it make sense to take on new work, and only if something is ready.

> **A note on WIP limit changes:** WIP limit changes should be informed by flow metrics, not made reactively in the moment. The check-in is rarely the right place for that discussion. Consistent pressure on limits in either direction is the signal that the conversation is needed, not the conversation itself.

## Step 2b: Are We Using Our Pull Criteria and Policies?

Work moves because it meets agreed criteria, not because it feels ready. If anyone is unsure what those criteria are, that's worth thirty seconds now rather than a rework conversation later.

The expedite policy applies too: one item at a time, swarmed until done.

## Step 3: What's Moving Today?

Confirm the team is clear on what progresses today. Every person should leave knowing exactly what they're working on.

If nothing obvious is ready to pull, that's worth a brief conversation about backlog readiness, not a long one.

## The After-Party

Some conversations are worth having, just not with the whole team, and not inside the check-in.

When a specific item needs more than a sentence or two, an investigation, a quick joint decision on a blocker, two people who need to align on something before it can move, close the check-in on time and invite the relevant people to stay on. Everyone else is free to go.

> **The signal to use it:** *"This needs three of us for five minutes, can you stay on after?"* Not: *"Let's just sort this now while we're all here."*

**The after-party is for:**
- Specific operational depth: a blocker that needs a quick decision, an investigation that needs two people to look at it together, a handover that's easier live than async.
- Conversations relevant to two or three people, not the whole team.
- Five to ten minutes. Time-boxed.

**The after-party is not for:**
- Systemic patterns, those go to the flow review (see below).
- Design or architecture decisions, those need the right people and the right time, not whatever is left over after standup.
- Anything that the whole team should hear, if everyone needs to know, it belongs in the check-in, not after it.

If the after-party is becoming a regular fixture, or lasting longer than ten minutes, that's a signal: either the check-in is surfacing things too late, or the right conversations aren't happening elsewhere. Name it and take it to the flow review.

## When the Conversation Goes Deeper

Most questions should have short answers. When they don't, that's the signal.

Common triggers for a longer conversation:
- Multiple items ageing simultaneously across the same stage
- The same blocker types are surfacing repeatedly
- WIP consistently at or over the limit
- Backlog regularly empty

These patterns belong in your flow review cadence. Note them, name them, and move on. Solving them in the daily check-in is the wrong conversation in the wrong room.

## What Good Looks Like

The check-in feels routine. Work is moving. Blockers are named early and owned. Items that are ageing get attention before they become problems. The board is an honest picture of where capacity is actually going. The team leaves knowing exactly what the day looks like.

If the check-in regularly surfaces surprises, the system needs attention, not a longer meeting.

## This Is a Team Event, Not a DM's Responsibility

The Flow Check-in belongs to the team. The delivery manager's role is to help the team build the habit, not to own the practice indefinitely.

A check-in where only the DM can see the metrics, only the DM surfaces the ageing items, and only the DM knows whether WIP limits are being respected, is not an embedded practice. It's a briefing. The team is receiving conclusions rather than developing the judgment to reach them.

**Three things that signal the practice is genuinely team-owned:**

1. **Everyone can see the artefacts.** The board and the Work Item Age chart are visible to the whole team, not just the facilitator. Shared sight is the precondition for shared understanding. If the DM is the only person looking at the metrics, the team will never develop the instinct to read them.

2. **The team surfaces the signals, not the DM.** The facilitator's job is to ask, not to tell. *"What's the oldest thing on the board right now?"* is a better question than naming it yourself. If the team can't answer without being prompted, the practice isn't embedded yet; that's the next thing to work on, not a reason to keep answering for them.

3. **Someone other than the DM can run it.** Until a team member facilitates the check-in themselves, with the DM present but silent, the practice is DM-dependent, not team-owned. Rotation isn't just good for resilience; it's the mechanism by which the team internalises the practice rather than observing it.

> **The test:** if you, as the DM, were absent tomorrow, would the team run a recognisable Flow Check-in on their own? If the answer is no, that's where your coaching energy should go, not into running a better check-in yourself.
