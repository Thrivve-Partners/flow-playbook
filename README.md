# Flow Playbook

Practices, not frameworks. Things that actually work when you try them on Monday morning.

This is a collection of flow-based practices, guides, and tooling built from 25+ years of consulting, coaching, and cleaning up messes. Everything here has been used with real teams in real organisations. Nothing is theoretical.

## What's in here

### Practices

The what and the how. Structured enough to start with, open enough to adapt.

| Practice | What it is |
|----------|-----------|
| [Flow Check-In](practices/flow-check-in.md) | A daily conversation structure for reading your system's health — three lenses, clear escalation, five minutes |

More coming.

### Skills

Claude Code skills for applying and evaluating flow practices. Install them into your project or globally and use them directly from your AI assistant.

| Skill | What it does |
|-------|-------------|
| [flow-checkin-effectiveness](skills/flow-checkin-effectiveness/) | Evaluates a standup transcript against the Flow Check-In standard. Returns what's working, what's missing, specific coaching opportunities, and a 0–10 effectiveness score with breakdown |

See [Installing Skills](#installing-skills) below.

## How to use this

Take what's useful. Adapt it to your context. These aren't templates to follow blindly — they're starting points for teams building their own practices.

If something doesn't fit, change it. If it does fit, make it yours.

## Installing Skills

Skills are Claude Code skill files. To install one:

1. Copy the skill folder (e.g. `skills/flow-checkin-effectiveness/`) into your Claude Code skills directory:
   - **macOS/Linux:** `~/.claude/skills/`
   - **Windows:** `%USERPROFILE%\.claude\skills\`
   - **Project-level:** `.claude/skills/` at the root of your project

2. Restart Claude Code or reload skills

3. Trigger the skill by describing what you want — e.g. *"Score this standup transcript"* or *"Analyse this flow check-in"*

Each skill folder contains a `README.md` with full installation and usage instructions.

## Who this is for

Delivery managers, product managers, team leads, and anyone trying to build flow-based ways of working without drowning in framework dogma. The skills are for teams that want to use AI tooling to embed and evaluate those practices — not to replace the coaching, but to make the feedback loop faster.

## Contributing

If you've adapted something here and it worked (or didn't), open an issue. The best version of any practice is the one that's been pressure-tested by practitioners.

## About

This playbook is maintained by [Thrivve Partners](https://thrivve.partners). We help organisations install flow as a strategy — building capability, not dependency.

---

*The goal is competency that remains after we leave. This repo is part of that.*
