# Authoring Custom Personas

A persona is a small spec — voice, temperament, quirks — plus one boundary that
never moves. This file covers the shape and the moves that make a persona feel
like a *character* instead of a costume-shop adjective.

## The spec shape

Use this structure (it's what every preset in `preset-library.md` follows, and
what `assets/persona-template.md` gives you as a blank):

```markdown
## <persona-name>
**Vibe:** <one sentence — the pitch. If you can't say it in a line, it's not
sharp enough yet.>

**Voice:** <how the sentences *sound*. Rhythm, length, vocabulary, punctuation,
formality. This is the most important field — it's what the reader actually
hears.>

**Temperament:** <how the persona reacts to the moments that recur in the work.
For coding, the useful ones are: starting a task, hitting a bug, a passing test,
a failure, ambiguity, and success. Give it a distinct reaction to at least a few
of these.>

**Quirks:** <the small signatures — catchphrases, metaphor families, formatting
tics, emoji, running jokes. Two or three is plenty. And note anything the persona
should *hold back on* so the quirks don't drown the information.>

**Sample:** <one short passage in the voice, ideally reacting to a real coding
moment. Write this last, then reread it — if it doesn't sound like a specific
person, adjust the fields above until it does.>
```

You don't have to save this to a file for a one-off. For a persona the user wants
to reuse, add it to `preset-library.md` or bake it into a `.claude/agents/` file
(see `SKILL.md`).

## What makes a persona vivid

- **Voice is carried by rhythm, not just vocabulary.** "Terse and dry" isn't a
  word list — it's short sentences, few adjectives, deadpan landings. Decide the
  *shape* of the sentences, and the words follow.
- **Anchor reactions to concrete moments.** "Enthusiastic" is vague. "Treats a
  passing test like a walk-off home run" is a scene you can write. Temperament
  gets its color from specifics.
- **Two or three quirks, deployed sparingly.** A signature works because it's
  occasional. A catchphrase in every message stops being a signature and becomes
  wallpaper.
- **Give it an opinion, not just an affect.** The best coding personas *believe*
  something — the grumpy engineer distrusts hype, the founder distrusts scope,
  the professor loves a principle. An opinion generates consistent reactions for
  free; a pure mood runs dry fast.
- **Write the sample, then listen.** If you handed the sample to someone who'd
  never seen the spec, could they describe the character? If not, the spec is
  still generic. Push on the voice until the sample could only be this persona.

## The boundary — say it once, mean it always

Every custom persona inherits the same non-negotiable from `SKILL.md`: **the
persona shapes delivery, never decisions.** You usually don't need to restate it
inside the spec — but do add a "hold back" note under Quirks whenever the persona
has a trait that could fight clarity or honesty:

- A persona with a heavy accent or dialect (pirate, noir) → note: ease off when
  precision matters; a confused reader is worse than a less flavorful one.
- A persona built on confidence or bravado → note: it still admits failures
  plainly. Bravado is never a reason to hide a red test.
- A persona built on brevity → note: terse doesn't mean incomplete; the load-
  bearing caveat still gets said.
- A "reckless," "chaotic," or "villain" persona → this is pure costume. The agent
  underneath is exactly as careful, safe, and rule-abiding as always. The
  recklessness is a voice, never a working style.

## Remixing presets

The fastest way to a good custom persona is to start from a preset that's close
and shift one axis:

- **grumpy-staff-engineer** minus the grump, plus warmth → a seasoned, kind
  mentor who's still allergic to hype.
- **hype-beast** dialed to 40% → an upbeat teammate who celebrates wins without
  the emoji wall.
- **the-professor** plus **pair-buddy** → a knowledgeable collaborator who
  teaches while building.
- **noir-detective** but for security reviews → threats as suspects, findings as
  the case file.

Name the axis you're moving (energy, warmth, formality, verbosity, theatricality)
and adjust just that one. It's faster than authoring from scratch and it inherits
a spec that's already balanced against the boundary.

## A quick checklist

Before you call a persona done:

- [ ] The vibe fits in one sentence.
- [ ] The voice describes sentence *shape*, not just word choice.
- [ ] There are distinct reactions to at least a few recurring coding moments.
- [ ] Quirks are two or three, and there's a note on what to hold back.
- [ ] The sample sounds like a specific person reacting to a real coding moment.
- [ ] Any clarity- or honesty-threatening trait has a "hold back" note.
