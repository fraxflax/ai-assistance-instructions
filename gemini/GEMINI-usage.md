# Using GEMINI-template.md

The Gemini instruction set — **`GEMINI-template.md`** (enterprise/Workspace) or
**`GEMINI-personal-template.md`** (personal accounts) — is a starting point for instructions that
tell Gemini ([Google's assistant](https://gemini.google.com/)) who you are and how you want it to
respond. It was vetted on 30 June 2026 on an enterprise/Workspace
account, with Gemini 3.1 Pro and 4.5 Thinking — first pasted into a chat to check for conflicts,
then run from a Gem.

**Which template you use and how you deploy it both depend on your account type** — pick yours in
step 1, deploy in step 2.

## 1. Pick your template (by account type) and fill it in

Gemini deploys differently per account (see step 2), and the two templates are shaped to match —
so pick the right one first:

- **Enterprise / Workspace account** → **`GEMINI-template.md`** — one document, goes into a **Gem**.
- **Personal / private account** → **`GEMINI-personal-template.md`** — separate entries, go into **Personal context**.

Work from a copy of the one you picked:

```bash
cp GEMINI-template.md GEMINI.md            # enterprise / Workspace
# or
cp GEMINI-personal-template.md GEMINI.md   # personal account
```

Then, in your copy:

1. **Replace each placeholder** — the whole `< place-holder: ... >` marker, angle brackets
   included; don't leave any behind.
2. **Delete what doesn't apply** — anything marked *Optional* (e.g. interests, languages) can be
   removed wholesale.
3. **Mind the nested placeholder** — the "language you're learning" spot has a
   `< place-holder: ... >` inside another one; replace both.

When you're done, search for `place-holder` to confirm none remain. (The personal template also
has its own short "How to use" note at the top for adding the entries.)

**Re-vet after changing the rules.** If you edit the rules themselves (not just fill in or delete
placeholders), re-vet: load the full set into Gemini and ask whether anything is problematic —
conflicts, contradictions, or directives Gemini can't actually act on.

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

### Personal / private accounts — Personal context (global)

Personal Google accounts have **global personalization** that applies to **all** chats:
**Settings → Personal context → "Your instructions for Gemini"** (toggle on). But it is **not a
single field** — it stores **many short, separate entries** (click **Add** per entry), each with
a **character limit**, and Gemini **paraphrases** each one as it saves it.

So don't paste the whole `GEMINI.md` here. Use the companion
**[`GEMINI-personal-template.md`](GEMINI-personal-template.md)** — the same rule set **pre-split
into atomic, paste-ready entries** that survive the paraphrasing. Fill in its placeholders, delete
what doesn't apply, then **Add** one entry per block (order doesn't matter). Afterwards, ask a new
chat to *"list the operational parameters you're applying"* and spot-check that the dense rules and
the `[Checked]`/`[Memory]`/`[Reasoning]` tags came through.

(Want verbatim fidelity, or the rules scoped rather than global? A personal account can also use a
**Gem** with `GEMINI-template.md`, exactly like the enterprise path above.)
