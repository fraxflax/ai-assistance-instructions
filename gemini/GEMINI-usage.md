# Using GEMINI-template.md

`GEMINI-template.md` is the Gemini instruction set: a starting point for a personal set of
instructions that tell Gemini ([Google's assistant](https://gemini.google.com/)) who you are
and how you want it to respond. It was vetted on 30 June 2026 on an enterprise/Workspace
account, with Gemini 3.1 Pro and 4.5 Thinking — first pasted into a chat to check for conflicts,
then run from a Gem.

Fill it in (or trim it), then deploy the result in Gemini. **How you deploy depends on your
Google account type** (see step 2).

## 1. Fill in and trim the template

The template marks every spot you need to edit with `< place-holder: ... >`, and the text
inside each marker describes what belongs there.

1. **Work from a copy** so the template stays clean for reuse:

   ```bash
   cp GEMINI-template.md GEMINI.md   # then edit GEMINI.md
   ```

2. **Replace each placeholder** with your own details. Replace the *entire* marker,
   angle brackets included — don't leave any `< place-holder: ... >` text behind.
3. **Delete what doesn't apply.** Sections labelled *Optional* (e.g. **My Interests**,
   **Languages I want to use**) can be removed wholesale.
4. **Mind the nested placeholder.** The language-correction bullet under **Languages I want
   to use** contains a `< place-holder: ... >` inside another one — replace both.

When you're done, search the file for `place-holder` to confirm none remain.

**Re-vet after changing the rules.** If you edit the rules themselves (not just fill in or
delete placeholders), re-vet the whole instruction set: paste the full `GEMINI.md` into Gemini
and ask whether anything in the instructions is problematic — conflicts, contradictions, or
directives Gemini can't actually act on.

## 2. Deploy in Gemini (web)

Gemini has no single deployment that fits every account — **it forks by account type.**

### Enterprise / Workspace accounts — use a Gem (recommended)

Managed/Workspace accounts (e.g. a company Google account) have **no global personalization** —
every chat starts blank. Apply your instructions with a **Gem** (a custom assistant) whose
instructions persist for every chat started in it:

1. In Gemini's left sidebar, click **Gems** to open the **Gem manager**, then **+ New Gem**
   (or the pencil icon to edit an existing Gem).
2. Give the Gem its instructions — **one** of these two equivalent ways (both are read and
   applied, so pick one; don't split your set across both):
   - **Paste** your filled-in `GEMINI.md` into the **Instructions** box (recommended — simplest), or
   - **Upload** `GEMINI.md` to the **Knowledge** section ("Add files for your Gem to reference").
3. Click **Save** (new Gem) / **Update** (existing Gem).
4. Start chats **inside that Gem** — the instructions apply to every chat there.

- **Don't put instructions in both** the Instructions box *and* a Knowledge file unless they
  fully agree: both are read, and when they conflict the precedence isn't guaranteed (you can
  steer it with an explicit clause like "unless otherwise stated", but single-source is simpler).
- **Update:** Instructions box → edit the text and save; Knowledge file → replace the uploaded file.
- **Tip:** name it memorably (e.g. "Default") and pin it for everyday chats.
- **Workspace visibility:** Gemini notes custom Gems are "visible in Gemini for Workspace" — if
  the instructions are personal, check whether the Gem is private to you or visible org-wide.

*(Exact menu labels may differ by Gemini version; verify against your UI.)*

### Personal / private accounts — global personalization

Personal Google accounts have **global personalization** that applies to **all** chats, so you
don't need a Gem. Add your instructions to Gemini's personalization (Settings → personalization)
so every new chat picks them up.

*(This personal-account path isn't hands-on-verified here — confirm the exact location in
Settings. You can also just use a Gem, as above, if you'd rather scope the instructions than
apply them globally.)*
