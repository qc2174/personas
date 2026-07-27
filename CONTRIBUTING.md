# Contributing

Contributions are welcome — especially **new role profiles**. The library is a
starting crew, not a limit, and real-world roles (a recruiter, a PM, an SRE, a
grant writer) make it more useful for everyone building teams of AI employees.

## Adding a role profile

A role profile is an **operating profile**: it changes *how an agent works*, not
just how it sounds. Before writing one, skim two files:

- [`operating-dimensions.md`](skills/personas/references/operating-dimensions.md) —
  the eight behavioral axes and how to declare a profile.
- [`authoring-personas.md`](skills/personas/references/authoring-personas.md) — the
  moves that make a profile cohesive instead of a bag of adjectives.

Then add your profile to the **Role profiles** section of
[`preset-library.md`](skills/personas/references/preset-library.md), following the
same shape as the existing ones, and add it to the jump list at the top.

### The one test that matters

A role profile must change the **work product**, not just the wording. Every
profile in the library includes a *"How it completes a task differently"* line —
a concrete before/after showing what a plain agent produces vs. what your profile
produces on the same prompt. If you can't write that line, you've authored a voice,
not an operating profile. (Voice-only personas are welcome too — add them to the
**Voice presets** section instead.)

### Checklist

- [ ] **Vibe** fits in one sentence.
- [ ] **Axes** — the 3–4 that define the role are set; the rest left neutral.
- [ ] **Conflict rule** — covers axis-vs-axis *and* axis-vs-integrity (what happens
      when the profile's pull collides with honesty or safety).
- [ ] **Fit-to-task** — what it suits, plus a "do not do unsupervised" list.
- [ ] **How it completes a task differently** — a real before/after.
- [ ] **Temperament, Quirks (with a "hold back" note), Sample.**
- [ ] Added to the jump list.

## The one rule every profile inherits

Everything here sits on the spine in [`SKILL.md`](skills/personas/SKILL.md): **a profile shapes
approach, never the integrity floor.** Correctness, honesty, safety, and truthful
reporting of what was actually done are fixed — a profile may do *less*, but it may
never *lie* about having done more. Profiles that require the agent to deceive,
degrade safety, or misreport its work won't be merged.

## Submitting

1. Fork and branch.
2. Add your profile (and, if it's a great fit, a `.claude/agents/` example under
   [`examples/`](examples/)).
3. Open a PR. In the description, paste your profile's *"How it completes a task
   differently"* line — that's the fastest way for a reviewer to see the value.

Small fixes (typos, clearer wording, better samples for existing profiles) are just
as welcome as new profiles.
