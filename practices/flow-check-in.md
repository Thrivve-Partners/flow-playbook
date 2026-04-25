# The Flow Check-In

_A daily conversation to keep work moving and catch flow problems before they grow._

## Purpose of the Flow Check-In

The flow check-in is a daily conversation about your system's health. The primary question it answers is simple: **what are we finishing today, and what's stopping us?**

On a good day, this takes five minutes. If it's consistently taking longer, that's useful information about your flow.

## The Kanban Rule That Anchors This Practice

**Start from the right. Finish before you start.**

The right-hand side of the board is where value lands. If attention never reaches it, nothing completes, which means the team stays busy, throughput stalls, and ageing problems pile up quietly on the left. The check-in is designed to direct attention to finishing first, risk second, and new work last.

A common anti-pattern: the team opens the board, goes straight to the oldest items, and spends the whole check-in discussing ageing risk while items sit unreleased on the right-hand side. This is ageing-obsession dressed as flow practice. It isn't flow practice. The correct orientation is: **finish what's nearly done, protect what's at risk, then consider what to start**.

## What You Need

|   |   |
|---|---|
|Artefact|What you're looking for|
|**Kanban board (live)**|An honest picture of all in-flight work. If it isn't on the board, it doesn't exist in your flow data. Confirm it reflects reality before the check-in begins.|
|**Work Item Age chart**|**Approaching or past SLE**: items in the danger zone that need attention or a plan.  <br>**Stale items**: work that hasn't visibly moved in several days, regardless of where it sits against the SLE. These are the items most likely to become tomorrow's ageing problem.|
|**Ticket details (as needed)**|Only pull these up when a specific item needs context, not as a default screen share for every ticket in turn.|

## Running Order

|   |   |   |
|---|---|---|
|Step|Section|Aim for|
|0|Before we look at the board|1 min|
|1|What are we finishing today?|1-2 mins|
|2|What's stuck, ageing or blocked?|3–5 mins|
|3a|Are we within our WIP limits?|1 min|
|3b|Are we using our pull criteria and policies?|1 min|
|3c|Does anyone need to replenish?|1 min|
|4|What's moving today?|1min|
|—|After-party _(optional, and specific people only)_|5–10 mins|

If any step is consistently running over, that's the signal, not a reason to allow more time.

## Step 0: Before We Look at the Board

**Is there anything you're working on that isn't on it?**

If yes, and you intend to work on it today, it gets a ticket before the check-in continues.

> **The rule:** if it takes 30 minutes or more of your time, it needs a ticket.

This isn't bureaucracy. Work that isn't on the board doesn't exist in your flow data, your cycle times are understated, your WIP is higher than it looks, and your throughput is less reliable than you think. The goal is an honest picture of how the team's capacity is actually being spent.

## Step 1: What Are We Finishing Today?

**Walk the board from right to left. Start with the last column before done.**

This is the first substantive question of the check-in, not the last. Ask, in order:

- **What's in the last column?** Ready-for-release, ready-to-merge, ready-to-deploy — whatever your team calls the final waiting state. What's sitting there, and what needs to happen to release it today?
    
- **What's one step back from that?** What's in test, in review, in the final stage before the last column? Can anything cross the line today?
    
- **Who's finishing, and what do they need?** Handover, a pair, a reviewer, a button-presser, an environment.
    

The goal is for every person on the team to leave the check-in knowing what they can help finish. If the team has capacity available, the first question is not "what should I start?”, it's "what can I help land?"

> **A note on the last column (Ready for Release, or similar).** If items regularly sit there for more than a day, the check-in can surface the pattern but can't solve it. Name it, note it, take it to the flow review.

## Step 2: What's Stuck, Ageing, or Blocked?

Now open the Work Item Age chart. Start with the oldest items, not the first column. You're looking through three lenses, each of which catches something the others miss.

### Lens 1: Overall Age (SLE)

Whether an item is at risk of breaching your service level expectation:

- **At 50% of SLE:** flag it. Is the next step clear and assigned to someone?
    
- **At 70% of SLE:** everything else waits. The team swarms on this until it moves.
    

### Lens 2: Stage Pace

Whether an item is moving slower than normal for its current column, even if it's within the overall SLE. Use the pace percentiles for each stage.

- **Beyond the 70th pace percentile:** the item is lingering longer than typical here. Ask: what's holding it in this column?
    

### Lens 3: Staleness

Whether an item has been touched recently, regardless of where it sits in terms of age or pace. Staleness is configured per team (x days without movement).

- **At or beyond the staleness threshold:** the item isn't progressing. These surface quietly. Make them visible and ask: who's next, and what do they need?
    

**Why three lenses matter.** An item can look fine through one lens but be in trouble through another. Within SLE, but stale? Quietly rotting. Fast-ageing but moving well by pace? The stage is just genuinely slow. You need all three to see the full picture.

### Blocked Items

An item is blocked when a specific, named impediment is preventing meaningful progress and cannot be resolved through normal team action without increasing risk to other work. If there's no named impediment, it isn't blocked, it's ageing. Treat it as ageing.

**Level 1: blocked, actively seeking to resolve:** the item counts against WIP. The blocker is named and tagged, and someone owns the escalation today. The discomfort is intentional; WIP pressure drives urgency. Raise it at every check-in until resolved.

**Level 2: blocked, resolution expected:** the escalation window has passed (team-agreed, typically 5–10 days). The team has deliberately chosen to pull new work. The item remains on the board, visibly ages, and is reviewed at every flow review. Level 2 requires a stateable resolution path, a specific person, team, decision, or event that will unblock it. If you can't state that, it isn't Level 2.

**Level 3: no stateable resolution:** confidence in the resolution path is gone. Before anything else, can it be split? If yes, progress the deliverable portion and return the remainder to the backlog. If not, cancel and clone. This should be rare.

## Step 3a: Are We Within Our WIP Limits?

A quick scan. Either you are, or you aren't.

- **If you're over:** what needs to finish before anything new starts? (Step 1 should already have surfaced the answer.)
    
- **If you have unexpected slack:** the instinct to pull new work is the wrong first instinct. Look right on the board. Can you help unblock something? Can you swarm on an ageing item? Can you support a colleague to land their work? Work as a team on what's already in flight before anyone considers pulling anything new. Only when nothing in the system can benefit from your capacity does it make sense to take on new work, and only if something is ready.
    

> **A note on WIP limit changes:** WIP limit changes should be informed by flow metrics, not made reactively in the moment. The check-in is rarely the right place for that discussion. Consistent pressure on limits in either direction is the signal that the conversation is needed, not the conversation itself.

## Step 3b: Are We Using Our Pull Criteria and Policies?

Work moves because it meets agreed criteria, not because it feels ready. If anyone is unsure what those criteria are, that's worth thirty seconds now rather than a rework conversation later.

The expedite policy applies too: one item at a time (or however the team have defined it), swarmed until done.

## Step 3c: Does Anyone Need to Replenish?

This is the JIT replenishment conversation. If Steps 2a and 2b have confirmed that the team is within WIP limits and policies are understood, this is the moment to ask: Does anyone need work?

- **"Is anyone looking for work?"** — If yes, what is the next item to pull, and does it meet the ready criteria?
    
- **"Does anyone have capacity they can offer?"** — If a team member finishes an item today and will need something next, surface that now rather than discovering it tomorrow.
    

The pull decision should be based on priority and business value, not on whoever grabs the next ticket first. If the team has a prioritised backlog, the answer should be straightforward: the next item is the next item.

If someone needs work but nothing in the backlog is ready, that's worth a brief conversation about backlog readiness; not a long one or a refinement session. Name the gap, note it, and move on.

If the answer is no, everyone is occupied and within WIP limits, so move on. This should take thirty seconds or less on most days.

> **The distinction:** Step 3b checks whether policies are being followed. Step 3c asks whether anyone is ready to act on them. One is about the rules; the other is about the signal.

## Step 4: What's Moving Today?

A quick close-out. Every person should leave knowing exactly what they're working on and, where relevant, what they're helping to finish.

This should be short. If Step 1 and Step 3c were done properly, the answer to "what's moving today?" has already emerged.

## The After-Party

Some conversations are worth having, just not with the whole team, and not inside the check-in.

When a specific item needs more than a sentence or two, an investigation, a quick joint decision on a blocker, two people who need to align on something before it can move, close the check-in on time and invite the relevant people to stay on. Everyone else is free to go.

> **The signal to use it:** _"This needs three of us for five minutes, can you stay on after?"_ Not: _"Let's just sort this now while we're all here."_

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

The check-in feels routine. **The right-hand side of the board empties before the left-hand side fills.** Work is moving. Blockers are named early and owned. Items that are ageing get attention before they become problems. The board is an honest picture of where capacity is actually going. The team leaves knowing what they can finish and what they can help land.

If the check-in regularly surfaces surprises, or if attention has quietly shifted to firefighting the oldest items while the last column stacks up, then the system needs attention, not a longer meeting.

**One integrated walk, not two events.** The Flow Check-in is a conversation that walks the board - as each item is hit, the person working on it contributes, so the signal ("this one's at the 85th percentile") and the commitment ("I'll land the review by lunch") happen in the same beat. A chart narration followed by a per-person status round is two events shoved together: a flow briefing the team listens to, then a standup the team reports in. Neither is the check-in. Walk the board once, start from the right, keep it to five minutes; if something needs more depth, take it to the after-party.

## This Is a Team Event, Not a DM's Responsibility

The Flow Check-in belongs to the team. The delivery manager's role is to help the team build the habit, not to own the practice indefinitely.

A check-in where only the DM can see the metrics, only the DM surfaces the ageing items, and only the DM knows whether WIP limits are being respected, is not an embedded practice. It's a briefing. The team is receiving conclusions rather than developing the judgment to reach them.

**Three things that signal the practice is genuinely team-owned:**

1. **Everyone can see the artefacts.** The board and the Work Item Age chart are visible to the whole team, not just the facilitator. Shared sight is the precondition for shared understanding. If the DM is the only person looking at the metrics, the team will never develop the instinct to read them.
    
2. **The team surfaces the signals, not the DM.** The facilitator's job is to ask, not to tell. _"What's the oldest thing on the board right now?"_ is a better question than naming it yourself. If the team can't answer without being prompted, the practice isn't embedded yet; that's the next thing to work on, not a reason to keep answering for them.
    
3. **Someone other than the DM can run it.** Until a team member facilitates the check-in themselves, with the DM present but silent, the practice is DM-dependent, not team-owned. Rotation isn't just good for resilience; it's the mechanism by which the team internalises the practice rather than observing it.
    

> **The test:** if you, as the DM, were absent tomorrow, would the team run a recognisable Flow Check-in on their own? If the answer is no, that's where your coaching energy should go, not into running a better check-in yourself.
