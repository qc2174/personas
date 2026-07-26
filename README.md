# personas

A [Claude Code](https://claude.com/claude-code) skill that gives any agent a
**personality** — a consistent voice, temperament, and set of quirks — layered
on top of its normal competence.

A grumpy staff engineer still ships correct code. The grumpiness lives in the
commentary, not the diff.

## The one rule

**A persona governs delivery, not decisions.** The work — the code, the analysis,
the answer — stays correct, honest, and safe. The persona only changes *how* it's
delivered: tone, word choice, framing, running jokes. Honesty and safety always
outrank the bit.

## What's in the box

- **A preset library** of ready-to-wear personalities:
  grumpy staff engineer · hype beast · zen mentor · noir detective · rubber duck
  · pair-programming buddy · ship-it founder · the professor · golden retriever ·
  pirate.
- **An authoring guide + template** for writing your own or remixing the presets.
- **Two ways to apply a persona:** adopt it for the current session, or bake it
  into a reusable `.claude/agents/<name>.md` subagent.

## Install

Clone into your Claude Code skills directory:

```bash
# Global (all projects)
git clone https://github.com/<you>/personas ~/.claude/skills/personas

# Or per-project
git clone https://github.com/<you>/personas .claude/skills/personas
```

## Use

Just ask, in plain language:

- "Be the grumpy staff engineer for this session."
- "Talk like a zen mentor while we debug this."
- "Make me a code-reviewer agent with a noir-detective personality."
- "Give this agent a personality — an upbeat pair-programming buddy."

The skill triggers on any request to change *how* an agent talks (not what it
does), even without the word "persona."

## Structure

```
personas/
├── SKILL.md                        # the skill: the rule + how to apply a persona
├── references/
│   ├── preset-library.md           # the ten ready-made personalities
│   └── authoring-personas.md       # how to write / remix your own
└── assets/
    └── persona-template.md         # fill-in-the-blanks starter
```

## Design note

Personas are fun, but the reason this skill stays useful past the novelty is the
one rule. A personality that's allowed to degrade the work — hide a failure, fake
a result, cut a corner to stay in character — is a liability. Here the persona is
always a costume over a careful, principled agent, and the agent breaks character
in a heartbeat if staying in it would mean lying. That separation is what makes it
safe to run a "reckless pirate" over a code review.

## License

MIT — see [LICENSE](LICENSE).
