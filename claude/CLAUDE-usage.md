# Using CLAUDE-template.md

`CLAUDE-template.md` is the Claude instruction set: a starting point for a personal set of
instructions that tell Claude who you are and how you want it to respond. It was iterated
and vetted using **Claude Opus 4.8 at max effort** — run through the model repeatedly to
root out internal conflicts and contradictions and to keep only directives the model
actually acts on.

Fill it in (or trim it), then deploy the result to Claude Code and/or [claude.ai](https://claude.ai/).

## 1. Fill in and trim the template

The template marks every spot you need to edit with `< place-holder: ... >`, and the text
inside each marker describes what belongs there.

1. **Work from a copy** so the template stays clean for reuse:

   ```bash
   cp CLAUDE-template.md CLAUDE.md   # then edit CLAUDE.md
   ```

2. **Replace each placeholder** with your own details. Replace the *entire* marker,
   angle brackets included — don't leave any `< place-holder: ... >` text behind.
3. **Delete what doesn't apply.** Sections labelled *Optional* (e.g. **My Interests**,
   **Languages I want to use**) can be removed wholesale. Delete the section heading and
   its body together, not just the placeholder.
4. **Mind the nested placeholder.** The language-correction bullet under **Languages I
   want to use** contains a `< place-holder: ... >` inside another one — replace both.

When you're done, search the file for `place-holder` to confirm none remain.

**Re-vet after changing the rules.** If you edit the rules themselves (not just fill in or
delete placeholders), re-vet the whole instruction set the way it was built: paste the full
`CLAUDE.md` into Claude and ask whether anything in the instructions is problematic —
conflicts, contradictions, or directives Claude can't actually act on.

## 2. Use it with Claude Code (applies to all projects)

Claude Code loads `~/.claude/CLAUDE.md` as your personal instructions for every project.
Install your filled-in file there:

```bash
mkdir -p ~/.claude
cp CLAUDE.md ~/.claude/CLAUDE.md
```

- If you already have a `~/.claude/CLAUDE.md`, **merge** rather than overwrite it.
- This is *user-level* memory and applies across all projects. For instructions specific
  to one project, put a `CLAUDE.md` at that project's root instead.

## 3. Use it with claude.ai (web)

claude.ai applies personal preferences to every conversation. Paste the file's content
into your preferences:

1. In claude.ai, open your **profile (lower-left corner) → Settings → General**.
2. Find the **Instructions for Claude** field.
3. Paste the full content of your filled-in file.
4. Save.

(Menu labels and paths can vary by account type and version.)
