# Using EURIA-template.md

`EURIA-template.md` is the Euria instruction set: a starting point for a personal set of
instructions that tell Euria ([Infomaniak's web assistant](https://euria.infomaniak.com/)) who
you are and how you want it to respond. It was iterated and vetted in Euria on 17 June 2026 — run through the assistant to
root out internal conflicts and contradictions and to keep only directives it actually acts
on.

Fill it in (or trim it), then deploy the result in Euria (web).

## 1. Fill in and trim the template

The template marks every spot you need to edit with `< place-holder: ... >`, and the text
inside each marker describes what belongs there.

1. **Work from a copy** so the template stays clean for reuse:

   ```bash
   cp EURIA-template.md EURIA.md   # then edit EURIA.md
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
delete placeholders), re-vet the whole instruction set: load the full `EURIA.md` into Euria
(paste it, or attach it in a chat) and ask whether anything in the instructions is
problematic — conflicts, contradictions, or directives Euria can't actually act on.

## 2. Deploy in Euria (web)

Euria is entirely web-based: there's no local file to install and no single "apply to all
new chats" setting. The way to apply your instructions everywhere is a **Project**; for
one-off chats outside a project, you add them per chat.

### Recommended — a Project (instructions apply to every chat in it)

A Euria **Project** holds instructions that apply to every chat started inside it.

**Create a project**

1. Hover **Projects** in the left sidebar and click the **+**.
2. In the dialog, give the project a **title**, then give it your instructions one of the
   two ways below, and click **Create**.

**Give the project your instructions — pick ONE (both are applied, so don't do both):**

- **Upload the file** — drop your edited `EURIA.md` onto **Drop or select files** (or click
  *select*).
- **Paste the text** — paste the full content into the **Project Instructions** box.

Either one alone is enough: Euria applies both the uploaded file *and* the Project
Instructions box, so doing both just duplicates the same instructions. (Uploading the file
is convenient — keep it in **kDrive** and it's a quick attach — but pasting works identically;
use whichever you prefer.)

**On a project that already exists**

Click the **project name** in the left sidebar to open its project view. In the right-hand
column you'll find **Instructions** with an **Update** button (to add or edit the instruction
text) and the **Drop or select files** upload area. This panel only shows on the project
view — if you open a *chat* inside the project it's hidden, so click the project name to get
back to it.

**Updating the instructions later**

- **Text** (Project Instructions box): click **Update**, edit, and save.
- **Uploaded file**: there's no in-place edit — open the file's **⋮** menu → **Delete**, then
  upload the new version.

**Tip — a "Default" project.** Create a project named **Default**, set your instructions on
it, and start all your misc/one-off chats inside it. They inherit the instructions
automatically, so you don't have to add them to every new chat.

### Fallback — per chat (chats outside any project)

A **New chat** (the sidebar button) starts with no instructions. Add them at the start of
the chat:

- **Paste** the full instructions into the **Ask Euria** box, or
- Click the **+** in the input box → **upload** your `EURIA.md` file or **choose it from
  kDrive**.

Keeping the edited file in **kDrive** means it syncs across devices and is one click to
attach to any new chat.
