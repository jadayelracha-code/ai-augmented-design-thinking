# AI-Augmented Human-Centered Design Thinking

> A working framework for running design thinking with AI as a thinking partner, not a replacement for human empathy or judgment. Structured as an 8-phase journey across two diamonds: first solve the right problem, then solve the problem right.

**Status:** 🚧 In progress

---

## The core idea

Design thinking is a human-centered process. AI doesn't change that goal. It changes the *speed and breadth* at which you can do the supporting work, synthesizing messy interview notes, surfacing patterns you might miss, generating more idea variations, drafting prototype copy in seconds.

Used well, AI removes grunt work so you spend more time on judgment. Used badly, it manufactures the *feeling* of insight without the substance.

The guiding principle: **AI handles volume, humans hold judgment.**

---

## The journey: 8 phases, two diamonds

```
Kick Off ──▶ [ 🔷 PROBLEM SPACE ]  ──▶  [ 🔶 SOLUTION SPACE ]  ──▶ Pitch
  Design      Understand · Observe        Ideate · Prototype       Stakeholder
  Challenge   · Point of View             · Test                   Presentation
```

### Kick Off — Design Challenge
Scope the challenge, set boundaries, and prepare before diverging. [`/kickoff`](./kickoff)

### 🔷 Problem space — *are we solving the right problem?*
| Phase | Folder | Focus |
| --- | --- | --- |
| Understand | [`/problem-space/understand`](./problem-space/understand) | Understanding the problem |
| Observe | [`/problem-space/observe`](./problem-space/observe) | Understanding the user |
| Point of View | [`/problem-space/point-of-view`](./problem-space/point-of-view) | Defining the point of view |

### 🔶 Solution space — *are we solving the problem right?*
| Phase | Folder | Focus |
| --- | --- | --- |
| Ideate | [`/solution-space/ideate`](./solution-space/ideate) | Finding ideas |
| Prototype | [`/solution-space/prototype`](./solution-space/prototype) | Developing prototypes |
| Test | [`/solution-space/test`](./solution-space/test) | Obtaining feedback |

### Pitch — Stakeholder Presentation
Turn the validated solution into a compelling case. [`/pitch`](./pitch)

---

## How to use this repo

Each phase folder contains three files:

- **`GUIDE.md`** — the method, the tools, where AI genuinely helps, and where it will mislead you. Copy-and-adapt prompts are embedded throughout, and each guide ends with a "before you move on" checklist.
- **`TEMPLATE.md`** — a fill-in worksheet for capturing that phase's outputs.
- **`AGENT.md`** — a portable AI agent for that phase (see below).

### Meet Rasha 👋

Every phase ships with an agent named **Rasha**, your design thinking coach. She's the same persona across all eight phases, so you get one consistent guide through the whole journey.

Rasha is deliberately built to be **friendly but not soft**. She:
- Interviews you **one question at a time** rather than dumping a checklist
- Won't accept a vague answer — she'll help you sharpen it before moving on
- Offers **three options with an honest opinion** when you're stuck
- **Stays in her lane** — each phase's agent works only on that phase's template, and will tell you when a question belongs to a different phase
- Pushes back when your thinking is weak, and says so plainly

**Tool-agnostic by design.** Each `AGENT.md` is plain markdown containing a system prompt. Copy it into Claude, ChatGPT, Cursor, Windsurf, opencode, or anything else. No proprietary config, no lock-in.

**To use one:** open the phase's `AGENT.md`, copy the system prompt block, paste it into your AI tool of choice, and start talking. Capture the outputs in that phase's `TEMPLATE.md`.

---

## Who this is for

Product managers, designers, founders, and teams who want to move faster through design thinking without hollowing out the human core that makes it work.

It works solo too — the agents are built to challenge you when there's no one else in the room to do it.

---

## Credits & honesty

The 8-phase structure and tool selection in this repo are **inspired by** *The Design Thinking Toolbox: A Guide to Mastering the Most Popular and Valuable Innovation Methods* by Michael Lewrick, Patrick Link & Larry Leifer (Wiley, 2020). That book catalogs 50 design thinking tools; this repo adapts the phase structure and adds an original AI-augmentation layer on top.

The "double diamond" framing originates with the UK Design Council. Jobs / pains & gains language draws on Jobs-to-be-Done and the Value Proposition Canvas. Design thinking has many schools (IDEO, Stanford d.school, and others); adapt freely.

This framework reflects one practitioner's working approach, not an official standard.

---

⭐️ If this saves you time, a star helps others find it.
