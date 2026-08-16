---
name: codepen-share
description: Prepare verified browser-only HTML, CSS, and JavaScript sample files as a CodePen Prefill launcher and, with approval, open an unsaved Pen. Use when the user asks to share or move a front-end demo to CodePen. Do not use for Node.js, server, CLI, build-tool, or multi-process examples.
---

# Share a verified sample on CodePen

Transfer a browser-only sample to an unsaved CodePen without taking ownership of publication choices.

## Confirm suitability

Read [the Prefill rules](references/codepen-prefill.md). Use this workflow only when:

- the sample runs with browser HTML, CSS, and JavaScript alone;
- its central behavior has already been validated locally;
- no secret, credential, private URL, or sensitive data will be transferred;
- it does not require Node.js, a server, a CLI, a bundler, or multiple processes.

CodePen is a sharing destination, not the validation environment. If local validation is unclear, ask for the evidence or direct the user back to validation before preparing the Pen.

## Prepare panel files

Separate content into the panels actually used:

- HTML: elements that belong inside `body`; omit document, `head`, `body`, `script`, and `style` wrappers.
- CSS: CSS only; omit `style` tags.
- JavaScript: JavaScript only; omit `script` tags.

Do not change the verified behavior merely to make the sample more decorative.

## Generate the launcher

Run `scripts/create-codepen-prefill.py` with the relevant panel files:

```bash
python3 <skill-directory>/scripts/create-codepen-prefill.py \
  --title "Demo title" \
  --description "Verified sample for a technical article" \
  --html path/to/codepen.html \
  --css path/to/codepen.css \
  --js path/to/codepen.js \
  --output path/to/open-in-codepen.html
```

Pass only panels the sample uses. The script rejects wrapper tags, empty panel files, missing files, and accidental overwrites.

## Obtain approval before transfer

Creating the local launcher does not transfer data. Before opening or submitting it, show the user:

- the title and description;
- the exact files that will be transferred;
- confirmation that the code was validated locally rather than on CodePen;
- confirmation that the resulting Pen will be unsaved.

Obtain explicit approval, then open the launcher and submit its form. Stop after the populated unsaved Pen opens.

Do not press Save, select a publication scope, or insert an iframe. The user owns saving, visibility, and the final share URL.

## Report completion

Report the launcher path, transferred panel files, local validation basis, and that the Pen remains unsaved. If opening the launcher is unavailable, give the user the path and explain that submitting the form opens the unsaved Pen.
