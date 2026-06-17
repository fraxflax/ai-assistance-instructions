# Using LUMO-template.md

`LUMO-template.md` is the Lumo instruction set: a starting point for a personal set of
instructions that tell Lumo ([Proton's web assistant](https://lumo.proton.me/)) who you are
and how you want it to respond. It was iterated and vetted on 17 June 2026 in Lumo (launched 23 July 2025) — run through the
assistant to root out internal conflicts and contradictions and to keep only directives it
actually acts on.

Fill it in (or trim it), then deploy the result in Lumo (web).

## 1. Fill in and trim the template

The template marks every spot you need to edit with `< place-holder: ... >`, and the text
inside each marker describes what belongs there.

1. **Work from a copy** so the template stays clean for reuse:

   ```bash
   cp LUMO-template.md LUMO.md   # then edit LUMO.md
   ```

2. **Replace each placeholder** with your own details. Replace the *entire* marker,
   angle brackets included — don't leave any `< place-holder: ... >` text behind.
3. **Delete what doesn't apply.** Sections labelled *Optional* (e.g. **Anything else Lumo
   should know about you?**, **Languages I want to use**) can be removed wholesale.
4. **Mind the nested placeholder.** The language-correction bullet under **Languages I want
   to use** contains a `< place-holder: ... >` inside another one — replace both.

When you're done, search the file for `place-holder` to confirm none remain.

**Re-vet after changing the rules.** If you edit the rules themselves (not just fill in or
delete placeholders), re-vet the whole instruction set: paste the full `LUMO.md` into Lumo
and ask whether anything in the instructions is problematic — conflicts, contradictions, or
directives Lumo can't actually act on.

## 2. Deploy in Lumo (web)

Lumo is entirely web-based, and its **personalization applies to every chat** (no per-chat
or per-file setup needed), via three boxes under **Settings → Personalization**. The
template is organized so each top-level (`##`) section maps to one box:

| Lumo box | Paste this template section |
|---|---|
| **What do you do?** | `## What do you do?` |
| **Anything else Lumo should know about you?** | `## Anything else Lumo should know about you?` |
| **How should Lumo behave?** | everything under `## How should Lumo behave?` — `### Languages I want to use` **and** `### General rules` (with its `####` subsections) |

1. Open Lumo → **Settings → Personalization**.
2. Paste each section's content into the matching box. You can keep the `###`/`####`
   sub-headers as structure inside the "How should Lumo behave?" box.
3. Save.

The full instruction set fits without trouble — no length limits were hit, including the
long "How should Lumo behave?" content.

(Lumo also has Projects for scoping instructions to a single project; the personalization
above is the simplest way to apply your instructions to every chat.)
