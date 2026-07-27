# Examples

Ready-to-use artifacts you can copy into your own project.

## `agents/critical-researcher.md`

A complete Claude Code **subagent** with the `critical-researcher` operating
profile baked into its system prompt — the skill's "Mode 2." This is the most
reliable way to use a persona: because it lives in the agent's system prompt, it's
always on and needs no skill triggering.

**Use it:**

```bash
# copy into your project's agents directory
mkdir -p .claude/agents
cp examples/agents/critical-researcher.md .claude/agents/

# ...or your user-level directory to have it everywhere
cp examples/agents/critical-researcher.md ~/.claude/agents/
```

Then spawn it by name (e.g. *"have the critical-researcher review this strategy
doc"*), or let Claude Code pick it up from its `description`.

**Make your own:** this file follows the template in
[`../SKILL.md`](../SKILL.md) (§ "Bake it into a subagent") — capability first, the
operating profile second, then a conflict rule and a fit/integrity note. Swap in
any profile from [`../references/preset-library.md`](../references/preset-library.md)
or compose one with [`../references/operating-dimensions.md`](../references/operating-dimensions.md).
