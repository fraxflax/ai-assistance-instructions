# ai-assistance-instructions

Instructions and configuration for AI coding assistants.

## Using CLAUDE-template.md

`CLAUDE-template.md` is a starting point for a personal set of instructions that tell an
AI assistant who you are and how you want it to respond. Fill it in (or trim it), then
deploy the result to Claude Code and/or claude.ai.

### 1. Fill in and trim the template

The template marks every spot you need to edit with `< place-holder: ... >`, and the text
inside each marker describes what belongs there.

1. **Replace each placeholder** with your own details. Replace the *entire* marker,
   angle brackets included — don't leave any `< place-holder: ... >` text behind.
2. **Delete what doesn't apply.** Sections labelled *Optional* (e.g. **My Interests**,
   **Languages I want to use**) can be removed wholesale. Delete the section heading and
   its body together, not just the placeholder.
3. **Mind the nested placeholder.** The language-correction bullet under **Languages I
   want to use** contains a `< place-holder: ... >` inside another one — replace both.
4. **Work from a copy** so the template stays clean for reuse:

   ```bash
   cp CLAUDE-template.md CLAUDE.md   # then edit CLAUDE.md
   ```

When you're done, search the file for `place-holder` to confirm none remain.

### 2. Use it with Claude Code (applies to all projects)

Claude Code loads `~/.claude/CLAUDE.md` as your personal instructions for every project.
Install your filled-in file there:

```bash
mkdir -p ~/.claude
cp CLAUDE.md ~/.claude/CLAUDE.md
```

- If you already have a `~/.claude/CLAUDE.md`, **merge** rather than overwrite it.
- This is *user-level* memory and applies across all projects. For instructions specific
  to one project, put a `CLAUDE.md` at that project's root instead.

### 3. Use it with claude.ai (web)

claude.ai applies personal preferences to every conversation. Paste the file's content
into your preferences:

1. In claude.ai, open your **profile (lower-left corner) → Settings → General**.
2. Find the **Instructions for Claude** field.
3. Paste the full content of your filled-in file.
4. Save.

(Menu labels and paths can vary by account type and version.)
