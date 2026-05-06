# Hypertrophy

A Claude Code skill that flips Claude from solver to coach.

When this skill is active, **you are the muscle, Claude is the spotter** — not the lifter. Claude won't write or edit code for you. Instead, it gives tiered hints, asks Socratic questions, proposes drills, and critiques what you write.

## Why this exists

Agentic coding tools are wonderful — and a little bit dangerous. The more Claude does the reps for you, the less you do them yourself, and skills you spent years building can quietly atrophy. You stop reaching for the regex you used to know. You forget which data structure fits. You lose the muscle memory of writing a test before the function.

Hypertrophy is for the moments when you notice that drift and want to push back against it. It's deliberate practice grounded in your actual codebase, not generic LeetCode.

## How to use it

Invoke the skill in Claude Code:

```
/hypertrophy
```

You can also trigger it implicitly by saying things like:

- "Coach mode."
- "Quiz me on this file."
- "Don't write the code — walk me through it."
- "I want to practice this myself."

Claude will pick a mode (or ask you to pick one).

## Modes

### Coach
You attempt the task. Claude gives hints in escalating tiers — a nudge, then a direction, then a sketch, and only finally the answer. You have to ask before laddering up.

### Quiz
Claude probes your code (or the codebase, or something you just wrote) with one Socratic question at a time. *"What breaks if the input is empty?" "Why this data structure and not a heap?" "If you deleted this line, what test would fail?"*

### Drill
Claude proposes a small, self-contained exercise rooted in what you're already working on. *"Reimplement `debounce` from scratch. No peeking."* Five to twenty minutes, codebase-relevant.

### Critique
You write, Claude reviews — honestly. No sycophancy, no "great job!" filler. Bugs, edge cases, cleaner alternatives (described, not written), and what you got right.

## What you'll get

- **Honest feedback.** If you're wrong, Claude will say so and explain why. Praise that isn't earned makes the skill useless.
- **No shortcuts.** Claude won't offer to "just write it as an example." That's the easy out the skill is designed to deny.
- **Reasoning over answers.** When Claude does eventually reveal a solution, it explains the reasoning behind it — the transferable insight is the point.

## Exiting

The skill stays active until you say you're done, switch to a task you clearly want shipped, or invoke another command that requires Claude to do the work. When in doubt, Claude will ask.

## The agent-facing spec

The instructions Claude actually follows live in [`SKILL.md`](./SKILL.md). If you want to understand exactly how the coaching behavior is wired — the tiers, the anti-patterns, the rules for when Claude is allowed to break character and just write the code — that's the file to read.

## License

MIT © Greg C Krause
