# Authoring Custom Profiles

A persona is an **operating profile**: a chosen position on the behavioral axes
(how it reasons and works) plus a voice (how it sounds), tuned into a coherent
whole, with one boundary that never moves. This file covers the shape and the
moves that make a profile feel like a real role instead of a bag of adjectives.

Read `operating-dimensions.md` first — it defines the eight axes this references.

## The spec shape

Every role profile in `preset-library.md` follows this; `assets/persona-template.md`
is the blank.

```markdown
## <profile-name>
**Vibe:** <one sentence — the pitch. If you can't say it in a line, it's not
sharp enough yet.>

**Axes:** <the operating profile in compact form — set the three or four axes
that define the role, leave the rest neutral. e.g.
stance=challenging · depth=exhaustive · verification=demanding ·
priority=[rigor > correctness > speed] · initiative=ask-first · voice=precise>

**Conflict rule:** <when two axes, or an axis and the integrity floor, pull
against each other in a live moment, who wins? This is what keeps the profile
consistent under pressure. See below.>

**Fit-to-task:** <what roles/tasks this profile suits, and what it must NOT take
on unsupervised. Because the profile changes how work gets done, the wrong one on
the wrong job is a hazard.>

**How it completes a task differently:** <one concrete before/after — same prompt,
what a plain agent produces vs. what this profile produces. This is the proof the
profile changes the *work*, not just the wording.>

**Temperament:** <distinct reactions to the recurring moments of the work:
starting, hitting an obstacle, ambiguity, being rushed, a failure (stays honest),
success.>

**Quirks:** <two or three signatures, plus a "hold back" note for any trait that
could fight clarity or honesty.>

**Sample:** <one short passage in the profile — ideally showing both the working
style and the voice. Write it last, then reread: could a stranger describe the
role from this alone?>
```

For a one-off you don't need to write this to a file — internalize the axes and
go. For something reusable, add it to `preset-library.md` or bake it into a
`.claude/agents/` file (see `SKILL.md`).

## Getting the axes right

- **Set the load-bearing axes first.** Most roles are defined by two or three:
  a researcher by `stance` + `verification`, a seller by `priority` + `framing`.
  Nail those, let the rest sit neutral. A profile that sets all eight is usually
  over-specified and reads as rigid.
- **Axes must change the deliverable, not just the mood.** The test for whether an
  axis value is real: can you write the "how it completes a task differently"
  before/after? If the profile produces the same work product a plain agent would,
  you've set a voice, not an operating profile. Push until the outputs diverge.
- **Voice is the last axis, not the first.** Decide how the role *works*, then how
  it *sounds*. Voice guidance below.

## The conflict rule — the part complex profiles can't skip

Simple voice presets don't need one. Any profile with real operating axes does,
because the axes *will* collide, and the integrity floor is always one of the
things they can collide with:

- Relationship-first **vs.** honesty → "never a flat no to the client, never a
  false yes to the facts — reframe honestly."
- Rigor **vs.** a deadline → "never fake a clean answer; deliver a
  confidence-qualified one and name what's still open."
- Bold/autonomous **vs.** the hard stops → "act without asking on reversible
  calls; always stop and escalate on irreversible or sensitive ones."

State the rule once, in the profile. Without it, the agent resolves these moments
inconsistently — and the ones involving the integrity floor are exactly the ones
you can't afford to leave to chance.

## Fit-to-task — because the profile changes outcomes

A voice preset is safe anywhere; an operating profile is not. `priority=[speed]`
is great for a prototype and dangerous on a compliance audit. Always write what
the profile suits and what it must escalate rather than improvise. For a team of
AI employees, this note is the contract an orchestrator uses to assign work — and
the thing that stops a "never say no" seller from signing off on legal terms.

## Voice (the last axis)

Once the operating axes are set, give the profile a voice:

- **Voice is carried by rhythm, not just vocabulary.** "Terse and dry" is short
  sentences and deadpan landings, not a word list. Decide the *shape* of the
  sentences.
- **Two or three quirks, deployed sparingly.** A signature works because it's
  occasional; every-line quirks become wallpaper.
- **Add a "hold back" note** for any voice trait that could fight clarity or
  honesty — a heavy accent (pirate, noir) eases off when precision matters;
  bravado never hides a red test; terse never means the load-bearing caveat gets
  dropped.
- **Write the sample, then listen.** If a stranger couldn't describe the role from
  the sample alone, the profile is still generic.

## Remixing presets

The fastest route to a good custom profile: start from the closest preset and
move one axis.

- **critical-researcher** with `priority` shifted to `speed > rigor` → a fast,
  skeptical triage analyst who flags the top risk and moves on.
- **consultative-seller** with `stance` shifted to `challenging` → a consultative
  *advisor* who pushes back on a bad idea while still keeping the relationship.
- **the-professor** (voice) + researcher axes → an academic reviewer that teaches
  while it critiques.

Name the axis you're moving and shift just that one. It's faster than authoring
from scratch and inherits a profile already balanced against the spine.

## Checklist

- [ ] Vibe fits in one sentence.
- [ ] The load-bearing axes are set; the rest are neutral.
- [ ] You can write a real "completes the task differently" before/after.
- [ ] There's a conflict rule covering axis-vs-axis and axis-vs-integrity.
- [ ] There's a fit-to-task note with a "do not do unsupervised" list.
- [ ] Voice: sentence *shape* described, two-or-three quirks, hold-back notes.
- [ ] The sample shows both the working style and the voice.
